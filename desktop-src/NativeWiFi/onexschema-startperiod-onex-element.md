---
description: Specifica il tempo di attesa, in secondi, prima dell'invio di un EAPOL-Start.
ms.assetid: 6163eeb9-23a8-4e34-ad3f-016946e241e2
title: Elemento startPeriod (OneX)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- startPeriod
api_type:
- Schema
api_location: ''
ms.openlocfilehash: a583403a354cbefe93387be2d5af06958bbf6b28
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104345346"
---
# <a name="startperiod-onex-element"></a><span data-ttu-id="ae475-103">Elemento startPeriod (OneX)</span><span class="sxs-lookup"><span data-stu-id="ae475-103">startPeriod (OneX) Element</span></span>

<span data-ttu-id="ae475-104">L'elemento startPeriod (OneX) specifica il periodo di tempo, in secondi, di attesa prima dell'invio di un EAPOL-Start.</span><span class="sxs-lookup"><span data-stu-id="ae475-104">The startPeriod (OneX) element specifies the length of time, in seconds, to wait before an EAPOL-Start is sent.</span></span> <span data-ttu-id="ae475-105">Viene inviato un messaggio di EAPOL-Start per avviare il processo di autenticazione 802.1 X.</span><span class="sxs-lookup"><span data-stu-id="ae475-105">An EAPOL-Start message is sent to start the 802.1X authentication process.</span></span>

<span data-ttu-id="ae475-106">Questo elemento è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="ae475-106">This element is optional.</span></span> <span data-ttu-id="ae475-107">Quando startPeriod non viene specificato in un profilo, viene utilizzato un valore di 5 secondi.</span><span class="sxs-lookup"><span data-stu-id="ae475-107">When startPeriod is not specified in a profile, a value of 5 seconds is used.</span></span>

<span data-ttu-id="ae475-108">**Windows XP con SP3 e l'API LAN wireless per Windows XP con SP2:** Questo elemento verrà ignorato se è presente in un profilo.</span><span class="sxs-lookup"><span data-stu-id="ae475-108">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element will be ignored if it is present in a profile.</span></span>

``` syntax
<xs:element name="startPeriod">
    <xs:simpleType>
        <xs:restriction
            base="integer"
        >
            <xs:enumeration
                value="1"
             />
            <xs:enumeration
                value="3600"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

<span data-ttu-id="ae475-109">L'elemento **startPeriod** è definito dall'elemento [**Onex**](onexschema-onex-element.md) .</span><span class="sxs-lookup"><span data-stu-id="ae475-109">The **startPeriod** element is defined by the [**OneX**](onexschema-onex-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="ae475-110">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ae475-110">Requirements</span></span>



| <span data-ttu-id="ae475-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="ae475-111">Requirement</span></span> | <span data-ttu-id="ae475-112">Valore</span><span class="sxs-lookup"><span data-stu-id="ae475-112">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="ae475-113">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ae475-113">Minimum supported client</span></span><br/> | <span data-ttu-id="ae475-114">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ae475-114">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="ae475-115">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ae475-115">Minimum supported server</span></span><br/> | <span data-ttu-id="ae475-116">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="ae475-116">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ae475-117">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ae475-117">See also</span></span>

<dl> <dt>

<span data-ttu-id="ae475-118">**Contesto di definizione dell'elemento nello schema**</span><span class="sxs-lookup"><span data-stu-id="ae475-118">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="ae475-119">**OneX**</span><span class="sxs-lookup"><span data-stu-id="ae475-119">**OneX**</span></span>](onexschema-onex-element.md)
</dt> <dt>

<span data-ttu-id="ae475-120">**Possibile elemento padre immediato nell'istanza dello schema**</span><span class="sxs-lookup"><span data-stu-id="ae475-120">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="ae475-121">**OneX**</span><span class="sxs-lookup"><span data-stu-id="ae475-121">**OneX**</span></span>](onexschema-onex-element.md)
</dt> </dl>

 

 




