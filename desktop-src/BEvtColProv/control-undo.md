---
description: Ripristinare la configurazione attiva dell'agente di raccolta dal file di backup precedente, in base al ritorno dal timestamp originale corrente.
ms.assetid: 150fa554-9efd-483e-a177-5fc7766a6a6c
ms.tgt_platform: multiple
title: Metodo Undo della classe Control
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Control.Undo
api_type:
- COM
api_location:
- BEvtCol.exe
ms.openlocfilehash: 285f1ec39ea52f6c388e324f72745d72f65207e6
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304448"
---
# <a name="undo-method-of-the-control-class"></a><span data-ttu-id="52ebb-103">Metodo Undo della classe Control</span><span class="sxs-lookup"><span data-stu-id="52ebb-103">Undo method of the Control class</span></span>

<span data-ttu-id="52ebb-104">Ripristinare la configurazione attiva dell'agente di raccolta dal file di backup precedente, in base al ritorno dal timestamp originale corrente.</span><span class="sxs-lookup"><span data-stu-id="52ebb-104">Restore the active configuration of the collector from the previous backup file (determined by going back from the current original timestamp).</span></span> <span data-ttu-id="52ebb-105">Se la configurazione è stata appena impostata, ciò significa che la modifica è stata annullata.</span><span class="sxs-lookup"><span data-stu-id="52ebb-105">If the configuration has been just set, this means undoing that change.</span></span> <span data-ttu-id="52ebb-106">Le chiamate consecutive vengono annullate alle configurazioni precedenti e precedenti.</span><span class="sxs-lookup"><span data-stu-id="52ebb-106">The consecutive calls will undo to the earlier and earlier configurations.</span></span> <span data-ttu-id="52ebb-107">Restituisce 1 in seguito all'esito positivo, 0 in seguito a un errore.</span><span class="sxs-lookup"><span data-stu-id="52ebb-107">Returns 1 on success, 0 on error.</span></span>

## <a name="syntax"></a><span data-ttu-id="52ebb-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="52ebb-108">Syntax</span></span>


```mof
Uint32 Undo(
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



## <a name="parameters"></a><span data-ttu-id="52ebb-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="52ebb-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="52ebb-110">*OldTimestampLow* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="52ebb-110">*OldTimestampLow* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="52ebb-111">Timestamp del momento in cui è stata impostata la configurazione precedente.</span><span class="sxs-lookup"><span data-stu-id="52ebb-111">The timestamp of when the previous configuration was set.</span></span> <span data-ttu-id="52ebb-112">Se non è 0, Abilita il controllo di atomicità: la nuova configurazione verrà applicata solo se il timestamp della configurazione precedente corrisponde a (ovvero la configurazione non è stata modificata in un intervallo compreso tra).</span><span class="sxs-lookup"><span data-stu-id="52ebb-112">If not 0, enables the atomicity check: the new configuration will be applied only if the timestamp of the old configuration matches (i.e. the configuration was not changed in between).</span></span> <span data-ttu-id="52ebb-113">Questa è la parte bassa di [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span><span class="sxs-lookup"><span data-stu-id="52ebb-113">This is the low part of [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span></span>

</dd> <dt>

<span data-ttu-id="52ebb-114">*OldTimestampHigh* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="52ebb-114">*OldTimestampHigh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="52ebb-115">Timestamp del momento in cui è stata impostata la configurazione precedente.</span><span class="sxs-lookup"><span data-stu-id="52ebb-115">The timestamp of when the previous configuration was set.</span></span> <span data-ttu-id="52ebb-116">Se non è 0, Abilita il controllo di atomicità: la nuova configurazione verrà applicata solo se il timestamp della configurazione precedente corrisponde a (ovvero la configurazione non è stata modificata in un intervallo compreso tra).</span><span class="sxs-lookup"><span data-stu-id="52ebb-116">If not 0, enables the atomicity check: the new configuration will be applied only if the timestamp of the old configuration matches (i.e. the configuration was not changed in between).</span></span> <span data-ttu-id="52ebb-117">Si tratta della parte superiore di [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span><span class="sxs-lookup"><span data-stu-id="52ebb-117">This is the high part of [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span></span>

</dd> <dt>

<span data-ttu-id="52ebb-118">*NewTimestampLow* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="52ebb-118">*NewTimestampLow* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="52ebb-119">Timestamp di quando è stata impostata la nuova configurazione, se la chiamata ha esito positivo.</span><span class="sxs-lookup"><span data-stu-id="52ebb-119">The timestamp of when the new configuration was set, if the call succeeds.</span></span> <span data-ttu-id="52ebb-120">Questa è la parte bassa di [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span><span class="sxs-lookup"><span data-stu-id="52ebb-120">This is the low part of [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span></span>

</dd> <dt>

<span data-ttu-id="52ebb-121">*NewTimestampHigh* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="52ebb-121">*NewTimestampHigh* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="52ebb-122">Timestamp di quando è stata impostata la nuova configurazione, se la chiamata ha esito positivo.</span><span class="sxs-lookup"><span data-stu-id="52ebb-122">The timestamp of when the new configuration was set, if the call succeeds.</span></span> <span data-ttu-id="52ebb-123">Si tratta della parte superiore di [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span><span class="sxs-lookup"><span data-stu-id="52ebb-123">This is the high part of [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span></span>

</dd> <dt>

<span data-ttu-id="52ebb-124">*OriginalTimestampLow* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="52ebb-124">*OriginalTimestampLow* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="52ebb-125">Timestamp originale del momento in cui la configurazione ripristinata è stata impostata per la prima volta.</span><span class="sxs-lookup"><span data-stu-id="52ebb-125">The original timestamp of when the restored configuration was set for the first time.</span></span> <span data-ttu-id="52ebb-126">Questa è la parte bassa di [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span><span class="sxs-lookup"><span data-stu-id="52ebb-126">This is the low part of [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span></span>

</dd> <dt>

<span data-ttu-id="52ebb-127">*OriginalTimestampHigh* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="52ebb-127">*OriginalTimestampHigh* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="52ebb-128">Timestamp originale del momento in cui la configurazione ripristinata è stata impostata per la prima volta.</span><span class="sxs-lookup"><span data-stu-id="52ebb-128">The original timestamp of when the restored configuration was set for the first time.</span></span> <span data-ttu-id="52ebb-129">Si tratta della parte superiore di [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span><span class="sxs-lookup"><span data-stu-id="52ebb-129">This is the high part of [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span></span>

</dd> <dt>

<span data-ttu-id="52ebb-130">*ErrorString* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="52ebb-130">*ErrorString* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="52ebb-131">Stringa di testo con la spiegazione dell'errore.</span><span class="sxs-lookup"><span data-stu-id="52ebb-131">The text string with explanation of the error.</span></span>

</dd> <dt>

<span data-ttu-id="52ebb-132">*WarningString* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="52ebb-132">*WarningString* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="52ebb-133">Stringa di testo con avvisi.</span><span class="sxs-lookup"><span data-stu-id="52ebb-133">The text string with warnings.</span></span>

</dd> <dt>

<span data-ttu-id="52ebb-134">*InfoString* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="52ebb-134">*InfoString* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="52ebb-135">Stringa di testo con le informazioni sulla configurazione.</span><span class="sxs-lookup"><span data-stu-id="52ebb-135">The text string with information about the configuration.</span></span>

</dd> <dt>

<span data-ttu-id="52ebb-136">*ErrorType* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="52ebb-136">*ErrorType* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="52ebb-137">Tipo di errore: si noti che 0 o assente indica l'esito positivo.</span><span class="sxs-lookup"><span data-stu-id="52ebb-137">The type of the error: note that 0 or absent indicates success.</span></span>

<dt>

<span data-ttu-id="52ebb-138">0</span><span class="sxs-lookup"><span data-stu-id="52ebb-138">0</span></span>
</dt> <dd>

<span data-ttu-id="52ebb-139">Esito positivo.</span><span class="sxs-lookup"><span data-stu-id="52ebb-139">Success.</span></span>

</dd> <dt>

<span data-ttu-id="52ebb-140">1</span><span class="sxs-lookup"><span data-stu-id="52ebb-140">1</span></span>
</dt> <dd>

<span data-ttu-id="52ebb-141">formato di argomento non valido</span><span class="sxs-lookup"><span data-stu-id="52ebb-141">bad argument format</span></span>

</dd> <dt>

<span data-ttu-id="52ebb-142">2</span><span class="sxs-lookup"><span data-stu-id="52ebb-142">2</span></span>
</dt> <dd>

<span data-ttu-id="52ebb-143">valore argomento non valido</span><span class="sxs-lookup"><span data-stu-id="52ebb-143">bad argument value</span></span>

</dd> <dt>

<span data-ttu-id="52ebb-144">3</span><span class="sxs-lookup"><span data-stu-id="52ebb-144">3</span></span>
</dt> <dd>

<span data-ttu-id="52ebb-145">errore di apertura della risorsa (socket)</span><span class="sxs-lookup"><span data-stu-id="52ebb-145">resource (socket) open error</span></span>

</dd> <dt>

<span data-ttu-id="52ebb-146">4</span><span class="sxs-lookup"><span data-stu-id="52ebb-146">4</span></span>
</dt> <dd>

<span data-ttu-id="52ebb-147">errore di persistenza (scrittura file)</span><span class="sxs-lookup"><span data-stu-id="52ebb-147">persistence (file write) error</span></span>

</dd> <dt>

<span data-ttu-id="52ebb-148">5</span><span class="sxs-lookup"><span data-stu-id="52ebb-148">5</span></span>
</dt> <dd>

<span data-ttu-id="52ebb-149">errore di atomicità (il timestamp precedente non corrisponde)</span><span class="sxs-lookup"><span data-stu-id="52ebb-149">atomicity error (the old timestamp didn't match)</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="52ebb-150">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="52ebb-150">Return value</span></span>

<dl> <dt>


</dt> <dd>

<span data-ttu-id="52ebb-151">0</span><span class="sxs-lookup"><span data-stu-id="52ebb-151">0</span></span>

<span data-ttu-id="52ebb-152">Errore</span><span class="sxs-lookup"><span data-stu-id="52ebb-152">Failure</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="52ebb-153">1</span><span class="sxs-lookup"><span data-stu-id="52ebb-153">1</span></span>

<span data-ttu-id="52ebb-154">Operazione completata</span><span class="sxs-lookup"><span data-stu-id="52ebb-154">Success</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="52ebb-155">Requisiti</span><span class="sxs-lookup"><span data-stu-id="52ebb-155">Requirements</span></span>



| <span data-ttu-id="52ebb-156">Requisito</span><span class="sxs-lookup"><span data-stu-id="52ebb-156">Requirement</span></span> | <span data-ttu-id="52ebb-157">Valore</span><span class="sxs-lookup"><span data-stu-id="52ebb-157">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="52ebb-158">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="52ebb-158">Minimum supported client</span></span><br/> | <span data-ttu-id="52ebb-159">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="52ebb-159">Windows 10 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="52ebb-160">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="52ebb-160">Minimum supported server</span></span><br/> | <span data-ttu-id="52ebb-161">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="52ebb-161">Windows Server 2016</span></span><br/>                                                                       |
| <span data-ttu-id="52ebb-162">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="52ebb-162">Namespace</span></span><br/>                | <span data-ttu-id="52ebb-163">Radice \\ Microsoft \\ Windows \\ BootEventCollector</span><span class="sxs-lookup"><span data-stu-id="52ebb-163">Root\\Microsoft\\Windows\\BootEventCollector</span></span><br/>                                              |
| <span data-ttu-id="52ebb-164">MOF</span><span class="sxs-lookup"><span data-stu-id="52ebb-164">MOF</span></span><br/>                      | <dl> <span data-ttu-id="52ebb-165"><dt>BootEventCollectorWMI. mof</dt></span><span class="sxs-lookup"><span data-stu-id="52ebb-165"><dt>BootEventCollectorWMI.mof</dt></span></span> </dl> |
| <span data-ttu-id="52ebb-166">DLL</span><span class="sxs-lookup"><span data-stu-id="52ebb-166">DLL</span></span><br/>                      | <dl> <span data-ttu-id="52ebb-167"><dt>BEvtCol.exe</dt></span><span class="sxs-lookup"><span data-stu-id="52ebb-167"><dt>BEvtCol.exe</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="52ebb-168">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="52ebb-168">See also</span></span>

<dl> <dt>

[<span data-ttu-id="52ebb-169">**Control**</span><span class="sxs-lookup"><span data-stu-id="52ebb-169">**Control**</span></span>](control.md)
</dt> </dl>

 

