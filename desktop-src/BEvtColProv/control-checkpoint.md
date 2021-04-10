---
description: Se la configurazione corrente è il risultato dell'operazione di annullamento/ripetizione/ripristino, lo contrassegna come se fosse stato impostato in modo esplicito, in modo che la cronologia manterrà l'ora in cui è stata impostata e verrà creato un file di backup alla successiva modifica della configurazione.
ms.assetid: 1b3d398a-c7f9-4e21-9e43-1245a13fe564
ms.tgt_platform: multiple
title: Metodo Checkpoint della classe Control (Srrestoreptapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Control.Checkpoint
api_type:
- COM
api_location:
- BEvtCol.exe
ms.openlocfilehash: 44453f647d55f29a9a6cfc5622e29dcc88ad2446
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104125844"
---
# <a name="checkpoint-method-of-the-control-class"></a><span data-ttu-id="f61ba-103">Metodo Checkpoint della classe Control</span><span class="sxs-lookup"><span data-stu-id="f61ba-103">Checkpoint method of the Control class</span></span>

<span data-ttu-id="f61ba-104">Se la configurazione corrente è il risultato dell'operazione di annullamento/ripetizione/ripristino, lo contrassegna come se fosse stato impostato in modo esplicito, in modo che la cronologia manterrà l'ora in cui è stata impostata e verrà creato un file di backup alla successiva modifica della configurazione.</span><span class="sxs-lookup"><span data-stu-id="f61ba-104">If the current configuration is a result of the Undo/Redo/Restore, marks it as if it has been set explicitly, so that the history will preserve the time when it was set, and a backup file will be created for it on the next configuration change.</span></span> <span data-ttu-id="f61ba-105">Se la configurazione corrente è già stata impostata in modo esplicito, non ha alcun effetto.</span><span class="sxs-lookup"><span data-stu-id="f61ba-105">If the current configuration was already set explicitly, has no effect.</span></span>

## <a name="syntax"></a><span data-ttu-id="f61ba-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f61ba-106">Syntax</span></span>


```mof
Uint32 Checkpoint(
  [in]  Uint32 OldTimestampLow,
  [in]  Uint32 OldTimestampHigh,
  [out] string ErrorString,
  [out] string WarningString,
  [out] string InfoString,
  [out] uint32 ErrorType
);
```



## <a name="parameters"></a><span data-ttu-id="f61ba-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="f61ba-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f61ba-108">*OldTimestampLow* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f61ba-108">*OldTimestampLow* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f61ba-109">Timestamp di quando è stata impostata la configurazione corrente.</span><span class="sxs-lookup"><span data-stu-id="f61ba-109">The timestamp of when the current configuration was set.</span></span> <span data-ttu-id="f61ba-110">Se non è 0, Abilita il controllo di atomicità: l'azione verrà applicata solo se il timestamp della configurazione precedente corrisponde a (ovvero la configurazione non è stata modificata in un intervallo compreso tra).</span><span class="sxs-lookup"><span data-stu-id="f61ba-110">If not 0, enables the atomicity check: the action will be applied only if the timestamp of the old configuration matches (i.e. the configuration was not changed in between).</span></span> <span data-ttu-id="f61ba-111">Questa è la parte bassa di [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span><span class="sxs-lookup"><span data-stu-id="f61ba-111">This is the low part of [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span></span>

</dd> <dt>

<span data-ttu-id="f61ba-112">*OldTimestampHigh* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f61ba-112">*OldTimestampHigh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f61ba-113">Timestamp di quando è stata impostata la configurazione corrente.</span><span class="sxs-lookup"><span data-stu-id="f61ba-113">The timestamp of when the current configuration was set.</span></span> <span data-ttu-id="f61ba-114">Se non è 0, Abilita il controllo di atomicità: l'azione verrà applicata solo se il timestamp della configurazione precedente corrisponde a (ovvero la configurazione non è stata modificata in un intervallo compreso tra).</span><span class="sxs-lookup"><span data-stu-id="f61ba-114">If not 0, enables the atomicity check: the action will be applied only if the timestamp of the old configuration matches (i.e. the configuration was not changed in between).</span></span> <span data-ttu-id="f61ba-115">Si tratta della parte superiore di [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span><span class="sxs-lookup"><span data-stu-id="f61ba-115">This is the high part of [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span></span>

</dd> <dt>

<span data-ttu-id="f61ba-116">*ErrorString* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="f61ba-116">*ErrorString* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f61ba-117">Stringa di testo con la spiegazione dell'errore.</span><span class="sxs-lookup"><span data-stu-id="f61ba-117">The text string with explanation of the error.</span></span>

</dd> <dt>

<span data-ttu-id="f61ba-118">*WarningString* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="f61ba-118">*WarningString* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f61ba-119">Stringa di testo con avvisi.</span><span class="sxs-lookup"><span data-stu-id="f61ba-119">The text string with warnings.</span></span>

</dd> <dt>

<span data-ttu-id="f61ba-120">*InfoString* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="f61ba-120">*InfoString* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f61ba-121">Stringa di testo con le informazioni sulla configurazione.</span><span class="sxs-lookup"><span data-stu-id="f61ba-121">The text string with information about the configuration.</span></span>

</dd> <dt>

<span data-ttu-id="f61ba-122">*ErrorType* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="f61ba-122">*ErrorType* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f61ba-123">Il tipo di errore,</span><span class="sxs-lookup"><span data-stu-id="f61ba-123">The type of the error.</span></span> <span data-ttu-id="f61ba-124">Si noti che 0 o assente indica l'esito positivo.</span><span class="sxs-lookup"><span data-stu-id="f61ba-124">Note that 0 or absent indicates success.</span></span>

<dt>

<span data-ttu-id="f61ba-125">0</span><span class="sxs-lookup"><span data-stu-id="f61ba-125">0</span></span>
</dt> <dd>

<span data-ttu-id="f61ba-126">Esito positivo.</span><span class="sxs-lookup"><span data-stu-id="f61ba-126">Success.</span></span>

</dd> <dt>

<span data-ttu-id="f61ba-127">1</span><span class="sxs-lookup"><span data-stu-id="f61ba-127">1</span></span>
</dt> <dd>

<span data-ttu-id="f61ba-128">formato di argomento non valido</span><span class="sxs-lookup"><span data-stu-id="f61ba-128">bad argument format</span></span>

</dd> <dt>

<span data-ttu-id="f61ba-129">2</span><span class="sxs-lookup"><span data-stu-id="f61ba-129">2</span></span>
</dt> <dd>

<span data-ttu-id="f61ba-130">valore argomento non valido</span><span class="sxs-lookup"><span data-stu-id="f61ba-130">bad argument value</span></span>

</dd> <dt>

<span data-ttu-id="f61ba-131">3</span><span class="sxs-lookup"><span data-stu-id="f61ba-131">3</span></span>
</dt> <dd>

<span data-ttu-id="f61ba-132">errore di apertura della risorsa (socket)</span><span class="sxs-lookup"><span data-stu-id="f61ba-132">resource (socket) open error</span></span>

</dd> <dt>

<span data-ttu-id="f61ba-133">4</span><span class="sxs-lookup"><span data-stu-id="f61ba-133">4</span></span>
</dt> <dd>

<span data-ttu-id="f61ba-134">errore di persistenza (scrittura file)</span><span class="sxs-lookup"><span data-stu-id="f61ba-134">persistence (file write) error</span></span>

</dd> <dt>

<span data-ttu-id="f61ba-135">5</span><span class="sxs-lookup"><span data-stu-id="f61ba-135">5</span></span>
</dt> <dd>

<span data-ttu-id="f61ba-136">errore di atomicità (il timestamp precedente non corrisponde)</span><span class="sxs-lookup"><span data-stu-id="f61ba-136">atomicity error (the old timestamp didn't match)</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f61ba-137">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f61ba-137">Return value</span></span>

<dl> <dt>


</dt> <dd>

<span data-ttu-id="f61ba-138">0</span><span class="sxs-lookup"><span data-stu-id="f61ba-138">0</span></span>

<span data-ttu-id="f61ba-139">Errore</span><span class="sxs-lookup"><span data-stu-id="f61ba-139">Failure</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="f61ba-140">1</span><span class="sxs-lookup"><span data-stu-id="f61ba-140">1</span></span>

<span data-ttu-id="f61ba-141">Operazione completata</span><span class="sxs-lookup"><span data-stu-id="f61ba-141">Success</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f61ba-142">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f61ba-142">Requirements</span></span>



| <span data-ttu-id="f61ba-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="f61ba-143">Requirement</span></span> | <span data-ttu-id="f61ba-144">Valore</span><span class="sxs-lookup"><span data-stu-id="f61ba-144">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f61ba-145">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f61ba-145">Minimum supported client</span></span><br/> | <span data-ttu-id="f61ba-146">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="f61ba-146">Windows 10 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="f61ba-147">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f61ba-147">Minimum supported server</span></span><br/> | <span data-ttu-id="f61ba-148">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="f61ba-148">Windows Server 2016</span></span><br/>                                                                       |
| <span data-ttu-id="f61ba-149">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="f61ba-149">Namespace</span></span><br/>                | <span data-ttu-id="f61ba-150">Radice \\ Microsoft \\ Windows \\ BootEventCollector</span><span class="sxs-lookup"><span data-stu-id="f61ba-150">Root\\Microsoft\\Windows\\BootEventCollector</span></span><br/>                                              |
| <span data-ttu-id="f61ba-151">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f61ba-151">Header</span></span><br/>                   | <dl> <span data-ttu-id="f61ba-152"><dt>Srrestoreptapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="f61ba-152"><dt>Srrestoreptapi.h</dt></span></span> </dl>          |
| <span data-ttu-id="f61ba-153">MOF</span><span class="sxs-lookup"><span data-stu-id="f61ba-153">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f61ba-154"><dt>BootEventCollectorWMI. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f61ba-154"><dt>BootEventCollectorWMI.mof</dt></span></span> </dl> |
| <span data-ttu-id="f61ba-155">DLL</span><span class="sxs-lookup"><span data-stu-id="f61ba-155">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f61ba-156"><dt>BEvtCol.exe</dt></span><span class="sxs-lookup"><span data-stu-id="f61ba-156"><dt>BEvtCol.exe</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="f61ba-157">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f61ba-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f61ba-158">**Control**</span><span class="sxs-lookup"><span data-stu-id="f61ba-158">**Control**</span></span>](control.md)
</dt> </dl>

 

