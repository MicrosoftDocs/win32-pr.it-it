---
description: Crea un oggetto di contesto che descrive il dispositivo Tablet specificato.
ms.assetid: 76f48485-a958-4457-9b87-73de73fa671e
title: 'Metodo ITablet:: CreateContext'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITablet.CreateContext
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: 9f1214f7f9e429b5f9b5b9614c2ccfc7fd1800b1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103884929"
---
# <a name="itabletcreatecontext-method"></a><span data-ttu-id="570ed-103">Metodo ITablet:: CreateContext</span><span class="sxs-lookup"><span data-stu-id="570ed-103">ITablet::CreateContext method</span></span>

<span data-ttu-id="570ed-104">Crea un oggetto di contesto che descrive il dispositivo Tablet specificato.</span><span class="sxs-lookup"><span data-stu-id="570ed-104">Creates a context object that describes the specified tablet device.</span></span>

## <a name="syntax"></a><span data-ttu-id="570ed-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="570ed-105">Syntax</span></span>


```C++
HRESULT CreateContext(
  [in]      HWND                    hWnd,
  [in]      RECT                    *prcInput,
  [in]      DWORD                   dwOptions,
  [in]      TABLET_CONTEXT_SETTINGS *pTCS,
  [in]      CONTEXT_ENABLE_TYPE     cet,
  [out]     ITabletContext          **ppCtx,
  [in, out] TABLET_CONTEXT_ID       *pTcid,
  [in, out] PACKET_DESCRIPTION      **ppPD,
  [in]      ITabletEventSink        *pSink
);
```



## <a name="parameters"></a><span data-ttu-id="570ed-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="570ed-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="570ed-107">*HWND* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="570ed-107">*hWnd* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="570ed-108">La finestra alla quale verrà collegato il contesto della tavoletta.</span><span class="sxs-lookup"><span data-stu-id="570ed-108">The window to which the tablet context will be attached.</span></span>

</dd> <dt>

<span data-ttu-id="570ed-109">*prcInput* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="570ed-109">*prcInput* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="570ed-110">\[in, univoco\]</span><span class="sxs-lookup"><span data-stu-id="570ed-110">\[in, unique\]</span></span>

<span data-ttu-id="570ed-111">Rettangolo di input dell'input penna.</span><span class="sxs-lookup"><span data-stu-id="570ed-111">The ink input rectangle.</span></span>

</dd> <dt>

<span data-ttu-id="570ed-112">*dwOptions* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="570ed-112">*dwOptions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="570ed-113">Flag che impostano le opzioni del contesto del tablet.</span><span class="sxs-lookup"><span data-stu-id="570ed-113">Flags that set tablet context options.</span></span>

</dd> <dt>

<span data-ttu-id="570ed-114">*pTCS* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="570ed-114">*pTCS* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="570ed-115">\[in, univoco\]</span><span class="sxs-lookup"><span data-stu-id="570ed-115">\[in, unique\]</span></span>

<span data-ttu-id="570ed-116">Informazioni dettagliate sul contesto del tablet da creare.</span><span class="sxs-lookup"><span data-stu-id="570ed-116">Detailed information about the tablet context to create.</span></span>

</dd> <dt>

<span data-ttu-id="570ed-117">*CET* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="570ed-117">*cet* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="570ed-118">Valore che Abilita o Disabilita i messaggi di contesto inviati alla finestra.</span><span class="sxs-lookup"><span data-stu-id="570ed-118">Value that enables or disables context messages being sent to the window.</span></span>

</dd> <dt>

<span data-ttu-id="570ed-119">*ppCtx* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="570ed-119">*ppCtx* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="570ed-120">Puntatore al nuovo contesto di creazione della tavoletta.</span><span class="sxs-lookup"><span data-stu-id="570ed-120">A pointer to the newly create tablet context.</span></span>

</dd> <dt>

<span data-ttu-id="570ed-121">*pTcid* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="570ed-121">*pTcid* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="570ed-122">Valore che identifica in modo univoco il tablet.</span><span class="sxs-lookup"><span data-stu-id="570ed-122">Value that uniquely identifies the tablet.</span></span>

</dd> <dt>

<span data-ttu-id="570ed-123">*ppPD* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="570ed-123">*ppPD* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="570ed-124">Puntatore alle informazioni sui dati contenuti in ogni pacchetto.</span><span class="sxs-lookup"><span data-stu-id="570ed-124">Pointer to information about what data is contained in each packet.</span></span>

</dd> <dt>

<span data-ttu-id="570ed-125">*pSink* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="570ed-125">*pSink* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="570ed-126">Oggetto [**ITabletEventSink**](itableteventsink.md) in cui verranno inviati i messaggi di notifica.</span><span class="sxs-lookup"><span data-stu-id="570ed-126">The [**ITabletEventSink**](itableteventsink.md) object where notification messages will be sent.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="570ed-127">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="570ed-127">Return value</span></span>

<span data-ttu-id="570ed-128">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="570ed-128">This method can return one of these values.</span></span>



| <span data-ttu-id="570ed-129">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="570ed-129">Return code</span></span>                                                                            | <span data-ttu-id="570ed-130">Descrizione</span><span class="sxs-lookup"><span data-stu-id="570ed-130">Description</span></span>                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="570ed-131"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="570ed-131"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="570ed-132">Esito positivo.</span><span class="sxs-lookup"><span data-stu-id="570ed-132">Success.</span></span><br/>                       |
| <dl> <span data-ttu-id="570ed-133"><dt>**E \_ non riescono**</dt></span><span class="sxs-lookup"><span data-stu-id="570ed-133"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="570ed-134">Si è verificato un errore non specificato.</span><span class="sxs-lookup"><span data-stu-id="570ed-134">An unspecified error occurred.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="570ed-135">Commenti</span><span class="sxs-lookup"><span data-stu-id="570ed-135">Remarks</span></span>

<span data-ttu-id="570ed-136">In genere, un'applicazione ottiene i valori predefiniti dal [**Metodo ITablet:: GetDefaultContextSettings**](itablet-getdefaultcontextsettings.md), modifica i valori in base alle proprie esigenze e quindi passa la struttura delle impostazioni modificate al **Metodo ITablet:: CreateContext**.</span><span class="sxs-lookup"><span data-stu-id="570ed-136">Typically, an application obtains the default values from the [**ITablet::GetDefaultContextSettings Method**](itablet-getdefaultcontextsettings.md), modifies values to suit their needs, and then passes the modified settings structure to the **ITablet::CreateContext Method**.</span></span>

> [!Note]  
> <span data-ttu-id="570ed-137">È necessario implementare l' [**interfaccia ITabletEventSink**](itableteventsink.md) quando si chiama il **Metodo ITablet:: CreateContext**.</span><span class="sxs-lookup"><span data-stu-id="570ed-137">You must implement the [**ITabletEventSink Interface**](itableteventsink.md) when calling the **ITablet::CreateContext Method**.</span></span>

 

<span data-ttu-id="570ed-138">Il parametro *dwOptions* è un set di flag di bit che descrivono le opzioni di contesto.</span><span class="sxs-lookup"><span data-stu-id="570ed-138">The *dwOptions* parameter is a set of bit flags that describe context options.</span></span> <span data-ttu-id="570ed-139">Nella tabella seguente vengono descritti questi flag.</span><span class="sxs-lookup"><span data-stu-id="570ed-139">The following table describes these flags.</span></span>



| <span data-ttu-id="570ed-140">Nome del flag</span><span class="sxs-lookup"><span data-stu-id="570ed-140">Flag Name</span></span>                                | <span data-ttu-id="570ed-141">Valore</span><span class="sxs-lookup"><span data-stu-id="570ed-141">Value</span></span>                                                                                                                                                                                         | <span data-ttu-id="570ed-142">Descrizione</span><span class="sxs-lookup"><span data-stu-id="570ed-142">Description</span></span>                                                                                                                                                                                                                                                              |
|------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="570ed-143">\_margine TCXO</span><span class="sxs-lookup"><span data-stu-id="570ed-143">TCXO\_MARGIN</span></span><br/>                  | <span data-ttu-id="570ed-144">0x00000001</span><span class="sxs-lookup"><span data-stu-id="570ed-144">0x00000001</span></span><br/>                                                                                                                                                                         | <span data-ttu-id="570ed-145">Specifica che il contesto di input nel Tablet avrà un margine.</span><span class="sxs-lookup"><span data-stu-id="570ed-145">Specifies that the input context on the tablet will have a margin.</span></span> <span data-ttu-id="570ed-146">Il margine è un'area al di fuori dell'area di input specificata in cui verrà eseguito il mapping degli eventi al bordo dell'area di input.</span><span class="sxs-lookup"><span data-stu-id="570ed-146">The margin is an area outside the specified input area where events will be mapped to the edge of the input area.</span></span> <span data-ttu-id="570ed-147">Questa funzionalità rende più semplice l'input dei punti al bordo del contesto.</span><span class="sxs-lookup"><span data-stu-id="570ed-147">This feature makes it easier to input points at the edge of the context.</span></span><br/> |
| <span data-ttu-id="570ed-148">prehook TCXO \_</span><span class="sxs-lookup"><span data-stu-id="570ed-148">TCXO\_PREHOOK</span></span><br/>                 | <span data-ttu-id="570ed-149">0x00000002</span><span class="sxs-lookup"><span data-stu-id="570ed-149">0x00000002</span></span><br/>                                                                                                                                                                         | <span data-ttu-id="570ed-150">Il prehook ottiene i pacchetti prima di contesti e posthook regolari.</span><span class="sxs-lookup"><span data-stu-id="570ed-150">Prehook gets packets before regular contexts and posthooks.</span></span> <span data-ttu-id="570ed-151">Ottengono i pacchetti nell'ordine di creazione.</span><span class="sxs-lookup"><span data-stu-id="570ed-151">They get packets in the order of their creation.</span></span><br/>                                                                                                                                                  |
| <span data-ttu-id="570ed-152">\_stato cursore \_ TCXO</span><span class="sxs-lookup"><span data-stu-id="570ed-152">TCXO\_CURSOR\_STATE</span></span><br/>           | <span data-ttu-id="570ed-153">0x00000004</span><span class="sxs-lookup"><span data-stu-id="570ed-153">0x00000004</span></span><br/>                                                                                                                                                                         | <span data-ttu-id="570ed-154">Il TC restituirà i pacchetti anche se il cursore è attivo.</span><span class="sxs-lookup"><span data-stu-id="570ed-154">The TC will return packets even if the cursor is up.</span></span> <span data-ttu-id="570ed-155">Per impostazione predefinita, un TC restituirà pacchetti solo quando il cursore è inattivo.</span><span class="sxs-lookup"><span data-stu-id="570ed-155">By default, a TC will only return packets when the cursor is down.</span></span><br/>                                                                                                                                       |
| <span data-ttu-id="570ed-156">TCXO \_ senza \_ cursore in \_ basso</span><span class="sxs-lookup"><span data-stu-id="570ed-156">TCXO\_NO\_CURSOR\_DOWN</span></span><br/>        | <span data-ttu-id="570ed-157">0x00000008</span><span class="sxs-lookup"><span data-stu-id="570ed-157">0x00000008</span></span><br/>                                                                                                                                                                         | <span data-ttu-id="570ed-158">Il TC non restituirà pacchetti quando il cursore non è attivo.</span><span class="sxs-lookup"><span data-stu-id="570ed-158">The TC will not return packets when the cursor is down.</span></span><br/>                                                                                                                                                                                                       |
| <span data-ttu-id="570ed-159">TCXO \_ non \_ integrato</span><span class="sxs-lookup"><span data-stu-id="570ed-159">TCXO\_NON\_INTEGRATED</span></span><br/>         | <span data-ttu-id="570ed-160">0x00000010</span><span class="sxs-lookup"><span data-stu-id="570ed-160">0x00000010</span></span><br/>                                                                                                                                                                         | <span data-ttu-id="570ed-161">Il contesto non sarà integrato.</span><span class="sxs-lookup"><span data-stu-id="570ed-161">The context will be non-integrated.</span></span><br/>                                                                                                                                                                                                                           |
| <span data-ttu-id="570ed-162">TCXO \_ POSThook</span><span class="sxs-lookup"><span data-stu-id="570ed-162">TCXO\_POSTHOOK</span></span><br/>                | <span data-ttu-id="570ed-163">0x00000020</span><span class="sxs-lookup"><span data-stu-id="570ed-163">0x00000020</span></span><br/>                                                                                                                                                                         | <span data-ttu-id="570ed-164">I posthook ottengono i pacchetti dopo i normali contesti di tablet ma prima del contesto di sistema.</span><span class="sxs-lookup"><span data-stu-id="570ed-164">Posthooks get packets after regular tablet contexts but before the system context.</span></span> <span data-ttu-id="570ed-165">Ottengono i pacchetti nell'ordine inverso rispetto alla loro creazione.</span><span class="sxs-lookup"><span data-stu-id="570ed-165">They get packets in the reverse order of their creation.</span></span><br/>                                                                                                                   |
| <span data-ttu-id="570ed-166">TCXO \_ non \_ Mostra \_ cursore</span><span class="sxs-lookup"><span data-stu-id="570ed-166">TCXO\_DONT\_SHOW\_CURSOR</span></span><br/>      | <span data-ttu-id="570ed-167">0x00000080</span><span class="sxs-lookup"><span data-stu-id="570ed-167">0x00000080</span></span><br/>                                                                                                                                                                         | <span data-ttu-id="570ed-168">Il TC non imposterà la posizione del cursore.</span><span class="sxs-lookup"><span data-stu-id="570ed-168">The TC will not set the cursor position.</span></span><br/>                                                                                                                                                                                                                      |
| <span data-ttu-id="570ed-169">TCXO \_ dont \_ Validate \_ TCS</span><span class="sxs-lookup"><span data-stu-id="570ed-169">TCXO\_DONT\_VALIDATE\_TCS</span></span><br/>     | <span data-ttu-id="570ed-170">0x00000100</span><span class="sxs-lookup"><span data-stu-id="570ed-170">0x00000100</span></span><br/>                                                                                                                                                                         | <span data-ttu-id="570ed-171">Il TC non convaliderà i GUID passati nelle impostazioni di contesto del tablet per le proprietà supportate del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="570ed-171">The TC will not validate the GUIDS passed in the tablet context settings against the supported properties of the device.</span></span><br/>                                                                                                                                      |
| <span data-ttu-id="570ed-172">TCXO \_ consentire i \_ gesti rapidi</span><span class="sxs-lookup"><span data-stu-id="570ed-172">TCXO\_ALLOW\_FLICKS</span></span><br/>           | <span data-ttu-id="570ed-173">0x00000400</span><span class="sxs-lookup"><span data-stu-id="570ed-173">0x00000400</span></span><br/>                                                                                                                                                                         | <span data-ttu-id="570ed-174">Il TC consentirà il rilevamento dei gesti rapidi (per impostazione predefinita è consentito solo nei contesti di sistema) e il client otterrà \_ gli eventi Flick.</span><span class="sxs-lookup"><span data-stu-id="570ed-174">The TC will allow flick detection to take place (by default this is only allowed on system contexts), and the client will get SE\_FLICK events.</span></span><br/>                                                                                                               |
| <span data-ttu-id="570ed-175">TCXO \_ consentire \_ i \_ rubinetti dei commenti</span><span class="sxs-lookup"><span data-stu-id="570ed-175">TCXO\_ALLOW\_FEEDBACK\_TAPS</span></span><br/>   | <span data-ttu-id="570ed-176">0x00000800</span><span class="sxs-lookup"><span data-stu-id="570ed-176">0x00000800</span></span><br/>                                                                                                                                                                         | <span data-ttu-id="570ed-177">Il TC consentirà di visualizzare il feedback della penna.</span><span class="sxs-lookup"><span data-stu-id="570ed-177">The TC will allow pen feedback to be shown.</span></span> <span data-ttu-id="570ed-178">Per impostazione predefinita, questa opzione è consentita solo nei contesti di sistema.</span><span class="sxs-lookup"><span data-stu-id="570ed-178">By default, this is only allowed on system contexts.</span></span><br/>                                                                                                                                                              |
| <span data-ttu-id="570ed-179">TCXO \_ Consenti \_ feedback \_ Barrel</span><span class="sxs-lookup"><span data-stu-id="570ed-179">TCXO\_ALLOW\_FEEDBACK\_BARREL</span></span><br/> | <span data-ttu-id="570ed-180">0x00001000</span><span class="sxs-lookup"><span data-stu-id="570ed-180">0x00001000</span></span><br/>                                                                                                                                                                         | <span data-ttu-id="570ed-181">Il TC consentirà di visualizzare il feedback della penna.</span><span class="sxs-lookup"><span data-stu-id="570ed-181">The TC will allow pen feedback to be shown.</span></span> <span data-ttu-id="570ed-182">Per impostazione predefinita, questa opzione è consentita solo nei contesti di sistema.</span><span class="sxs-lookup"><span data-stu-id="570ed-182">By default, this is only allowed on system contexts.</span></span><br/>                                                                                                                                                              |
| <span data-ttu-id="570ed-183">TCXO \_ tutto</span><span class="sxs-lookup"><span data-stu-id="570ed-183">TCXO\_ALL</span></span><br/>                     | <span data-ttu-id="570ed-184">TCXO \_ margin \| TCXO \_ prehook \| TCXO \_ Cursor \_ state \| TCXO \_ No \_ Cursor \_ down \| TCXO \_ non \_ Integrated \| TCXO \_ posthook \| TCXO \_ dont \_ Show \_ Cursor \| TCXO \_ dont \_ Validate \_ TCS</span><span class="sxs-lookup"><span data-stu-id="570ed-184">TCXO\_MARGIN \| TCXO\_PREHOOK \| TCXO\_CURSOR\_STATE \| TCXO\_NO\_CURSOR\_DOWN \| TCXO\_NON\_INTEGRATED \| TCXO\_POSTHOOK \| TCXO\_DONT\_SHOW\_CURSOR \| TCXO\_DONT\_VALIDATE\_TCS</span></span><br/> | <span data-ttu-id="570ed-185">Tutte le opzioni di contesto del Tablet definite.</span><span class="sxs-lookup"><span data-stu-id="570ed-185">All defined tablet context options.</span></span><br/>                                                                                                                                                                                                                           |
| <span data-ttu-id="570ed-186">\_hook TCXO</span><span class="sxs-lookup"><span data-stu-id="570ed-186">TCXO\_HOOK</span></span><br/>                    | <span data-ttu-id="570ed-187">TCXO \_ prehook \| TCXO \_</span><span class="sxs-lookup"><span data-stu-id="570ed-187">TCXO\_PREHOOK \| TCXO\_POSTHOOK</span></span><br/>                                                                                                                                                    | <span data-ttu-id="570ed-188">Combina la funzionalità di pre-Hook e post-hook.</span><span class="sxs-lookup"><span data-stu-id="570ed-188">Combines pre-hook and post-hook functionality.</span></span><br/>                                                                                                                                                                                                                |



 

## <a name="requirements"></a><span data-ttu-id="570ed-189">Requisiti</span><span class="sxs-lookup"><span data-stu-id="570ed-189">Requirements</span></span>



| <span data-ttu-id="570ed-190">Requisito</span><span class="sxs-lookup"><span data-stu-id="570ed-190">Requirement</span></span> | <span data-ttu-id="570ed-191">Valore</span><span class="sxs-lookup"><span data-stu-id="570ed-191">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="570ed-192">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="570ed-192">Minimum supported client</span></span><br/> | <span data-ttu-id="570ed-193">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="570ed-193">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="570ed-194">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="570ed-194">Minimum supported server</span></span><br/> | <span data-ttu-id="570ed-195">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="570ed-195">None supported</span></span><br/>                                                              |
| <span data-ttu-id="570ed-196">Libreria</span><span class="sxs-lookup"><span data-stu-id="570ed-196">Library</span></span><br/>                  | <dl> <span data-ttu-id="570ed-197"><dt>Wisptis.exe</dt></span><span class="sxs-lookup"><span data-stu-id="570ed-197"><dt>Wisptis.exe</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="570ed-198">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="570ed-198">See also</span></span>

<dl> <dt>

[<span data-ttu-id="570ed-199">**Interfaccia ITablet**</span><span class="sxs-lookup"><span data-stu-id="570ed-199">**ITablet Interface**</span></span>](itablet.md)
</dt> <dt>

[<span data-ttu-id="570ed-200">**\_Enumerazione del tipo abilitata per il contesto \_**</span><span class="sxs-lookup"><span data-stu-id="570ed-200">**CONTEXT\_ENABLE\_TYPE Enumeration**</span></span>](context-enable-type.md)
</dt> <dt>

[<span data-ttu-id="570ed-201">**\_ \_ Struttura delle impostazioni di contesto del Tablet**</span><span class="sxs-lookup"><span data-stu-id="570ed-201">**TABLET\_CONTEXT\_SETTINGS Structure**</span></span>](tablet-context-settings.md)
</dt> <dt>

[<span data-ttu-id="570ed-202">**\_Struttura di descrizione pacchetti**</span><span class="sxs-lookup"><span data-stu-id="570ed-202">**PACKET\_DESCRIPTION Structure**</span></span>](/windows/desktop/api/tpcshrd/ns-tpcshrd-packet_description)
</dt> <dt>

[<span data-ttu-id="570ed-203">**Interfaccia ITabletContextP**</span><span class="sxs-lookup"><span data-stu-id="570ed-203">**ITabletContextP Interface**</span></span>](itabletcontextp.md)
</dt> <dt>

[<span data-ttu-id="570ed-204">**Interfaccia ITabletEventSink**</span><span class="sxs-lookup"><span data-stu-id="570ed-204">**ITabletEventSink Interface**</span></span>](itableteventsink.md)
</dt> </dl>

 

 




