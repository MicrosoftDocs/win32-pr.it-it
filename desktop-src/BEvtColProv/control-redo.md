---
description: Reimpostare la configurazione attiva dell'agente di raccolta dal file di backup successivo, determinato dal timestamp originale corrente. Se la configurazione è stata annullata, significa ripetere la modifica annullata.
ms.assetid: bd153ea3-9148-4e65-a44e-3f9fa1855f2f
ms.tgt_platform: multiple
title: Metodo Redo della classe Control
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Control.Redo
api_type:
- COM
api_location:
- BEvtCol.exe
ms.openlocfilehash: 5ed77aac62dca0bf81ed13474e8acebb0235ea71
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104125835"
---
# <a name="redo-method-of-the-control-class"></a><span data-ttu-id="9d924-104">Metodo Redo della classe Control</span><span class="sxs-lookup"><span data-stu-id="9d924-104">Redo method of the Control class</span></span>

<span data-ttu-id="9d924-105">Reimpostare la configurazione attiva dell'agente di raccolta dal file di backup successivo, determinato dal timestamp originale corrente.</span><span class="sxs-lookup"><span data-stu-id="9d924-105">Reset the active configuration of the collector from the later backup file (determined by going forward from the current original timestamp).</span></span> <span data-ttu-id="9d924-106">Se la configurazione è stata annullata, significa ripetere la modifica annullata.</span><span class="sxs-lookup"><span data-stu-id="9d924-106">If the configuration has been undone, this means redoing the undone change.</span></span>

## <a name="syntax"></a><span data-ttu-id="9d924-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9d924-107">Syntax</span></span>


```mof
Uint32 Redo(
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



## <a name="parameters"></a><span data-ttu-id="9d924-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="9d924-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9d924-109">*OldTimestampLow* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9d924-109">*OldTimestampLow* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9d924-110">Timestamp del momento in cui è stata impostata la configurazione precedente.</span><span class="sxs-lookup"><span data-stu-id="9d924-110">The timestamp of when the previous configuration was set.</span></span> <span data-ttu-id="9d924-111">Se non è 0, Abilita il controllo di atomicità: la nuova configurazione verrà applicata solo se il timestamp della configurazione precedente corrisponde a (ovvero la configurazione non è stata modificata in un intervallo compreso tra).</span><span class="sxs-lookup"><span data-stu-id="9d924-111">If not 0, enables the atomicity check: the new configuration will be applied only if the timestamp of the old configuration matches (i.e. the configuration was not changed in between).</span></span> <span data-ttu-id="9d924-112">Questa è la parte bassa di [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span><span class="sxs-lookup"><span data-stu-id="9d924-112">This is the low part of [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span></span>

</dd> <dt>

<span data-ttu-id="9d924-113">*OldTimestampHigh* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9d924-113">*OldTimestampHigh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9d924-114">Timestamp del momento in cui è stata impostata la configurazione precedente.</span><span class="sxs-lookup"><span data-stu-id="9d924-114">The timestamp of when the previous configuration was set.</span></span> <span data-ttu-id="9d924-115">Se non è 0, Abilita il controllo di atomicità: la nuova configurazione verrà applicata solo se il timestamp della configurazione precedente corrisponde a (ovvero la configurazione non è stata modificata in un intervallo compreso tra).</span><span class="sxs-lookup"><span data-stu-id="9d924-115">If not 0, enables the atomicity check: the new configuration will be applied only if the timestamp of the old configuration matches (i.e. the configuration was not changed in between).</span></span> <span data-ttu-id="9d924-116">Si tratta della parte superiore di [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span><span class="sxs-lookup"><span data-stu-id="9d924-116">This is the high part of [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span></span>

</dd> <dt>

<span data-ttu-id="9d924-117">*NewTimestampLow* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="9d924-117">*NewTimestampLow* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9d924-118">Timestamp di quando è stata impostata la nuova configurazione, se la chiamata ha esito positivo.</span><span class="sxs-lookup"><span data-stu-id="9d924-118">The timestamp of when the new configuration was set, if the call succeeds.</span></span> <span data-ttu-id="9d924-119">Questa è la parte bassa di [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span><span class="sxs-lookup"><span data-stu-id="9d924-119">This is the low part of [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span></span>

</dd> <dt>

<span data-ttu-id="9d924-120">*NewTimestampHigh* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="9d924-120">*NewTimestampHigh* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9d924-121">Timestamp di quando è stata impostata la nuova configurazione, se la chiamata ha esito positivo.</span><span class="sxs-lookup"><span data-stu-id="9d924-121">The timestamp of when the new configuration was set, if the call succeeds.</span></span> <span data-ttu-id="9d924-122">Si tratta della parte superiore di [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span><span class="sxs-lookup"><span data-stu-id="9d924-122">This is the high part of [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span></span>

</dd> <dt>

<span data-ttu-id="9d924-123">*OriginalTimestampLow* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="9d924-123">*OriginalTimestampLow* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9d924-124">Timestamp originale del momento in cui la configurazione ripristinata è stata impostata per la prima volta.</span><span class="sxs-lookup"><span data-stu-id="9d924-124">The original timestamp of when the restored configuration was set for the first time.</span></span> <span data-ttu-id="9d924-125">Questa è la parte bassa di [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span><span class="sxs-lookup"><span data-stu-id="9d924-125">This is the low part of [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span></span>

</dd> <dt>

<span data-ttu-id="9d924-126">*OriginalTimestampHigh* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="9d924-126">*OriginalTimestampHigh* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9d924-127">Timestamp originale del momento in cui la configurazione ripristinata è stata impostata per la prima volta.</span><span class="sxs-lookup"><span data-stu-id="9d924-127">The original timestamp of when the restored configuration was set for the first time.</span></span> <span data-ttu-id="9d924-128">Si tratta della parte superiore di [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span><span class="sxs-lookup"><span data-stu-id="9d924-128">This is the high part of [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span></span>

</dd> <dt>

<span data-ttu-id="9d924-129">*ErrorString* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="9d924-129">*ErrorString* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9d924-130">Stringa di testo con la spiegazione dell'errore.</span><span class="sxs-lookup"><span data-stu-id="9d924-130">The text string with explanation of the error.</span></span>

</dd> <dt>

<span data-ttu-id="9d924-131">*WarningString* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="9d924-131">*WarningString* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9d924-132">Stringa di testo con avvisi.</span><span class="sxs-lookup"><span data-stu-id="9d924-132">The text string with warnings.</span></span>

</dd> <dt>

<span data-ttu-id="9d924-133">*InfoString* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="9d924-133">*InfoString* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9d924-134">Stringa di testo con le informazioni sulla configurazione.</span><span class="sxs-lookup"><span data-stu-id="9d924-134">The text string with information about the configuration.</span></span>

</dd> <dt>

<span data-ttu-id="9d924-135">*ErrorType* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="9d924-135">*ErrorType* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9d924-136">Il tipo di errore,</span><span class="sxs-lookup"><span data-stu-id="9d924-136">The type of the error.</span></span> <span data-ttu-id="9d924-137">Si noti che 0 o assente indica l'esito positivo.</span><span class="sxs-lookup"><span data-stu-id="9d924-137">Note that 0 or absent indicates success.</span></span>

<dt>

<span data-ttu-id="9d924-138">0</span><span class="sxs-lookup"><span data-stu-id="9d924-138">0</span></span>
</dt> <dd>

<span data-ttu-id="9d924-139">Esito positivo.</span><span class="sxs-lookup"><span data-stu-id="9d924-139">Success.</span></span>

</dd> <dt>

<span data-ttu-id="9d924-140">1</span><span class="sxs-lookup"><span data-stu-id="9d924-140">1</span></span>
</dt> <dd>

<span data-ttu-id="9d924-141">formato di argomento non valido</span><span class="sxs-lookup"><span data-stu-id="9d924-141">bad argument format</span></span>

</dd> <dt>

<span data-ttu-id="9d924-142">2</span><span class="sxs-lookup"><span data-stu-id="9d924-142">2</span></span>
</dt> <dd>

<span data-ttu-id="9d924-143">valore argomento non valido</span><span class="sxs-lookup"><span data-stu-id="9d924-143">bad argument value</span></span>

</dd> <dt>

<span data-ttu-id="9d924-144">3</span><span class="sxs-lookup"><span data-stu-id="9d924-144">3</span></span>
</dt> <dd>

<span data-ttu-id="9d924-145">errore di apertura della risorsa (socket)</span><span class="sxs-lookup"><span data-stu-id="9d924-145">resource (socket) open error</span></span>

</dd> <dt>

<span data-ttu-id="9d924-146">4</span><span class="sxs-lookup"><span data-stu-id="9d924-146">4</span></span>
</dt> <dd>

<span data-ttu-id="9d924-147">errore di persistenza (scrittura file)</span><span class="sxs-lookup"><span data-stu-id="9d924-147">persistence (file write) error</span></span>

</dd> <dt>

<span data-ttu-id="9d924-148">5</span><span class="sxs-lookup"><span data-stu-id="9d924-148">5</span></span>
</dt> <dd>

<span data-ttu-id="9d924-149">errore di atomicità (il timestamp precedente non corrisponde)</span><span class="sxs-lookup"><span data-stu-id="9d924-149">atomicity error (the old timestamp didn't match)</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9d924-150">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="9d924-150">Return value</span></span>

<dl> <dt>


</dt> <dd>

<span data-ttu-id="9d924-151">0</span><span class="sxs-lookup"><span data-stu-id="9d924-151">0</span></span>

<span data-ttu-id="9d924-152">Errore</span><span class="sxs-lookup"><span data-stu-id="9d924-152">Failure</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="9d924-153">1</span><span class="sxs-lookup"><span data-stu-id="9d924-153">1</span></span>

<span data-ttu-id="9d924-154">Operazione completata</span><span class="sxs-lookup"><span data-stu-id="9d924-154">Success</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="9d924-155">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9d924-155">Requirements</span></span>



| <span data-ttu-id="9d924-156">Requisito</span><span class="sxs-lookup"><span data-stu-id="9d924-156">Requirement</span></span> | <span data-ttu-id="9d924-157">Valore</span><span class="sxs-lookup"><span data-stu-id="9d924-157">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9d924-158">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9d924-158">Minimum supported client</span></span><br/> | <span data-ttu-id="9d924-159">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="9d924-159">Windows 10 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="9d924-160">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9d924-160">Minimum supported server</span></span><br/> | <span data-ttu-id="9d924-161">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="9d924-161">Windows Server 2016</span></span><br/>                                                                       |
| <span data-ttu-id="9d924-162">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="9d924-162">Namespace</span></span><br/>                | <span data-ttu-id="9d924-163">Radice \\ Microsoft \\ Windows \\ BootEventCollector</span><span class="sxs-lookup"><span data-stu-id="9d924-163">Root\\Microsoft\\Windows\\BootEventCollector</span></span><br/>                                              |
| <span data-ttu-id="9d924-164">MOF</span><span class="sxs-lookup"><span data-stu-id="9d924-164">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9d924-165"><dt>BootEventCollectorWMI. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9d924-165"><dt>BootEventCollectorWMI.mof</dt></span></span> </dl> |
| <span data-ttu-id="9d924-166">DLL</span><span class="sxs-lookup"><span data-stu-id="9d924-166">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9d924-167"><dt>BEvtCol.exe</dt></span><span class="sxs-lookup"><span data-stu-id="9d924-167"><dt>BEvtCol.exe</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="9d924-168">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9d924-168">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9d924-169">**Control**</span><span class="sxs-lookup"><span data-stu-id="9d924-169">**Control**</span></span>](control.md)
</dt> </dl>

 

