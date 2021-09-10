# HDL

    `default_nettype none
    module hardweario_webinar_poc(
        input wire key,
        output wire open
        );

        assign open = ! key;
    endmodule

# GDS

hardened using openlane to the gds file included.

# spice

* hardweario_webinar_poc_inv2.spice is the one used for LVS by openlane
* hardweario_webinar_poc_inv2_extracted.spice is the one extracted from the GDS by running the following commands in magic:
    *    extract
    *    ext2spice lvs
    *    ext2spice

# simulation

* run make ok to use the 1st spice, which works.
* run make broken to use the 2nd spice, which gives a non changing 1v output
