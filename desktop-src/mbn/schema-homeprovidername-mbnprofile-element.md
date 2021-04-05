---
description: Identifica il nome del provider Home per la SIM/dispositivo specificato.
ms.assetid: 05d65091-5a1d-427a-8f51-1e1b9d189571
title: Elemento HomeProviderName (MBNProfile)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- HomeProviderName
api_type:
- Schema
ms.openlocfilehash: 3d0af51e4873915838f2d55f683d07e9098aad3f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751290"
---
# <a name="homeprovidername-mbnprofile-element"></a><span data-ttu-id="50369-103">Elemento HomeProviderName (MBNProfile)</span><span class="sxs-lookup"><span data-stu-id="50369-103">HomeProviderName (MBNProfile) Element</span></span>

<span data-ttu-id="50369-104">L'elemento **HomeProviderName (MBNProfile)** identifica il nome del provider Home per la SIM/dispositivo specificato.</span><span class="sxs-lookup"><span data-stu-id="50369-104">The **HomeProviderName (MBNProfile)** element identifies the name of Home provider for the given SIM/Device.</span></span>

<span data-ttu-id="50369-105">Questo elemento è facoltativo e viene impostato dal servizio Mobile Broadband per uso interno.</span><span class="sxs-lookup"><span data-stu-id="50369-105">This element is optional and is set by the Mobile Broadband service for internal use.</span></span> <span data-ttu-id="50369-106">Un'applicazione non deve impostare questo campo durante la creazione o l'aggiornamento di un profilo.</span><span class="sxs-lookup"><span data-stu-id="50369-106">An application should not set this field while creating or updating a profile.</span></span>

``` syntax
<xs:element name="HomeProviderName"
    type="providerNameType"
 />
```

<span data-ttu-id="50369-107">L'elemento **HomeProviderName** è definito dall'elemento [**MBNProfile**](schema-mbnprofile-element.md) .</span><span class="sxs-lookup"><span data-stu-id="50369-107">The **HomeProviderName** element is defined by the [**MBNProfile**](schema-mbnprofile-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="50369-108">Requisiti</span><span class="sxs-lookup"><span data-stu-id="50369-108">Requirements</span></span>



| <span data-ttu-id="50369-109">Requisito</span><span class="sxs-lookup"><span data-stu-id="50369-109">Requirement</span></span> | <span data-ttu-id="50369-110">Valore</span><span class="sxs-lookup"><span data-stu-id="50369-110">Value</span></span> |
|-------------------------------------|---------------------------------------------------|
| <span data-ttu-id="50369-111">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="50369-111">Minimum supported client</span></span><br/> | <span data-ttu-id="50369-112">App desktop di Windows 7 \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="50369-112">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="50369-113">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="50369-113">Minimum supported server</span></span><br/> | <span data-ttu-id="50369-114">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="50369-114">None supported</span></span><br/>                         |



## <a name="see-also"></a><span data-ttu-id="50369-115">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="50369-115">See also</span></span>

<dl> <dt>

<span data-ttu-id="50369-116">**Contesto di definizione dell'elemento nello schema**</span><span class="sxs-lookup"><span data-stu-id="50369-116">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="50369-117">**MBNProfile**</span><span class="sxs-lookup"><span data-stu-id="50369-117">**MBNProfile**</span></span>](schema-mbnprofile-element.md)
</dt> <dt>

<span data-ttu-id="50369-118">**Possibile elemento padre immediato nell'istanza dello schema**</span><span class="sxs-lookup"><span data-stu-id="50369-118">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="50369-119">**MBNProfile**</span><span class="sxs-lookup"><span data-stu-id="50369-119">**MBNProfile**</span></span>](schema-mbnprofile-element.md)
</dt> </dl>

 

 




