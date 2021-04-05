---
description: Specifica, in secondi, il ritardo massimo prima che il tentativo di connessione Single Sign-on abbia esito negativo.
ms.assetid: ba8c137e-dd05-4ebc-9a83-cd612f65d4dc
title: Elemento maxDelay (singleSignOn)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- maxDelay
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 8efd069687a2db4b06b90aa594ec31132ce6fc9d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103881457"
---
# <a name="maxdelay-singlesignon-element"></a><span data-ttu-id="8a60b-103">Elemento maxDelay (singleSignOn)</span><span class="sxs-lookup"><span data-stu-id="8a60b-103">maxDelay (singleSignOn) Element</span></span>

<span data-ttu-id="8a60b-104">L'elemento maxDelay (singleSignOn) specifica, in secondi, il ritardo massimo prima che il tentativo di connessione Single Sign-on abbia esito negativo.</span><span class="sxs-lookup"><span data-stu-id="8a60b-104">The maxDelay (singleSignOn) element specifies, in seconds, the maximum delay before the single sign on connection attempt fails.</span></span>

<span data-ttu-id="8a60b-105">Questo elemento è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="8a60b-105">This element is optional.</span></span> <span data-ttu-id="8a60b-106">Quando maxDelay non viene specificato in un profilo, viene utilizzato un valore di 10 secondi.</span><span class="sxs-lookup"><span data-stu-id="8a60b-106">When maxDelay is not specified in a profile, a value of 10 seconds is used.</span></span>

<span data-ttu-id="8a60b-107">**Windows XP con SP3 e l'API LAN wireless per Windows XP con SP2:** Questo elemento verrà ignorato se è presente in un profilo.</span><span class="sxs-lookup"><span data-stu-id="8a60b-107">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element will be ignored if it is present in a profile.</span></span>

``` syntax
<xs:element name="maxDelay">
    <xs:simpleType>
        <xs:restriction
            base="integer"
        >
            <xs:enumeration
                value="0"
             />
            <xs:enumeration
                value="120"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

<span data-ttu-id="8a60b-108">L'elemento **maxDelay** è definito dall'elemento [**singleSignOn**](onexschema-singlesignon-onex-element.md) .</span><span class="sxs-lookup"><span data-stu-id="8a60b-108">The **maxDelay** element is defined by the [**singleSignOn**](onexschema-singlesignon-onex-element.md) element.</span></span>

## <a name="remarks"></a><span data-ttu-id="8a60b-109">Commenti</span><span class="sxs-lookup"><span data-stu-id="8a60b-109">Remarks</span></span>

<span data-ttu-id="8a60b-110">Questo parametro può essere impostato dalla riga di comando tramite il comando **netsh wlan set profileparameter** .</span><span class="sxs-lookup"><span data-stu-id="8a60b-110">This parameter can be set at the command line using the **netsh wlan set profileparameter** command.</span></span> <span data-ttu-id="8a60b-111">Per ulteriori informazioni, vedere [comandi Netsh per WLAN (wireless local area network)](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc755301(v=ws.10)).</span><span class="sxs-lookup"><span data-stu-id="8a60b-111">For more information, see [Netsh Commands for Wireless Local Area Network (wlan)](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc755301(v=ws.10)).</span></span>

## <a name="requirements"></a><span data-ttu-id="8a60b-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8a60b-112">Requirements</span></span>



| <span data-ttu-id="8a60b-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="8a60b-113">Requirement</span></span> | <span data-ttu-id="8a60b-114">Valore</span><span class="sxs-lookup"><span data-stu-id="8a60b-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="8a60b-115">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8a60b-115">Minimum supported client</span></span><br/> | <span data-ttu-id="8a60b-116">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="8a60b-116">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="8a60b-117">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8a60b-117">Minimum supported server</span></span><br/> | <span data-ttu-id="8a60b-118">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="8a60b-118">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="8a60b-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8a60b-119">See also</span></span>

<dl> <dt>

<span data-ttu-id="8a60b-120">**Contesto di definizione dell'elemento nello schema**</span><span class="sxs-lookup"><span data-stu-id="8a60b-120">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="8a60b-121">**singleSignOn**</span><span class="sxs-lookup"><span data-stu-id="8a60b-121">**singleSignOn**</span></span>](onexschema-singlesignon-onex-element.md)
</dt> <dt>

<span data-ttu-id="8a60b-122">**Possibile elemento padre immediato nell'istanza dello schema**</span><span class="sxs-lookup"><span data-stu-id="8a60b-122">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="8a60b-123">**singleSignOn (OneX)**</span><span class="sxs-lookup"><span data-stu-id="8a60b-123">**singleSignOn (OneX)**</span></span>](onexschema-singlesignon-onex-element.md)
</dt> </dl>

 

 
