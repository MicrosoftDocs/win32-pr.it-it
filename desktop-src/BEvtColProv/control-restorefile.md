---
description: Ripristinare la configurazione attiva dell'agente di raccolta da un file di backup.
ms.assetid: b59b04a5-d2b3-4299-8347-5026b982dc02
ms.tgt_platform: multiple
title: Metodo RestoreFile della classe Control
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Control.RestoreFile
api_type:
- COM
api_location:
- BEvtCol.exe
ms.openlocfilehash: 330486da86c9cac5c5f700d2aea91e0844fdca09
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103965911"
---
# <a name="restorefile-method-of-the-control-class"></a><span data-ttu-id="8ed14-103">Metodo RestoreFile della classe Control</span><span class="sxs-lookup"><span data-stu-id="8ed14-103">RestoreFile method of the Control class</span></span>

<span data-ttu-id="8ed14-104">Ripristinare la configurazione attiva dell'agente di raccolta da un file di backup.</span><span class="sxs-lookup"><span data-stu-id="8ed14-104">Restore the active configuration of the collector from a backup file.</span></span>

## <a name="syntax"></a><span data-ttu-id="8ed14-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8ed14-105">Syntax</span></span>


```mof
Uint32 RestoreFile(
  [in]  string File,
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



## <a name="parameters"></a><span data-ttu-id="8ed14-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="8ed14-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8ed14-107">*File* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8ed14-107">*File* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8ed14-108">Nome del file di backup da ripristinare dall'elenco restituito da ListBackups ().</span><span class="sxs-lookup"><span data-stu-id="8ed14-108">Name of the backup file to restore, from the list returned by ListBackups().</span></span>

</dd> <dt>

<span data-ttu-id="8ed14-109">*OldTimestampLow* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8ed14-109">*OldTimestampLow* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8ed14-110">Timestamp del momento in cui è stata impostata la configurazione precedente.</span><span class="sxs-lookup"><span data-stu-id="8ed14-110">The timestamp of when the previous configuration was set.</span></span> <span data-ttu-id="8ed14-111">Se non è 0, Abilita il controllo di atomicità: la nuova configurazione verrà applicata solo se il timestamp della configurazione precedente corrisponde a (ovvero la configurazione non è stata modificata in un intervallo compreso tra).</span><span class="sxs-lookup"><span data-stu-id="8ed14-111">If not 0, enables the atomicity check: the new configuration will be applied only if the timestamp of the old configuration matches (i.e. the configuration was not changed in between).</span></span> <span data-ttu-id="8ed14-112">Questa è la parte bassa di [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span><span class="sxs-lookup"><span data-stu-id="8ed14-112">This is the low part of [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span></span>

</dd> <dt>

<span data-ttu-id="8ed14-113">*OldTimestampHigh* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8ed14-113">*OldTimestampHigh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8ed14-114">Timestamp del momento in cui è stata impostata la configurazione precedente.</span><span class="sxs-lookup"><span data-stu-id="8ed14-114">The timestamp of when the previous configuration was set.</span></span> <span data-ttu-id="8ed14-115">Se non è 0, Abilita il controllo di atomicità: la nuova configurazione verrà applicata solo se il timestamp della configurazione precedente corrisponde a (ovvero la configurazione non è stata modificata in un intervallo compreso tra).</span><span class="sxs-lookup"><span data-stu-id="8ed14-115">If not 0, enables the atomicity check: the new configuration will be applied only if the timestamp of the old configuration matches (i.e. the configuration was not changed in between).</span></span> <span data-ttu-id="8ed14-116">Si tratta della parte superiore di [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span><span class="sxs-lookup"><span data-stu-id="8ed14-116">This is the high part of [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span></span>

</dd> <dt>

<span data-ttu-id="8ed14-117">*NewTimestampLow* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="8ed14-117">*NewTimestampLow* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8ed14-118">Timestamp di quando è stata impostata la nuova configurazione, se la chiamata ha esito positivo.</span><span class="sxs-lookup"><span data-stu-id="8ed14-118">The timestamp of when the new configuration was set, if the call succeeds.</span></span> <span data-ttu-id="8ed14-119">Questa è la parte bassa di [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span><span class="sxs-lookup"><span data-stu-id="8ed14-119">This is the low part of [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span></span>

</dd> <dt>

<span data-ttu-id="8ed14-120">*NewTimestampHigh* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="8ed14-120">*NewTimestampHigh* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8ed14-121">Timestamp di quando è stata impostata la nuova configurazione, se la chiamata ha esito positivo.</span><span class="sxs-lookup"><span data-stu-id="8ed14-121">The timestamp of when the new configuration was set, if the call succeeds.</span></span> <span data-ttu-id="8ed14-122">Si tratta della parte superiore di [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span><span class="sxs-lookup"><span data-stu-id="8ed14-122">This is the high part of [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span></span>

</dd> <dt>

<span data-ttu-id="8ed14-123">*OriginalTimestampLow* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="8ed14-123">*OriginalTimestampLow* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8ed14-124">Timestamp originale del momento in cui la configurazione ripristinata è stata impostata per la prima volta.</span><span class="sxs-lookup"><span data-stu-id="8ed14-124">The original timestamp of when the restored configuration was set for the first time.</span></span> <span data-ttu-id="8ed14-125">Questa è la parte bassa di [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span><span class="sxs-lookup"><span data-stu-id="8ed14-125">This is the low part of [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span></span>

</dd> <dt>

<span data-ttu-id="8ed14-126">*OriginalTimestampHigh* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="8ed14-126">*OriginalTimestampHigh* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8ed14-127">Timestamp originale del momento in cui la configurazione ripristinata è stata impostata per la prima volta.</span><span class="sxs-lookup"><span data-stu-id="8ed14-127">The original timestamp of when the restored configuration was set for the first time.</span></span> <span data-ttu-id="8ed14-128">Si tratta della parte superiore di [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span><span class="sxs-lookup"><span data-stu-id="8ed14-128">This is the high part of [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span></span>

</dd> <dt>

<span data-ttu-id="8ed14-129">*ErrorString* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="8ed14-129">*ErrorString* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8ed14-130">Stringa di testo con la spiegazione dell'errore.</span><span class="sxs-lookup"><span data-stu-id="8ed14-130">The text string with explanation of the error.</span></span>

</dd> <dt>

<span data-ttu-id="8ed14-131">*WarningString* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="8ed14-131">*WarningString* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8ed14-132">Stringa di testo con avvisi.</span><span class="sxs-lookup"><span data-stu-id="8ed14-132">The text string with warnings.</span></span>

</dd> <dt>

<span data-ttu-id="8ed14-133">*InfoString* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="8ed14-133">*InfoString* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8ed14-134">Stringa di testo con le informazioni sulla configurazione.</span><span class="sxs-lookup"><span data-stu-id="8ed14-134">The text string with information about the configuration.</span></span>

</dd> <dt>

<span data-ttu-id="8ed14-135">*ErrorType* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="8ed14-135">*ErrorType* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8ed14-136">Tipo di errore: si noti che 0 o assente indica l'esito positivo.</span><span class="sxs-lookup"><span data-stu-id="8ed14-136">The type of the error: note that 0 or absent indicates success.</span></span>

<dt>

<span data-ttu-id="8ed14-137">0</span><span class="sxs-lookup"><span data-stu-id="8ed14-137">0</span></span>
</dt> <dd>

<span data-ttu-id="8ed14-138">Esito positivo.</span><span class="sxs-lookup"><span data-stu-id="8ed14-138">Success.</span></span>

</dd> <dt>

<span data-ttu-id="8ed14-139">1</span><span class="sxs-lookup"><span data-stu-id="8ed14-139">1</span></span>
</dt> <dd>

<span data-ttu-id="8ed14-140">formato di argomento non valido</span><span class="sxs-lookup"><span data-stu-id="8ed14-140">bad argument format</span></span>

</dd> <dt>

<span data-ttu-id="8ed14-141">2</span><span class="sxs-lookup"><span data-stu-id="8ed14-141">2</span></span>
</dt> <dd>

<span data-ttu-id="8ed14-142">valore argomento non valido</span><span class="sxs-lookup"><span data-stu-id="8ed14-142">bad argument value</span></span>

</dd> <dt>

<span data-ttu-id="8ed14-143">3</span><span class="sxs-lookup"><span data-stu-id="8ed14-143">3</span></span>
</dt> <dd>

<span data-ttu-id="8ed14-144">errore di apertura della risorsa (socket)</span><span class="sxs-lookup"><span data-stu-id="8ed14-144">resource (socket) open error</span></span>

</dd> <dt>

<span data-ttu-id="8ed14-145">4</span><span class="sxs-lookup"><span data-stu-id="8ed14-145">4</span></span>
</dt> <dd>

<span data-ttu-id="8ed14-146">errore di persistenza (scrittura file)</span><span class="sxs-lookup"><span data-stu-id="8ed14-146">persistence (file write) error</span></span>

</dd> <dt>

<span data-ttu-id="8ed14-147">5</span><span class="sxs-lookup"><span data-stu-id="8ed14-147">5</span></span>
</dt> <dd>

<span data-ttu-id="8ed14-148">errore di atomicità (il timestamp precedente non corrisponde)</span><span class="sxs-lookup"><span data-stu-id="8ed14-148">atomicity error (the old timestamp didn't match)</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8ed14-149">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8ed14-149">Return value</span></span>

<dl> <dt>


</dt> <dd>

<span data-ttu-id="8ed14-150">0</span><span class="sxs-lookup"><span data-stu-id="8ed14-150">0</span></span>

<span data-ttu-id="8ed14-151">Errore</span><span class="sxs-lookup"><span data-stu-id="8ed14-151">Failure</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="8ed14-152">1</span><span class="sxs-lookup"><span data-stu-id="8ed14-152">1</span></span>

<span data-ttu-id="8ed14-153">Operazione completata</span><span class="sxs-lookup"><span data-stu-id="8ed14-153">Success</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8ed14-154">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8ed14-154">Requirements</span></span>



| <span data-ttu-id="8ed14-155">Requisito</span><span class="sxs-lookup"><span data-stu-id="8ed14-155">Requirement</span></span> | <span data-ttu-id="8ed14-156">Valore</span><span class="sxs-lookup"><span data-stu-id="8ed14-156">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8ed14-157">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8ed14-157">Minimum supported client</span></span><br/> | <span data-ttu-id="8ed14-158">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="8ed14-158">Windows 10 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="8ed14-159">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8ed14-159">Minimum supported server</span></span><br/> | <span data-ttu-id="8ed14-160">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="8ed14-160">Windows Server 2016</span></span><br/>                                                                       |
| <span data-ttu-id="8ed14-161">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="8ed14-161">Namespace</span></span><br/>                | <span data-ttu-id="8ed14-162">Radice \\ Microsoft \\ Windows \\ BootEventCollector</span><span class="sxs-lookup"><span data-stu-id="8ed14-162">Root\\Microsoft\\Windows\\BootEventCollector</span></span><br/>                                              |
| <span data-ttu-id="8ed14-163">MOF</span><span class="sxs-lookup"><span data-stu-id="8ed14-163">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8ed14-164"><dt>BootEventCollectorWMI. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8ed14-164"><dt>BootEventCollectorWMI.mof</dt></span></span> </dl> |
| <span data-ttu-id="8ed14-165">DLL</span><span class="sxs-lookup"><span data-stu-id="8ed14-165">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8ed14-166"><dt>BEvtCol.exe</dt></span><span class="sxs-lookup"><span data-stu-id="8ed14-166"><dt>BEvtCol.exe</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="8ed14-167">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8ed14-167">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8ed14-168">**Control**</span><span class="sxs-lookup"><span data-stu-id="8ed14-168">**Control**</span></span>](control.md)
</dt> </dl>

 

