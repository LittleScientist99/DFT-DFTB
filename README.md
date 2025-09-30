# DFT-DFTB
MAgnetic field_DFTB
P = [-0.2,	-0.16,	-0.12,	-0.08,	-0.04,	0,	0.04,	0.08,	0.12,	0.16,	0.2]
E_6 = [-37.7636232409,	-37.77260603,	-37.78079279,	-37.7881818977,	-37.7947718,	-37.8005609939,	-37.80554804,	-37.80973156,	-37.81311022,	-37.81568272,	-37.81744782]
E_5 = [-37.76362324,	-37.77260603,	-37.78079279,	-37.7881819,	-37.7947718,	-37.8005609939,	-37.80554804,	-37.80973156,	-37.81311022,	-37.81568272,	-37.81744782]
E_4 = [-37.70101561,	-37.72258661,	-37.743328,	-37.76323841,	-37.78231651,	-37.8005609939,	-37.81797059,	-37.83454404,	-37.85028012,	-37.86517763,	-37.87923541]
E_3 = [-37.70101561, -37.72258661,	-37.743328,	-37.76323841,	-37.78231651,	-37.8005609939,	-37.81797059,	-37.83454404,	-37.85028012,	-37.86517763,	-37.87923541]
E_2 = [-35.75394727,	-36.17235495,	-36.58625048,	-36.99560263,	-37.40038203,	-37.8005609939,	-38.19611344,	-38.58701473,	-38.97324157,	-39.35477193,	-39.73158491]
E_1 = [-35.75394727,	-36.17235495,	-36.58625048,	-36.99560263,	-37.40038203,	-37.8005609939,	-38.19611344,	-38.58701473,	-38.97324157,	-39.35477193,	-39.73158491]
dE_6 = [-0.0369377530,	-0.0279549669,	-0.0197682064,	-0.0123790962,	-0.0057891951,	0.0000000000,	0.0049870498,	0.0091705689,	0.0125492225,	0.0151217230,	0.0168868274]
dE_5 = [-0.0369377530,	-0.0279549669,	-0.0197682064,	-0.0123790962,	-0.0057891951,	0.0000000000,	0.0049870498,	0.0091705689,	0.0125492225,	0.0151217230,	0.0168868274]
dE_4 = [-0.0995453813,	-0.0779743795,	-0.0572329939,	-0.0373225849,	-0.0182444852,	0.0000000000,	0.0174095924,	0.0339830412,	0.0497191218,	0.0646166363,	0.0786744125]
dE_3 = [-0.0995453813,	-0.0779743795,	-0.0572329939,	-0.0373225849,	-0.0182444852,	0.0000000000,	0.0174095924,	0.0339830412,	0.0497191218,	0.0646166363,	0.0786744125]
dE_2 = [-2.0466137250,	-1.6282060418,	-1.2143105096,	-0.8049583592,	-0.4001789666,	0.0000000000,	0.3955524472,	0.7864537376,	1.1726805804,	1.5542109337,	1.9310239137]
dE_1 = [-2.0466137250,	-1.6282060418,	-1.2143105096,	-0.8049583592,	-0.4001789666,	0.0000000000,	0.3955524472,	0.7864537376,	1.1726805804,	1.5542109337,	1.9310239137]


plt.figure(figsize=(6, 4))
plt.plot(P, dE_6, marker='o', linewidth = '3', label='n=6', color = 'blue')
plt.plot(P, dE_5, marker='o',linestyle='--', linewidth = '2',  label='n=5', color = 'yellow')
plt.plot(P, dE_4, marker='o',linewidth = '3',  label='n=4', color = 'green')
plt.plot(P, dE_3, marker='o',linestyle='--',linewidth = '2',  label='n=3', color = 'red')
plt.plot(P, dE_2, marker='o',linewidth = '3',  label='n=2', color = 'purple')
plt.plot(P, dE_1, marker='o',linestyle='--',linewidth = '2',  label='n=1', color = 'orange')
plt.axhline(0, color='gray', linestyle='--', linewidth=0.8)
plt.xlabel('Perturbation')
plt.ylabel('Energy Shift, a.u.')
plt.title('Energy Shifts vs Perturbation')
plt.legend()
plt.grid(True)
plt.tight_layout()
plt.text(
    -0.1, 1.1, "Fig. 1A", 
    transform=plt.gca().transAxes,   # place relative to axes
    fontsize=12, fontweight="bold", va="top", ha="left"
)
#plt.savefig("energy_shifts.png", dpi=300, bbox_inches="tight")  
plt.show()

plt.figure(figsize=(6, 4))
plt.plot(P, dE_6, marker='o', linewidth = '3', label='n=6', color = 'blue')
plt.plot(P, dE_5, marker='o',linestyle='--', linewidth = '2',  label='n=5', color = 'yellow')
plt.plot(P, dE_4, marker='o',linewidth = '3',  label='n=4', color = 'green')
plt.plot(P, dE_3, marker='o',linestyle='--',linewidth = '2',  label='n=3', color = 'red')
#plt.plot(P, dE_2, marker='o',linewidth = '3',  label='n=2', color = 'purple')
#plt.plot(P, dE_1, marker='o',linestyle='--',linewidth = '2',  label='n=1', color = 'orange')
plt.axhline(0, color='gray', linestyle='--', linewidth=0.8)
plt.xlabel('Perturbation')
plt.ylabel('Energy Shift, a.u.')
plt.title('Zoomed in Energy Shifts vs Perturbation')
plt.legend()
plt.grid(True)
plt.tight_layout()
plt.text(
    -0.1, 1.1, "Fig. 1B", 
    transform=plt.gca().transAxes,   # place relative to axes
    fontsize=12, fontweight="bold", va="top", ha="left")
plt.savefig("energy_shifts_zoomed_in.png", dpi=300, bbox_inches="tight")  
plt.show()