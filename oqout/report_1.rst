Classical PSHA at WLG, single pt source
=======================================

============== ===================
checksum32     1_041_920_075      
date           2020-05-06T02:05:54
engine_version 3.10.0             
============== ===================

num_sites = 1, num_levels = 29, num_rlzs = 1

Parameters
----------
=============================== ==================
calculation_mode                'classical'       
number_of_logic_tree_samples    0                 
maximum_distance                {'default': 400.0}
investigation_time              50.0              
ses_per_logic_tree_path         1                 
truncation_level                3.0               
rupture_mesh_spacing            0.2               
complex_fault_mesh_spacing      0.2               
width_of_mfd_bin                0.1               
area_source_discretization      10.0              
pointsource_distance            None              
ground_motion_correlation_model None              
minimum_intensity               {}                
random_seed                     23                
master_seed                     0                 
ses_seed                        42                
=============================== ==================

Input files
-----------
======================= ====================================================================================
Name                    File                                                                                
======================= ====================================================================================
gsim_logic_tree         `gmpe_logic_tree-original_Abr14_ONLY.xml <gmpe_logic_tree-original_Abr14_ONLY.xml>`_
job_ini                 `job-WLG.ini <job-WLG.ini>`_                                                        
source_model_logic_tree `source_model_logic_tree.xml <source_model_logic_tree.xml>`_                        
======================= ====================================================================================

Composite source model
----------------------
========= ======= ================
smlt_path weight  num_realizations
========= ======= ================
b1        1.00000 1               
========= ======= ================

Required parameters per tectonic region type
--------------------------------------------
====== ====================== =============== ======================= =======================
grp_id gsims                  distances       siteparams              ruptparams             
====== ====================== =============== ======================= =======================
0      '[AbrahamsonEtAl2014]' rjb rrup rx ry0 vs30 vs30measured z1pt0 dip mag rake width ztor
====== ====================== =============== ======================= =======================

Slowest sources
---------------
========= ==== ============ ========= ========= ============
source_id code multiplicity calc_time num_sites eff_ruptures
========= ==== ============ ========= ========= ============
03723     P    1            0.03482   1.00000   22          
========= ==== ============ ========= ========= ============

Computation times by source typology
------------------------------------
==== =========
code calc_time
==== =========
P    0.03482  
==== =========

Information about the tasks
---------------------------
====================== ======= ====== ======= ======= =======
operation-duration     mean    stddev min     max     outputs
build_hazard           0.00486 NaN    0.00486 0.00486 1      
classical_split_filter 0.03712 NaN    0.03712 0.03712 1      
read_source_model      0.00195 NaN    0.00195 0.00195 1      
====================== ======= ====== ======= ======= =======

Data transfer
-------------
====================== ========================================= ========
task                   sent                                      received
read_source_model                                                1.45 KB 
classical_split_filter srcs=1.15 KB params=919 B srcfilter=221 B 3.41 KB 
classical                                                        0 B     
build_hazard                                                     729 B   
====================== ========================================= ========

Slowest operations
------------------
============================ ========= ========= ======
calc_1                       time_sec  memory_mb counts
============================ ========= ========= ======
ClassicalCalculator.run      1.44132   2.25391   1     
composite source model       0.20384   0.57031   1     
total classical_split_filter 0.03712   1.27734   1     
make_contexts                0.01485   0.0       1     
computing mean_std           0.00941   0.0       22    
iter_ruptures                0.00718   0.0       1     
aggregate curves             0.00525   0.0       1     
total build_hazard           0.00486   0.01562   1     
read PoEs                    0.00420   0.01562   1     
get_poes                     0.00288   0.0       22    
total read_source_model      0.00195   0.01953   1     
splitting/filtering sources  0.00156   1.12891   1     
saving probability maps      0.00138   0.0       1     
store source_info            9.146E-04 0.0       1     
saving statistics            7.658E-04 0.0       1     
composing pnes               3.769E-04 0.0       22    
compute stats                2.301E-04 0.0       1     
combine pmaps                3.910E-05 0.0       1     
============================ ========= ========= ======