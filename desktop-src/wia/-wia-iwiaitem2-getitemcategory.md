---
description: Ottiene le informazioni sulla categoria di un elemento.
ms.assetid: 4d6f7a6a-280d-4b36-8e1d-8d9fcaa8a1de
title: 'Metodo IWiaItem2:: GetItemCategory (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaItem2.GetItemCategory
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: fdf650e8b540fcb9dc58f93f34771462fbc0a5c3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307362"
---
# <a name="iwiaitem2getitemcategory-method"></a><span data-ttu-id="c5e23-103">Metodo IWiaItem2:: GetItemCategory</span><span class="sxs-lookup"><span data-stu-id="c5e23-103">IWiaItem2::GetItemCategory method</span></span>

<span data-ttu-id="c5e23-104">Ottiene le informazioni sulla categoria di un elemento.</span><span class="sxs-lookup"><span data-stu-id="c5e23-104">Gets an item's category information.</span></span>

## <a name="syntax"></a><span data-ttu-id="c5e23-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c5e23-105">Syntax</span></span>


```C++
HRESULT GetItemCategory(
  [out] GUID *pItemCategoryGUID
);
```



## <a name="parameters"></a><span data-ttu-id="c5e23-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="c5e23-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c5e23-107">*pItemCategoryGUID* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="c5e23-107">*pItemCategoryGUID* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c5e23-108">Tipo: \**GUID \** _</span><span class="sxs-lookup"><span data-stu-id="c5e23-108">Type: \**GUID\** _</span></span>

<span data-ttu-id="c5e23-109">Riceve un puntatore al GUID che identifica la categoria dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="c5e23-109">Receives a pointer to the GUID that identifies the category of the item.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c5e23-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c5e23-110">Return value</span></span>

<span data-ttu-id="c5e23-111">Tipo: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="c5e23-111">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="c5e23-112">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="c5e23-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="c5e23-113">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="c5e23-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="c5e23-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="c5e23-114">Remarks</span></span>

<span data-ttu-id="c5e23-115">Ogni oggetto [**IWiaItem2**](-wia-iwiaitem2.md) nell'albero gerarchico di oggetti associati a un dispositivo hardware Windows Image Acquisition (WIA) 2,0 dispone di una categoria specifica.</span><span class="sxs-lookup"><span data-stu-id="c5e23-115">Every [**IWiaItem2**](-wia-iwiaitem2.md) object in the hierarchical tree of objects associated with a Windows Image Acquisition (WIA) 2.0 hardware device has a specific category.</span></span> <span data-ttu-id="c5e23-116">Questo metodo consente alle applicazioni di identificare la categoria di qualsiasi elemento in un albero gerarchico di oggetti elemento in un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c5e23-116">This method enables applications to identify the category of any item in a hierarchical tree of item objects in a device.</span></span>

## <a name="requirements"></a><span data-ttu-id="c5e23-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c5e23-117">Requirements</span></span>



| <span data-ttu-id="c5e23-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="c5e23-118">Requirement</span></span> | <span data-ttu-id="c5e23-119">Valore</span><span class="sxs-lookup"><span data-stu-id="c5e23-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="c5e23-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c5e23-120">Minimum supported client</span></span><br/> | <span data-ttu-id="c5e23-121">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c5e23-121">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="c5e23-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c5e23-122">Minimum supported server</span></span><br/> | <span data-ttu-id="c5e23-123">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="c5e23-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="c5e23-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c5e23-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="c5e23-125"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="c5e23-125"><dt>Wia.h</dt></span></span> </dl>   |
| <span data-ttu-id="c5e23-126">IDL</span><span class="sxs-lookup"><span data-stu-id="c5e23-126">IDL</span></span><br/>                      | <dl> <span data-ttu-id="c5e23-127"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="c5e23-127"><dt>Wia.idl</dt></span></span> </dl> |



 

 




