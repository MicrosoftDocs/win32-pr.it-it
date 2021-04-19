---
title: EQUALIZERSETTINGS.gainLevels
description: L'attributo gainLevels specifica o Recupera il livello di guadagno della banda corrispondente all'indice fornito.
ms.assetid: fb70e2ef-4cee-457e-a06b-7a1ae6930986
keywords:
- Media Player Windows EQUALIZERSETTINGS. gainLevels
topic_type:
- apiref
api_name:
- EQUALIZERSETTINGS.gainLevels
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d083ac829582f2abc45837cf441b2f0a565ee03a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326130"
---
# <a name="equalizersettingsgainlevels"></a><span data-ttu-id="7e7fa-104">EQUALIZERSETTINGS.gainLevels</span><span class="sxs-lookup"><span data-stu-id="7e7fa-104">EQUALIZERSETTINGS.gainLevels</span></span>

<span data-ttu-id="7e7fa-105">L'attributo **gainLevels** specifica o Recupera il livello di guadagno della banda corrispondente all'indice fornito.</span><span class="sxs-lookup"><span data-stu-id="7e7fa-105">The **gainLevels** attribute specifies or retrieves the gain level of the band corresponding to the index provided.</span></span>

``` syntax
        elementID.gainLevels(theBand)
```

## <a name="possible-values"></a><span data-ttu-id="7e7fa-106">Valori possibili</span><span class="sxs-lookup"><span data-stu-id="7e7fa-106">Possible Values</span></span>

<span data-ttu-id="7e7fa-107">Questo attributo è un **numero** di lettura/scrittura (**float**) con un valore normalmente compreso tra 20 e + 20.</span><span class="sxs-lookup"><span data-stu-id="7e7fa-107">This attribute is a read/write **Number** (**float**) with a value normally ranging from  20 to +20.</span></span>

## <a name="parameters"></a><span data-ttu-id="7e7fa-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="7e7fa-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7e7fa-109"><span id="theBand"></span><span id="theband"></span><span id="THEBAND"></span>*theBand*</span><span class="sxs-lookup"><span data-stu-id="7e7fa-109"><span id="theBand"></span><span id="theband"></span><span id="THEBAND"></span>*theBand*</span></span>
</dt> <dd>

<span data-ttu-id="7e7fa-110">**Numero**(**Long**) compreso tra 1 e 10 che indica l'indice della banda.</span><span class="sxs-lookup"><span data-stu-id="7e7fa-110">**Number**(**long**) between 1 and 10 indicating the index of the band.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7e7fa-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="7e7fa-111">Remarks</span></span>

<span data-ttu-id="7e7fa-112">Questo attributo accetta un parametro, ma il relativo valore viene specificato nel codice di script allo stesso modo degli altri valori di attributo.</span><span class="sxs-lookup"><span data-stu-id="7e7fa-112">This attribute takes a parameter, but its value is specified in script code the same way as other attribute values.</span></span> <span data-ttu-id="7e7fa-113">Non può essere specificato nell'elemento EQUALIZERSETTINGS, né può essere usato con l'attributo di ascolto **wmpprop** .</span><span class="sxs-lookup"><span data-stu-id="7e7fa-113">It cannot be specified in the EQUALIZERSETTINGS element, nor can it be used with the **wmpprop** listening attribute.</span></span> <span data-ttu-id="7e7fa-114">Al contrario, vengono forniti gli attributi a livello di guadagno numerato per queste situazioni.</span><span class="sxs-lookup"><span data-stu-id="7e7fa-114">Instead, the numbered gain level attributes are provided for these situations.</span></span>

## <a name="requirements"></a><span data-ttu-id="7e7fa-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7e7fa-115">Requirements</span></span>



| <span data-ttu-id="7e7fa-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="7e7fa-116">Requirement</span></span> | <span data-ttu-id="7e7fa-117">Valore</span><span class="sxs-lookup"><span data-stu-id="7e7fa-117">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="7e7fa-118">Versione</span><span class="sxs-lookup"><span data-stu-id="7e7fa-118">Version</span></span><br/> | <span data-ttu-id="7e7fa-119">Windows Media Player versione 7,0 o successiva</span><span class="sxs-lookup"><span data-stu-id="7e7fa-119">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="7e7fa-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7e7fa-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7e7fa-121">**Elemento EQUALIZERSETTINGS**</span><span class="sxs-lookup"><span data-stu-id="7e7fa-121">**EQUALIZERSETTINGS Element**</span></span>](equalizersettings-element.md)
</dt> <dt>

[<span data-ttu-id="7e7fa-122">**Attributi di ascolto**</span><span class="sxs-lookup"><span data-stu-id="7e7fa-122">**Listening Attributes**</span></span>](listening-attributes.md)
</dt> </dl>

 

 





