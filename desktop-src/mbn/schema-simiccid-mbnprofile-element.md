---
description: Identifica il numero di identificazione della SIM per i dispositivi GSM.
ms.assetid: 980afba4-fc31-4da0-ba01-6eb8e3db0ac8
title: Elemento SimIccID (MBNProfile)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SimIccID
api_type:
- Schema
ms.openlocfilehash: f566253ad3e86b4f7ee7317cf125d9e649034847
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306772"
---
# <a name="simiccid-mbnprofile-element"></a><span data-ttu-id="af4ff-103">Elemento SimIccID (MBNProfile)</span><span class="sxs-lookup"><span data-stu-id="af4ff-103">SimIccID (MBNProfile) Element</span></span>

<span data-ttu-id="af4ff-104">L'elemento **SimIccID (MBNProfile)** identifica il numero di identificazione della SIM per i dispositivi GSM.</span><span class="sxs-lookup"><span data-stu-id="af4ff-104">The **SimIccID (MBNProfile)** element identifies the SIM Identification number for GSM devices.</span></span>

<span data-ttu-id="af4ff-105">Questo elemento è facoltativo e viene impostato dal servizio Mobile Broadband per uso interno.</span><span class="sxs-lookup"><span data-stu-id="af4ff-105">This element is optional and is set by the Mobile Broadband service for internal use.</span></span> <span data-ttu-id="af4ff-106">Un'applicazione non deve impostare questo campo durante la creazione o l'aggiornamento di un profilo.</span><span class="sxs-lookup"><span data-stu-id="af4ff-106">An application should not set this field while creating or updating a profile.</span></span>

``` syntax
<xs:element name="SimIccID"
    type="simIccIDType"
 />
```

<span data-ttu-id="af4ff-107">L'elemento **SimIccID** è definito dall'elemento [**MBNProfile**](schema-mbnprofile-element.md) .</span><span class="sxs-lookup"><span data-stu-id="af4ff-107">The **SimIccID** element is defined by the [**MBNProfile**](schema-mbnprofile-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="af4ff-108">Requisiti</span><span class="sxs-lookup"><span data-stu-id="af4ff-108">Requirements</span></span>



| <span data-ttu-id="af4ff-109">Requisito</span><span class="sxs-lookup"><span data-stu-id="af4ff-109">Requirement</span></span> | <span data-ttu-id="af4ff-110">Valore</span><span class="sxs-lookup"><span data-stu-id="af4ff-110">Value</span></span> |
|-------------------------------------|---------------------------------------------------|
| <span data-ttu-id="af4ff-111">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="af4ff-111">Minimum supported client</span></span><br/> | <span data-ttu-id="af4ff-112">App desktop di Windows 7 \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="af4ff-112">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="af4ff-113">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="af4ff-113">Minimum supported server</span></span><br/> | <span data-ttu-id="af4ff-114">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="af4ff-114">None supported</span></span><br/>                         |



## <a name="see-also"></a><span data-ttu-id="af4ff-115">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="af4ff-115">See also</span></span>

<dl> <dt>

<span data-ttu-id="af4ff-116">**Contesto di definizione dell'elemento nello schema**</span><span class="sxs-lookup"><span data-stu-id="af4ff-116">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="af4ff-117">**MBNProfile**</span><span class="sxs-lookup"><span data-stu-id="af4ff-117">**MBNProfile**</span></span>](schema-mbnprofile-element.md)
</dt> <dt>

<span data-ttu-id="af4ff-118">**Possibile elemento padre immediato nell'istanza dello schema**</span><span class="sxs-lookup"><span data-stu-id="af4ff-118">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="af4ff-119">**MBNProfile**</span><span class="sxs-lookup"><span data-stu-id="af4ff-119">**MBNProfile**</span></span>](schema-mbnprofile-element.md)
</dt> </dl>

 

 




