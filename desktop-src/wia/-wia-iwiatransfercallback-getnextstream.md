---
description: Ottiene un nuovo flusso per l'elemento specificato.
ms.assetid: fe25843c-2051-42fe-8737-eea39f6aeab9
title: 'Metodo IWiaTransferCallback:: GetNextStream (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaTransferCallback.GetNextStream
api_type:
- COM
api_location:
- Wiaguid.lib
- Wiaguid.dll
ms.openlocfilehash: fb2e92c9cade1dfd48efc3051b617997bf8473e9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307353"
---
# <a name="iwiatransfercallbackgetnextstream-method"></a><span data-ttu-id="89339-103">Metodo IWiaTransferCallback:: GetNextStream</span><span class="sxs-lookup"><span data-stu-id="89339-103">IWiaTransferCallback::GetNextStream method</span></span>

<span data-ttu-id="89339-104">Ottiene un nuovo flusso per l'elemento specificato.</span><span class="sxs-lookup"><span data-stu-id="89339-104">Gets a new stream for the specified item.</span></span>

## <a name="syntax"></a><span data-ttu-id="89339-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="89339-105">Syntax</span></span>


```C++
HRESULT GetNextStream(
  [in]  LONG    lFlags,
  [in]  BSTR    bstrItemName,
  [in]  BSTR    bstrFullItemName,
  [out] IStream **ppDestination
);
```



## <a name="parameters"></a><span data-ttu-id="89339-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="89339-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="89339-107">*è* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="89339-107">*lFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="89339-108">Tipo: **Long**</span><span class="sxs-lookup"><span data-stu-id="89339-108">Type: **LONG**</span></span>

<span data-ttu-id="89339-109">Attualmente non usato.</span><span class="sxs-lookup"><span data-stu-id="89339-109">Currently unused.</span></span> <span data-ttu-id="89339-110">Deve essere impostato su zero.</span><span class="sxs-lookup"><span data-stu-id="89339-110">Should be set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="89339-111">*bstrItemName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="89339-111">*bstrItemName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="89339-112">Tipo: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="89339-112">Type: **BSTR**</span></span>

<span data-ttu-id="89339-113">Specifica il nome dell'elemento per cui creare il flusso.</span><span class="sxs-lookup"><span data-stu-id="89339-113">Specifies the name of the item to create stream for.</span></span>

</dd> <dt>

<span data-ttu-id="89339-114">*bstrFullItemName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="89339-114">*bstrFullItemName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="89339-115">Tipo: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="89339-115">Type: **BSTR**</span></span>

<span data-ttu-id="89339-116">Specifica il nome completo dell'elemento per il quale creare il flusso.</span><span class="sxs-lookup"><span data-stu-id="89339-116">Specifies the full name of the item to create stream for.</span></span>

</dd> <dt>

<span data-ttu-id="89339-117">*ppDestination* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="89339-117">*ppDestination* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="89339-118">Tipo: **[IStream](/windows/win32/api/objidl/nn-objidl-istream)\*\***</span><span class="sxs-lookup"><span data-stu-id="89339-118">Type: **[IStream](/windows/win32/api/objidl/nn-objidl-istream)\*\***</span></span>

<span data-ttu-id="89339-119">Riceve l'indirizzo di un puntatore al nuovo oggetto [IStream](/windows/win32/api/objidl/nn-objidl-istream) .</span><span class="sxs-lookup"><span data-stu-id="89339-119">Receives the address of a pointer to the new [IStream](/windows/win32/api/objidl/nn-objidl-istream) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="89339-120">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="89339-120">Return value</span></span>

<span data-ttu-id="89339-121">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="89339-121">Type: **HRESULT**</span></span>

<span data-ttu-id="89339-122">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="89339-122">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="89339-123">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="89339-123">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="89339-124">Commenti</span><span class="sxs-lookup"><span data-stu-id="89339-124">Remarks</span></span>

<span data-ttu-id="89339-125">Quando questo metodo viene implementato da un filtro di elaborazione delle immagini, Windows Image Acquisition (WIA) 2,0 minidriver lo chiama durante l'acquisizione dell'immagine per ottenere il flusso di destinazione dal client.</span><span class="sxs-lookup"><span data-stu-id="89339-125">When this method is implemented by an image processing filter, the Windows Image Acquisition (WIA) 2.0 minidriver calls it during image acquisition to get the destination stream from the client.</span></span>

<span data-ttu-id="89339-126">Un filtro **IWiaTransferCallback:: GetNextStream** deve delegare al metodo di callback dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="89339-126">A filter's **IWiaTransferCallback::GetNextStream** must delegate to the application's callback method.</span></span> <span data-ttu-id="89339-127">Il filtro usa il flusso restituito dall'implementazione **IWiaTransferCallback:: GetNextStream** del callback dell'applicazione per creare il proprio flusso che passa di nuovo al servizio WIA 2,0.</span><span class="sxs-lookup"><span data-stu-id="89339-127">The filter uses the stream returned by the application callback's **IWiaTransferCallback::GetNextStream** implementation to create its own stream that it passes back to the WIA 2.0 service.</span></span> <span data-ttu-id="89339-128">Il filtro viene eseguito quando il flusso del filtro chiama il metodo [IStream:: Write](/windows/win32/api/objidl/nf-objidl-isequentialstream-write) .</span><span class="sxs-lookup"><span data-stu-id="89339-128">The filtering is done when the filter's stream calls the [IStream::Write](/windows/win32/api/objidl/nf-objidl-isequentialstream-write) method.</span></span>

<span data-ttu-id="89339-129">Il flusso del filtro non può ipotizzare il numero di byte scritti in ogni scrittura, poiché i dati dell'immagine non filtrata possono provenire dal componente WIA 2,0 Preview anziché dal driver.</span><span class="sxs-lookup"><span data-stu-id="89339-129">The filter's stream cannot make any assumptions on the number of bytes that are written to it on each write, since the unfiltered image data may come from the WIA 2.0 Preview Component rather than the driver.</span></span> <span data-ttu-id="89339-130">Il componente WIA 2,0 Preview scrive sempre tutti i dati dell'immagine non filtrati nel flusso del filtro una sola volta, il che significa che il flusso del filtro contiene una scrittura di origine.</span><span class="sxs-lookup"><span data-stu-id="89339-130">The WIA 2.0 Preview Component always writes the whole unfiltered image data into the filter's stream only once, which means that the filter's stream has one source writing into it.</span></span> <span data-ttu-id="89339-131">Se il driver e il componente di anteprima vengono scritti nel flusso del filtro, il flusso del filtro non può presumere, ad esempio, che riceva l'intestazione completa la prima volta che [IStream:: Write](/windows/win32/api/objidl/nf-objidl-isequentialstream-write) viene chiamato, sebbene il driver corrispondente scriva sempre i dati dell'intestazione prima in un'unica operazione di scrittura.</span><span class="sxs-lookup"><span data-stu-id="89339-131">If both the driver and the preview component write into the filter's stream, the filter's stream cannot assume, for example, that it will receive the full header the first time [IStream::Write](/windows/win32/api/objidl/nf-objidl-isequentialstream-write) is called although its corresponding driver always writes the header data first in one write.</span></span> <span data-ttu-id="89339-132">Non è possibile presupporre che una scrittura successiva contenga esattamente una riga di analisi.</span><span class="sxs-lookup"><span data-stu-id="89339-132">Nor can it assume that a subsequent write contains exactly one scan line.</span></span> <span data-ttu-id="89339-133">Il flusso di filtro potrebbe quindi dover contare il numero di byte scritti per determinare, ad esempio, dove vengono avviati i dati dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="89339-133">So the filtering stream may have to count the number of bytes written to it to determine, for example, where the image data starts.</span></span>

<span data-ttu-id="89339-134">L'implementazione di **IWiaTransferCallback:: GetNextStream** del filtro di elaborazione delle immagini deve leggere le proprietà necessarie per l'elaborazione delle immagini dall'elemento per il quale viene acquisita l'immagine.</span><span class="sxs-lookup"><span data-stu-id="89339-134">The image processing filter's **IWiaTransferCallback::GetNextStream** implementation should read the properties needed for its image processing from the item for which the image is being acquired.</span></span> <span data-ttu-id="89339-135">Il filtro non legge le proprietà direttamente da *pWiaItem2* passato in [**InitializeFilter**](-wia-iwiaimagefilter-initializefilter.md).</span><span class="sxs-lookup"><span data-stu-id="89339-135">The filter does not read the properties directly from the *pWiaItem2* passed into [**InitializeFilter**](-wia-iwiaimagefilter-initializefilter.md).</span></span> <span data-ttu-id="89339-136">Il filtro deve invece chiamare [**FindItemByName**](-wia-iwiaitem2-finditembyname.md) su questo elemento WIA 2,0 per ottenere l'elemento WIA 2,0 effettivo.</span><span class="sxs-lookup"><span data-stu-id="89339-136">Instead the filter must call [**FindItemByName**](-wia-iwiaitem2-finditembyname.md) on this WIA 2.0 item to obtain the actual WIA 2.0 item.</span></span> <span data-ttu-id="89339-137">Il motivo è che l'immagine acquisita può effettivamente essere un elemento figlio di *pWiaItem2*.</span><span class="sxs-lookup"><span data-stu-id="89339-137">The reason for this is that the image being acquired may actually be a child item of *pWiaItem2*.</span></span> <span data-ttu-id="89339-138">Ad esempio, durante l'acquisizione di una cartella il filtro usa *pWiaItem2* per ottenere gli elementi figlio di *pWiaItem2* in **IWiaTransferCallback:: GetNextStream** (durante l'acquisizione di una cartella, il driver restituisce le immagini rappresentate dagli elementi figlio di *pWiaItem2*).</span><span class="sxs-lookup"><span data-stu-id="89339-138">For example, during a folder acquisition the filter uses *pWiaItem2* to obtain *pWiaItem2*'s child items in **IWiaTransferCallback::GetNextStream** (during a folder acquisition the driver returns the images represented by the child items of *pWiaItem2*).</span></span> <span data-ttu-id="89339-139">Lo stesso accade quando il componente WIA 2,0 Preview chiama il filtro di elaborazione dell'immagine passando un elemento WIA 2,0 figlio.</span><span class="sxs-lookup"><span data-stu-id="89339-139">The same is true when the WIA 2.0 Preview Component calls into the image processing filter passing a child WIA 2.0 item.</span></span>

## <a name="requirements"></a><span data-ttu-id="89339-140">Requisiti</span><span class="sxs-lookup"><span data-stu-id="89339-140">Requirements</span></span>



| <span data-ttu-id="89339-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="89339-141">Requirement</span></span> | <span data-ttu-id="89339-142">Valore</span><span class="sxs-lookup"><span data-stu-id="89339-142">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="89339-143">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="89339-143">Minimum supported client</span></span><br/> | <span data-ttu-id="89339-144">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="89339-144">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="89339-145">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="89339-145">Minimum supported server</span></span><br/> | <span data-ttu-id="89339-146">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="89339-146">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="89339-147">Intestazione</span><span class="sxs-lookup"><span data-stu-id="89339-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="89339-148"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="89339-148"><dt>Wia.h</dt></span></span> </dl>       |
| <span data-ttu-id="89339-149">IDL</span><span class="sxs-lookup"><span data-stu-id="89339-149">IDL</span></span><br/>                      | <dl> <span data-ttu-id="89339-150"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="89339-150"><dt>Wia.idl</dt></span></span> </dl>     |
| <span data-ttu-id="89339-151">Libreria</span><span class="sxs-lookup"><span data-stu-id="89339-151">Library</span></span><br/>                  | <dl> <span data-ttu-id="89339-152"><dt>Wiaguid. lib</dt></span><span class="sxs-lookup"><span data-stu-id="89339-152"><dt>Wiaguid.lib</dt></span></span> </dl> |



 

 
