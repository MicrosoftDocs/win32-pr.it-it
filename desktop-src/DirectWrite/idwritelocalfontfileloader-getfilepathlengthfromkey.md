---
title: Metodo IDWriteLocalFontFileLoader GetFilePathLengthFromKey
description: Ottiene la lunghezza del percorso del file assoluto dalla chiave di riferimento del file del tipo di carattere.
ms.assetid: bdd84d75-5a7a-448a-a52c-0f5997ab07b9
keywords:
- Scrittura diretta metodo GetFilePathLengthFromKey
- Metodo GetFilePathLengthFromKey scrittura diretta, interfaccia IDWriteLocalFontFileLoader
- IDWriteLocalFontFileLoader Interface Direct Write, metodo GetFilePathLengthFromKey
topic_type:
- apiref
api_name:
- IDWriteLocalFontFileLoader.GetFilePathLengthFromKey
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 091c3cd5f1e13c40d364a3db005793f1dd0bf5f1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330159"
---
# <a name="idwritelocalfontfileloadergetfilepathlengthfromkey-method"></a><span data-ttu-id="1caca-106">Metodo IDWriteLocalFontFileLoader:: GetFilePathLengthFromKey</span><span class="sxs-lookup"><span data-stu-id="1caca-106">IDWriteLocalFontFileLoader::GetFilePathLengthFromKey method</span></span>

<span data-ttu-id="1caca-107">Ottiene la lunghezza del percorso del file assoluto dalla chiave di riferimento del file del tipo di carattere.</span><span class="sxs-lookup"><span data-stu-id="1caca-107">Obtains the length of the absolute file path from the font file reference key.</span></span>

## <a name="syntax"></a><span data-ttu-id="1caca-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1caca-108">Syntax</span></span>


```C++
HRESULT GetFilePathLengthFromKey(
  [in]  const void   *fontFileReferenceKey,
              UINT32 fontFileReferenceKeySize,
  [out]       UINT32 *filePathLength
);
```



## <a name="parameters"></a><span data-ttu-id="1caca-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="1caca-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1caca-110">*fontFileReferenceKey* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1caca-110">*fontFileReferenceKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1caca-111">Tipo: **const \* void**</span><span class="sxs-lookup"><span data-stu-id="1caca-111">Type: **const void\***</span></span>

<span data-ttu-id="1caca-112">Chiave di riferimento del file del tipo di carattere che identifica in modo univoco il file del tipo di carattere locale nell'ambito del caricatore del tipo di carattere utilizzato.</span><span class="sxs-lookup"><span data-stu-id="1caca-112">Font file reference key that uniquely identifies the local font file within the scope of the font loader being used.</span></span>

</dd> <dt>

<span data-ttu-id="1caca-113">*fontFileReferenceKeySize*</span><span class="sxs-lookup"><span data-stu-id="1caca-113">*fontFileReferenceKeySize*</span></span> 
</dt> <dd>

<span data-ttu-id="1caca-114">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1caca-114">Type: **UINT32**</span></span>

<span data-ttu-id="1caca-115">Dimensione della chiave di riferimento del file del tipo di carattere in byte.</span><span class="sxs-lookup"><span data-stu-id="1caca-115">Size of font file reference key in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="1caca-116">*filePathLength* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="1caca-116">*filePathLength* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1caca-117">Tipo: **UInt32 \***</span><span class="sxs-lookup"><span data-stu-id="1caca-117">Type: **UINT32\***</span></span>

<span data-ttu-id="1caca-118">Lunghezza della stringa del percorso del file, escluso il carattere **null** terminato.</span><span class="sxs-lookup"><span data-stu-id="1caca-118">Length of the file path string, not including the terminated **NULL** character.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1caca-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="1caca-119">Return value</span></span>

<span data-ttu-id="1caca-120">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="1caca-120">Type: **HRESULT**</span></span>

<span data-ttu-id="1caca-121">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="1caca-121">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="1caca-122">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="1caca-122">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="1caca-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1caca-123">Requirements</span></span>



| <span data-ttu-id="1caca-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="1caca-124">Requirement</span></span> | <span data-ttu-id="1caca-125">Valore</span><span class="sxs-lookup"><span data-stu-id="1caca-125">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1caca-126">Libreria</span><span class="sxs-lookup"><span data-stu-id="1caca-126">Library</span></span><br/> | <dl> <span data-ttu-id="1caca-127"><dt>DWrite. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1caca-127"><dt>Dwrite.lib</dt></span></span> </dl> |
| <span data-ttu-id="1caca-128">DLL</span><span class="sxs-lookup"><span data-stu-id="1caca-128">DLL</span></span><br/>     | <dl> <span data-ttu-id="1caca-129"><dt>Dwrite.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1caca-129"><dt>Dwrite.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1caca-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1caca-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1caca-131">**IDWriteLocalFontFileLoader**</span><span class="sxs-lookup"><span data-stu-id="1caca-131">**IDWriteLocalFontFileLoader**</span></span>](idwritelocalfontfileloader.md)
</dt> </dl>

 

 





