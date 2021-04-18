---
description: Indica se una chiave condivisa è crittografata.
ms.assetid: 9206ef74-cd3e-4374-bea9-0c10505d10bf
title: Elemento Protected (sharedKey)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- protected
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 0b48ef0e07e5502ea8577904facc52f9f7e69838
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306484"
---
# <a name="protected-sharedkey-element"></a><span data-ttu-id="70903-103">Elemento Protected (sharedKey)</span><span class="sxs-lookup"><span data-stu-id="70903-103">protected (sharedKey) Element</span></span>

<span data-ttu-id="70903-104">L'elemento Protected (sharedKey) indica se una chiave condivisa è crittografata.</span><span class="sxs-lookup"><span data-stu-id="70903-104">The protected (sharedKey) element indicates whether a shared key is encrypted.</span></span>

``` syntax
<xs:element name="protected"
    type="boolean"
 />
```

<span data-ttu-id="70903-105">L'elemento è definito dall'elemento [**sharedKey**](wlan-profileschema-sharedkey-security-element.md) .</span><span class="sxs-lookup"><span data-stu-id="70903-105">The element is defined by the [**sharedKey**](wlan-profileschema-sharedkey-security-element.md) element.</span></span>

## <a name="remarks"></a><span data-ttu-id="70903-106">Commenti</span><span class="sxs-lookup"><span data-stu-id="70903-106">Remarks</span></span>

<span data-ttu-id="70903-107">Per Windows Vista e Windows Server 2008, **protected** always ha il valore true se il profilo è stato recuperato dall'archivio profili, ad esempio chiamando [**WlanGetProfile**](/windows/desktop/api/wlanapi/nf-wlanapi-wlangetprofile).</span><span class="sxs-lookup"><span data-stu-id="70903-107">For Windows Vista and Windows Server 2008, **protected** always has a value of TRUE if the profile was retrieved from the profile store (for example, by calling [**WlanGetProfile**](/windows/desktop/api/wlanapi/nf-wlanapi-wlangetprofile)).</span></span>

<span data-ttu-id="70903-108">Per i profili destinati all'uso in Windows XP con Service Pack 3 (SP3) o l'API LAN wireless per Windows XP con Service Pack 2 (SP2), il valore **protetto** deve essere false.</span><span class="sxs-lookup"><span data-stu-id="70903-108">For profiles intended for use on Windows XP with Service Pack 3 (SP3) or Wireless LAN API for Windows XP with Service Pack 2 (SP2), **protected** must have a value of FALSE.</span></span>

## <a name="examples"></a><span data-ttu-id="70903-109">Esempio</span><span class="sxs-lookup"><span data-stu-id="70903-109">Examples</span></span>

<span data-ttu-id="70903-110">Per visualizzare i profili di esempio che usano l'elemento **protetto** , vedere esempi di profili [wireless](wireless-profile-samples.md).</span><span class="sxs-lookup"><span data-stu-id="70903-110">To view sample profiles that use the **protected** element, see [Wireless Profile Samples](wireless-profile-samples.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="70903-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="70903-111">Requirements</span></span>



| <span data-ttu-id="70903-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="70903-112">Requirement</span></span> | <span data-ttu-id="70903-113">Valore</span><span class="sxs-lookup"><span data-stu-id="70903-113">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="70903-114">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="70903-114">Minimum supported client</span></span><br/> | <span data-ttu-id="70903-115">Windows Vista, Windows XP con \[ solo app desktop SP3\]</span><span class="sxs-lookup"><span data-stu-id="70903-115">Windows Vista, Windows XP with SP3 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="70903-116">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="70903-116">Minimum supported server</span></span><br/> | <span data-ttu-id="70903-117">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="70903-117">Windows Server 2008 \[desktop apps only\]</span></span><br/>                |
| <span data-ttu-id="70903-118">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="70903-118">Redistributable</span></span><br/>          | <span data-ttu-id="70903-119">API LAN wireless per Windows XP con SP2</span><span class="sxs-lookup"><span data-stu-id="70903-119">Wireless LAN API for Windows XP with SP2</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="70903-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="70903-120">See also</span></span>

<dl> <dt>

<span data-ttu-id="70903-121">**Contesto di definizione dell'elemento nello schema**</span><span class="sxs-lookup"><span data-stu-id="70903-121">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="70903-122">**sharedKey**</span><span class="sxs-lookup"><span data-stu-id="70903-122">**sharedKey**</span></span>](wlan-profileschema-sharedkey-security-element.md)
</dt> <dt>

<span data-ttu-id="70903-123">**Possibile elemento padre immediato nell'istanza dello schema**</span><span class="sxs-lookup"><span data-stu-id="70903-123">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="70903-124">**sharedKey (sicurezza)**</span><span class="sxs-lookup"><span data-stu-id="70903-124">**sharedKey (security)**</span></span>](wlan-profileschema-sharedkey-security-element.md)
</dt> </dl>

 

 




