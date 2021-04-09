---
description: Restituisce il frame richiesto da un'acquisizione caricata.
ms.assetid: efd1cff5-a3a1-4910-b003-25b6e10dad6e
title: Funzione ExpertGetFrame (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ExpertGetFrame
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 2bd02bde8caf157b6df6b1dd772a8f7574df0e57
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103878665"
---
# <a name="expertgetframe-function"></a><span data-ttu-id="64bdc-103">ExpertGetFrame (funzione)</span><span class="sxs-lookup"><span data-stu-id="64bdc-103">ExpertGetFrame function</span></span>

<span data-ttu-id="64bdc-104">La funzione **ExpertGetFrame** restituisce il frame richiesto da un'acquisizione caricata.</span><span class="sxs-lookup"><span data-stu-id="64bdc-104">The **ExpertGetFrame** function returns the requested frame from a loaded capture.</span></span>

## <a name="syntax"></a><span data-ttu-id="64bdc-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="64bdc-105">Syntax</span></span>


```C++
DWORD WINAPI ExpertGetFrame(
  _In_  HEXPERTKEY              hExpertKey,
  _In_  DWORD                   Direction,
  _In_  DWORD                   RequestFlags,
  _In_  DWORD                   RequestedFrameNumber,
  _In_  HFILTER                 hFilter,
  _Out_ LPEXPERTFRAMEDESCRIPTOR pEFrameDescriptor
);
```



## <a name="parameters"></a><span data-ttu-id="64bdc-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="64bdc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="64bdc-107">*hExpertKey* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="64bdc-107">*hExpertKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="64bdc-108">Identificatore univoco di un esperto.</span><span class="sxs-lookup"><span data-stu-id="64bdc-108">A unique expert identifier.</span></span> <span data-ttu-id="64bdc-109">Network Monitor passa l'identificatore *hExpertKey* all'esperto quando chiama la funzione [**Run**](run.md) .</span><span class="sxs-lookup"><span data-stu-id="64bdc-109">Network Monitor passes the *hExpertKey* identifier to the expert when it calls the [**Run**](run.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="64bdc-110">*Direzione* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="64bdc-110">*Direction* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="64bdc-111">Valore che identifica il modo in cui Network Monitor cerca il frame.</span><span class="sxs-lookup"><span data-stu-id="64bdc-111">A value that identifies how Network Monitor searches for the frame.</span></span>



| <span data-ttu-id="64bdc-112">Valore</span><span class="sxs-lookup"><span data-stu-id="64bdc-112">Value</span></span>                                                                                                                                                                                         | <span data-ttu-id="64bdc-113">Significato</span><span class="sxs-lookup"><span data-stu-id="64bdc-113">Meaning</span></span>                                |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------|
| <span id="GET_SPECIFIED_FRAME"></span><span id="get_specified_frame"></span><dl> <span data-ttu-id="64bdc-114"><dt>**OTTENERE \_ il \_ frame specificato**</dt></span><span class="sxs-lookup"><span data-stu-id="64bdc-114"><dt>**GET\_SPECIFIED\_FRAME**</dt></span></span> </dl>              | <span data-ttu-id="64bdc-115">Restituisce il frame richiesto.</span><span class="sxs-lookup"><span data-stu-id="64bdc-115">Return the requested frame.</span></span><br/> |
| <span id="GET_FRAME_NEXT_FORWARD"></span><span id="get_frame_next_forward"></span><dl> <span data-ttu-id="64bdc-116"><dt>**OTTENERE il \_ frame \_ successivo \_**</dt></span><span class="sxs-lookup"><span data-stu-id="64bdc-116"><dt>**GET\_FRAME\_NEXT\_FORWARD**</dt></span></span> </dl>    | <span data-ttu-id="64bdc-117">Restituisce il frame successivo.</span><span class="sxs-lookup"><span data-stu-id="64bdc-117">Return the next frame.</span></span><br/>      |
| <span id="GET_FRAME_NEXT_BACKWARD"></span><span id="get_frame_next_backward"></span><dl> <span data-ttu-id="64bdc-118"><dt>**OTTENERE il \_ frame \_ successivo all' \_ indietro**</dt></span><span class="sxs-lookup"><span data-stu-id="64bdc-118"><dt>**GET\_FRAME\_NEXT\_BACKWARD**</dt></span></span> </dl> | <span data-ttu-id="64bdc-119">Restituisce il frame precedente.</span><span class="sxs-lookup"><span data-stu-id="64bdc-119">Return the previous frame.</span></span><br/>  |



 

</dd> <dt>

<span data-ttu-id="64bdc-120">*RequestFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="64bdc-120">*RequestFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="64bdc-121">Flag che specificano il modo in cui Network Monitor deve gestire la richiesta.</span><span class="sxs-lookup"><span data-stu-id="64bdc-121">The flags that specify how Network Monitor should handle the request.</span></span> <span data-ttu-id="64bdc-122">Specificare uno o più dei flag seguenti.</span><span class="sxs-lookup"><span data-stu-id="64bdc-122">Specify one or more of the following flags.</span></span>



| <span data-ttu-id="64bdc-123">Valore</span><span class="sxs-lookup"><span data-stu-id="64bdc-123">Value</span></span>                                                                                                                                                                                             | <span data-ttu-id="64bdc-124">Significato</span><span class="sxs-lookup"><span data-stu-id="64bdc-124">Meaning</span></span>                                                                                                                                                                                                                                                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="FLAGS_DEFER_TO_UI_FILTER"></span><span id="flags_defer_to_ui_filter"></span><dl> <span data-ttu-id="64bdc-125"><dt>**FLAG \_ rinviato \_ al \_ filtro dell'interfaccia utente \_**</dt></span><span class="sxs-lookup"><span data-stu-id="64bdc-125"><dt>**FLAGS\_DEFER\_TO\_UI\_FILTER**</dt></span></span> </dl> | <span data-ttu-id="64bdc-126">Prima di applicare il parametro del filtro di visualizzazione dell'esperto specificato in *hFilter*, applicare il filtro di visualizzazione che Network Monitor sta utilizzando all'avvio dell'esperto.</span><span class="sxs-lookup"><span data-stu-id="64bdc-126">Before applying the display filter parameter of the expert which is specified in *hFilter*, apply the display filter that Network Monitor is using when the expert starts.</span></span><br/>                                                                                                                              |
| <span id="FLAGS_ATTACH_PROPERTIES"></span><span id="flags_attach_properties"></span><dl> <span data-ttu-id="64bdc-127"><dt>**FLAGs \_ Connetti \_ Proprietà**</dt></span><span class="sxs-lookup"><span data-stu-id="64bdc-127"><dt>**FLAGS\_ATTACH\_PROPERTIES**</dt></span></span> </dl>      | <span data-ttu-id="64bdc-128">Le proprietà individuate da tutti i parser di protocollo con le sezioni richieste di questo frame sono collegate al frame.</span><span class="sxs-lookup"><span data-stu-id="64bdc-128">The properties that all protocol parsers find with claimed sections of this frame are attached to the frame.</span></span> <span data-ttu-id="64bdc-129">Se il flag non è impostato, il campo **lpPropertyTable** della struttura [**EXPERTFRAMEDESCRIPTOR**](expertframedescriptor.md) (restituito da **PEFrameDescriptor**) verrà impostato su **null**.</span><span class="sxs-lookup"><span data-stu-id="64bdc-129">If the flag is not set, the **lpPropertyTable** field of the [**EXPERTFRAMEDESCRIPTOR**](expertframedescriptor.md) structure (returned by **pEFrameDescriptor**) will be set to **NULL**.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="64bdc-130">*RequestedFrameNumber* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="64bdc-130">*RequestedFrameNumber* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="64bdc-131">Numero del frame richiesto.</span><span class="sxs-lookup"><span data-stu-id="64bdc-131">The number of the requested frame.</span></span>

</dd> <dt>

<span data-ttu-id="64bdc-132">*hFilter* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="64bdc-132">*hFilter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="64bdc-133">Handle per il filtro di visualizzazione esperto.</span><span class="sxs-lookup"><span data-stu-id="64bdc-133">A handle to the expert display filter.</span></span> <span data-ttu-id="64bdc-134">Se l'esperto non dispone di un filtro di visualizzazione, impostare il parametro su **null**.</span><span class="sxs-lookup"><span data-stu-id="64bdc-134">If the expert does not have a display filter, set the parameter to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="64bdc-135">*pEFrameDescriptor* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="64bdc-135">*pEFrameDescriptor* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="64bdc-136">Struttura [**EXPERTFRAMEDESCRIPTOR**](expertframedescriptor.md) che, al ritorno, descrive il frame.</span><span class="sxs-lookup"><span data-stu-id="64bdc-136">The [**EXPERTFRAMEDESCRIPTOR**](expertframedescriptor.md) structure that, on return, describes the frame.</span></span> <span data-ttu-id="64bdc-137">L'esperto deve allocare e liberare la memoria utilizzata da questa struttura.</span><span class="sxs-lookup"><span data-stu-id="64bdc-137">The expert must allocate and free the memory that this structure uses.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="64bdc-138">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="64bdc-138">Return value</span></span>

<span data-ttu-id="64bdc-139">Se la funzione ha esito positivo, il valore restituito è NMERR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="64bdc-139">If the function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="64bdc-140">Se la funzione ha esito negativo, il valore restituito indica il motivo dell'errore.</span><span class="sxs-lookup"><span data-stu-id="64bdc-140">If the function is unsuccessful, the return value indicates the reason for the failure.</span></span> <span data-ttu-id="64bdc-141">Se il valore restituito è NMERR \_ Expert \_ Terminate, l'esperto deve eseguire immediatamente la pulizia e la restituzione; l'utente ha interrotto l'esecuzione dell'esperto.</span><span class="sxs-lookup"><span data-stu-id="64bdc-141">If the return value is NMERR\_EXPERT\_TERMINATE, the expert must immediately clean up and return; the user has aborted the expert run.</span></span>

## <a name="remarks"></a><span data-ttu-id="64bdc-142">Commenti</span><span class="sxs-lookup"><span data-stu-id="64bdc-142">Remarks</span></span>

<span data-ttu-id="64bdc-143">Se si impostano le \_ proprietà di associazione dei flag \_ , la chiamata richiede più risorse rispetto a quando non si imposta il flag.</span><span class="sxs-lookup"><span data-stu-id="64bdc-143">If you set FLAGS\_ATTACH\_PROPERTIES, the call requires more resources than if you do not set the flag.</span></span> <span data-ttu-id="64bdc-144">Se il flag non è impostato, un puntatore punta al frame non elaborato e ai dati relativi al frame.</span><span class="sxs-lookup"><span data-stu-id="64bdc-144">If the flag is not set, a pointer points to the raw frame and to data about the frame.</span></span> <span data-ttu-id="64bdc-145">Se questo flag è impostato, Network Monitor connette tutte le proprietà al frame chiamando ogni parser che attesta una parte del frame.</span><span class="sxs-lookup"><span data-stu-id="64bdc-145">If this flag is set, Network Monitor attaches all properties to the frame by calling every parser that claims a portion of the frame.</span></span> <span data-ttu-id="64bdc-146">Questo può essere un processo lento.</span><span class="sxs-lookup"><span data-stu-id="64bdc-146">This can be a slow process.</span></span>

<span data-ttu-id="64bdc-147">Gli esperti non devono impostare il \_ flag delle proprietà di associazione dei flag \_ a meno che gli esperti non richiedano le proprietà che i parser alleghino al frame.</span><span class="sxs-lookup"><span data-stu-id="64bdc-147">Experts should not set the FLAGS\_ATTACH\_PROPERTIES flag unless the experts require the properties that parsers attach to the frame.</span></span> <span data-ttu-id="64bdc-148">Se possibile, gli esperti devono chiamare la funzione **ExpertGetFrame** senza il flag, quindi estrarre i dati richiesti direttamente dal frame.</span><span class="sxs-lookup"><span data-stu-id="64bdc-148">If possible, experts should call the **ExpertGetFrame** function without the flag, and then extract the required data directly from the frame.</span></span>

<span data-ttu-id="64bdc-149">Se l'esperto chiama **ExpertGetFrame** senza il flag delle proprietà di associazione dei flag \_ \_ e richiede le proprietà associate a tale frame (ad esempio, un evento), l'esperto chiama **ExpertGetFrame** con gli stessi parametri tranne i seguenti:</span><span class="sxs-lookup"><span data-stu-id="64bdc-149">If the expert calls **ExpertGetFrame** without the FLAGS\_ATTACH\_PROPERTIES flag and requires the properties associated with that frame (an event, for example), the expert calls **ExpertGetFrame** with the same parameters except for the following:</span></span>

``` syntax
Direction = EXPERT_GET_SPECIFIED_FRAME;
RequestFlags &= (~EXPERT_DEFER_TO_UI_FILTER) | EXPERT_ATTACH_PROPERTIES;
RequestedFrameNumber= (The actual frame number you want);
hFilter = NULL;
pEFrameDescriptor = (The same one as last time);
```

<span data-ttu-id="64bdc-150">L'uso del codice precedente garantisce che l'esperto ottenga il frame necessario senza dover chiamare di nuovo il codice di filtro.</span><span class="sxs-lookup"><span data-stu-id="64bdc-150">Using the preceding code ensures that the expert gets the required frame without having to call filter code again.</span></span>

<span data-ttu-id="64bdc-151">È possibile impostare il parametro *hFilter* come **LPVOID**.</span><span class="sxs-lookup"><span data-stu-id="64bdc-151">You can set the *hFilter* parameter as an **LPVOID**.</span></span> <span data-ttu-id="64bdc-152">Se esiste, il frame restituito passa il filtro.</span><span class="sxs-lookup"><span data-stu-id="64bdc-152">If it exists, the returned frame passes this filter.</span></span> <span data-ttu-id="64bdc-153">Se l'esperto non dispone di un filtro di visualizzazione da passare alla funzione (se *hFilter* è **null** ), il frame restituito non viene filtrato.</span><span class="sxs-lookup"><span data-stu-id="64bdc-153">If the expert does not have a display filter to pass to the function (if *hFilter* is **NULL** ), then the frame returned is not filtered.</span></span>

<span data-ttu-id="64bdc-154">La funzione **ExpertGetFrame** può essere chiamata solo da esperti che implementano la funzione di esportazione [**Run**](run.md) o [**Configure**](configure.md) .</span><span class="sxs-lookup"><span data-stu-id="64bdc-154">The **ExpertGetFrame** function can only be called by experts that implement the [**Run**](run.md) or [**Configure**](configure.md) export function.</span></span>

## <a name="requirements"></a><span data-ttu-id="64bdc-155">Requisiti</span><span class="sxs-lookup"><span data-stu-id="64bdc-155">Requirements</span></span>



| <span data-ttu-id="64bdc-156">Requisito</span><span class="sxs-lookup"><span data-stu-id="64bdc-156">Requirement</span></span> | <span data-ttu-id="64bdc-157">Valore</span><span class="sxs-lookup"><span data-stu-id="64bdc-157">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="64bdc-158">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="64bdc-158">Minimum supported client</span></span><br/> | <span data-ttu-id="64bdc-159">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="64bdc-159">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="64bdc-160">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="64bdc-160">Minimum supported server</span></span><br/> | <span data-ttu-id="64bdc-161">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="64bdc-161">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="64bdc-162">Intestazione</span><span class="sxs-lookup"><span data-stu-id="64bdc-162">Header</span></span><br/>                   | <dl> <span data-ttu-id="64bdc-163"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="64bdc-163"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="64bdc-164">Libreria</span><span class="sxs-lookup"><span data-stu-id="64bdc-164">Library</span></span><br/>                  | <dl> <span data-ttu-id="64bdc-165"><dt>Nmap. lib</dt></span><span class="sxs-lookup"><span data-stu-id="64bdc-165"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="64bdc-166">DLL</span><span class="sxs-lookup"><span data-stu-id="64bdc-166">DLL</span></span><br/>                      | <dl> <span data-ttu-id="64bdc-167"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="64bdc-167"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 




