---
title: StringCollection. getItemInfo, metodo
description: Il metodo getItemInfo recupera la stringa corrispondente all'indice e al nome dell'elemento StringCollection specificato.
ms.assetid: a031b91e-9d3b-47ac-bc5b-c111d5e3bc12
keywords:
- metodo getItemInfo Windows Media Player
- metodo getItemInfo Windows Media Player, classe StringCollection
- StringCollection (classe) Windows Media Player, metodo getItemInfo
topic_type:
- apiref
api_name:
- StringCollection.getItemInfo
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1c9552dcebbc7d565ebc797c62ac3bc00ee109fb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328870"
---
# <a name="stringcollectiongetiteminfo-method"></a><span data-ttu-id="ba48a-106">StringCollection. getItemInfo, metodo</span><span class="sxs-lookup"><span data-stu-id="ba48a-106">StringCollection.getItemInfo method</span></span>

<span data-ttu-id="ba48a-107">Il metodo **GetItemInfo** recupera la stringa corrispondente all'indice e al nome dell'elemento **StringCollection** specificato.</span><span class="sxs-lookup"><span data-stu-id="ba48a-107">The **getItemInfo** method retrieves the string corresponding to the specified **StringCollection** item index and name.</span></span>

## <a name="syntax"></a><span data-ttu-id="ba48a-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ba48a-108">Syntax</span></span>


```JScript
strRetVal = StringCollection.getItemInfo(
  index,
  name
)
```



## <a name="parameters"></a><span data-ttu-id="ba48a-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="ba48a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ba48a-110">*Indice* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="ba48a-110">*index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ba48a-111">**Numero** (**Long**) che specifica l'indice in base zero dell'elemento **StringCollection** da cui ottenere l'attributo.</span><span class="sxs-lookup"><span data-stu-id="ba48a-111">**Number** (**long**) specifying the zero-based index of the **StringCollection** item from which to get the attribute.</span></span>

</dd> <dt>

<span data-ttu-id="ba48a-112">*nome* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ba48a-112">*name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ba48a-113">**Stringa** contenente il nome dell'attributo.</span><span class="sxs-lookup"><span data-stu-id="ba48a-113">**String** containing the attribute name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ba48a-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ba48a-114">Return value</span></span>

<span data-ttu-id="ba48a-115">Questo metodo restituisce una **stringa** che rappresenta il valore dell'attributo specificato.</span><span class="sxs-lookup"><span data-stu-id="ba48a-115">This method returns a **String** representing the value of the specified attribute.</span></span> <span data-ttu-id="ba48a-116">Per gli attributi il cui valore sottostante è **booleano**, viene restituita la stringa "true" o "false".</span><span class="sxs-lookup"><span data-stu-id="ba48a-116">For attributes whose underlying value is **Boolean**, it returns the string "true" or "false".</span></span>

## <a name="remarks"></a><span data-ttu-id="ba48a-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="ba48a-117">Remarks</span></span>

<span data-ttu-id="ba48a-118">Per recuperare gli attributi con più valori e attributi con valori complessi, usare il metodo **getItemInfoByType** .</span><span class="sxs-lookup"><span data-stu-id="ba48a-118">To retrieve attributes with multiple values and attributes with complex values, use the **getItemInfoByType** method.</span></span>

<span data-ttu-id="ba48a-119">Per usare questo metodo, è necessario l'accesso in lettura alla libreria.</span><span class="sxs-lookup"><span data-stu-id="ba48a-119">To use this method, read access to the library is required.</span></span> <span data-ttu-id="ba48a-120">Per altre informazioni, vedere [accesso alla libreria](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="ba48a-120">For more information, see [Library Access](library-access.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ba48a-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ba48a-121">Requirements</span></span>



| <span data-ttu-id="ba48a-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="ba48a-122">Requirement</span></span> | <span data-ttu-id="ba48a-123">Valore</span><span class="sxs-lookup"><span data-stu-id="ba48a-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="ba48a-124">Versione</span><span class="sxs-lookup"><span data-stu-id="ba48a-124">Version</span></span><br/> | <span data-ttu-id="ba48a-125">Windows Media Player 11.</span><span class="sxs-lookup"><span data-stu-id="ba48a-125">Windows Media Player 11.</span></span><br/>                                                |
| <span data-ttu-id="ba48a-126">DLL</span><span class="sxs-lookup"><span data-stu-id="ba48a-126">DLL</span></span><br/>     | <dl> <span data-ttu-id="ba48a-127"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ba48a-127"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ba48a-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ba48a-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ba48a-129">**StringCollection. getItemInfoByType**</span><span class="sxs-lookup"><span data-stu-id="ba48a-129">**StringCollection.getItemInfoByType**</span></span>](stringcollection-getiteminfobytype.md)
</dt> <dt>

[<span data-ttu-id="ba48a-130">**StringCollection (oggetto)**</span><span class="sxs-lookup"><span data-stu-id="ba48a-130">**StringCollection Object**</span></span>](stringcollection-object.md)
</dt> </dl>

 

 





