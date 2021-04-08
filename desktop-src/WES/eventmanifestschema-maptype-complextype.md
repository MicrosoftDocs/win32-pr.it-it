---
title: Tipo complesso MapType
description: Definisce un elenco di coppie nome/valore.
ms.assetid: 208ae219-8f79-4049-b946-a57b33c97b1b
keywords:
- Log eventi di tipo complesso MapType
topic_type:
- apiref
api_name:
- MapType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4daf6cfe677ab5585ac580e19c868f1bba17de45
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740391"
---
# <a name="maptype-complex-type"></a><span data-ttu-id="26832-104">Tipo complesso MapType</span><span class="sxs-lookup"><span data-stu-id="26832-104">MapType Complex Type</span></span>

<span data-ttu-id="26832-105">Definisce un elenco di coppie nome/valore.</span><span class="sxs-lookup"><span data-stu-id="26832-105">Defines a list of name/value pairs.</span></span>

``` syntax
<xs:complexType name="MapType">
    <xs:choice
        maxOccurs="unbounded"
    >
        <xs:element name="valueMap"
            type="ValueMapType"
         />
        <xs:element name="bitMap"
            type="BitMapType"
         />
    </xs:choice>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="26832-106">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="26832-106">Child elements</span></span>



| <span data-ttu-id="26832-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="26832-107">Element</span></span>                                                          | <span data-ttu-id="26832-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="26832-108">Type</span></span>                                                                 | <span data-ttu-id="26832-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="26832-109">Description</span></span>                                                                              |
|------------------------------------------------------------------|----------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| [<span data-ttu-id="26832-110">**bitMap**</span><span class="sxs-lookup"><span data-stu-id="26832-110">**bitMap**</span></span>](eventmanifestschema-bitmap-maptype-element.md)     | [<span data-ttu-id="26832-111">**BitMapType**</span><span class="sxs-lookup"><span data-stu-id="26832-111">**BitMapType**</span></span>](eventmanifestschema-bitmaptype-complextype.md)     | <span data-ttu-id="26832-112">Definisce un elenco di coppie nome/valore che mappano valori di bit e valori di stringa.</span><span class="sxs-lookup"><span data-stu-id="26832-112">Defines a list of name/value pairs that map bit values and string values.</span></span><br/>     |
| [<span data-ttu-id="26832-113">**valueMap**</span><span class="sxs-lookup"><span data-stu-id="26832-113">**valueMap**</span></span>](eventmanifestschema-valuemap-maptype-element.md) | [<span data-ttu-id="26832-114">**ValueMapType**</span><span class="sxs-lookup"><span data-stu-id="26832-114">**ValueMapType**</span></span>](eventmanifestschema-valuemaptype-complextype.md) | <span data-ttu-id="26832-115">Definisce un elenco di coppie nome/valore che mappano valori interi e valori di stringa.</span><span class="sxs-lookup"><span data-stu-id="26832-115">Defines a list of name/value pairs that map integer values and string values.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="26832-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="26832-116">Remarks</span></span>

<span data-ttu-id="26832-117">In genere, si creano mappe per fornire valori stringa enumerati per i dati dell'evento.</span><span class="sxs-lookup"><span data-stu-id="26832-117">Typically, you create maps to provide enumerated string values for event data.</span></span>

## <a name="examples"></a><span data-ttu-id="26832-118">Esempio</span><span class="sxs-lookup"><span data-stu-id="26832-118">Examples</span></span>

<span data-ttu-id="26832-119">Nell'esempio seguente viene illustrato come specificare una mappa di valori e una bitmap.</span><span class="sxs-lookup"><span data-stu-id="26832-119">The following example shows how to specify a value map and bitmap.</span></span>


```XML
<maps>
   <valueMap name="MyValueMap">
       <map value="5" message="$(string.value5)"/>
       <map value="45" message="$(string.value45)"/>
   </valueMap>
 
   <bitMap name="MyBitmap">
       <map value="0x8" message="$(string.bit3)/>
       <map value="0x80" message="$(string.bit7)/>
   </bitMap>
</maps>
```



## <a name="requirements"></a><span data-ttu-id="26832-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="26832-120">Requirements</span></span>



| <span data-ttu-id="26832-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="26832-121">Requirement</span></span> | <span data-ttu-id="26832-122">Valore</span><span class="sxs-lookup"><span data-stu-id="26832-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="26832-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="26832-123">Minimum supported client</span></span><br/> | <span data-ttu-id="26832-124">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="26832-124">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="26832-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="26832-125">Minimum supported server</span></span><br/> | <span data-ttu-id="26832-126">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="26832-126">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





