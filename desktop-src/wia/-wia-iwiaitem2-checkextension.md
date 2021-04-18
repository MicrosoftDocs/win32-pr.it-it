---
description: "Verifica se un'estensione specificata è disponibile nel computer e può essere usata dal metodo IWiaItem2:: GetExtension."
ms.assetid: 672f6418-4ce3-4570-a412-fe639c9f5eb8
title: 'Metodo IWiaItem2:: CheckExtension (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaItem2.CheckExtension
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 65b0b5b3ace1634a20dfa63382d82099fef0686e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308222"
---
# <a name="iwiaitem2checkextension-method"></a><span data-ttu-id="950e8-103">Metodo IWiaItem2:: CheckExtension</span><span class="sxs-lookup"><span data-stu-id="950e8-103">IWiaItem2::CheckExtension method</span></span>

<span data-ttu-id="950e8-104">Verifica se un'estensione specificata è disponibile nel computer e può essere usata dal metodo [**IWiaItem2:: GetExtension**](-wia-iwiaitem2-getextension.md) .</span><span class="sxs-lookup"><span data-stu-id="950e8-104">Checks whether a specified extension is available on the machine and can be used by the [**IWiaItem2::GetExtension**](-wia-iwiaitem2-getextension.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="950e8-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="950e8-105">Syntax</span></span>


```C++
HRESULT CheckExtension(
  [in]  LONG   lFlags,
  [in]  BSTR   bstrName,
  [in]  REFIID riidExtensionInterface,
  [out] BOOL   *pbExtensionExists
);
```



## <a name="parameters"></a><span data-ttu-id="950e8-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="950e8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="950e8-107">*è* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="950e8-107">*lFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="950e8-108">Tipo: **Long**</span><span class="sxs-lookup"><span data-stu-id="950e8-108">Type: **LONG**</span></span>

<span data-ttu-id="950e8-109">Attualmente non usato.</span><span class="sxs-lookup"><span data-stu-id="950e8-109">Currently unused.</span></span> <span data-ttu-id="950e8-110">Deve essere impostato su zero.</span><span class="sxs-lookup"><span data-stu-id="950e8-110">Should be set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="950e8-111">*bstrName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="950e8-111">*bstrName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="950e8-112">Tipo: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="950e8-112">Type: **BSTR**</span></span>

<span data-ttu-id="950e8-113">Specifica il nome dell'estensione.</span><span class="sxs-lookup"><span data-stu-id="950e8-113">Specifies the name of the extension.</span></span>

</dd> <dt>

<span data-ttu-id="950e8-114">*riidExtensionInterface* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="950e8-114">*riidExtensionInterface* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="950e8-115">Tipo: **REFIID**</span><span class="sxs-lookup"><span data-stu-id="950e8-115">Type: **REFIID**</span></span>

<span data-ttu-id="950e8-116">Attualmente non usato.</span><span class="sxs-lookup"><span data-stu-id="950e8-116">Currently unused.</span></span>

</dd> <dt>

<span data-ttu-id="950e8-117">*pbExtensionExists* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="950e8-117">*pbExtensionExists* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="950e8-118">Tipo: \**bool \** _</span><span class="sxs-lookup"><span data-stu-id="950e8-118">Type: \**BOOL\** _</span></span>

<span data-ttu-id="950e8-119">Riceve un puntatore a _ \* BOOL \* \*.</span><span class="sxs-lookup"><span data-stu-id="950e8-119">Receives a pointer to a _\*BOOL\*\*.</span></span>

<dt>

<span id="FALSE"></span><span id="false"></span>

<span data-ttu-id="950e8-120"><span id="FALSE"></span><span id="false"></span>**FALSE**</span><span class="sxs-lookup"><span data-stu-id="950e8-120"><span id="FALSE"></span><span id="false"></span>**FALSE**</span></span>


</dt> <dd>

<span data-ttu-id="950e8-121">L'estensione specificata non è disponibile.</span><span class="sxs-lookup"><span data-stu-id="950e8-121">The specified extension is not available.</span></span>

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span data-ttu-id="950e8-122"><span id="TRUE"></span><span id="true"></span>**TRUE**</span><span class="sxs-lookup"><span data-stu-id="950e8-122"><span id="TRUE"></span><span id="true"></span>**TRUE**</span></span>


</dt> <dd>

<span data-ttu-id="950e8-123">L'estensione specificata è disponibile.</span><span class="sxs-lookup"><span data-stu-id="950e8-123">The specified extension is available.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="950e8-124">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="950e8-124">Return value</span></span>

<span data-ttu-id="950e8-125">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="950e8-125">Type: **HRESULT**</span></span>

<span data-ttu-id="950e8-126">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="950e8-126">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="950e8-127">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="950e8-127">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="950e8-128">Commenti</span><span class="sxs-lookup"><span data-stu-id="950e8-128">Remarks</span></span>

<span data-ttu-id="950e8-129">Utilizzando questo metodo, le applicazioni possono verificare se un'estensione è disponibile prima di chiamare il metodo [**IWiaItem2:: GetExtension**](-wia-iwiaitem2-getextension.md) .</span><span class="sxs-lookup"><span data-stu-id="950e8-129">Using this method, applications can check whether an extension is available before calling the [**IWiaItem2::GetExtension**](-wia-iwiaitem2-getextension.md) method.</span></span> <span data-ttu-id="950e8-130">Inoltre, l'applicazione può verificare quali estensioni sono disponibili senza co-creazione di ognuna di esse, quindi decidere quale usare.</span><span class="sxs-lookup"><span data-stu-id="950e8-130">Also, the application can check which extensions are available without co-creating each of them, and then decide which one to use.</span></span>

## <a name="examples"></a><span data-ttu-id="950e8-131">Esempio</span><span class="sxs-lookup"><span data-stu-id="950e8-131">Examples</span></span>

<span data-ttu-id="950e8-132">CheckImgFilter controlla se il driver ha un filtro di elaborazione delle immagini.</span><span class="sxs-lookup"><span data-stu-id="950e8-132">CheckImgFilter checks if the driver has an image processing filter.</span></span> <span data-ttu-id="950e8-133">Prima di chiamare il componente di anteprima, un'applicazione deve verificare che il driver disponga di un filtro di elaborazione delle immagini.</span><span class="sxs-lookup"><span data-stu-id="950e8-133">Before calling into the preview component, an application should ensure that the driver has an image processing filter.</span></span>


```C++
HRESULT
CheckImgFilter(
   IN  IWiaItem2 *pWiaItem2,
   OUT BOOL      *pbHasImgFilter)
{
   HRESULT     hr = S_OK;

   if (!pWiaItem2 || !pbHasImgFilter)
   {
      hr = E_INVALIDARG;
   }

   if (SUCCEEDED(hr))
   {
     *pbHasImgFilter = FALSE;
   }

   if (SUCCEEDED(hr))
   {
      BSTR    bstrFilterString = SysAllocString(WIA_IMAGEPROC_FILTER_STR);

      if (bstrFilterString)
      {
         hr = pWiaItem2->CheckExtension(0,
                                        bstrFilterString,
                                        IID_IWiaSegmentationFilter,
                                        pbHasImgFilter);

         SysFreeString(bstrFilterString);
         bstrFilterString = NULL;
      }
      else
      {
         hr = E_OUTOFMEMORY;
      }
   }

   return hr;

}
```



## <a name="requirements"></a><span data-ttu-id="950e8-134">Requisiti</span><span class="sxs-lookup"><span data-stu-id="950e8-134">Requirements</span></span>



| <span data-ttu-id="950e8-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="950e8-135">Requirement</span></span> | <span data-ttu-id="950e8-136">Valore</span><span class="sxs-lookup"><span data-stu-id="950e8-136">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="950e8-137">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="950e8-137">Minimum supported client</span></span><br/> | <span data-ttu-id="950e8-138">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="950e8-138">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="950e8-139">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="950e8-139">Minimum supported server</span></span><br/> | <span data-ttu-id="950e8-140">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="950e8-140">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="950e8-141">Intestazione</span><span class="sxs-lookup"><span data-stu-id="950e8-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="950e8-142"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="950e8-142"><dt>Wia.h</dt></span></span> </dl>   |
| <span data-ttu-id="950e8-143">IDL</span><span class="sxs-lookup"><span data-stu-id="950e8-143">IDL</span></span><br/>                      | <dl> <span data-ttu-id="950e8-144"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="950e8-144"><dt>Wia.idl</dt></span></span> </dl> |



 

 




