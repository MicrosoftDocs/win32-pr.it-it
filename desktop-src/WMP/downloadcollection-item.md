---
title: Metodo DownloadCollection. Item
description: Si noti che questa sezione descrive la funzionalità progettata per l'uso da parte degli archivi online. L'uso di questa funzionalità al di fuori del contesto di un archivio online non è supportato. Il metodo Item recupera un oggetto download in sospeso.
ms.assetid: a79db9db-e80c-48db-aee6-9bd8f77a7dff
keywords:
- Metodo Item Media Player Windows
- Metodo Item Media Player Windows, classe DownloadCollection
- Scaricacollection (classe) Windows Media Player, metodo Item
topic_type:
- apiref
api_name:
- DownloadCollection.item
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d57db60a776c71d9ff16eceb1584c79a125bbf46
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331486"
---
# <a name="downloadcollectionitem-method"></a><span data-ttu-id="61339-108">Metodo DownloadCollection. Item</span><span class="sxs-lookup"><span data-stu-id="61339-108">DownloadCollection.item method</span></span>

> [!Note]  
> <span data-ttu-id="61339-109">In questa sezione viene descritta la funzionalità progettata per l'utilizzo da parte degli archivi online.</span><span class="sxs-lookup"><span data-stu-id="61339-109">This section describes functionality designed for use by online stores.</span></span> <span data-ttu-id="61339-110">L'uso di questa funzionalità al di fuori del contesto di un archivio online non è supportato.</span><span class="sxs-lookup"><span data-stu-id="61339-110">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="61339-111">Il metodo **Item** recupera un oggetto download in sospeso.</span><span class="sxs-lookup"><span data-stu-id="61339-111">The **item** method retrieves a pending download object.</span></span>

## <a name="syntax"></a><span data-ttu-id="61339-112">Sintassi</span><span class="sxs-lookup"><span data-stu-id="61339-112">Syntax</span></span>


```JScript
retVal = DownloadCollection.item(
  itemId
)
```



## <a name="parameters"></a><span data-ttu-id="61339-113">Parametri</span><span class="sxs-lookup"><span data-stu-id="61339-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="61339-114">*ID* \[ elemento in\]</span><span class="sxs-lookup"><span data-stu-id="61339-114">*itemId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="61339-115">**Numero** (**Long**) che specifica l'indice di **DownloadItem** da recuperare.</span><span class="sxs-lookup"><span data-stu-id="61339-115">**Number** (**long**) specifying the index of the **DownloadItem** to retrieve.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="61339-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="61339-116">Return value</span></span>

<span data-ttu-id="61339-117">Questo metodo restituisce un oggetto **DownloadItem** .</span><span class="sxs-lookup"><span data-stu-id="61339-117">This method returns a **DownloadItem** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="61339-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="61339-118">Remarks</span></span>

<span data-ttu-id="61339-119">Il valore *ItemId* è in base zero.</span><span class="sxs-lookup"><span data-stu-id="61339-119">The *itemID* value is zero-based.</span></span>

## <a name="requirements"></a><span data-ttu-id="61339-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="61339-120">Requirements</span></span>



| <span data-ttu-id="61339-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="61339-121">Requirement</span></span> | <span data-ttu-id="61339-122">Valore</span><span class="sxs-lookup"><span data-stu-id="61339-122">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="61339-123">Versione</span><span class="sxs-lookup"><span data-stu-id="61339-123">Version</span></span><br/> | <span data-ttu-id="61339-124">Windows Media Player 9 serie o versione successiva</span><span class="sxs-lookup"><span data-stu-id="61339-124">Windows Media Player 9 Series or later</span></span><br/>                                  |
| <span data-ttu-id="61339-125">DLL</span><span class="sxs-lookup"><span data-stu-id="61339-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="61339-126"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="61339-126"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="61339-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="61339-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="61339-128">**Download (oggetto)**</span><span class="sxs-lookup"><span data-stu-id="61339-128">**DownloadCollection Object**</span></span>](downloadcollection-object.md)
</dt> <dt>

[<span data-ttu-id="61339-129">**Oggetto DownloadItem**</span><span class="sxs-lookup"><span data-stu-id="61339-129">**DownloadItem Object**</span></span>](downloaditem-object.md)
</dt> </dl>

 

 





