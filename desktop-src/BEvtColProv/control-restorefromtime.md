---
description: Ripristinare la configurazione attiva dell'agente di raccolta da un file di backup, selezionato da un timestamp.
ms.assetid: 3ee4156b-c68f-4c44-b9be-dd86e8f4b340
ms.tgt_platform: multiple
title: Metodo RestoreFromTime della classe Control
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Control.RestoreFromTime
api_type:
- COM
api_location:
- BEvtCol.exe
ms.openlocfilehash: 79b89c0c89e4954d8a641d037e08757f83cad618
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305303"
---
# <a name="restorefromtime-method-of-the-control-class"></a><span data-ttu-id="0d5d2-103">Metodo RestoreFromTime della classe Control</span><span class="sxs-lookup"><span data-stu-id="0d5d2-103">RestoreFromTime method of the Control class</span></span>

<span data-ttu-id="0d5d2-104">Ripristinare la configurazione attiva dell'agente di raccolta da un file di backup, selezionato da un timestamp.</span><span class="sxs-lookup"><span data-stu-id="0d5d2-104">Restore the active configuration of the collector from a backup file, selected by a timestamp.</span></span>

## <a name="syntax"></a><span data-ttu-id="0d5d2-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0d5d2-105">Syntax</span></span>


```mof
Uint32 RestoreFromTime(
  [in]  Uint32 TargetTimestampLow,
  [in]  Uint32 TargetTimestampHigh,
  [in]  Uint32 OldTimestampLow,
  [in]  Uint32 OldTimestampHigh,
  [out] Uint32 NewTimestampLow,
  [out] Uint32 NewTimestampHigh,
  [out] Uint32 OriginalTimestampLow,
  [out] Uint32 OriginalTimestampHigh,
  [out] string ErrorString,
  [out] string WarningString,
  [out] string InfoString,
  [out] uint32 ErrorType
);
```



## <a name="parameters"></a><span data-ttu-id="0d5d2-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="0d5d2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0d5d2-107">*TargetTimestampLow* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0d5d2-107">*TargetTimestampLow* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0d5d2-108">Ripristinare il file di backup in questo timestamp.</span><span class="sxs-lookup"><span data-stu-id="0d5d2-108">Restore to the backup file at this timestamp.</span></span> <span data-ttu-id="0d5d2-109">Questa è la parte bassa di [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span><span class="sxs-lookup"><span data-stu-id="0d5d2-109">This is the low part of [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span></span>

</dd> <dt>

<span data-ttu-id="0d5d2-110">*TargetTimestampHigh* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0d5d2-110">*TargetTimestampHigh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0d5d2-111">Ripristinare il file di backup in questo timestamp.</span><span class="sxs-lookup"><span data-stu-id="0d5d2-111">Restore to the backup file at this timestamp.</span></span> <span data-ttu-id="0d5d2-112">Si tratta della parte superiore di [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span><span class="sxs-lookup"><span data-stu-id="0d5d2-112">This is the high part of [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span></span>

</dd> <dt>

<span data-ttu-id="0d5d2-113">*OldTimestampLow* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0d5d2-113">*OldTimestampLow* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0d5d2-114">Timestamp del momento in cui è stata impostata la configurazione precedente.</span><span class="sxs-lookup"><span data-stu-id="0d5d2-114">The timestamp of when the previous configuration was set.</span></span> <span data-ttu-id="0d5d2-115">Se non è 0, Abilita il controllo di atomicità: la nuova configurazione verrà applicata solo se il timestamp della configurazione precedente corrisponde a (ovvero la configurazione non è stata modificata in un intervallo compreso tra).</span><span class="sxs-lookup"><span data-stu-id="0d5d2-115">If not 0, enables the atomicity check: the new configuration will be applied only if the timestamp of the old configuration matches (i.e. the configuration was not changed in between).</span></span> <span data-ttu-id="0d5d2-116">Questa è la parte bassa di [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span><span class="sxs-lookup"><span data-stu-id="0d5d2-116">This is the low part of [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span></span>

</dd> <dt>

<span data-ttu-id="0d5d2-117">*OldTimestampHigh* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0d5d2-117">*OldTimestampHigh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0d5d2-118">Timestamp del momento in cui è stata impostata la configurazione precedente.</span><span class="sxs-lookup"><span data-stu-id="0d5d2-118">The timestamp of when the previous configuration was set.</span></span> <span data-ttu-id="0d5d2-119">Se non è 0, Abilita il controllo di atomicità: la nuova configurazione verrà applicata solo se il timestamp della configurazione precedente corrisponde a (ovvero la configurazione non è stata modificata in un intervallo compreso tra).</span><span class="sxs-lookup"><span data-stu-id="0d5d2-119">If not 0, enables the atomicity check: the new configuration will be applied only if the timestamp of the old configuration matches (i.e. the configuration was not changed in between).</span></span> <span data-ttu-id="0d5d2-120">Si tratta della parte superiore di [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span><span class="sxs-lookup"><span data-stu-id="0d5d2-120">This is the high part of [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span></span>

</dd> <dt>

<span data-ttu-id="0d5d2-121">*NewTimestampLow* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="0d5d2-121">*NewTimestampLow* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0d5d2-122">Timestamp di quando è stata impostata la nuova configurazione, se la chiamata ha esito positivo.</span><span class="sxs-lookup"><span data-stu-id="0d5d2-122">The timestamp of when the new configuration was set, if the call succeeds.</span></span> <span data-ttu-id="0d5d2-123">Questa è la parte bassa di [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span><span class="sxs-lookup"><span data-stu-id="0d5d2-123">This is the low part of [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span></span>

</dd> <dt>

<span data-ttu-id="0d5d2-124">*NewTimestampHigh* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="0d5d2-124">*NewTimestampHigh* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0d5d2-125">Timestamp di quando è stata impostata la nuova configurazione, se la chiamata ha esito positivo.</span><span class="sxs-lookup"><span data-stu-id="0d5d2-125">The timestamp of when the new configuration was set, if the call succeeds.</span></span> <span data-ttu-id="0d5d2-126">Si tratta della parte superiore di [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span><span class="sxs-lookup"><span data-stu-id="0d5d2-126">This is the high part of [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span></span>

</dd> <dt>

<span data-ttu-id="0d5d2-127">*OriginalTimestampLow* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="0d5d2-127">*OriginalTimestampLow* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0d5d2-128">Timestamp originale del momento in cui la configurazione ripristinata è stata impostata per la prima volta.</span><span class="sxs-lookup"><span data-stu-id="0d5d2-128">The original timestamp of when the restored configuration was set for the first time.</span></span> <span data-ttu-id="0d5d2-129">Questa è la parte bassa di [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span><span class="sxs-lookup"><span data-stu-id="0d5d2-129">This is the low part of [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span></span>

</dd> <dt>

<span data-ttu-id="0d5d2-130">*OriginalTimestampHigh* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="0d5d2-130">*OriginalTimestampHigh* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0d5d2-131">Timestamp originale del momento in cui la configurazione ripristinata è stata impostata per la prima volta.</span><span class="sxs-lookup"><span data-stu-id="0d5d2-131">The original timestamp of when the restored configuration was set for the first time.</span></span> <span data-ttu-id="0d5d2-132">Si tratta della parte superiore di [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span><span class="sxs-lookup"><span data-stu-id="0d5d2-132">This is the high part of [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span></span>

</dd> <dt>

<span data-ttu-id="0d5d2-133">*ErrorString* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="0d5d2-133">*ErrorString* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0d5d2-134">Stringa di testo con la spiegazione dell'errore.</span><span class="sxs-lookup"><span data-stu-id="0d5d2-134">The text string with explanation of the error.</span></span>

</dd> <dt>

<span data-ttu-id="0d5d2-135">*WarningString* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="0d5d2-135">*WarningString* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0d5d2-136">Stringa di testo con avvisi.</span><span class="sxs-lookup"><span data-stu-id="0d5d2-136">The text string with warnings.</span></span>

</dd> <dt>

<span data-ttu-id="0d5d2-137">*InfoString* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="0d5d2-137">*InfoString* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0d5d2-138">Stringa di testo con le informazioni sulla configurazione.</span><span class="sxs-lookup"><span data-stu-id="0d5d2-138">The text string with information about the configuration.</span></span>

</dd> <dt>

<span data-ttu-id="0d5d2-139">*ErrorType* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="0d5d2-139">*ErrorType* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0d5d2-140">Tipo di errore: si noti che 0 o assente indica l'esito positivo.</span><span class="sxs-lookup"><span data-stu-id="0d5d2-140">The type of the error: note that 0 or absent indicates success.</span></span>

<dt>

<span data-ttu-id="0d5d2-141">0</span><span class="sxs-lookup"><span data-stu-id="0d5d2-141">0</span></span>
</dt> <dd>

<span data-ttu-id="0d5d2-142">Esito positivo.</span><span class="sxs-lookup"><span data-stu-id="0d5d2-142">Success.</span></span>

</dd> <dt>

<span data-ttu-id="0d5d2-143">1</span><span class="sxs-lookup"><span data-stu-id="0d5d2-143">1</span></span>
</dt> <dd>

<span data-ttu-id="0d5d2-144">formato di argomento non valido</span><span class="sxs-lookup"><span data-stu-id="0d5d2-144">bad argument format</span></span>

</dd> <dt>

<span data-ttu-id="0d5d2-145">2</span><span class="sxs-lookup"><span data-stu-id="0d5d2-145">2</span></span>
</dt> <dd>

<span data-ttu-id="0d5d2-146">valore argomento non valido</span><span class="sxs-lookup"><span data-stu-id="0d5d2-146">bad argument value</span></span>

</dd> <dt>

<span data-ttu-id="0d5d2-147">3</span><span class="sxs-lookup"><span data-stu-id="0d5d2-147">3</span></span>
</dt> <dd>

<span data-ttu-id="0d5d2-148">errore di apertura della risorsa (socket)</span><span class="sxs-lookup"><span data-stu-id="0d5d2-148">resource (socket) open error</span></span>

</dd> <dt>

<span data-ttu-id="0d5d2-149">4</span><span class="sxs-lookup"><span data-stu-id="0d5d2-149">4</span></span>
</dt> <dd>

<span data-ttu-id="0d5d2-150">errore di persistenza (scrittura file)</span><span class="sxs-lookup"><span data-stu-id="0d5d2-150">persistence (file write) error</span></span>

</dd> <dt>

<span data-ttu-id="0d5d2-151">5</span><span class="sxs-lookup"><span data-stu-id="0d5d2-151">5</span></span>
</dt> <dd>

<span data-ttu-id="0d5d2-152">errore di atomicità (il timestamp precedente non corrisponde)</span><span class="sxs-lookup"><span data-stu-id="0d5d2-152">atomicity error (the old timestamp didn't match)</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0d5d2-153">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0d5d2-153">Return value</span></span>

<dl> <dt>


</dt> <dd>

<span data-ttu-id="0d5d2-154">0</span><span class="sxs-lookup"><span data-stu-id="0d5d2-154">0</span></span>

<span data-ttu-id="0d5d2-155">Errore</span><span class="sxs-lookup"><span data-stu-id="0d5d2-155">Failure</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="0d5d2-156">1</span><span class="sxs-lookup"><span data-stu-id="0d5d2-156">1</span></span>

<span data-ttu-id="0d5d2-157">Operazione completata</span><span class="sxs-lookup"><span data-stu-id="0d5d2-157">Success</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0d5d2-158">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0d5d2-158">Requirements</span></span>



| <span data-ttu-id="0d5d2-159">Requisito</span><span class="sxs-lookup"><span data-stu-id="0d5d2-159">Requirement</span></span> | <span data-ttu-id="0d5d2-160">Valore</span><span class="sxs-lookup"><span data-stu-id="0d5d2-160">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0d5d2-161">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0d5d2-161">Minimum supported client</span></span><br/> | <span data-ttu-id="0d5d2-162">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="0d5d2-162">Windows 10 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="0d5d2-163">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0d5d2-163">Minimum supported server</span></span><br/> | <span data-ttu-id="0d5d2-164">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="0d5d2-164">Windows Server 2016</span></span><br/>                                                                       |
| <span data-ttu-id="0d5d2-165">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="0d5d2-165">Namespace</span></span><br/>                | <span data-ttu-id="0d5d2-166">Radice \\ Microsoft \\ Windows \\ BootEventCollector</span><span class="sxs-lookup"><span data-stu-id="0d5d2-166">Root\\Microsoft\\Windows\\BootEventCollector</span></span><br/>                                              |
| <span data-ttu-id="0d5d2-167">MOF</span><span class="sxs-lookup"><span data-stu-id="0d5d2-167">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0d5d2-168"><dt>BootEventCollectorWMI. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0d5d2-168"><dt>BootEventCollectorWMI.mof</dt></span></span> </dl> |
| <span data-ttu-id="0d5d2-169">DLL</span><span class="sxs-lookup"><span data-stu-id="0d5d2-169">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0d5d2-170"><dt>BEvtCol.exe</dt></span><span class="sxs-lookup"><span data-stu-id="0d5d2-170"><dt>BEvtCol.exe</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="0d5d2-171">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0d5d2-171">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0d5d2-172">**Control**</span><span class="sxs-lookup"><span data-stu-id="0d5d2-172">**Control**</span></span>](control.md)
</dt> </dl>

 

