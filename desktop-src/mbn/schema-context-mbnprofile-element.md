---
description: Specifica i parametri necessari per configurare una connessione dati.
ms.assetid: 7a3d3b9d-f799-4927-9c18-04b025788a4a
title: Elemento context (MBNProfile)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Context
api_type:
- Schema
ms.openlocfilehash: dac98101dade85fbbaa63275933885241ef206fc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307542"
---
# <a name="context-mbnprofile-element"></a><span data-ttu-id="7063b-103">Elemento context (MBNProfile)</span><span class="sxs-lookup"><span data-stu-id="7063b-103">Context (MBNProfile) Element</span></span>

<span data-ttu-id="7063b-104">L'elemento **Context (MBNProfile)** specifica i parametri necessari per configurare una connessione dati.</span><span class="sxs-lookup"><span data-stu-id="7063b-104">The **Context (MBNProfile)** element specifies the parameters required to setup a data connection.</span></span>

<span data-ttu-id="7063b-105">L'elemento può avere gli elementi figlio seguenti.</span><span class="sxs-lookup"><span data-stu-id="7063b-105">The element can have the following child elements.</span></span>

-   [<span data-ttu-id="7063b-106">**AccessString**</span><span class="sxs-lookup"><span data-stu-id="7063b-106">**AccessString**</span></span>](schema-accessstring-contexttype-element.md)
-   [<span data-ttu-id="7063b-107">**UserLogonCred**</span><span class="sxs-lookup"><span data-stu-id="7063b-107">**UserLogonCred**</span></span>](schema-userlogoncred-contexttype-element.md)
-   [<span data-ttu-id="7063b-108">**Compressione**</span><span class="sxs-lookup"><span data-stu-id="7063b-108">**Compression**</span></span>](schema-compression-contexttype-element.md)
-   [<span data-ttu-id="7063b-109">**AuthProtocol**</span><span class="sxs-lookup"><span data-stu-id="7063b-109">**AuthProtocol**</span></span>](schema-authprotocol-contexttype-element.md)

<span data-ttu-id="7063b-110">Questo elemento può avere un massimo di un'occorrenza.</span><span class="sxs-lookup"><span data-stu-id="7063b-110">This element can have a maximum of one occurrence.</span></span>

``` syntax
<xs:element name="Context"
    type="contextType"
 />
```

<span data-ttu-id="7063b-111">L'elemento **context** è definito dall'elemento [**MBNProfile**](schema-mbnprofile-element.md) .</span><span class="sxs-lookup"><span data-stu-id="7063b-111">The **Context** element is defined by the [**MBNProfile**](schema-mbnprofile-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="7063b-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7063b-112">Requirements</span></span>



| <span data-ttu-id="7063b-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="7063b-113">Requirement</span></span> | <span data-ttu-id="7063b-114">Valore</span><span class="sxs-lookup"><span data-stu-id="7063b-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------|
| <span data-ttu-id="7063b-115">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7063b-115">Minimum supported client</span></span><br/> | <span data-ttu-id="7063b-116">App desktop di Windows 7 \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="7063b-116">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="7063b-117">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7063b-117">Minimum supported server</span></span><br/> | <span data-ttu-id="7063b-118">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="7063b-118">None supported</span></span><br/>                         |



## <a name="see-also"></a><span data-ttu-id="7063b-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7063b-119">See also</span></span>

<dl> <dt>

<span data-ttu-id="7063b-120">**Contesto di definizione dell'elemento nello schema**</span><span class="sxs-lookup"><span data-stu-id="7063b-120">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="7063b-121">**MBNProfile**</span><span class="sxs-lookup"><span data-stu-id="7063b-121">**MBNProfile**</span></span>](schema-mbnprofile-element.md)
</dt> <dt>

<span data-ttu-id="7063b-122">**Possibile elemento padre immediato nell'istanza dello schema**</span><span class="sxs-lookup"><span data-stu-id="7063b-122">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="7063b-123">**MBNProfile**</span><span class="sxs-lookup"><span data-stu-id="7063b-123">**MBNProfile**</span></span>](schema-mbnprofile-element.md)
</dt> </dl>

 

 




