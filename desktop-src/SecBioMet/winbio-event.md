---
title: Struttura WINBIO_EVENT ( \_ tipi WINBIO. h)
description: Contiene informazioni sullo stato inviate alla routine di callback quando viene generata una notifica di evento.
ms.assetid: f46df7ff-8197-49cb-b1f8-4e7e3288e3df
keywords:
- Struttura di WINBIO_EVENT Windows Biometric Framework API
- API Windows Biometric Framework puntatore alla struttura PWINBIO_EVENT
topic_type:
- apiref
api_name:
- WINBIO_EVENT
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 75b6a8301ea5dab7d860e5bd7fb32c69277bad63
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302344"
---
# <a name="winbio_event-structure"></a><span data-ttu-id="83d4c-105">\_Struttura dell'evento WINBIO</span><span class="sxs-lookup"><span data-stu-id="83d4c-105">WINBIO\_EVENT structure</span></span>

<span data-ttu-id="83d4c-106">La struttura dell' **\_ evento WINBIO** contiene le informazioni sullo stato inviate alla routine di callback quando viene generata una notifica di evento.</span><span class="sxs-lookup"><span data-stu-id="83d4c-106">The **WINBIO\_EVENT** structure contains status information sent to the callback routine when an event notice is raised.</span></span>

## <a name="syntax"></a><span data-ttu-id="83d4c-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="83d4c-107">Syntax</span></span>


```C++
typedef struct _WINBIO_EVENT {
  WINBIO_EVENT_TYPE Type;
  union {
    struct {
      WINBIO_UNIT_ID       UnitId;
      WINBIO_REJECT_DETAIL RejectDetail;
    } Unclaimed;
    struct {
      WINBIO_UNIT_ID           UnitId;
      WINBIO_IDENTITY          Identity;
      WINBIO_BIOMETRIC_SUBTYPE SubFactor;
      WINBIO_REJECT_DETAIL     RejectDetail;
    } UnclaimedIdentify;
    struct {
      HRESULT ErrorCode;
    } Error;
  } Parameters;
} WINBIO_EVENT, *PWINBIO_EVENT;
```



## <a name="members"></a><span data-ttu-id="83d4c-108">Members</span><span class="sxs-lookup"><span data-stu-id="83d4c-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="83d4c-109">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="83d4c-109">**Type**</span></span>
</dt> <dd>

<span data-ttu-id="83d4c-110">Valore che specifica il tipo di avviso di evento del provider di servizi generato.</span><span class="sxs-lookup"><span data-stu-id="83d4c-110">A value that specifies the type of service provider event notice raised.</span></span> <span data-ttu-id="83d4c-111">L'unico provider attualmente supportato è il sensore di impronta digitale.</span><span class="sxs-lookup"><span data-stu-id="83d4c-111">The only provider currently supported is the fingerprint sensor.</span></span> <span data-ttu-id="83d4c-112">Questo sensore supporta i flag seguenti.</span><span class="sxs-lookup"><span data-stu-id="83d4c-112">This sensor supports the following flags.</span></span>

<dl> <dt>

<span data-ttu-id="83d4c-113"><span id="WINBIO_EVENT_FP_UNCLAIMED"></span><span id="winbio_event_fp_unclaimed"></span>**WINBIO \_ EVENTO \_ FP non \_ recuperato** (il sensore ha rilevato una swipe del dito non richiesto dall'applicazione o dalla finestra che attualmente ha lo stato attivo.</span><span class="sxs-lookup"><span data-stu-id="83d4c-113"><span id="WINBIO_EVENT_FP_UNCLAIMED"></span><span id="winbio_event_fp_unclaimed"></span>**WINBIO\_EVENT\_FP\_UNCLAIMED** (The sensor detected a finger swipe that was not requested by the application or by the window that currently has focus.</span></span> <span data-ttu-id="83d4c-114">Il Windows Biometric Framework chiama la funzione di callback per indicare che si è verificato un dito sfiorato ma non tenta di identificare l'impronta digitale.</span><span class="sxs-lookup"><span data-stu-id="83d4c-114">The Windows Biometric Framework calls into your callback function to indicate that a finger swipe has occurred but does not try to identify the fingerprint.)</span></span>
</dt> <dt>

<span data-ttu-id="83d4c-115"><span id="WINBIO_EVENT_FP_UNCLAIMED_IDENTIFY"></span><span id="winbio_event_fp_unclaimed_identify"></span>**WINBIO \_ EVENTO \_ FP senza \_ attestazione \_** (il sensore ha rilevato una striscia di dita non richiesta dall'applicazione o dalla finestra che attualmente ha lo stato attivo.</span><span class="sxs-lookup"><span data-stu-id="83d4c-115"><span id="WINBIO_EVENT_FP_UNCLAIMED_IDENTIFY"></span><span id="winbio_event_fp_unclaimed_identify"></span>**WINBIO\_EVENT\_FP\_UNCLAIMED\_IDENTIFY** (The sensor detected a finger swipe that was not requested by the application or by the window that currently has focus.</span></span> <span data-ttu-id="83d4c-116">Il Windows Biometric Framework tenta di identificare l'impronta digitale e passa il risultato di tale processo alla funzione di callback.</span><span class="sxs-lookup"><span data-stu-id="83d4c-116">The Windows Biometric Framework attempts to identify the fingerprint and passes the result of that process to your callback function.)</span></span>
</dt> </dl> </dd> <dt>

<span data-ttu-id="83d4c-117">**Parametri**</span><span class="sxs-lookup"><span data-stu-id="83d4c-117">**Parameters**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83d4c-118">**Richiesti**</span><span class="sxs-lookup"><span data-stu-id="83d4c-118">**Unclaimed**</span></span>
</dt> <dd>

<span data-ttu-id="83d4c-119">Struttura restituita per l'acquisizione di esempio biometrica.</span><span class="sxs-lookup"><span data-stu-id="83d4c-119">Structure returned for biometric sample capture.</span></span>

<dl> <dt>

<span data-ttu-id="83d4c-120">**UnitId**</span><span class="sxs-lookup"><span data-stu-id="83d4c-120">**UnitId**</span></span>
</dt> <dd>

<span data-ttu-id="83d4c-121">Unità biometrica che ha generato l'esempio.</span><span class="sxs-lookup"><span data-stu-id="83d4c-121">The biometric unit that generated the sample.</span></span>

</dd> <dt>

<span data-ttu-id="83d4c-122">**RejectDetail**</span><span class="sxs-lookup"><span data-stu-id="83d4c-122">**RejectDetail**</span></span>
</dt> <dd>

<span data-ttu-id="83d4c-123">Valore **ULONG** che contiene informazioni aggiuntive sull'errore di acquisizione di un campione biometrico.</span><span class="sxs-lookup"><span data-stu-id="83d4c-123">A **ULONG** value that contains additional information regarding failure to capture a biometric sample.</span></span> <span data-ttu-id="83d4c-124">Se un'acquisizione ha avuto esito positivo, questo parametro è impostato su zero.</span><span class="sxs-lookup"><span data-stu-id="83d4c-124">If a capture succeeded, this parameter is set to zero.</span></span> <span data-ttu-id="83d4c-125">Per l'acquisizione di impronte digitali vengono definiti i valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="83d4c-125">The following values are defined for fingerprint capture:</span></span>

-   <span data-ttu-id="83d4c-126">WINBIO \_ FP \_ troppo \_ alta</span><span class="sxs-lookup"><span data-stu-id="83d4c-126">WINBIO\_FP\_TOO\_HIGH</span></span>
-   <span data-ttu-id="83d4c-127">WINBIO \_ FP \_ troppo \_ basso</span><span class="sxs-lookup"><span data-stu-id="83d4c-127">WINBIO\_FP\_TOO\_LOW</span></span>
-   <span data-ttu-id="83d4c-128">WINBIO \_ FP \_ troppo a \_ sinistra</span><span class="sxs-lookup"><span data-stu-id="83d4c-128">WINBIO\_FP\_TOO\_LEFT</span></span>
-   <span data-ttu-id="83d4c-129">WINBIO \_ FP \_ troppo a \_ destra</span><span class="sxs-lookup"><span data-stu-id="83d4c-129">WINBIO\_FP\_TOO\_RIGHT</span></span>
-   <span data-ttu-id="83d4c-130">WINBIO \_ FP \_ troppo \_ veloce</span><span class="sxs-lookup"><span data-stu-id="83d4c-130">WINBIO\_FP\_TOO\_FAST</span></span>
-   <span data-ttu-id="83d4c-131">WINBIO \_ FP \_ troppo \_ lento</span><span class="sxs-lookup"><span data-stu-id="83d4c-131">WINBIO\_FP\_TOO\_SLOW</span></span>
-   <span data-ttu-id="83d4c-132">WINBIO \_ FP \_ scarsa \_ qualità</span><span class="sxs-lookup"><span data-stu-id="83d4c-132">WINBIO\_FP\_POOR\_QUALITY</span></span>
-   <span data-ttu-id="83d4c-133">WINBIO \_ FP \_ troppo \_ sbilanciato</span><span class="sxs-lookup"><span data-stu-id="83d4c-133">WINBIO\_FP\_TOO\_SKEWED</span></span>
-   <span data-ttu-id="83d4c-134">WINBIO \_ FP \_ troppo \_ breve</span><span class="sxs-lookup"><span data-stu-id="83d4c-134">WINBIO\_FP\_TOO\_SHORT</span></span>
-   <span data-ttu-id="83d4c-135">\_errore di \_ merge WINBIO FP \_</span><span class="sxs-lookup"><span data-stu-id="83d4c-135">WINBIO\_FP\_MERGE\_FAILURE</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="83d4c-136">**UnclaimedIdentify**</span><span class="sxs-lookup"><span data-stu-id="83d4c-136">**UnclaimedIdentify**</span></span>
</dt> <dd>

<span data-ttu-id="83d4c-137">Struttura restituita per l'acquisizione e l'identificazione biometriche.</span><span class="sxs-lookup"><span data-stu-id="83d4c-137">Structure returned for biometric capture and identification.</span></span> <span data-ttu-id="83d4c-138">L'identificazione determina se un campione può essere associato a un modello biometrico esistente.</span><span class="sxs-lookup"><span data-stu-id="83d4c-138">Identification determines whether a sample can be associated with an existing biometric template.</span></span>

<dl> <dt>

<span data-ttu-id="83d4c-139">**UnitId**</span><span class="sxs-lookup"><span data-stu-id="83d4c-139">**UnitId**</span></span>
</dt> <dd>

<span data-ttu-id="83d4c-140">Unità biometrica che ha generato l'esempio.</span><span class="sxs-lookup"><span data-stu-id="83d4c-140">The biometric unit that generated the sample.</span></span>

</dd> <dt>

<span data-ttu-id="83d4c-141">**Identità**</span><span class="sxs-lookup"><span data-stu-id="83d4c-141">**Identity**</span></span>
</dt> <dd>

<span data-ttu-id="83d4c-142">Struttura [**di \_ identità WINBIO**](winbio-identity.md) che contiene il GUID o il SID dell'utente che fornisce l'esempio biometrico.</span><span class="sxs-lookup"><span data-stu-id="83d4c-142">A [**WINBIO\_IDENTITY**](winbio-identity.md) structure that contains the GUID or SID of the user providing the biometric sample.</span></span>

</dd> <dt>

<span data-ttu-id="83d4c-143">**Sottofattore**</span><span class="sxs-lookup"><span data-stu-id="83d4c-143">**SubFactor**</span></span>
</dt> <dd>

<span data-ttu-id="83d4c-144">Valore [**del \_ \_ SOTTOtipo biometrico WINBIO**](winbio-biometric-subtype-constants.md) che specifica il Sottofattore associato a un campione biometrico.</span><span class="sxs-lookup"><span data-stu-id="83d4c-144">A [**WINBIO\_BIOMETRIC\_SUBTYPE**](winbio-biometric-subtype-constants.md) value that specifies the sub-factor associated with a biometric sample.</span></span> <span data-ttu-id="83d4c-145">Il Windows Biometric Framework (WBF) supporta attualmente solo l'acquisizione di impronte digitali e usa le costanti seguenti per rappresentare le informazioni sui sottotipi.</span><span class="sxs-lookup"><span data-stu-id="83d4c-145">The Windows Biometric Framework (WBF) currently supports only fingerprint capture and uses the following constants to represent sub-type information.</span></span>

-   <span data-ttu-id="83d4c-146">WINBIO \_ ANSI \_ 381 \_ POS \_ sconosciuta</span><span class="sxs-lookup"><span data-stu-id="83d4c-146">WINBIO\_ANSI\_381\_POS\_UNKNOWN</span></span>
-   <span data-ttu-id="83d4c-147">WINBIO \_ ANSI \_ 381 \_ POS \_ \_ pollice RH</span><span class="sxs-lookup"><span data-stu-id="83d4c-147">WINBIO\_ANSI\_381\_POS\_RH\_THUMB</span></span>
-   <span data-ttu-id="83d4c-148">WINBIO \_ ANSI \_ 381 \_ POS \_ RH \_ - \_ dito indice</span><span class="sxs-lookup"><span data-stu-id="83d4c-148">WINBIO\_ANSI\_381\_POS\_RH\_INDEX\_FINGER</span></span>
-   <span data-ttu-id="83d4c-149">WINBIO \_ ANSI \_ 381 \_ POS \_ \_ secondo \_ dito medio</span><span class="sxs-lookup"><span data-stu-id="83d4c-149">WINBIO\_ANSI\_381\_POS\_RH\_MIDDLE\_FINGER</span></span>
-   <span data-ttu-id="83d4c-150">WINBIO \_ ANSI \_ 381 \_ POS \_ RH \_ \_ anulare</span><span class="sxs-lookup"><span data-stu-id="83d4c-150">WINBIO\_ANSI\_381\_POS\_RH\_RING\_FINGER</span></span>
-   <span data-ttu-id="83d4c-151">WINBIO \_ ANSI \_ 381 \_ POS \_ RH \_ piccolo \_ dito</span><span class="sxs-lookup"><span data-stu-id="83d4c-151">WINBIO\_ANSI\_381\_POS\_RH\_LITTLE\_FINGER</span></span>
-   <span data-ttu-id="83d4c-152">WINBIO \_ ANSI \_ 381 \_ POS \_ LH \_ Thumb</span><span class="sxs-lookup"><span data-stu-id="83d4c-152">WINBIO\_ANSI\_381\_POS\_LH\_THUMB</span></span>
-   <span data-ttu-id="83d4c-153">WINBIO \_ ANSI \_ 381 \_ POS \_ - \_ dito indice LH \_</span><span class="sxs-lookup"><span data-stu-id="83d4c-153">WINBIO\_ANSI\_381\_POS\_LH\_INDEX\_FINGER</span></span>
-   <span data-ttu-id="83d4c-154">WINBIO \_ ANSI \_ 381 \_ POS \_ - \_ dito medio SX \_</span><span class="sxs-lookup"><span data-stu-id="83d4c-154">WINBIO\_ANSI\_381\_POS\_LH\_MIDDLE\_FINGER</span></span>
-   <span data-ttu-id="83d4c-155">WINBIO \_ ANSI \_ 381 \_ POS \_ - \_ \_ dito sinistro</span><span class="sxs-lookup"><span data-stu-id="83d4c-155">WINBIO\_ANSI\_381\_POS\_LH\_RING\_FINGER</span></span>
-   <span data-ttu-id="83d4c-156">WINBIO \_ ANSI \_ 381 \_ POS \_ LH \_ Little \_ Finger</span><span class="sxs-lookup"><span data-stu-id="83d4c-156">WINBIO\_ANSI\_381\_POS\_LH\_LITTLE\_FINGER</span></span>
-   <span data-ttu-id="83d4c-157">WINBIO \_ ANSI \_ 381 \_ POS \_ RH \_ quattro \_ dita</span><span class="sxs-lookup"><span data-stu-id="83d4c-157">WINBIO\_ANSI\_381\_POS\_RH\_FOUR\_FINGERS</span></span>
-   <span data-ttu-id="83d4c-158">WINBIO \_ ANSI \_ 381 \_ POS \_ LH \_ quattro \_ dita</span><span class="sxs-lookup"><span data-stu-id="83d4c-158">WINBIO\_ANSI\_381\_POS\_LH\_FOUR\_FINGERS</span></span>
-   <span data-ttu-id="83d4c-159">WINBIO \_ ANSI \_ 381 \_ POS \_ due \_ pollici</span><span class="sxs-lookup"><span data-stu-id="83d4c-159">WINBIO\_ANSI\_381\_POS\_TWO\_THUMBS</span></span>

> [!IMPORTANT]
>
> <span data-ttu-id="83d4c-160">Non tentare di convalidare il valore specificato per il valore del *Sottofattore* .</span><span class="sxs-lookup"><span data-stu-id="83d4c-160">Do not attempt to validate the value supplied for the *SubFactor* value.</span></span> <span data-ttu-id="83d4c-161">Il servizio biometria di Windows convaliderà il valore fornito prima di passarlo all'implementazione.</span><span class="sxs-lookup"><span data-stu-id="83d4c-161">The Windows Biometrics Service will validate the supplied value before passing it through to your implementation.</span></span> <span data-ttu-id="83d4c-162">Se il valore è **WINBIO, non vi sono \_ \_ \_ informazioni** o **\_ sottotipi \_ di WINBIO**, quindi eseguire la convalida laddove appropriato.</span><span class="sxs-lookup"><span data-stu-id="83d4c-162">If the value is **WINBIO\_SUBTYPE\_NO\_INFORMATION** or **WINBIO\_SUBTYPE\_ANY**, then validate where appropriate.</span></span>

 

</dd> <dt>

<span data-ttu-id="83d4c-163">**RejectDetail**</span><span class="sxs-lookup"><span data-stu-id="83d4c-163">**RejectDetail**</span></span>
</dt> <dd>

<span data-ttu-id="83d4c-164">Valore **ULONG** che contiene informazioni aggiuntive sull'errore di acquisizione di un campione biometrico.</span><span class="sxs-lookup"><span data-stu-id="83d4c-164">A **ULONG** value that contains additional information about the failure to capture a biometric sample.</span></span> <span data-ttu-id="83d4c-165">Se l'acquisizione ha avuto esito positivo, questo parametro è impostato su zero.</span><span class="sxs-lookup"><span data-stu-id="83d4c-165">If the capture succeeded, this parameter is set to zero.</span></span> <span data-ttu-id="83d4c-166">Per l'acquisizione di impronte digitali vengono definiti i valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="83d4c-166">The following values are defined for fingerprint capture:</span></span>

-   <span data-ttu-id="83d4c-167">WINBIO \_ FP \_ troppo \_ alta</span><span class="sxs-lookup"><span data-stu-id="83d4c-167">WINBIO\_FP\_TOO\_HIGH</span></span>
-   <span data-ttu-id="83d4c-168">WINBIO \_ FP \_ troppo \_ basso</span><span class="sxs-lookup"><span data-stu-id="83d4c-168">WINBIO\_FP\_TOO\_LOW</span></span>
-   <span data-ttu-id="83d4c-169">WINBIO \_ FP \_ troppo a \_ sinistra</span><span class="sxs-lookup"><span data-stu-id="83d4c-169">WINBIO\_FP\_TOO\_LEFT</span></span>
-   <span data-ttu-id="83d4c-170">WINBIO \_ FP \_ troppo a \_ destra</span><span class="sxs-lookup"><span data-stu-id="83d4c-170">WINBIO\_FP\_TOO\_RIGHT</span></span>
-   <span data-ttu-id="83d4c-171">WINBIO \_ FP \_ troppo \_ veloce</span><span class="sxs-lookup"><span data-stu-id="83d4c-171">WINBIO\_FP\_TOO\_FAST</span></span>
-   <span data-ttu-id="83d4c-172">WINBIO \_ FP \_ troppo \_ lento</span><span class="sxs-lookup"><span data-stu-id="83d4c-172">WINBIO\_FP\_TOO\_SLOW</span></span>
-   <span data-ttu-id="83d4c-173">WINBIO \_ FP \_ scarsa \_ qualità</span><span class="sxs-lookup"><span data-stu-id="83d4c-173">WINBIO\_FP\_POOR\_QUALITY</span></span>
-   <span data-ttu-id="83d4c-174">WINBIO \_ FP \_ troppo \_ sbilanciato</span><span class="sxs-lookup"><span data-stu-id="83d4c-174">WINBIO\_FP\_TOO\_SKEWED</span></span>
-   <span data-ttu-id="83d4c-175">WINBIO \_ FP \_ troppo \_ breve</span><span class="sxs-lookup"><span data-stu-id="83d4c-175">WINBIO\_FP\_TOO\_SHORT</span></span>
-   <span data-ttu-id="83d4c-176">\_errore di \_ merge WINBIO FP \_</span><span class="sxs-lookup"><span data-stu-id="83d4c-176">WINBIO\_FP\_MERGE\_FAILURE</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="83d4c-177">**Error (Errore) (Error (Errore)e)**</span><span class="sxs-lookup"><span data-stu-id="83d4c-177">**Error**</span></span>
</dt> <dd>

<span data-ttu-id="83d4c-178">Struttura che identifica l'esito positivo o negativo dell'operazione sottoposta a monitoraggio.</span><span class="sxs-lookup"><span data-stu-id="83d4c-178">Structure that identifies the success or failure of the operation being monitored.</span></span>

<dl> <dt>

<span data-ttu-id="83d4c-179">**ErrorCode**</span><span class="sxs-lookup"><span data-stu-id="83d4c-179">**ErrorCode**</span></span>
</dt> <dd>

<span data-ttu-id="83d4c-180">Valore **HRESULT** che contiene S \_ OK o un codice di errore risultante da calcoli eseguiti dal Windows Biometric Framework.</span><span class="sxs-lookup"><span data-stu-id="83d4c-180">**HRESULT** value that contains S\_OK or an error code that resulted from computations performed by the Windows Biometric Framework.</span></span>

</dd> </dl> </dd> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="83d4c-181">Commenti</span><span class="sxs-lookup"><span data-stu-id="83d4c-181">Remarks</span></span>

<span data-ttu-id="83d4c-182">Chiamare la funzione [**WinBioRegisterEventMonitor**](/windows/desktop/api/Winbio/nf-winbio-winbioregistereventmonitor) per registrare una routine di callback per ricevere notifiche degli eventi dal Windows Biometric Framework.</span><span class="sxs-lookup"><span data-stu-id="83d4c-182">Call the [**WinBioRegisterEventMonitor**](/windows/desktop/api/Winbio/nf-winbio-winbioregistereventmonitor) function to register a callback routine to receive event notifications from the Windows Biometric Framework.</span></span> <span data-ttu-id="83d4c-183">Il callback è una funzione personalizzata che è necessario definire per l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="83d4c-183">The callback is a custom function that you must define for your application.</span></span>

## <a name="requirements"></a><span data-ttu-id="83d4c-184">Requisiti</span><span class="sxs-lookup"><span data-stu-id="83d4c-184">Requirements</span></span>



| <span data-ttu-id="83d4c-185">Requisito</span><span class="sxs-lookup"><span data-stu-id="83d4c-185">Requirement</span></span> | <span data-ttu-id="83d4c-186">Valore</span><span class="sxs-lookup"><span data-stu-id="83d4c-186">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="83d4c-187">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="83d4c-187">Minimum supported client</span></span><br/> | <span data-ttu-id="83d4c-188">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="83d4c-188">Windows 7 \[desktop apps only\]</span></span><br/>                                                                    |
| <span data-ttu-id="83d4c-189">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="83d4c-189">Minimum supported server</span></span><br/> | <span data-ttu-id="83d4c-190">Solo app desktop Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="83d4c-190">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="83d4c-191">Intestazione</span><span class="sxs-lookup"><span data-stu-id="83d4c-191">Header</span></span><br/>                   | <dl> <span data-ttu-id="83d4c-192"><dt>\_Tipi WinBio. h (includere WinBio. h)</dt></span><span class="sxs-lookup"><span data-stu-id="83d4c-192"><dt>Winbio\_types.h (include Winbio.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="83d4c-193">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="83d4c-193">See also</span></span>

<dl> <dt>

[<span data-ttu-id="83d4c-194">Strutture delle applicazioni client</span><span class="sxs-lookup"><span data-stu-id="83d4c-194">Client Application Structures</span></span>](client-application-structures.md)
</dt> <dt>

[<span data-ttu-id="83d4c-195">**WinBioRegisterEventMonitor**</span><span class="sxs-lookup"><span data-stu-id="83d4c-195">**WinBioRegisterEventMonitor**</span></span>](/windows/desktop/api/Winbio/nf-winbio-winbioregistereventmonitor)
</dt> </dl>

 

 





