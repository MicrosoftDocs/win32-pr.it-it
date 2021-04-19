---
description: Il metodo SetMediaType specifica il tipo di supporto per la connessione sul pin di input del grabber di esempio.
ms.assetid: 9568832f-6666-45c9-9421-485c877affb3
title: 'Metodo ISampleGrabber:: SetMediaType (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISampleGrabber.SetMediaType
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: a39aa79e9311fe3491d0925fdc1b2dd3b1cc65c2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332641"
---
# <a name="isamplegrabbersetmediatype-method"></a><span data-ttu-id="efdf4-103">Metodo ISampleGrabber:: SetMediaType</span><span class="sxs-lookup"><span data-stu-id="efdf4-103">ISampleGrabber::SetMediaType method</span></span>

> [!Note]  
> <span data-ttu-id="efdf4-104">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="efdf4-104">\[Deprecated.</span></span> <span data-ttu-id="efdf4-105">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="efdf4-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="efdf4-106">Il `SetMediaType` metodo specifica il tipo di supporto per la connessione sul pin di input del grabber di esempio.</span><span class="sxs-lookup"><span data-stu-id="efdf4-106">The `SetMediaType` method specifies the media type for the connection on the input pin of the Sample Grabber.</span></span>

## <a name="syntax"></a><span data-ttu-id="efdf4-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="efdf4-107">Syntax</span></span>


```C++
HRESULT SetMediaType(
   const AM_MEDIA_TYPE *pType
);
```



## <a name="parameters"></a><span data-ttu-id="efdf4-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="efdf4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="efdf4-109">*pType*</span><span class="sxs-lookup"><span data-stu-id="efdf4-109">*pType*</span></span> 
</dt> <dd>

<span data-ttu-id="efdf4-110">Puntatore a una struttura del [**\_ \_ tipo di supporto am**](/windows/win32/api/strmif/ns-strmif-am_media_type) specifica il tipo di supporto richiesto.</span><span class="sxs-lookup"><span data-stu-id="efdf4-110">Pointer to an [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure specifies the required media type.</span></span> <span data-ttu-id="efdf4-111">Non è necessario impostare tutti i membri della struttura. per informazioni dettagliate, vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="efdf4-111">It is not necessary to set all the structure members; see Remarks for details.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="efdf4-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="efdf4-112">Return value</span></span>

<span data-ttu-id="efdf4-113">Restituisce \_ OK.</span><span class="sxs-lookup"><span data-stu-id="efdf4-113">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="efdf4-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="efdf4-114">Remarks</span></span>

<span data-ttu-id="efdf4-115">Per impostazione predefinita, il grabber di esempio non ha un tipo di supporto preferito.</span><span class="sxs-lookup"><span data-stu-id="efdf4-115">By default, the Sample Grabber has no preferred media type.</span></span> <span data-ttu-id="efdf4-116">Per assicurarsi che il grabber di esempio si connetta al filtro corretto, chiamare questo metodo prima di compilare il grafico del filtro.</span><span class="sxs-lookup"><span data-stu-id="efdf4-116">To ensure that the Sample Grabber connects to the correct filter, call this method before building the filter graph.</span></span>

<span data-ttu-id="efdf4-117">Questo metodo limita l'intervallo di tipi di supporti che verrà accettato dal filtro.</span><span class="sxs-lookup"><span data-stu-id="efdf4-117">This method restricts the range of media types that the filter will accept.</span></span> <span data-ttu-id="efdf4-118">Quando il filtro si connette, tenta di trovare la corrispondenza con il tipo di supporto specificato in *pType*.</span><span class="sxs-lookup"><span data-stu-id="efdf4-118">When the filter connects, it tries to match the media type given in *pType*.</span></span> <span data-ttu-id="efdf4-119">A tale scopo, vengono confrontati i GUID di tipo principale, sottotipo e tipo di formato, in questo ordine.</span><span class="sxs-lookup"><span data-stu-id="efdf4-119">To do so, it compares the major type, subtype, and format type GUIDs, in that order.</span></span> <span data-ttu-id="efdf4-120">Per ognuno di questi GUID, se *pType* ha il valore GUID \_ null, il grabber di esempio accetta il tipo di supporto senza ulteriori controlli.</span><span class="sxs-lookup"><span data-stu-id="efdf4-120">For each of these GUIDs, if *pType* has the value GUID\_NULL, the Sample Grabber accepts the media type without any further checks.</span></span> <span data-ttu-id="efdf4-121">Se *pType* ha un altro valore, il grabber di esempio lo confronta con il GUID nel tipo di connessione.</span><span class="sxs-lookup"><span data-stu-id="efdf4-121">If *pType* has any other value, the Sample Grabber compares it to the GUID in the connection type.</span></span> <span data-ttu-id="efdf4-122">A meno che i due GUID corrispondano esattamente, il grabber di esempio rifiuta la connessione.</span><span class="sxs-lookup"><span data-stu-id="efdf4-122">Unless the two GUIDs match exactly, the Sample Grabber rejects the connection.</span></span>

<span data-ttu-id="efdf4-123">Per i tipi di supporti video, il grabber di esempio ignora il blocco di formato.</span><span class="sxs-lookup"><span data-stu-id="efdf4-123">For video media types, the Sample Grabber ignores the format block.</span></span> <span data-ttu-id="efdf4-124">Pertanto, accetterà qualsiasi dimensione video e frequenza dei fotogrammi.</span><span class="sxs-lookup"><span data-stu-id="efdf4-124">Therefore, it will accept any video size and frame rate.</span></span> <span data-ttu-id="efdf4-125">Quando si chiama `SetMediaType` , impostare il blocco di formato (**pbFormat**) su **null** e la dimensione (**cbFormat**) su zero.</span><span class="sxs-lookup"><span data-stu-id="efdf4-125">When you call `SetMediaType`, set the format block (**pbFormat**) to **NULL** and the size (**cbFormat**) to zero.</span></span> <span data-ttu-id="efdf4-126">Per i tipi di supporti audio, il grabber di esempio esaminerà la struttura [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) e richiederà l'altro filtro per la connessione a tale formato, a meno che il blocco di formato in *pType* non sia **null** o il tag format sia un formato Wave \_ \_ PCM e gli altri membri della struttura siano pari a zero.</span><span class="sxs-lookup"><span data-stu-id="efdf4-126">For audio media types, the Sample Grabber will examine the [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) structure and will require the other filter to connect with that format — unless the format block in *pType* is **NULL**, or the format tag is WAVE\_FORMAT\_PCM and the other structure members are zero.</span></span>

<span data-ttu-id="efdf4-127">Esempio 1:</span><span class="sxs-lookup"><span data-stu-id="efdf4-127">Example 1:</span></span>

-   <span data-ttu-id="efdf4-128">Tipo principale: video di MEDIATYPE \_</span><span class="sxs-lookup"><span data-stu-id="efdf4-128">Major type: MEDIATYPE\_Video</span></span>
-   <span data-ttu-id="efdf4-129">Sottotipo: GUID \_ null</span><span class="sxs-lookup"><span data-stu-id="efdf4-129">Subtype: GUID\_NULL</span></span>
-   <span data-ttu-id="efdf4-130">Tipo di formato: GUID \_ null</span><span class="sxs-lookup"><span data-stu-id="efdf4-130">Format type: GUID\_NULL</span></span>

<span data-ttu-id="efdf4-131">Il grabber di esempio accetterà qualsiasi tipo di video in cui il tipo principale è uguale a MEDIATYPE \_ video.</span><span class="sxs-lookup"><span data-stu-id="efdf4-131">The Sample Grabber will accept any video type where the major type equals MEDIATYPE\_Video.</span></span> <span data-ttu-id="efdf4-132">Non controllerà il sottotipo.</span><span class="sxs-lookup"><span data-stu-id="efdf4-132">It will not check the subtype.</span></span>

<span data-ttu-id="efdf4-133">Esempio 2:</span><span class="sxs-lookup"><span data-stu-id="efdf4-133">Example 2:</span></span>

-   <span data-ttu-id="efdf4-134">Tipo principale: video di MEDIATYPE \_</span><span class="sxs-lookup"><span data-stu-id="efdf4-134">Major type: MEDIATYPE\_Video</span></span>
-   <span data-ttu-id="efdf4-135">Sottotipo: MEDIASUBTYPE \_ RGB24</span><span class="sxs-lookup"><span data-stu-id="efdf4-135">Subtype: MEDIASUBTYPE\_RGB24</span></span>
-   <span data-ttu-id="efdf4-136">Tipo di formato: GUID \_ null</span><span class="sxs-lookup"><span data-stu-id="efdf4-136">Format type: GUID\_NULL</span></span>

<span data-ttu-id="efdf4-137">A questo punto, il grabber di esempio controllerà il sottotipo e accetterà solo il video RGB 24.</span><span class="sxs-lookup"><span data-stu-id="efdf4-137">Now the Sample Grabber will check the subtype, and accept only RGB 24 video.</span></span>

<span data-ttu-id="efdf4-138">**Limitazioni:** Indipendentemente dal tipo impostato, il filtro Grabber di esempio rifiuta tutti i tipi di video con orientamento dall'alto in basso ( *bialtezza* negativa) o con un tipo di formato formato \_ VideoInfo2.</span><span class="sxs-lookup"><span data-stu-id="efdf4-138">**Limitations:** Regardless of what type you set, the Sample Grabber Filter rejects any video types with top-down orientation (negative *biHeight*), or with a format type of FORMAT\_VideoInfo2.</span></span> <span data-ttu-id="efdf4-139">In questo caso, anche se il `SetMediaType` metodo ha esito positivo, il filtro non si connette.</span><span class="sxs-lookup"><span data-stu-id="efdf4-139">In this case, although the `SetMediaType` method succeeds, the filter will not connect.</span></span>

> [!Note]  
> <span data-ttu-id="efdf4-140">Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="efdf4-140">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="efdf4-141">Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="efdf4-141">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="efdf4-142">Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="efdf4-142">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="efdf4-143">Requisiti</span><span class="sxs-lookup"><span data-stu-id="efdf4-143">Requirements</span></span>



| <span data-ttu-id="efdf4-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="efdf4-144">Requirement</span></span> | <span data-ttu-id="efdf4-145">Valore</span><span class="sxs-lookup"><span data-stu-id="efdf4-145">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="efdf4-146">Intestazione</span><span class="sxs-lookup"><span data-stu-id="efdf4-146">Header</span></span><br/>  | <dl> <span data-ttu-id="efdf4-147"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="efdf4-147"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="efdf4-148">Libreria</span><span class="sxs-lookup"><span data-stu-id="efdf4-148">Library</span></span><br/> | <dl> <span data-ttu-id="efdf4-149"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="efdf4-149"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="efdf4-150">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="efdf4-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="efdf4-151">Uso del grabber di esempio</span><span class="sxs-lookup"><span data-stu-id="efdf4-151">Using the Sample Grabber</span></span>](using-the-sample-grabber.md)
</dt> <dt>

[<span data-ttu-id="efdf4-152">**Interfaccia ISampleGrabber**</span><span class="sxs-lookup"><span data-stu-id="efdf4-152">**ISampleGrabber Interface**</span></span>](isamplegrabber.md)
</dt> </dl>

 

 
