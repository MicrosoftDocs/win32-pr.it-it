---
title: StringCollection. getAttributeCountByType, metodo
description: Il metodo getAttributeCountByType Recupera il numero di attributi associati all'indice dell'elemento StringCollection, al nome dell'attributo e alla lingua specificati.
ms.assetid: 3671b7b7-d6d4-4049-8710-d0f34c740b1e
keywords:
- Metodo getAttributeCountByType Windows Media Player
- Metodo getAttributeCountByType Windows Media Player, classe StringCollection
- StringCollection (classe) Windows Media Player, metodo getAttributeCountByType
topic_type:
- apiref
api_name:
- StringCollection.getAttributeCountByType
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2acf2d7a1f8849f9bd0e83ead3880ca90d2d6149
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328711"
---
# <a name="stringcollectiongetattributecountbytype-method"></a><span data-ttu-id="ecb24-106">StringCollection. getAttributeCountByType, metodo</span><span class="sxs-lookup"><span data-stu-id="ecb24-106">StringCollection.getAttributeCountByType method</span></span>

<span data-ttu-id="ecb24-107">Il metodo **getAttributeCountByType** Recupera il numero di attributi associati all'indice dell'elemento **StringCollection** , al nome dell'attributo e alla lingua specificati.</span><span class="sxs-lookup"><span data-stu-id="ecb24-107">The **getAttributeCountByType** method retrieves the number of attributes associated with the specified **StringCollection** item index, attribute name, and language.</span></span>

## <a name="syntax"></a><span data-ttu-id="ecb24-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ecb24-108">Syntax</span></span>


```JScript
retVal = StringCollection.getAttributeCountByType(
  index,
  name,
  language
)
```



## <a name="parameters"></a><span data-ttu-id="ecb24-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="ecb24-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ecb24-110">*Indice* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="ecb24-110">*index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ecb24-111">**Numero** (**Long**) che specifica l'indice in base zero dell'elemento **StringCollection** da cui ottenere l'attributo.</span><span class="sxs-lookup"><span data-stu-id="ecb24-111">**Number** (**long**) specifying the zero-based index of the **StringCollection** item from which to get the attribute.</span></span>

</dd> <dt>

<span data-ttu-id="ecb24-112">*nome* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ecb24-112">*name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ecb24-113">**Stringa** contenente il nome dell'attributo.</span><span class="sxs-lookup"><span data-stu-id="ecb24-113">**String** containing the name of the attribute.</span></span>

</dd> <dt>

<span data-ttu-id="ecb24-114">*lingua* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="ecb24-114">*language* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ecb24-115">**Stringa** contenente il linguaggio.</span><span class="sxs-lookup"><span data-stu-id="ecb24-115">**String** containing the language.</span></span> <span data-ttu-id="ecb24-116">Se il valore è impostato su null o su una stringa vuota (""), viene utilizzata la stringa delle impostazioni locali corrente.</span><span class="sxs-lookup"><span data-stu-id="ecb24-116">If the value is set to null or the empty string (""), the current locale string is used.</span></span> <span data-ttu-id="ecb24-117">In caso contrario, il valore deve essere una stringa di linguaggio RFC 1766 valida, ad esempio "en-US".</span><span class="sxs-lookup"><span data-stu-id="ecb24-117">Otherwise, the value must be a valid RFC 1766 language string such as "en-us".</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ecb24-118">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ecb24-118">Return value</span></span>

<span data-ttu-id="ecb24-119">Questo metodo restituisce un **numero** (**Long**).</span><span class="sxs-lookup"><span data-stu-id="ecb24-119">This method returns a **Number** (**long**).</span></span>

## <a name="remarks"></a><span data-ttu-id="ecb24-120">Commenti</span><span class="sxs-lookup"><span data-stu-id="ecb24-120">Remarks</span></span>

<span data-ttu-id="ecb24-121">Questo metodo viene utilizzato per determinare il numero di attributi corrispondenti a un nome di attributo specifico per un particolare elemento **StringCollection** .</span><span class="sxs-lookup"><span data-stu-id="ecb24-121">This method is used to determine the number of attributes corresponding to a particular attribute name for a particular **StringCollection** item.</span></span> <span data-ttu-id="ecb24-122">I numeri di indice possono quindi essere passati al quarto parametro del metodo **StringCollection. getItemInfoByType** .</span><span class="sxs-lookup"><span data-stu-id="ecb24-122">Index numbers can then be passed to the fourth parameter of the **StringCollection.getItemInfoByType** method.</span></span>

<span data-ttu-id="ecb24-123">Per usare questo metodo, è necessario l'accesso in lettura alla libreria.</span><span class="sxs-lookup"><span data-stu-id="ecb24-123">To use this method, read access to the library is required.</span></span> <span data-ttu-id="ecb24-124">Per altre informazioni, vedere [accesso alla libreria](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="ecb24-124">For more information, see [Library Access](library-access.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ecb24-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ecb24-125">Requirements</span></span>



| <span data-ttu-id="ecb24-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="ecb24-126">Requirement</span></span> | <span data-ttu-id="ecb24-127">Valore</span><span class="sxs-lookup"><span data-stu-id="ecb24-127">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="ecb24-128">Versione</span><span class="sxs-lookup"><span data-stu-id="ecb24-128">Version</span></span><br/> | <span data-ttu-id="ecb24-129">Windows Media Player 11.</span><span class="sxs-lookup"><span data-stu-id="ecb24-129">Windows Media Player 11.</span></span><br/>                                                |
| <span data-ttu-id="ecb24-130">DLL</span><span class="sxs-lookup"><span data-stu-id="ecb24-130">DLL</span></span><br/>     | <dl> <span data-ttu-id="ecb24-131"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ecb24-131"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ecb24-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ecb24-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ecb24-133">**StringCollection (oggetto)**</span><span class="sxs-lookup"><span data-stu-id="ecb24-133">**StringCollection Object**</span></span>](stringcollection-object.md)
</dt> </dl>

 

 





