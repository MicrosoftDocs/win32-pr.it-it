---
description: Identifica l'identificatore univoco del profilo.
ms.assetid: 7572ef4f-ce7a-4595-a5ad-ade96e36d7d7
title: Elemento SubscriberID (MBNProfile)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SubscriberID
api_type:
- Schema
ms.openlocfilehash: ca098383aadd51e1e05d6b02bdd02a563eb0a09c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526617"
---
# <a name="subscriberid-mbnprofile-element"></a><span data-ttu-id="53383-103">Elemento SubscriberID (MBNProfile)</span><span class="sxs-lookup"><span data-stu-id="53383-103">SubscriberID (MBNProfile) Element</span></span>

<span data-ttu-id="53383-104">L'elemento **SubscriberID (MBNProfile)** identifica l'identificatore univoco del profilo.</span><span class="sxs-lookup"><span data-stu-id="53383-104">The **SubscriberID (MBNProfile)** element identifies the unique identifier of the profile.</span></span>

<span data-ttu-id="53383-105">Per una rete GSM questo deve contenere IMSI (International Mobile Subscriber Identity) della SIM e per i dispositivi CDMA deve contenere il numero minimo di identificazione mobile del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="53383-105">For a GSM network this should contain the IMSI (International Mobile Subscriber Identity) of the SIM and for CDMA devices it should contain the MIN (Mobile Identification Number) of the device.</span></span>

<span data-ttu-id="53383-106">L'elemento è una stringa numerica con una lunghezza massima di 15 cifre.</span><span class="sxs-lookup"><span data-stu-id="53383-106">The element is is a numeric string with a maximum length 15 digits.</span></span>

<span data-ttu-id="53383-107">L'elemento è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="53383-107">The element is required.</span></span>

``` syntax
<xs:element name="SubscriberID"
    type="subscriberIdType"
 />
```

<span data-ttu-id="53383-108">L'elemento **SubscriberID** è definito dall'elemento [**MBNProfile**](schema-mbnprofile-element.md) .</span><span class="sxs-lookup"><span data-stu-id="53383-108">The **SubscriberID** element is defined by the [**MBNProfile**](schema-mbnprofile-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="53383-109">Requisiti</span><span class="sxs-lookup"><span data-stu-id="53383-109">Requirements</span></span>



| <span data-ttu-id="53383-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="53383-110">Requirement</span></span> | <span data-ttu-id="53383-111">Valore</span><span class="sxs-lookup"><span data-stu-id="53383-111">Value</span></span> |
|-------------------------------------|---------------------------------------------------|
| <span data-ttu-id="53383-112">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="53383-112">Minimum supported client</span></span><br/> | <span data-ttu-id="53383-113">App desktop di Windows 7 \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="53383-113">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="53383-114">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="53383-114">Minimum supported server</span></span><br/> | <span data-ttu-id="53383-115">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="53383-115">None supported</span></span><br/>                         |



## <a name="see-also"></a><span data-ttu-id="53383-116">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="53383-116">See also</span></span>

<dl> <dt>

<span data-ttu-id="53383-117">**Contesto di definizione dell'elemento nello schema**</span><span class="sxs-lookup"><span data-stu-id="53383-117">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="53383-118">**MBNProfile**</span><span class="sxs-lookup"><span data-stu-id="53383-118">**MBNProfile**</span></span>](schema-mbnprofile-element.md)
</dt> <dt>

<span data-ttu-id="53383-119">**Possibile elemento padre immediato nell'istanza dello schema**</span><span class="sxs-lookup"><span data-stu-id="53383-119">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="53383-120">**MBNProfile**</span><span class="sxs-lookup"><span data-stu-id="53383-120">**MBNProfile**</span></span>](schema-mbnprofile-element.md)
</dt> </dl>

 

 




