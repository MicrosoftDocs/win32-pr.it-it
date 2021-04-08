---
description: Specifica l'origine delle impostazioni di sicurezza 802.1 X utilizzate da un componente di sicurezza IHV.
ms.assetid: 9c216319-d962-4c68-89a3-116eff3f4376
title: Elemento useMSOneX (IHV)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- useMSOneX
api_type:
- Schema
api_location: ''
ms.openlocfilehash: aa9f2092ac0e76feae89b02f333ae3098288ccef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103967726"
---
# <a name="usemsonex-ihv-element"></a><span data-ttu-id="ab65d-103">Elemento useMSOneX (IHV)</span><span class="sxs-lookup"><span data-stu-id="ab65d-103">useMSOneX (IHV) Element</span></span>

<span data-ttu-id="ab65d-104">L'elemento **useMSOneX** (IHV) specifica l'origine delle impostazioni di sicurezza 802.1 x utilizzate da un componente di sicurezza IHV.</span><span class="sxs-lookup"><span data-stu-id="ab65d-104">The **useMSOneX** (IHV) element specifies the origin of 802.1X security settings used by an IHV security component.</span></span>

<span data-ttu-id="ab65d-105">Quando **useMSOneX** è true, i componenti di sicurezza di IHV utilizzano le impostazioni 802.1 x definite da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="ab65d-105">When **useMSOneX** is true, IHV security components use Microsoft-defined 802.1X settings.</span></span> <span data-ttu-id="ab65d-106">Quando **useMSOneX** è false, i componenti di sicurezza di IHV utilizzano le impostazioni 802.1 x fornite dal fornitore.</span><span class="sxs-lookup"><span data-stu-id="ab65d-106">When **useMSOneX** is false, IHV security components use vendor-supplied 802.1X settings.</span></span>

<span data-ttu-id="ab65d-107">**Windows XP con SP3 e l'API LAN wireless per Windows XP con SP2:** Questo elemento non è supportato.</span><span class="sxs-lookup"><span data-stu-id="ab65d-107">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span>

``` syntax
<xs:element name="useMSOneX"
    type="boolean"
    minOccurs="0"
 />
```

<span data-ttu-id="ab65d-108">L'elemento è definito dall'elemento [**IHV**](wlan-profileschema-ihv-wlanprofile-element.md) .</span><span class="sxs-lookup"><span data-stu-id="ab65d-108">The element is defined by the [**IHV**](wlan-profileschema-ihv-wlanprofile-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="ab65d-109">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ab65d-109">Requirements</span></span>



| <span data-ttu-id="ab65d-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="ab65d-110">Requirement</span></span> | <span data-ttu-id="ab65d-111">Valore</span><span class="sxs-lookup"><span data-stu-id="ab65d-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="ab65d-112">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ab65d-112">Minimum supported client</span></span><br/> | <span data-ttu-id="ab65d-113">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ab65d-113">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="ab65d-114">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ab65d-114">Minimum supported server</span></span><br/> | <span data-ttu-id="ab65d-115">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="ab65d-115">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ab65d-116">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ab65d-116">See also</span></span>

<dl> <dt>

<span data-ttu-id="ab65d-117">**Contesto di definizione dell'elemento nello schema**</span><span class="sxs-lookup"><span data-stu-id="ab65d-117">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="ab65d-118">**IHV**</span><span class="sxs-lookup"><span data-stu-id="ab65d-118">**IHV**</span></span>](wlan-profileschema-ihv-wlanprofile-element.md)
</dt> <dt>

<span data-ttu-id="ab65d-119">**Possibile elemento padre immediato nell'istanza dello schema**</span><span class="sxs-lookup"><span data-stu-id="ab65d-119">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="ab65d-120">**IHV (WLANProfile)**</span><span class="sxs-lookup"><span data-stu-id="ab65d-120">**IHV (WLANProfile)**</span></span>](wlan-profileschema-ihv-wlanprofile-element.md)
</dt> </dl>

 

 




