---
description: Contiene informazioni sulle condizioni in base alle quali deve essere recuperato lo stato della batteria.
ms.assetid: 1750fe0f-ba3d-4118-938c-789c6d62c3f7
title: Struttura BATTERY_WAIT_STATUS (Poclass. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- BATTERY_WAIT_STATUS
api_type:
- HeaderDef
api_location:
- Poclass.h
- Batclass.h
ms.openlocfilehash: 08d1e3b85d22122426f1e4648f47a808468bfb8f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106312058"
---
# <a name="battery_wait_status-structure"></a><span data-ttu-id="4027c-103">\_ \_ Struttura dello stato di attesa della batteria</span><span class="sxs-lookup"><span data-stu-id="4027c-103">BATTERY\_WAIT\_STATUS structure</span></span>

<span data-ttu-id="4027c-104">Contiene informazioni sulle condizioni in base alle quali deve essere recuperato lo stato della batteria.</span><span class="sxs-lookup"><span data-stu-id="4027c-104">Contains information about the conditions under which the battery status is to be retrieved.</span></span> <span data-ttu-id="4027c-105">Questa struttura viene utilizzata dal codice di controllo [**\_ \_ \_ dello stato delle query della batteria IOCTL**](ioctl-battery-query-status.md) .</span><span class="sxs-lookup"><span data-stu-id="4027c-105">This structure is used by the [**IOCTL\_BATTERY\_QUERY\_STATUS**](ioctl-battery-query-status.md) control code.</span></span>

## <a name="syntax"></a><span data-ttu-id="4027c-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4027c-106">Syntax</span></span>


```C++
typedef struct _BATTERY_WAIT_STATUS {
  ULONG BatteryTag;
  ULONG Timeout;
  ULONG PowerState;
  ULONG LowCapacity;
  ULONG HighCapacity;
} BATTERY_WAIT_STATUS, *PBATTERY_WAIT_STATUS;
```



## <a name="members"></a><span data-ttu-id="4027c-107">Members</span><span class="sxs-lookup"><span data-stu-id="4027c-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="4027c-108">**BatteryTag**</span><span class="sxs-lookup"><span data-stu-id="4027c-108">**BatteryTag**</span></span>
</dt> <dd>

<span data-ttu-id="4027c-109">Tag della batteria corrente per la batteria.</span><span class="sxs-lookup"><span data-stu-id="4027c-109">The current battery tag for the battery.</span></span> <span data-ttu-id="4027c-110">Possono essere restituite solo le informazioni per una batteria corrispondente al tag.</span><span class="sxs-lookup"><span data-stu-id="4027c-110">Only information for a battery matching the tag can be returned.</span></span> <span data-ttu-id="4027c-111">Ogni volta che questo valore non corrisponde al tag corrente della batteria, l'operazione [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) ha esito negativo e viene visualizzato un codice di errore \_ non trovato nel file di errore \_ \_ , che indica al chiamante che la batteria per cui ha un tag non è più installata. il chiamante può scegliere di usare l'operazione di [**tag di \_ query della batteria \_ \_ IOCTL**](ioctl-battery-query-tag.md) per determinare il tag della batteria appena installata.</span><span class="sxs-lookup"><span data-stu-id="4027c-111">Whenever this value does not match the battery's current tag, the [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) operation will fail with an error code of ERROR\_FILE\_NOT\_FOUND, which indicates to the caller that the battery for which it has a tag is no longer installed The caller may opt to use the [**IOCTL\_BATTERY\_QUERY\_TAG**](ioctl-battery-query-tag.md) operation to determine the tag of the newly installed battery, if any.</span></span> <span data-ttu-id="4027c-112">Inoltre, se la richiesta è in corso quando la batteria viene rimossa o il tag viene modificato, l'operazione viene interrotta con lo stato del file di errore \_ \_ non \_ trovato.</span><span class="sxs-lookup"><span data-stu-id="4027c-112">In addition, if the request is in progress when the battery is removed, or the tag changes, the operation is aborted with the status of ERROR\_FILE\_NOT\_FOUND.</span></span> <span data-ttu-id="4027c-113">Per ulteriori informazioni, vedere la pagina relativa ai [tag della batteria](battery-information.md) .</span><span class="sxs-lookup"><span data-stu-id="4027c-113">(See [Battery Tags](battery-information.md) for more information.)</span></span>

</dd> <dt>

<span data-ttu-id="4027c-114">**Timeout**</span><span class="sxs-lookup"><span data-stu-id="4027c-114">**Timeout**</span></span>
</dt> <dd>

<span data-ttu-id="4027c-115">Il numero di millisecondi di attesa della richiesta per la condizione specificata dai membri **PowerState**, **LowCapacity** e **HighCapacity** prima del completamento.</span><span class="sxs-lookup"><span data-stu-id="4027c-115">The number of milliseconds the request will wait for the condition specified by the **PowerState**, **LowCapacity**, and **HighCapacity** members before completing.</span></span> <span data-ttu-id="4027c-116">Un valore pari a-1 indica che la richiesta attende indefinitamente che le condizioni vengano soddisfatte.</span><span class="sxs-lookup"><span data-stu-id="4027c-116">A value of -1 indicates that the request will wait indefinitely for the conditions to be satisfied.</span></span> <span data-ttu-id="4027c-117">Un valore pari a zero indica che le informazioni sulla batteria richieste devono essere restituite immediatamente, indipendentemente dalle altre condizioni.</span><span class="sxs-lookup"><span data-stu-id="4027c-117">A value of zero indicates that the requested battery information is to be returned immediately, regardless of the other conditions.</span></span> <span data-ttu-id="4027c-118">Qualsiasi altro valore indica che la richiesta deve attendere tale periodo di tempo o fino a quando non viene soddisfatta una delle altre condizioni.</span><span class="sxs-lookup"><span data-stu-id="4027c-118">Any other value indicates that the request should wait that length of time, or until any one of the other conditions is satisfied.</span></span>

<span data-ttu-id="4027c-119">Se il computer è entrato in modalità sospensione, l'orologio continuerà a essere eseguito, ma l'esaurimento del conteggio non riattiverà il computer.</span><span class="sxs-lookup"><span data-stu-id="4027c-119">If the computer has entered sleep mode, the clock will continue to run, but exhausting the count will not wake the computer up.</span></span> <span data-ttu-id="4027c-120">Se il conteggio viene esaurito quando il computer viene riattivato e le altre condizioni vengono soddisfatte, la chiamata verrà immediatamente restituita in fase di riattivazione.</span><span class="sxs-lookup"><span data-stu-id="4027c-120">If the count is exhausted when the computer is awoken, and other conditions are satisfied, the call will return immediately on awakening.</span></span>

</dd> <dt>

<span data-ttu-id="4027c-121">**PowerState**</span><span class="sxs-lookup"><span data-stu-id="4027c-121">**PowerState**</span></span>
</dt> <dd>

<span data-ttu-id="4027c-122">Zero, uno o più dei seguenti bit di stato, che indicano lo stato della batteria.</span><span class="sxs-lookup"><span data-stu-id="4027c-122">Zero, one, or more of the following status bits, which indicate the state of the battery.</span></span> <span data-ttu-id="4027c-123">È identico al membro **PowerState** della struttura [**\_ dello stato della batteria**](battery-status-str.md) .</span><span class="sxs-lookup"><span data-stu-id="4027c-123">It is identical to the **PowerState** member of the [**BATTERY\_STATUS**](battery-status-str.md) structure.</span></span>



| <span data-ttu-id="4027c-124">Valore</span><span class="sxs-lookup"><span data-stu-id="4027c-124">Value</span></span>                                                                                                                                                                                                                                                   | <span data-ttu-id="4027c-125">Significato</span><span class="sxs-lookup"><span data-stu-id="4027c-125">Meaning</span></span>                                                                                              |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| <span id="BATTERY_CHARGING"></span><span id="battery_charging"></span><dl> <span data-ttu-id="4027c-126"><dt>**Batteria \_ CARICAMENTO**</dt> di <dt>0x00000004</dt></span><span class="sxs-lookup"><span data-stu-id="4027c-126"><dt>**BATTERY\_CHARGING**</dt> <dt>0x00000004</dt></span></span> </dl>                  | <span data-ttu-id="4027c-127">Indica che la batteria è in fase di caricamento.</span><span class="sxs-lookup"><span data-stu-id="4027c-127">Indicates that the battery is currently charging.</span></span><br/>                                         |
| <span id="BATTERY_CRITICAL"></span><span id="battery_critical"></span><dl> <span data-ttu-id="4027c-128"><dt>**Batteria \_**</dt> <dt>0x00000008</dt> critico</span><span class="sxs-lookup"><span data-stu-id="4027c-128"><dt>**BATTERY\_CRITICAL**</dt> <dt>0x00000008</dt></span></span> </dl>                  | <span data-ttu-id="4027c-129">Indica che l'errore della batteria è imminente.</span><span class="sxs-lookup"><span data-stu-id="4027c-129">Indicates that battery failure is imminent.</span></span> <span data-ttu-id="4027c-130">Per altre informazioni, vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="4027c-130">See the Remarks section for more information.</span></span><br/> |
| <span id="BATTERY_DISCHARGING"></span><span id="battery_discharging"></span><dl> <span data-ttu-id="4027c-131"><dt>**Batteria \_ Discaricamento**</dt> di <dt>0x00000002</dt></span><span class="sxs-lookup"><span data-stu-id="4027c-131"><dt>**BATTERY\_DISCHARGING**</dt> <dt>0x00000002</dt></span></span> </dl>         | <span data-ttu-id="4027c-132">Indica che la batteria è in fase di disattivazione.</span><span class="sxs-lookup"><span data-stu-id="4027c-132">Indicates that the battery is currently discharging.</span></span><br/>                                      |
| <span id="BATTERY_POWER_ON_LINE"></span><span id="battery_power_on_line"></span><dl> <span data-ttu-id="4027c-133"><dt>**Batteria \_ POWER \_ on \_ line**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="4027c-133"><dt>**BATTERY\_POWER\_ON\_LINE**</dt> <dt>0x00000001</dt></span></span> </dl> | <span data-ttu-id="4027c-134">Indica che la batteria ha accesso alla rete elettrica.</span><span class="sxs-lookup"><span data-stu-id="4027c-134">Indicates that the battery has access to AC power.</span></span><br/>                                        |



 

</dd> <dt>

<span data-ttu-id="4027c-135">**LowCapacity**</span><span class="sxs-lookup"><span data-stu-id="4027c-135">**LowCapacity**</span></span>
</dt> <dd>

<span data-ttu-id="4027c-136">Capacità corrente della batteria, in mWh (o relativa).</span><span class="sxs-lookup"><span data-stu-id="4027c-136">The current battery capacity, in mWh (or relative).</span></span> <span data-ttu-id="4027c-137">Questo valore è identico al membro **Capacity** della [**struttura \_ dello stato della batteria**](battery-status-str.md) .</span><span class="sxs-lookup"><span data-stu-id="4027c-137">This value is identical to the **Capacity** member of the [**BATTERY\_STATUS**](battery-status-str.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="4027c-138">**HighCapacity**</span><span class="sxs-lookup"><span data-stu-id="4027c-138">**HighCapacity**</span></span>
</dt> <dd>

<span data-ttu-id="4027c-139">Capacità corrente della batteria, in mWh (o relativa).</span><span class="sxs-lookup"><span data-stu-id="4027c-139">The current battery capacity, in mWh (or relative).</span></span> <span data-ttu-id="4027c-140">Questo valore è identico al membro **Capacity** della [**struttura \_ dello stato della batteria**](battery-status-str.md) .</span><span class="sxs-lookup"><span data-stu-id="4027c-140">This value is identical to the **Capacity** member of the [**BATTERY\_STATUS**](battery-status-str.md) structure.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4027c-141">Commenti</span><span class="sxs-lookup"><span data-stu-id="4027c-141">Remarks</span></span>

<span data-ttu-id="4027c-142">Le richieste di informazioni sulla batteria vengono posticipate fino a quando non si verifica una delle condizioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="4027c-142">Requests for battery information are postponed until one of the following occurs:</span></span>

-   <span data-ttu-id="4027c-143">Scade il timeout (presupponendo che il **timeout** non sia-1).</span><span class="sxs-lookup"><span data-stu-id="4027c-143">The time-out expires (assuming **Timeout** is not -1).</span></span>
-   <span data-ttu-id="4027c-144">Lo stato corrente della batteria non corrisponde a **PowerState**.</span><span class="sxs-lookup"><span data-stu-id="4027c-144">The battery's current status does not match **PowerState**.</span></span>
-   <span data-ttu-id="4027c-145">La capacità della batteria è inferiore a **LowCapacity**.</span><span class="sxs-lookup"><span data-stu-id="4027c-145">The battery's capacity is below **LowCapacity**.</span></span>
-   <span data-ttu-id="4027c-146">La capacità della batteria è superiore a **HighCapacity**.</span><span class="sxs-lookup"><span data-stu-id="4027c-146">The battery's capacity is above **HighCapacity**.</span></span>
-   <span data-ttu-id="4027c-147">Il tag della batteria viene modificato.</span><span class="sxs-lookup"><span data-stu-id="4027c-147">The battery tag changes.</span></span>

<span data-ttu-id="4027c-148">Quando viene soddisfatta una di queste condizioni, i dati vengono raccolti e l'operazione restituisce.</span><span class="sxs-lookup"><span data-stu-id="4027c-148">When any one of these conditions is satisfied, the data is collected and the operation returns.</span></span> <span data-ttu-id="4027c-149">Questo consente alle applicazioni di monitorare le informazioni tipiche della batteria dinamica senza eseguire il polling del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="4027c-149">This allows applications to monitor typical dynamic battery information without polling the device.</span></span>

<span data-ttu-id="4027c-150">Prima di usare una delle due condizioni di capacità, assicurarsi che la batteria li supporti usando il codice di controllo [**\_ \_ \_ dello stato di query della batteria IOCTL**](ioctl-battery-query-status.md) con un timeout di zero.</span><span class="sxs-lookup"><span data-stu-id="4027c-150">Before using either of the two Capacity conditions, make sure the battery supports them by using the [**IOCTL\_BATTERY\_QUERY\_STATUS**](ioctl-battery-query-status.md) control code with a time-out of zero.</span></span> <span data-ttu-id="4027c-151">Esaminare i risultati per determinare se il membro di **capacità** è supportato (ovvero la \_ capacità sconosciuta della batteria \_ ).</span><span class="sxs-lookup"><span data-stu-id="4027c-151">Examine the results to determine if the **Capacity** member is supported (that is, not BATTERY\_UNKNOWN\_CAPACITY).</span></span>

## <a name="requirements"></a><span data-ttu-id="4027c-152">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4027c-152">Requirements</span></span>



| <span data-ttu-id="4027c-153">Requisito</span><span class="sxs-lookup"><span data-stu-id="4027c-153">Requirement</span></span> | <span data-ttu-id="4027c-154">Valore</span><span class="sxs-lookup"><span data-stu-id="4027c-154">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4027c-155">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4027c-155">Minimum supported client</span></span><br/> | <span data-ttu-id="4027c-156">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="4027c-156">Windows XP \[desktop apps only\]</span></span><br/>                                                                                                                                                                                                                         |
| <span data-ttu-id="4027c-157">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4027c-157">Minimum supported server</span></span><br/> | <span data-ttu-id="4027c-158">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="4027c-158">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                                                                                                                                                                                |
| <span data-ttu-id="4027c-159">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4027c-159">Header</span></span><br/>                   | <dl> <span data-ttu-id="4027c-160"><dt>Poclass. h; </dt> <dt>Batclass. h in Windows server 2008 R2, Windows 7, Windows server 2008, Windows Vista, Windows server 2003 e Windows XP</dt></span><span class="sxs-lookup"><span data-stu-id="4027c-160"><dt>Poclass.h; </dt> <dt>Batclass.h on Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4027c-161">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4027c-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4027c-162">**stato della batteria \_**</span><span class="sxs-lookup"><span data-stu-id="4027c-162">**BATTERY\_STATUS**</span></span>](battery-status-str.md)
</dt> <dt>

[<span data-ttu-id="4027c-163">**\_stato della \_ query della batteria IOCTL \_**</span><span class="sxs-lookup"><span data-stu-id="4027c-163">**IOCTL\_BATTERY\_QUERY\_STATUS**</span></span>](ioctl-battery-query-status.md)
</dt> <dt>

[<span data-ttu-id="4027c-164">**\_tag di \_ query della batteria IOCTL \_**</span><span class="sxs-lookup"><span data-stu-id="4027c-164">**IOCTL\_BATTERY\_QUERY\_TAG**</span></span>](ioctl-battery-query-tag.md)
</dt> </dl>

 

