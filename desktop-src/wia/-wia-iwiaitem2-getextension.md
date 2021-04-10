---
description: Ottiene le interfacce di estensione che possono essere dotate di un driver di dispositivo Windows Image Acquisition (WIA) 2,0.
ms.assetid: 70f20f33-905c-4a88-8065-1cf876e98302
title: 'Metodo IWiaItem2:: GetExtension (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaItem2.GetExtension
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 2fea4c4b9a2dd909b7ec49097ee94664b47f7e47
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049515"
---
# <a name="iwiaitem2getextension-method"></a><span data-ttu-id="265b1-103">Metodo IWiaItem2:: GetExtension</span><span class="sxs-lookup"><span data-stu-id="265b1-103">IWiaItem2::GetExtension method</span></span>

<span data-ttu-id="265b1-104">Ottiene le interfacce di estensione che possono essere dotate di un driver di dispositivo Windows Image Acquisition (WIA) 2,0.</span><span class="sxs-lookup"><span data-stu-id="265b1-104">Gets the extension interfaces that might come with a Windows Image Acquisition (WIA) 2.0 device driver.</span></span>

## <a name="syntax"></a><span data-ttu-id="265b1-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="265b1-105">Syntax</span></span>


```C++
HRESULT GetExtension(
  [in]  LONG   lFlags,
  [in]  BSTR   bstrName,
  [in]  REFIID riidExtensionInterface,
  [out] VOID   **ppOut
);
```



## <a name="parameters"></a><span data-ttu-id="265b1-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="265b1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="265b1-107">*è* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="265b1-107">*lFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="265b1-108">Tipo: **Long**</span><span class="sxs-lookup"><span data-stu-id="265b1-108">Type: **LONG**</span></span>

<span data-ttu-id="265b1-109">Attualmente non usato.</span><span class="sxs-lookup"><span data-stu-id="265b1-109">Currently unused.</span></span> <span data-ttu-id="265b1-110">Deve essere impostato su zero.</span><span class="sxs-lookup"><span data-stu-id="265b1-110">Should be set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="265b1-111">*bstrName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="265b1-111">*bstrName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="265b1-112">Tipo: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="265b1-112">Type: **BSTR**</span></span>

<span data-ttu-id="265b1-113">Specifica il nome dell'estensione a cui l'applicazione chiamante richiede un puntatore.</span><span class="sxs-lookup"><span data-stu-id="265b1-113">Specifies the name of the extension that the calling application requires a pointer to.</span></span>

<dt>

<span id="SegmentationFilter"></span><span id="segmentationfilter"></span><span id="SEGMENTATIONFILTER"></span>

<span data-ttu-id="265b1-114"><span id="SegmentationFilter"></span><span id="segmentationfilter"></span><span id="SEGMENTATIONFILTER"></span>**SegmentationFilter**</span><span class="sxs-lookup"><span data-stu-id="265b1-114"><span id="SegmentationFilter"></span><span id="segmentationfilter"></span><span id="SEGMENTATIONFILTER"></span>**SegmentationFilter**</span></span>


</dt> <dd>

<span data-ttu-id="265b1-115">Estensione del filtro di segmentazione.</span><span class="sxs-lookup"><span data-stu-id="265b1-115">The segmentation filter extension.</span></span> <span data-ttu-id="265b1-116">Si tratta attualmente dell'unico valore valido per questo parametro.</span><span class="sxs-lookup"><span data-stu-id="265b1-116">This is currently the only valid value for this parameter.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="265b1-117">*riidExtensionInterface* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="265b1-117">*riidExtensionInterface* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="265b1-118">Tipo: **REFIID**</span><span class="sxs-lookup"><span data-stu-id="265b1-118">Type: **REFIID**</span></span>

<span data-ttu-id="265b1-119">Specifica l'identificatore dell'interfaccia di estensione.</span><span class="sxs-lookup"><span data-stu-id="265b1-119">Specifies the identifier of the extension interface.</span></span>

</dd> <dt>

<span data-ttu-id="265b1-120">*ppOut* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="265b1-120">*ppOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="265b1-121">Tipo: **void \* \***</span><span class="sxs-lookup"><span data-stu-id="265b1-121">Type: **VOID\*\***</span></span>

<span data-ttu-id="265b1-122">Riceve l'indirizzo di un puntatore all'interfaccia di estensione.</span><span class="sxs-lookup"><span data-stu-id="265b1-122">Receives the address of a pointer to the extension interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="265b1-123">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="265b1-123">Return value</span></span>

<span data-ttu-id="265b1-124">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="265b1-124">Type: **HRESULT**</span></span>

<span data-ttu-id="265b1-125">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="265b1-125">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="265b1-126">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="265b1-126">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="265b1-127">Commenti</span><span class="sxs-lookup"><span data-stu-id="265b1-127">Remarks</span></span>

<span data-ttu-id="265b1-128">Un'applicazione richiama questo metodo per creare un oggetto di estensione che implementa una delle interfacce di estensione del driver WIA 2,0.</span><span class="sxs-lookup"><span data-stu-id="265b1-128">An application invokes this method to create an extension object implementing one of the WIA 2.0 driver extension interfaces.</span></span> <span data-ttu-id="265b1-129">**IWiaItem2:: GetExtension** archivia l'indirizzo dell'interfaccia di estensione dell'oggetto estensione nel parametro *riidExtensionInterface* .</span><span class="sxs-lookup"><span data-stu-id="265b1-129">**IWiaItem2::GetExtension** stores the address of the extension object's extension interface in the *riidExtensionInterface* parameter.</span></span> <span data-ttu-id="265b1-130">L'applicazione usa quindi il puntatore di interfaccia per chiamare i relativi metodi.</span><span class="sxs-lookup"><span data-stu-id="265b1-130">The application then uses the interface pointer to call its methods.</span></span>

<span data-ttu-id="265b1-131">Le applicazioni devono chiamare il metodo [IUnknown:: Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) sui puntatori di interfaccia ricevuti tramite il parametro *riidExtensionInterface* .</span><span class="sxs-lookup"><span data-stu-id="265b1-131">Applications must call the [IUnknown::Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) method on the interface pointers they receive through the *riidExtensionInterface* parameter.</span></span>

## <a name="examples"></a><span data-ttu-id="265b1-132">Esempio</span><span class="sxs-lookup"><span data-stu-id="265b1-132">Examples</span></span>

<span data-ttu-id="265b1-133">CreateSegmentationFilter crea un'istanza del filtro di segmentazione ([**IWiaSegmentationFilter**](-wia-iwiasegmentationfilter.md)) del driver chiamando **IWiaItem2:: GetExtension** sull'interfaccia [**IWiaItem2**](-wia-iwiaitem2.md) passata.</span><span class="sxs-lookup"><span data-stu-id="265b1-133">CreateSegmentationFilter creates an instance of the driver's segmentation filter ([**IWiaSegmentationFilter**](-wia-iwiasegmentationfilter.md)) by calling **IWiaItem2::GetExtension** on the passed-in [**IWiaItem2**](-wia-iwiaitem2.md) interface.</span></span>


```C++
HRESULT
CreateSegmentationFilter(
   IWiaItem2               *pWiaItem2,
   IWiaSegmentationFilter  **ppSegmentationFilter)
{
   HRESULT                 hr         = S_OK;
   IWiaSegmentationFilter *pSegFilter = NULL;
    
   if (!pWiaItem2 || !ppSegmentationFilter)
   {
      hr = E_INVALIDARG;
   }

   if (SUCCEEDED(hr))
   {
      BSTR    bstrFilterString = SysAllocString(WIA_SEGMENTATION_FILTER_STR);

      if (bstrFilterString)
      {
         hr = pWiaItem2->GetExtension(0,
                                      bstrFilterString,
                                      IID_IWiaSegmentationFilter,
                                      (void**)&pSegFilter);
         SysFreeString(bstrFilterString);
         bstrFilterString = NULL;
      }
      else
      {
         hr = E_OUTOFMEMORY;
      }
   }

   if (SUCCEEDED(hr))
   {
     *ppSegmentationFilter = pSegFilter;
      pSegFilter = NULL;
   }
   return hr;
}
```



## <a name="requirements"></a><span data-ttu-id="265b1-134">Requisiti</span><span class="sxs-lookup"><span data-stu-id="265b1-134">Requirements</span></span>



| <span data-ttu-id="265b1-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="265b1-135">Requirement</span></span> | <span data-ttu-id="265b1-136">Valore</span><span class="sxs-lookup"><span data-stu-id="265b1-136">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="265b1-137">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="265b1-137">Minimum supported client</span></span><br/> | <span data-ttu-id="265b1-138">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="265b1-138">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="265b1-139">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="265b1-139">Minimum supported server</span></span><br/> | <span data-ttu-id="265b1-140">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="265b1-140">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="265b1-141">Intestazione</span><span class="sxs-lookup"><span data-stu-id="265b1-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="265b1-142"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="265b1-142"><dt>Wia.h</dt></span></span> </dl>   |
| <span data-ttu-id="265b1-143">IDL</span><span class="sxs-lookup"><span data-stu-id="265b1-143">IDL</span></span><br/>                      | <dl> <span data-ttu-id="265b1-144"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="265b1-144"><dt>Wia.idl</dt></span></span> </dl> |



 

 
