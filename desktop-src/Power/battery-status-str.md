---
description: Contiene lo stato corrente della batteria.
ms.assetid: 514906a1-9d7a-40cb-9798-84f6b93d7bfe
title: Struttura BATTERY_STATUS (Poclass. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- BATTERY_STATUS
api_type:
- HeaderDef
api_location:
- Poclass.h
- Batclass.h
ms.openlocfilehash: d6e68f5cec0215687fe4fde66698ea1be0d62c6e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106312059"
---
# <a name="battery_status-structure"></a><span data-ttu-id="53fe6-103">\_Struttura dello stato della batteria</span><span class="sxs-lookup"><span data-stu-id="53fe6-103">BATTERY\_STATUS structure</span></span>

<span data-ttu-id="53fe6-104">Contiene lo stato corrente della batteria.</span><span class="sxs-lookup"><span data-stu-id="53fe6-104">Contains the current state of the battery.</span></span> <span data-ttu-id="53fe6-105">Questa struttura viene utilizzata dal codice di controllo [**\_ \_ \_ dello stato delle query della batteria IOCTL**](ioctl-battery-query-status.md) .</span><span class="sxs-lookup"><span data-stu-id="53fe6-105">This structure is used by the [**IOCTL\_BATTERY\_QUERY\_STATUS**](ioctl-battery-query-status.md) control code.</span></span>

## <a name="syntax"></a><span data-ttu-id="53fe6-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="53fe6-106">Syntax</span></span>


```C++
typedef struct _BATTERY_STATUS {
  ULONG PowerState;
  ULONG Capacity;
  ULONG Voltage;
  LONG  Rate;
} BATTERY_STATUS, *PBATTERY_STATUS;
```



## <a name="members"></a><span data-ttu-id="53fe6-107">Members</span><span class="sxs-lookup"><span data-stu-id="53fe6-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="53fe6-108">**PowerState**</span><span class="sxs-lookup"><span data-stu-id="53fe6-108">**PowerState**</span></span>
</dt> <dd>

<span data-ttu-id="53fe6-109">Stato della batteria.</span><span class="sxs-lookup"><span data-stu-id="53fe6-109">The battery state.</span></span> <span data-ttu-id="53fe6-110">Questo membro può essere zero, uno o più dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="53fe6-110">This member can be zero, one, or more of the following values.</span></span>



| <span data-ttu-id="53fe6-111">Valore</span><span class="sxs-lookup"><span data-stu-id="53fe6-111">Value</span></span>                                                                                                                                                                                                                                                   | <span data-ttu-id="53fe6-112">Significato</span><span class="sxs-lookup"><span data-stu-id="53fe6-112">Meaning</span></span>                                                                                              |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| <span id="BATTERY_CHARGING"></span><span id="battery_charging"></span><dl> <span data-ttu-id="53fe6-113"><dt>**Batteria \_ CARICAMENTO**</dt> di <dt>0x00000004</dt></span><span class="sxs-lookup"><span data-stu-id="53fe6-113"><dt>**BATTERY\_CHARGING**</dt> <dt>0x00000004</dt></span></span> </dl>                  | <span data-ttu-id="53fe6-114">Indica che la batteria è in fase di caricamento.</span><span class="sxs-lookup"><span data-stu-id="53fe6-114">Indicates that the battery is currently charging.</span></span><br/>                                         |
| <span id="BATTERY_CRITICAL"></span><span id="battery_critical"></span><dl> <span data-ttu-id="53fe6-115"><dt>**Batteria \_**</dt> <dt>0x00000008</dt> critico</span><span class="sxs-lookup"><span data-stu-id="53fe6-115"><dt>**BATTERY\_CRITICAL**</dt> <dt>0x00000008</dt></span></span> </dl>                  | <span data-ttu-id="53fe6-116">Indica che l'errore della batteria è imminente.</span><span class="sxs-lookup"><span data-stu-id="53fe6-116">Indicates that battery failure is imminent.</span></span> <span data-ttu-id="53fe6-117">Per altre informazioni, vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="53fe6-117">See the Remarks section for more information.</span></span><br/> |
| <span id="BATTERY_DISCHARGING"></span><span id="battery_discharging"></span><dl> <span data-ttu-id="53fe6-118"><dt>**Batteria \_ Discaricamento**</dt> di <dt>0x00000002</dt></span><span class="sxs-lookup"><span data-stu-id="53fe6-118"><dt>**BATTERY\_DISCHARGING**</dt> <dt>0x00000002</dt></span></span> </dl>         | <span data-ttu-id="53fe6-119">Indica che la batteria è in fase di disattivazione.</span><span class="sxs-lookup"><span data-stu-id="53fe6-119">Indicates that the battery is currently discharging.</span></span><br/>                                      |
| <span id="BATTERY_POWER_ON_LINE"></span><span id="battery_power_on_line"></span><dl> <span data-ttu-id="53fe6-120"><dt>**Batteria \_ POWER \_ on \_ line**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="53fe6-120"><dt>**BATTERY\_POWER\_ON\_LINE**</dt> <dt>0x00000001</dt></span></span> </dl> | <span data-ttu-id="53fe6-121">Indica che il sistema ha accesso alla rete elettrica, quindi nessuna batteria viene ricaricata.</span><span class="sxs-lookup"><span data-stu-id="53fe6-121">Indicates that the system has access to AC power, so no batteries are being discharged.</span></span><br/>   |



 

</dd> <dt>

<span data-ttu-id="53fe6-122">**Capacity**</span><span class="sxs-lookup"><span data-stu-id="53fe6-122">**Capacity**</span></span>
</dt> <dd>

<span data-ttu-id="53fe6-123">Capacità corrente della batteria, in mWh (o relativa).</span><span class="sxs-lookup"><span data-stu-id="53fe6-123">The current battery capacity, in mWh (or relative).</span></span> <span data-ttu-id="53fe6-124">Questo valore può essere usato per generare una visualizzazione "misuratore di gas" dividendo il membro **FullChargedCapacity** della struttura delle [**\_ informazioni sulla batteria**](battery-information-str.md) .</span><span class="sxs-lookup"><span data-stu-id="53fe6-124">This value can be used to generate a "gas gauge" display by dividing it by **FullChargedCapacity** member of the [**BATTERY\_INFORMATION**](battery-information-str.md) structure.</span></span> <span data-ttu-id="53fe6-125">Se la capacità non è disponibile, questo membro è una \_ capacità sconosciuta a batteria \_ .</span><span class="sxs-lookup"><span data-stu-id="53fe6-125">If the capacity is unavailable, this member is BATTERY\_UNKNOWN\_CAPACITY.</span></span>

</dd> <dt>

<span data-ttu-id="53fe6-126">**Tensione**</span><span class="sxs-lookup"><span data-stu-id="53fe6-126">**Voltage**</span></span>
</dt> <dd>

<span data-ttu-id="53fe6-127">Tensione della batteria corrente nei terminali della batteria, in millivolt (MV).</span><span class="sxs-lookup"><span data-stu-id="53fe6-127">The current battery voltage across the battery terminals, in millivolts (mv).</span></span> <span data-ttu-id="53fe6-128">Se la tensione non è disponibile, il membro è una \_ tensione sconosciuta a batteria \_ .</span><span class="sxs-lookup"><span data-stu-id="53fe6-128">If the voltage is unavailable, this member is BATTERY\_UNKNOWN\_VOLTAGE.</span></span>

</dd> <dt>

<span data-ttu-id="53fe6-129">**Frequenza di campionamento**</span><span class="sxs-lookup"><span data-stu-id="53fe6-129">**Rate**</span></span>
</dt> <dd>

<span data-ttu-id="53fe6-130">Frequenza corrente di carica o scaricamento della batteria.</span><span class="sxs-lookup"><span data-stu-id="53fe6-130">The current rate of battery charge or discharge.</span></span> <span data-ttu-id="53fe6-131">Questo valore sarà in milliwatt, a meno che le informazioni sulla frequenza della batteria siano relative, nel qual caso saranno in unità arbitrarie all'ora.</span><span class="sxs-lookup"><span data-stu-id="53fe6-131">This value will be in milliwatts unless the battery rate information is relative, in which case it will be in arbitrary units per hour.</span></span> <span data-ttu-id="53fe6-132">Per determinare se le informazioni sulla batteria sono relative, esaminare il \_ flag relativo di capacità della batteria \_ nel membro delle **funzionalità** della struttura delle [**\_ informazioni sulla batteria**](battery-information-str.md) .</span><span class="sxs-lookup"><span data-stu-id="53fe6-132">To determine if battery information is relative, examine the BATTERY\_CAPACITY\_RELATIVE flag in the **Capabilities** member of the [**BATTERY\_INFORMATION**](battery-information-str.md) structure.</span></span> <span data-ttu-id="53fe6-133">Un tasso positivo diverso da zero indica una ricarica; una frequenza negativa indica la discaricamento.</span><span class="sxs-lookup"><span data-stu-id="53fe6-133">A nonzero, positive rate indicates charging; a negative rate indicates discharging.</span></span> <span data-ttu-id="53fe6-134">Alcune batterie segnalano solo le tariffe di discarico.</span><span class="sxs-lookup"><span data-stu-id="53fe6-134">Some batteries report only discharging rates.</span></span> <span data-ttu-id="53fe6-135">Se la frequenza non è disponibile, il membro è una \_ frequenza sconosciuta della batteria \_ .</span><span class="sxs-lookup"><span data-stu-id="53fe6-135">If the rate is unavailable, this member is BATTERY\_UNKNOWN\_RATE.</span></span> <span data-ttu-id="53fe6-136">Se viene modificato lo stato della batteria o dell'alimentazione, è possibile che la velocità diventi disponibile.</span><span class="sxs-lookup"><span data-stu-id="53fe6-136">If the state of the battery or power source changes, the rate may become available.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="53fe6-137">Commenti</span><span class="sxs-lookup"><span data-stu-id="53fe6-137">Remarks</span></span>

<span data-ttu-id="53fe6-138">Il \_ flag critico della batteria nel membro **PowerState** della struttura indica una condizione hardware "batteria critica".</span><span class="sxs-lookup"><span data-stu-id="53fe6-138">The BATTERY\_CRITICAL flag in the **PowerState** member of this structure indicates a hardware "battery critical" condition.</span></span> <span data-ttu-id="53fe6-139">Questo livello critico viene impostato dal produttore della batteria, non dall'utente nell'"allarme batteria critica".</span><span class="sxs-lookup"><span data-stu-id="53fe6-139">This critical level is set by the battery manufacturer, not by the user in the "critical battery alarm."</span></span> <span data-ttu-id="53fe6-140">In genere significa che il sistema di batteria ha calcolato che la batteria è completamente scaricata e qualsiasi potenza disegnata è superiore a quanto previsto.</span><span class="sxs-lookup"><span data-stu-id="53fe6-140">It generally means that the battery system has calculated that the battery is totally drained, and any power being drawn is beyond what is expected.</span></span>

## <a name="requirements"></a><span data-ttu-id="53fe6-141">Requisiti</span><span class="sxs-lookup"><span data-stu-id="53fe6-141">Requirements</span></span>



| <span data-ttu-id="53fe6-142">Requisito</span><span class="sxs-lookup"><span data-stu-id="53fe6-142">Requirement</span></span> | <span data-ttu-id="53fe6-143">Valore</span><span class="sxs-lookup"><span data-stu-id="53fe6-143">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="53fe6-144">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="53fe6-144">Minimum supported client</span></span><br/> | <span data-ttu-id="53fe6-145">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="53fe6-145">Windows XP \[desktop apps only\]</span></span><br/>                                                                                                                                                                                                                         |
| <span data-ttu-id="53fe6-146">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="53fe6-146">Minimum supported server</span></span><br/> | <span data-ttu-id="53fe6-147">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="53fe6-147">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                                                                                                                                                                                |
| <span data-ttu-id="53fe6-148">Intestazione</span><span class="sxs-lookup"><span data-stu-id="53fe6-148">Header</span></span><br/>                   | <dl> <span data-ttu-id="53fe6-149"><dt>Poclass. h; </dt> <dt>Batclass. h in Windows server 2008 R2, Windows 7, Windows server 2008, Windows Vista, Windows server 2003 e Windows XP</dt></span><span class="sxs-lookup"><span data-stu-id="53fe6-149"><dt>Poclass.h; </dt> <dt>Batclass.h on Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="53fe6-150">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="53fe6-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="53fe6-151">**\_informazioni sulla batteria**</span><span class="sxs-lookup"><span data-stu-id="53fe6-151">**BATTERY\_INFORMATION**</span></span>](battery-information-str.md)
</dt> <dt>

[<span data-ttu-id="53fe6-152">**\_stato della \_ query della batteria IOCTL \_**</span><span class="sxs-lookup"><span data-stu-id="53fe6-152">**IOCTL\_BATTERY\_QUERY\_STATUS**</span></span>](ioctl-battery-query-status.md)
</dt> </dl>

 

 




