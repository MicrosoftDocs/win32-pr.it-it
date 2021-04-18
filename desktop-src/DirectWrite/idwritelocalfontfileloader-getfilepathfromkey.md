---
title: Metodo IDWriteLocalFontFileLoader GetFilePathFromKey
description: Ottiene il percorso del file del tipo di carattere assoluto dalla chiave di riferimento del file del tipo di carattere.
ms.assetid: a61cfe80-100d-4813-b04f-a39f626893dd
keywords:
- Scrittura diretta metodo GetFilePathFromKey
- Metodo GetFilePathFromKey scrittura diretta, interfaccia IDWriteLocalFontFileLoader
- IDWriteLocalFontFileLoader Interface Direct Write, metodo GetFilePathFromKey
topic_type:
- apiref
api_name:
- IDWriteLocalFontFileLoader.GetFilePathFromKey
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 14fb3070ddc2f0d82554c86f005343faa3c087fe
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329142"
---
# <a name="idwritelocalfontfileloadergetfilepathfromkey-method"></a><span data-ttu-id="89109-106">Metodo IDWriteLocalFontFileLoader:: GetFilePathFromKey</span><span class="sxs-lookup"><span data-stu-id="89109-106">IDWriteLocalFontFileLoader::GetFilePathFromKey method</span></span>

<span data-ttu-id="89109-107">Ottiene il percorso del file del tipo di carattere assoluto dalla chiave di riferimento del file del tipo di carattere.</span><span class="sxs-lookup"><span data-stu-id="89109-107">Obtains the absolute font file path from the font file reference key.</span></span>

## <a name="syntax"></a><span data-ttu-id="89109-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="89109-108">Syntax</span></span>


```C++
virtual HRESULT GetFilePathFromKey(
  [in]  const void   *fontFileReferenceKey,
              UINT32 fontFileReferenceKeySize,
  [out]       WCHAR  *filePath,
              UINT32 filePathSize
) = 0;
```



## <a name="parameters"></a><span data-ttu-id="89109-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="89109-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="89109-110">*fontFileReferenceKey* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="89109-110">*fontFileReferenceKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="89109-111">Tipo: **const \* void**</span><span class="sxs-lookup"><span data-stu-id="89109-111">Type: **const void\***</span></span>

<span data-ttu-id="89109-112">Chiave di riferimento del file del tipo di carattere che identifica in modo univoco il file del tipo di carattere locale nell'ambito del caricatore del tipo di carattere utilizzato.</span><span class="sxs-lookup"><span data-stu-id="89109-112">The font file reference key that uniquely identifies the local font file within the scope of the font loader being used.</span></span>

</dd> <dt>

<span data-ttu-id="89109-113">*fontFileReferenceKeySize*</span><span class="sxs-lookup"><span data-stu-id="89109-113">*fontFileReferenceKeySize*</span></span> 
</dt> <dd>

<span data-ttu-id="89109-114">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="89109-114">Type: **UINT32**</span></span>

<span data-ttu-id="89109-115">Dimensioni in byte della chiave di riferimento del file del tipo di carattere.</span><span class="sxs-lookup"><span data-stu-id="89109-115">The size of font file reference key in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="89109-116">*filePath* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="89109-116">*filePath* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="89109-117">Tipo: **WCHAR \***</span><span class="sxs-lookup"><span data-stu-id="89109-117">Type: **WCHAR\***</span></span>

<span data-ttu-id="89109-118">Matrice di caratteri che riceve il percorso del file locale.</span><span class="sxs-lookup"><span data-stu-id="89109-118">The character array that receives the local file path.</span></span>

</dd> <dt>

<span data-ttu-id="89109-119">*filePathSize*</span><span class="sxs-lookup"><span data-stu-id="89109-119">*filePathSize*</span></span> 
</dt> <dd>

<span data-ttu-id="89109-120">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="89109-120">Type: **UINT32**</span></span>

<span data-ttu-id="89109-121">Lunghezza della matrice di caratteri del percorso del file.</span><span class="sxs-lookup"><span data-stu-id="89109-121">The length of the file path character array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="89109-122">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="89109-122">Return value</span></span>

<span data-ttu-id="89109-123">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="89109-123">Type: **HRESULT**</span></span>

<span data-ttu-id="89109-124">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="89109-124">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="89109-125">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="89109-125">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="89109-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="89109-126">Requirements</span></span>



| <span data-ttu-id="89109-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="89109-127">Requirement</span></span> | <span data-ttu-id="89109-128">Valore</span><span class="sxs-lookup"><span data-stu-id="89109-128">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="89109-129">Libreria</span><span class="sxs-lookup"><span data-stu-id="89109-129">Library</span></span><br/> | <dl> <span data-ttu-id="89109-130"><dt>DWrite. lib</dt></span><span class="sxs-lookup"><span data-stu-id="89109-130"><dt>Dwrite.lib</dt></span></span> </dl> |
| <span data-ttu-id="89109-131">DLL</span><span class="sxs-lookup"><span data-stu-id="89109-131">DLL</span></span><br/>     | <dl> <span data-ttu-id="89109-132"><dt>Dwrite.dll</dt></span><span class="sxs-lookup"><span data-stu-id="89109-132"><dt>Dwrite.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="89109-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="89109-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="89109-134">**IDWriteLocalFontFileLoader**</span><span class="sxs-lookup"><span data-stu-id="89109-134">**IDWriteLocalFontFileLoader**</span></span>](idwritelocalfontfileloader.md)
</dt> </dl>

 

 





