---
title: Metodo StringCollection. Item
description: Il metodo Item recupera la stringa in corrispondenza dell'indice specificato.
ms.assetid: 5f6afff2-3ecc-4b28-8c67-f859f5440d4f
keywords:
- Metodo Item Media Player Windows
- elemento Method Media Player di Windows, classe StringCollection
- StringCollection (classe) Windows Media Player, metodo Item
topic_type:
- apiref
api_name:
- StringCollection.item
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c4244ad194ff3426dab81baddc0b7188214e0360
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324458"
---
# <a name="stringcollectionitem-method"></a><span data-ttu-id="3f373-106">Metodo StringCollection. Item</span><span class="sxs-lookup"><span data-stu-id="3f373-106">StringCollection.item method</span></span>

<span data-ttu-id="3f373-107">Il metodo **Item** recupera la stringa in corrispondenza dell'indice specificato.</span><span class="sxs-lookup"><span data-stu-id="3f373-107">The **item** method retrieves the string at the specified index.</span></span>

## <a name="syntax"></a><span data-ttu-id="3f373-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3f373-108">Syntax</span></span>


```JScript
strRetVal = StringCollection.item(
  index
)
```



## <a name="parameters"></a><span data-ttu-id="3f373-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="3f373-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3f373-110">*Indice* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="3f373-110">*index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3f373-111">**Numero** (**Long**) che contiene l'indice.</span><span class="sxs-lookup"><span data-stu-id="3f373-111">**Number** (**long**) containing the index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3f373-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3f373-112">Return value</span></span>

<span data-ttu-id="3f373-113">Questo metodo restituisce una **stringa**.</span><span class="sxs-lookup"><span data-stu-id="3f373-113">This method returns a **String**.</span></span>

## <a name="remarks"></a><span data-ttu-id="3f373-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="3f373-114">Remarks</span></span>

<span data-ttu-id="3f373-115">L'oggetto **StringCollection** viene utilizzato per recuperare il set di valori disponibili per un attributo.</span><span class="sxs-lookup"><span data-stu-id="3f373-115">The **StringCollection** object is used to retrieve the set of values available for an attribute.</span></span> <span data-ttu-id="3f373-116">Ad esempio, *mediacollection*. il metodo **getAttributeStringCollection** può essere usato per recuperare un oggetto **StringCollection** che rappresenta tutti i valori per l'attributo Genre all'interno del tipo di supporto audio.</span><span class="sxs-lookup"><span data-stu-id="3f373-116">For example, the *MediaCollection*.**getAttributeStringCollection** method can be used to retrieve a **StringCollection** object representing all the values for the Genre attribute within the Audio media type.</span></span> <span data-ttu-id="3f373-117">La proprietà **Item** può quindi essere usata per scorrere tutti i valori possibili per l'attributo Genre.</span><span class="sxs-lookup"><span data-stu-id="3f373-117">The **item** property can then be used to iterate through all of the possible values for the Genre attribute.</span></span>

<span data-ttu-id="3f373-118">Per usare questo metodo, è necessario l'accesso in lettura alla libreria.</span><span class="sxs-lookup"><span data-stu-id="3f373-118">To use this method, read access to the library is required.</span></span> <span data-ttu-id="3f373-119">Per altre informazioni, vedere [accesso alla libreria](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="3f373-119">For more information, see [Library Access](library-access.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="3f373-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3f373-120">Requirements</span></span>



| <span data-ttu-id="3f373-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="3f373-121">Requirement</span></span> | <span data-ttu-id="3f373-122">Valore</span><span class="sxs-lookup"><span data-stu-id="3f373-122">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="3f373-123">Versione</span><span class="sxs-lookup"><span data-stu-id="3f373-123">Version</span></span><br/> | <span data-ttu-id="3f373-124">Windows Media Player versione 7,0 o successiva.</span><span class="sxs-lookup"><span data-stu-id="3f373-124">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="3f373-125">DLL</span><span class="sxs-lookup"><span data-stu-id="3f373-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="3f373-126"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3f373-126"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3f373-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3f373-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3f373-128">**Mediacollection. getAttributeStringCollection**</span><span class="sxs-lookup"><span data-stu-id="3f373-128">**MediaCollection.getAttributeStringCollection**</span></span>](mediacollection-getattributestringcollection.md)
</dt> <dt>

[<span data-ttu-id="3f373-129">**Settings. mediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="3f373-129">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="3f373-130">**Settings. requestMediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="3f373-130">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="3f373-131">**StringCollection (oggetto)**</span><span class="sxs-lookup"><span data-stu-id="3f373-131">**StringCollection Object**</span></span>](stringcollection-object.md)
</dt> </dl>

 

 





