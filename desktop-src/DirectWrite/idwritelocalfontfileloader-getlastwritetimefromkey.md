---
title: Metodo IDWriteLocalFontFileLoader GetLastWriteTimeFromKey
description: Ottiene l'ora dell'ultima scrittura del file dalla chiave di riferimento del file del tipo di carattere.
ms.assetid: ce7f5321-8ad8-4412-a54c-7102790e99c0
keywords:
- Scrittura diretta metodo GetLastWriteTimeFromKey
- Metodo GetLastWriteTimeFromKey scrittura diretta, interfaccia IDWriteLocalFontFileLoader
- IDWriteLocalFontFileLoader Interface Direct Write, metodo GetLastWriteTimeFromKey
topic_type:
- apiref
api_name:
- IDWriteLocalFontFileLoader.GetLastWriteTimeFromKey
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ea9817917a59761278a961a6fcafcdeaea5fda32
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330158"
---
# <a name="idwritelocalfontfileloadergetlastwritetimefromkey-method"></a><span data-ttu-id="4f551-106">Metodo IDWriteLocalFontFileLoader:: GetLastWriteTimeFromKey</span><span class="sxs-lookup"><span data-stu-id="4f551-106">IDWriteLocalFontFileLoader::GetLastWriteTimeFromKey method</span></span>

<span data-ttu-id="4f551-107">Ottiene l'ora dell'ultima scrittura del file dalla chiave di riferimento del file del tipo di carattere.</span><span class="sxs-lookup"><span data-stu-id="4f551-107">Obtains the last write time of the file from the font file reference key.</span></span>

## <a name="syntax"></a><span data-ttu-id="4f551-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4f551-108">Syntax</span></span>


```C++
virtual HRESULT GetLastWriteTimeFromKey(
  [in]  const void     *fontFileReferenceKey,
              UINT32   fontFileReferenceKeySize,
  [out]       FILETIME *lastWriteTime
) = 0;
```



## <a name="parameters"></a><span data-ttu-id="4f551-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="4f551-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4f551-110">*fontFileReferenceKey* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4f551-110">*fontFileReferenceKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4f551-111">Tipo: **const \* void**</span><span class="sxs-lookup"><span data-stu-id="4f551-111">Type: **const void\***</span></span>

<span data-ttu-id="4f551-112">Chiave di riferimento del file del tipo di carattere che identifica in modo univoco il file del tipo di carattere locale nell'ambito del caricatore del tipo di carattere utilizzato.</span><span class="sxs-lookup"><span data-stu-id="4f551-112">The font file reference key that uniquely identifies the local font file within the scope of the font loader being used.</span></span>

</dd> <dt>

<span data-ttu-id="4f551-113">*fontFileReferenceKeySize*</span><span class="sxs-lookup"><span data-stu-id="4f551-113">*fontFileReferenceKeySize*</span></span> 
</dt> <dd>

<span data-ttu-id="4f551-114">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4f551-114">Type: **UINT32**</span></span>

<span data-ttu-id="4f551-115">Dimensioni in byte della chiave di riferimento del file del tipo di carattere.</span><span class="sxs-lookup"><span data-stu-id="4f551-115">The size of font file reference key in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="4f551-116">*LastWriteTime* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="4f551-116">*lastWriteTime* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4f551-117">Tipo: **FILEtime \***</span><span class="sxs-lookup"><span data-stu-id="4f551-117">Type: **FILETIME\***</span></span>

<span data-ttu-id="4f551-118">Ora dell'Ultima modifica del file del tipo di carattere.</span><span class="sxs-lookup"><span data-stu-id="4f551-118">The time of the last font file modification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4f551-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4f551-119">Return value</span></span>

<span data-ttu-id="4f551-120">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="4f551-120">Type: **HRESULT**</span></span>

<span data-ttu-id="4f551-121">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="4f551-121">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="4f551-122">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="4f551-122">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="4f551-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4f551-123">Requirements</span></span>



| <span data-ttu-id="4f551-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="4f551-124">Requirement</span></span> | <span data-ttu-id="4f551-125">Valore</span><span class="sxs-lookup"><span data-stu-id="4f551-125">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4f551-126">Libreria</span><span class="sxs-lookup"><span data-stu-id="4f551-126">Library</span></span><br/> | <dl> <span data-ttu-id="4f551-127"><dt>DWrite. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4f551-127"><dt>Dwrite.lib</dt></span></span> </dl> |
| <span data-ttu-id="4f551-128">DLL</span><span class="sxs-lookup"><span data-stu-id="4f551-128">DLL</span></span><br/>     | <dl> <span data-ttu-id="4f551-129"><dt>Dwrite.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4f551-129"><dt>Dwrite.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4f551-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4f551-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4f551-131">**IDWriteLocalFontFileLoader**</span><span class="sxs-lookup"><span data-stu-id="4f551-131">**IDWriteLocalFontFileLoader**</span></span>](idwritelocalfontfileloader.md)
</dt> </dl>

 

 





