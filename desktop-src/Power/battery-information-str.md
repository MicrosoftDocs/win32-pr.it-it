---
description: Contiene informazioni sulla batteria.
ms.assetid: 6a236f48-5a06-4537-a769-bd68e5c0eb27
title: Struttura BATTERY_INFORMATION (Poclass. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- BATTERY_INFORMATION
api_type:
- HeaderDef
api_location:
- Poclass.h
- Batclass.h
ms.openlocfilehash: 1e892a14263822ddd009b162c6343975e1689683
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106312063"
---
# <a name="battery_information-structure"></a><span data-ttu-id="108c3-103">\_Struttura delle informazioni sulla batteria</span><span class="sxs-lookup"><span data-stu-id="108c3-103">BATTERY\_INFORMATION structure</span></span>

<span data-ttu-id="108c3-104">Contiene informazioni sulla batteria.</span><span class="sxs-lookup"><span data-stu-id="108c3-104">Contains battery information.</span></span> <span data-ttu-id="108c3-105">Questa struttura viene restituita dal codice di controllo delle [**\_ \_ \_ informazioni sulle query della batteria IOCTL**](ioctl-battery-query-information.md) quando è richiesto il livello di informazioni BatteryInformation.</span><span class="sxs-lookup"><span data-stu-id="108c3-105">This structure is returned by the [**IOCTL\_BATTERY\_QUERY\_INFORMATION**](ioctl-battery-query-information.md) control code when the BatteryInformation information level is requested.</span></span>

## <a name="syntax"></a><span data-ttu-id="108c3-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="108c3-106">Syntax</span></span>


```C++
typedef struct _BATTERY_INFORMATION {
  ULONG Capabilities;
  UCHAR Technology;
  UCHAR Reserved[3];
  UCHAR Chemistry[4];
  ULONG DesignedCapacity;
  ULONG FullChargedCapacity;
  ULONG DefaultAlert1;
  ULONG DefaultAlert2;
  ULONG CriticalBias;
  ULONG CycleCount;
} BATTERY_INFORMATION, *PBATTERY_INFORMATION;
```



## <a name="members"></a><span data-ttu-id="108c3-107">Members</span><span class="sxs-lookup"><span data-stu-id="108c3-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="108c3-108">**Capabilities**</span><span class="sxs-lookup"><span data-stu-id="108c3-108">**Capabilities**</span></span>
</dt> <dd>

<span data-ttu-id="108c3-109">Funzionalità della batteria.</span><span class="sxs-lookup"><span data-stu-id="108c3-109">The battery capabilities.</span></span> <span data-ttu-id="108c3-110">Il membro può essere costituito da uno o più dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="108c3-110">This member can be one or more of the following values.</span></span>



| <span data-ttu-id="108c3-111">Valore</span><span class="sxs-lookup"><span data-stu-id="108c3-111">Value</span></span>                                                                                                                                                                                                                                                                                 | <span data-ttu-id="108c3-112">Significato</span><span class="sxs-lookup"><span data-stu-id="108c3-112">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="BATTERY_CAPACITY_RELATIVE"></span><span id="battery_capacity_relative"></span><dl> <span data-ttu-id="108c3-113"><dt>**Batteria \_ 0x40000000 \_ relativa alla capacità**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="108c3-113"><dt>**BATTERY\_CAPACITY\_RELATIVE**</dt> <dt>0x40000000</dt></span></span> </dl>                    | <span data-ttu-id="108c3-114">Indica che le informazioni sulla capacità e sulla frequenza della batteria sono relative e non in unità specifiche.</span><span class="sxs-lookup"><span data-stu-id="108c3-114">Indicates that the battery capacity and rate information are relative, and not in any specific units.</span></span> <span data-ttu-id="108c3-115">Se questo bit non è impostato, le unità di report sono milliwatt ore (mWh) per la capacità e milliwatt (mW) per la frequenza.</span><span class="sxs-lookup"><span data-stu-id="108c3-115">If this bit is not set, the reporting units are milliwatt-hours (mWh) for capacity and milliwatts (mW) for rate.</span></span> <span data-ttu-id="108c3-116">Se questo bit è impostato, tutti i riferimenti alle unità nell'altra documentazione della batteria possono essere ignorati.</span><span class="sxs-lookup"><span data-stu-id="108c3-116">If this bit is set, all references to units in the other battery documentation can be ignored.</span></span> <span data-ttu-id="108c3-117">Tutte le informazioni sulla frequenza sono indicate in unità all'ora.</span><span class="sxs-lookup"><span data-stu-id="108c3-117">All rate information is reported in units per hour.</span></span> <span data-ttu-id="108c3-118">Se ad esempio la capacità completamente addebitata è indicata come 100, la velocità 200 indica che la batteria utilizzerà tutta la sua capacità in mezz'ora.</span><span class="sxs-lookup"><span data-stu-id="108c3-118">For example, if the fully charged capacity is reported as 100, a rate of 200 indicates that the battery will use all of its capacity in half an hour.</span></span><br/> |
| <span id="BATTERY_IS_SHORT_TERM"></span><span id="battery_is_short_term"></span><dl> <span data-ttu-id="108c3-119"><dt>**Batteria \_ 0x20000000 a \_ breve \_ termine**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="108c3-119"><dt>**BATTERY\_IS\_SHORT\_TERM**</dt> <dt>0x20000000</dt></span></span> </dl>                               | <span data-ttu-id="108c3-120">Indica che l'operazione normale è per una funzione non affidabile.</span><span class="sxs-lookup"><span data-stu-id="108c3-120">Indicates that the normal operation is for a fail-safe function.</span></span> <span data-ttu-id="108c3-121">Se questo bit non è impostato, si prevede che la batteria venga utilizzata durante il normale utilizzo del sistema.</span><span class="sxs-lookup"><span data-stu-id="108c3-121">If this bit is not set the battery is expected to be used during normal system usage.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                          |
| <span id="BATTERY_SET_CHARGE_SUPPORTED"></span><span id="battery_set_charge_supported"></span><dl> <span data-ttu-id="108c3-122"><dt>**Batteria \_ IMPOSTA \_ addebito 0x00000001 \_ supportato**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="108c3-122"><dt>**BATTERY\_SET\_CHARGE\_SUPPORTED**</dt> <dt>0x00000001</dt></span></span> </dl>          | <span data-ttu-id="108c3-123">Indica che il dispositivo batteria supporta le richieste di impostazione delle informazioni del tipo BatteryCharge.</span><span class="sxs-lookup"><span data-stu-id="108c3-123">Indicates that set information requests of the type BatteryCharge are supported by this battery device.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span id="BATTERY_SET_DISCHARGE_SUPPORTED"></span><span id="battery_set_discharge_supported"></span><dl> <span data-ttu-id="108c3-124"><dt>**Batteria \_ IMPOSTA \_ \_**</dt> il <dt>0x00000002</dt> supportato</span><span class="sxs-lookup"><span data-stu-id="108c3-124"><dt>**BATTERY\_SET\_DISCHARGE\_SUPPORTED**</dt> <dt>0x00000002</dt></span></span> </dl> | <span data-ttu-id="108c3-125">Indica che il dispositivo batteria supporta le richieste di impostazione delle informazioni del tipo BatteryDischarge.</span><span class="sxs-lookup"><span data-stu-id="108c3-125">Indicates that set information requests of the type BatteryDischarge are supported by this battery device.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="BATTERY_SYSTEM_BATTERY"></span><span id="battery_system_battery"></span><dl> <span data-ttu-id="108c3-126"><dt>**Batteria \_ \_Batteria del sistema**</dt> <dt>0x80000000</dt></span><span class="sxs-lookup"><span data-stu-id="108c3-126"><dt>**BATTERY\_SYSTEM\_BATTERY**</dt> <dt>0x80000000</dt></span></span> </dl>                             | <span data-ttu-id="108c3-127">Indica che la batteria può fornire l'alimentazione generale per l'esecuzione del sistema.</span><span class="sxs-lookup"><span data-stu-id="108c3-127">Indicates that the battery can provide general power to run the system.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                         |



 

</dd> <dt>

<span data-ttu-id="108c3-128">**Tecnologia**</span><span class="sxs-lookup"><span data-stu-id="108c3-128">**Technology**</span></span>
</dt> <dd>

<span data-ttu-id="108c3-129">Tecnologia della batteria.</span><span class="sxs-lookup"><span data-stu-id="108c3-129">The battery technology.</span></span> <span data-ttu-id="108c3-130">Il membro può essere uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="108c3-130">This member can be one of the following values.</span></span>



| <span data-ttu-id="108c3-131">Valore</span><span class="sxs-lookup"><span data-stu-id="108c3-131">Value</span></span>                                                                        | <span data-ttu-id="108c3-132">Significato</span><span class="sxs-lookup"><span data-stu-id="108c3-132">Meaning</span></span>                                                    |
|------------------------------------------------------------------------------|------------------------------------------------------------|
| <dl> <span data-ttu-id="108c3-133"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="108c3-133"><dt>0</dt></span></span> </dl> | <span data-ttu-id="108c3-134">Batteria non ricaricabile, ad esempio, alcalina.</span><span class="sxs-lookup"><span data-stu-id="108c3-134">Nonrechargeable battery, for example, alkaline.</span></span><br/> |
| <dl> <span data-ttu-id="108c3-135"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="108c3-135"><dt>1</dt></span></span> </dl> | <span data-ttu-id="108c3-136">Batteria ricaricabile, ad esempio acido di piombo.</span><span class="sxs-lookup"><span data-stu-id="108c3-136">Rechargeable battery, for example, lead acid.</span></span><br/>   |



 

</dd> <dt>

<span data-ttu-id="108c3-137">**Reserved**</span><span class="sxs-lookup"><span data-stu-id="108c3-137">**Reserved**</span></span>
</dt> <dd>

<span data-ttu-id="108c3-138">Riservato.</span><span class="sxs-lookup"><span data-stu-id="108c3-138">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="108c3-139">**Chimica**</span><span class="sxs-lookup"><span data-stu-id="108c3-139">**Chemistry**</span></span>
</dt> <dd>

<span data-ttu-id="108c3-140">Stringa di caratteri abbreviata che indica la chimica della batteria.</span><span class="sxs-lookup"><span data-stu-id="108c3-140">An abbreviated character string that indicates the battery's chemistry.</span></span> <span data-ttu-id="108c3-141">Questa stringa non è necessariamente con terminazione zero.</span><span class="sxs-lookup"><span data-stu-id="108c3-141">This string is not necessarily zero-terminated.</span></span> <span data-ttu-id="108c3-142">Di seguito è riportato un elenco parziale delle abbreviazioni che possono essere restituite e del chimiche associato.</span><span class="sxs-lookup"><span data-stu-id="108c3-142">The following is a partial list of abbreviations that can be returned and the associated chemistries.</span></span>



| <span data-ttu-id="108c3-143">Stringa Unicode</span><span class="sxs-lookup"><span data-stu-id="108c3-143">Unicode string</span></span>                                                                                                                                           | <span data-ttu-id="108c3-144">Significato</span><span class="sxs-lookup"><span data-stu-id="108c3-144">Meaning</span></span>                                    |
|----------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------|
| <span id="PbAc"></span><span id="pbac"></span><span id="PBAC"></span><dl> <span data-ttu-id="108c3-145"><dt>**PbAc**</dt></span><span class="sxs-lookup"><span data-stu-id="108c3-145"><dt>**PbAc**</dt></span></span> </dl> | <span data-ttu-id="108c3-146">Acido lead</span><span class="sxs-lookup"><span data-stu-id="108c3-146">Lead Acid</span></span><br/>                       |
| <span id="LION"></span><span id="lion"></span><dl> <span data-ttu-id="108c3-147"><dt>**LION**</dt></span><span class="sxs-lookup"><span data-stu-id="108c3-147"><dt>**LION**</dt></span></span> </dl>                        | <span data-ttu-id="108c3-148">Ioni di litio</span><span class="sxs-lookup"><span data-stu-id="108c3-148">Lithium Ion</span></span><br/>                     |
| <span id="Li-I"></span><span id="li-i"></span><span id="LI-I"></span><dl> <span data-ttu-id="108c3-149"><dt>**Li-I**</dt></span><span class="sxs-lookup"><span data-stu-id="108c3-149"><dt>**Li-I**</dt></span></span> </dl> | <span data-ttu-id="108c3-150">Ioni di litio</span><span class="sxs-lookup"><span data-stu-id="108c3-150">Lithium Ion</span></span><br/>                     |
| <span id="NiCd"></span><span id="nicd"></span><span id="NICD"></span><dl> <span data-ttu-id="108c3-151"><dt>**NiCd**</dt></span><span class="sxs-lookup"><span data-stu-id="108c3-151"><dt>**NiCd**</dt></span></span> </dl> | <span data-ttu-id="108c3-152">Nichel cadmio</span><span class="sxs-lookup"><span data-stu-id="108c3-152">Nickel Cadmium</span></span><br/>                  |
| <span id="NiMH"></span><span id="nimh"></span><span id="NIMH"></span><dl> <span data-ttu-id="108c3-153"><dt>**NiMH**</dt></span><span class="sxs-lookup"><span data-stu-id="108c3-153"><dt>**NiMH**</dt></span></span> </dl> | <span data-ttu-id="108c3-154">Idruro Nickel metal</span><span class="sxs-lookup"><span data-stu-id="108c3-154">Nickel Metal Hydride</span></span><br/>            |
| <span id="NiZn"></span><span id="nizn"></span><span id="NIZN"></span><dl> <span data-ttu-id="108c3-155"><dt>**NiZn**</dt></span><span class="sxs-lookup"><span data-stu-id="108c3-155"><dt>**NiZn**</dt></span></span> </dl> | <span data-ttu-id="108c3-156">Zinco nichel</span><span class="sxs-lookup"><span data-stu-id="108c3-156">Nickel Zinc</span></span><br/>                     |
| <span id="RAM"></span><span id="ram"></span><dl> <span data-ttu-id="108c3-157"><dt>**RAM**</dt></span><span class="sxs-lookup"><span data-stu-id="108c3-157"><dt>**RAM**</dt></span></span> </dl>                           | <span data-ttu-id="108c3-158">Alkaline-Manganese ricaricabile</span><span class="sxs-lookup"><span data-stu-id="108c3-158">Rechargeable Alkaline-Manganese</span></span><br/> |



 

<span data-ttu-id="108c3-159">Altri chimiche possono essere visualizzati in futuro e il codice deve essere in grado di gestirli.</span><span class="sxs-lookup"><span data-stu-id="108c3-159">Other chemistries may appear in the future and your code should be able to handle them.</span></span>

</dd> <dt>

<span data-ttu-id="108c3-160">**DesignedCapacity**</span><span class="sxs-lookup"><span data-stu-id="108c3-160">**DesignedCapacity**</span></span>
</dt> <dd>

<span data-ttu-id="108c3-161">Capacità teorica della batteria quando è nuova, in mWh, a meno che non \_ sia impostata la capacità della batteria \_ relativa.</span><span class="sxs-lookup"><span data-stu-id="108c3-161">The theoretical capacity of the battery when new, in mWh unless BATTERY\_CAPACITY\_RELATIVE is set.</span></span> <span data-ttu-id="108c3-162">In tal caso, le unità non sono definite.</span><span class="sxs-lookup"><span data-stu-id="108c3-162">In that case, the units are undefined.</span></span>

</dd> <dt>

<span data-ttu-id="108c3-163">**FullChargedCapacity**</span><span class="sxs-lookup"><span data-stu-id="108c3-163">**FullChargedCapacity**</span></span>
</dt> <dd>

<span data-ttu-id="108c3-164">Capacità corrente completamente addebitata della batteria in mWh (o relativa).</span><span class="sxs-lookup"><span data-stu-id="108c3-164">The battery's current fully charged capacity in mWh (or relative).</span></span> <span data-ttu-id="108c3-165">Confrontare questo valore con **DesignedCapacity** per stimare l'usura della batteria.</span><span class="sxs-lookup"><span data-stu-id="108c3-165">Compare this value to **DesignedCapacity** to estimate the battery's wear.</span></span>

</dd> <dt>

<span data-ttu-id="108c3-166">**DefaultAlert1**</span><span class="sxs-lookup"><span data-stu-id="108c3-166">**DefaultAlert1**</span></span>
</dt> <dd>

<span data-ttu-id="108c3-167">Capacità consigliata dal produttore, in mWh, in cui deve verificarsi un avviso di batteria basso.</span><span class="sxs-lookup"><span data-stu-id="108c3-167">The manufacturer's suggested capacity, in mWh, at which a low battery alert should occur.</span></span> <span data-ttu-id="108c3-168">Le definizioni del basso variano dal produttore al produttore.</span><span class="sxs-lookup"><span data-stu-id="108c3-168">Definitions of low vary from manufacturer to manufacturer.</span></span> <span data-ttu-id="108c3-169">In generale, si verificherà uno stato di avviso prima di uno stato basso, ma è preferibile non presupporre che sia sempre.</span><span class="sxs-lookup"><span data-stu-id="108c3-169">In general, a warning state will occur before a low state, but you should not assume that it always will.</span></span> <span data-ttu-id="108c3-170">Per ridurre il rischio di perdita di dati, questo valore viene in genere usato come impostazione predefinita per l'allarme della batteria critica.</span><span class="sxs-lookup"><span data-stu-id="108c3-170">To reduce risk of data loss, this value is usually used as the default setting for the critical battery alarm.</span></span>

</dd> <dt>

<span data-ttu-id="108c3-171">**DefaultAlert2**</span><span class="sxs-lookup"><span data-stu-id="108c3-171">**DefaultAlert2**</span></span>
</dt> <dd>

<span data-ttu-id="108c3-172">Capacità consigliata dal produttore, in mWh, in corrispondenza della quale deve verificarsi un avviso di batteria.</span><span class="sxs-lookup"><span data-stu-id="108c3-172">The manufacturer's suggested capacity, in mWh, at which a warning battery alert should occur.</span></span> <span data-ttu-id="108c3-173">Le definizioni di avviso variano dal produttore al produttore.</span><span class="sxs-lookup"><span data-stu-id="108c3-173">Definitions of warning vary from manufacturer to manufacturer.</span></span> <span data-ttu-id="108c3-174">In generale, si verificherà uno stato di avviso prima di uno stato basso, ma è preferibile non presupporre che sia sempre.</span><span class="sxs-lookup"><span data-stu-id="108c3-174">In general, a warning state will occur before a low state, but you should not assume that it always will.</span></span> <span data-ttu-id="108c3-175">Per ridurre il rischio di perdita di dati, questo valore viene in genere usato come impostazione predefinita per l'allarme batteria basso.</span><span class="sxs-lookup"><span data-stu-id="108c3-175">To reduce risk of data loss, this value is usually used as the default setting for the low battery alarm.</span></span>

</dd> <dt>

<span data-ttu-id="108c3-176">**CriticalBias**</span><span class="sxs-lookup"><span data-stu-id="108c3-176">**CriticalBias**</span></span>
</dt> <dd>

<span data-ttu-id="108c3-177">Distorsione da zero, in mWh, applicata alla funzionalità di segnalazione della batteria.</span><span class="sxs-lookup"><span data-stu-id="108c3-177">A bias from zero, in mWh, which is applied to battery reporting.</span></span> <span data-ttu-id="108c3-178">Alcune batterie riservano un costo ridotto, che è prevenuto dai valori di capacità della batteria per mostrare "0" come livello di batteria critico.</span><span class="sxs-lookup"><span data-stu-id="108c3-178">Some batteries reserve a small charge that is biased out of the battery's capacity values to show "0" as the critical battery level.</span></span> <span data-ttu-id="108c3-179">La distorsione critica è analoga all'impostazione di un misuratore di carburante per mostrare "Empty" quando ci sono più litri di carburante a sinistra.</span><span class="sxs-lookup"><span data-stu-id="108c3-179">Critical bias is analogous to setting a fuel gauge to show "empty" when there are several liters of fuel left.</span></span>

</dd> <dt>

<span data-ttu-id="108c3-180">**CycleCount**</span><span class="sxs-lookup"><span data-stu-id="108c3-180">**CycleCount**</span></span>
</dt> <dd>

<span data-ttu-id="108c3-181">Il numero di cicli di addebito/scaricamento che la batteria ha riscontrato.</span><span class="sxs-lookup"><span data-stu-id="108c3-181">The number of charge/discharge cycles the battery has experienced.</span></span> <span data-ttu-id="108c3-182">Questo consente di determinare il consumo della batteria.</span><span class="sxs-lookup"><span data-stu-id="108c3-182">This provides a means to determine the battery's wear.</span></span> <span data-ttu-id="108c3-183">Se la batteria non supporta un contatore di cicli, questo membro è zero.</span><span class="sxs-lookup"><span data-stu-id="108c3-183">If the battery does not support a cycle counter, this member is zero.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="108c3-184">Commenti</span><span class="sxs-lookup"><span data-stu-id="108c3-184">Remarks</span></span>

<span data-ttu-id="108c3-185">In genere, uno stato di avviso si verifica prima di uno stato basso, ma è preferibile non presupporre che sia.</span><span class="sxs-lookup"><span data-stu-id="108c3-185">Generally, a warning state occurs before a low state, but you should not assume it will.</span></span> <span data-ttu-id="108c3-186">È possibile eseguire il polling di una batteria e rilevare che non si è verificato alcun livello di avviso e quindi eseguire di nuovo il polling della batteria e individuarne l'addebito nella misura in cui sono stati realizzati entrambi i livelli.</span><span class="sxs-lookup"><span data-stu-id="108c3-186">It is possible to poll a battery and find that neither alert level has occurred, and poll the battery again and find it discharged to the extent that both levels have been achieved.</span></span> <span data-ttu-id="108c3-187">Questo può indicare che il polling non è abbastanza frequente.</span><span class="sxs-lookup"><span data-stu-id="108c3-187">This may indicate that you are not polling often enough.</span></span> <span data-ttu-id="108c3-188">Potrebbe inoltre indicare che la batteria non è in grado di sostenere un addebito per molto tempo e viene ricaricata più velocemente del previsto.</span><span class="sxs-lookup"><span data-stu-id="108c3-188">It may also indicate that the battery is unable to hold a charge for very long and is discharging more rapidly than you expected.</span></span> <span data-ttu-id="108c3-189">Una batteria di questo tipo può essere vicina alla fine della sua vita utile oppure potrebbe essere danneggiata.</span><span class="sxs-lookup"><span data-stu-id="108c3-189">Such a battery may be nearing the end of its useful life, or it may be damaged.</span></span>

## <a name="requirements"></a><span data-ttu-id="108c3-190">Requisiti</span><span class="sxs-lookup"><span data-stu-id="108c3-190">Requirements</span></span>



| <span data-ttu-id="108c3-191">Requisito</span><span class="sxs-lookup"><span data-stu-id="108c3-191">Requirement</span></span> | <span data-ttu-id="108c3-192">Valore</span><span class="sxs-lookup"><span data-stu-id="108c3-192">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="108c3-193">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="108c3-193">Minimum supported client</span></span><br/> | <span data-ttu-id="108c3-194">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="108c3-194">Windows XP \[desktop apps only\]</span></span><br/>                                                                                                                                                                                                                         |
| <span data-ttu-id="108c3-195">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="108c3-195">Minimum supported server</span></span><br/> | <span data-ttu-id="108c3-196">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="108c3-196">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                                                                                                                                                                                |
| <span data-ttu-id="108c3-197">Intestazione</span><span class="sxs-lookup"><span data-stu-id="108c3-197">Header</span></span><br/>                   | <dl> <span data-ttu-id="108c3-198"><dt>Poclass. h; </dt> <dt>Batclass. h in Windows server 2008 R2, Windows 7, Windows server 2008, Windows Vista, Windows server 2003 e Windows XP</dt></span><span class="sxs-lookup"><span data-stu-id="108c3-198"><dt>Poclass.h; </dt> <dt>Batclass.h on Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="108c3-199">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="108c3-199">See also</span></span>

<dl> <dt>

[<span data-ttu-id="108c3-200">**\_ \_ informazioni sulle query della batteria IOCTL \_**</span><span class="sxs-lookup"><span data-stu-id="108c3-200">**IOCTL\_BATTERY\_QUERY\_INFORMATION**</span></span>](ioctl-battery-query-information.md)
</dt> </dl>

 

 




