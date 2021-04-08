---
description: Ottiene le informazioni sul tipo di un elemento.
ms.assetid: 9670f184-e8ba-4596-af6d-2967320dfd95
title: 'Metodo IWiaItem2:: GetItemType (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaItem2.GetItemType
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 3bf177ddcc117cdfe21a1b9322a0e457cf899c0c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751783"
---
# <a name="iwiaitem2getitemtype-method"></a><span data-ttu-id="ef1b5-103">Metodo IWiaItem2:: GetItemType</span><span class="sxs-lookup"><span data-stu-id="ef1b5-103">IWiaItem2::GetItemType method</span></span>

<span data-ttu-id="ef1b5-104">Ottiene le informazioni sul tipo di un elemento.</span><span class="sxs-lookup"><span data-stu-id="ef1b5-104">Gets an item's type information.</span></span>

## <a name="syntax"></a><span data-ttu-id="ef1b5-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ef1b5-105">Syntax</span></span>


```C++
HRESULT GetItemType(
  [out] LONG *pItemType
);
```



## <a name="parameters"></a><span data-ttu-id="ef1b5-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="ef1b5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ef1b5-107">*pItemType* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="ef1b5-107">*pItemType* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ef1b5-108">Tipo: \**Long \** _</span><span class="sxs-lookup"><span data-stu-id="ef1b5-108">Type: \**LONG\** _</span></span>

<span data-ttu-id="ef1b5-109">Riceve un puntatore a un oggetto _ *Long*\* che contiene una combinazione di flag di tipo.</span><span class="sxs-lookup"><span data-stu-id="ef1b5-109">Receives a pointer to a _ *LONG*\* that contains a combination of type flags.</span></span> <span data-ttu-id="ef1b5-110">Vedere i [**flag del tipo di elemento WIA**](-wia-wia-item-type-flags.md).</span><span class="sxs-lookup"><span data-stu-id="ef1b5-110">See [**WIA Item Type Flags**](-wia-wia-item-type-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ef1b5-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ef1b5-111">Return value</span></span>

<span data-ttu-id="ef1b5-112">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="ef1b5-112">Type: **HRESULT**</span></span>

<span data-ttu-id="ef1b5-113">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="ef1b5-113">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="ef1b5-114">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="ef1b5-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="ef1b5-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="ef1b5-115">Remarks</span></span>

<span data-ttu-id="ef1b5-116">Ogni oggetto [**IWiaItem2**](-wia-iwiaitem2.md) nell'albero gerarchico di oggetti associati a un dispositivo hardware Windows Image Acquisition (WIA) 2,0 dispone di un tipo di dati specifico.</span><span class="sxs-lookup"><span data-stu-id="ef1b5-116">Every [**IWiaItem2**](-wia-iwiaitem2.md) object in the hierarchical tree of objects associated with a Windows Image Acquisition (WIA) 2.0 hardware device has a specific data type.</span></span> <span data-ttu-id="ef1b5-117">Gli oggetti Item rappresentano cartelle e file.</span><span class="sxs-lookup"><span data-stu-id="ef1b5-117">Item objects represent folders and files.</span></span> <span data-ttu-id="ef1b5-118">Le cartelle contengono oggetti file.</span><span class="sxs-lookup"><span data-stu-id="ef1b5-118">Folders contain file objects.</span></span> <span data-ttu-id="ef1b5-119">Gli oggetti file contengono i dati acquisiti dal dispositivo, ad esempio immagini e suoni.</span><span class="sxs-lookup"><span data-stu-id="ef1b5-119">File objects contain data acquired by the device such as images and sounds.</span></span> <span data-ttu-id="ef1b5-120">Questo metodo consente alle applicazioni di identificare il tipo di qualsiasi elemento in un albero gerarchico di oggetti elemento in un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ef1b5-120">This method enables applications to identify the type of any item in a hierarchical tree of item objects in a device.</span></span>

<span data-ttu-id="ef1b5-121">Un elemento può avere più di un tipo.</span><span class="sxs-lookup"><span data-stu-id="ef1b5-121">An item may have more than one type.</span></span> <span data-ttu-id="ef1b5-122">Ad esempio, un elemento che rappresenta un file audio avrà gli attributi di tipo [**WiaItemTypeAudio**](-wia-wia-item-type-flags.md) \| **WiaItemTypeFile**.</span><span class="sxs-lookup"><span data-stu-id="ef1b5-122">For example, an item that represents an audio file will have the type attributes [**WiaItemTypeAudio**](-wia-wia-item-type-flags.md) \| **WiaItemTypeFile**.</span></span>

## <a name="requirements"></a><span data-ttu-id="ef1b5-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ef1b5-123">Requirements</span></span>



| <span data-ttu-id="ef1b5-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="ef1b5-124">Requirement</span></span> | <span data-ttu-id="ef1b5-125">Valore</span><span class="sxs-lookup"><span data-stu-id="ef1b5-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="ef1b5-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ef1b5-126">Minimum supported client</span></span><br/> | <span data-ttu-id="ef1b5-127">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ef1b5-127">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="ef1b5-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ef1b5-128">Minimum supported server</span></span><br/> | <span data-ttu-id="ef1b5-129">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="ef1b5-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="ef1b5-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ef1b5-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="ef1b5-131"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="ef1b5-131"><dt>Wia.h</dt></span></span> </dl>   |
| <span data-ttu-id="ef1b5-132">IDL</span><span class="sxs-lookup"><span data-stu-id="ef1b5-132">IDL</span></span><br/>                      | <dl> <span data-ttu-id="ef1b5-133"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="ef1b5-133"><dt>Wia.idl</dt></span></span> </dl> |



 

 




