---
description: Specifica se la LAN virtuale (VLAN) usata dal dispositivo viene modificata in base alle credenziali dell'utente.
ms.assetid: 4ac92954-adb2-4b0c-9c4e-81f772ea03ed
title: Elemento userBasedVirtualLan (singleSignOn)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- userBasedVirtualLan
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 6ef421e35f7fa121c31e58cfeba4eee969a1b6fb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129731"
---
# <a name="userbasedvirtuallan-singlesignon-element"></a><span data-ttu-id="43d4a-103">Elemento userBasedVirtualLan (singleSignOn)</span><span class="sxs-lookup"><span data-stu-id="43d4a-103">userBasedVirtualLan (singleSignOn) Element</span></span>

<span data-ttu-id="43d4a-104">L'elemento userBasedVirtualLan (singleSignOn) specifica se la LAN virtuale (VLAN) usata dal dispositivo viene modificata in base alle credenziali dell'utente.</span><span class="sxs-lookup"><span data-stu-id="43d4a-104">The userBasedVirtualLan (singleSignOn) element specifies if the virtual LAN (VLAN) used by the device changes based on the user's credentials.</span></span> <span data-ttu-id="43d4a-105">Alcuni dispositivi NAS (Network Access Server) modificano la VLAN dopo l'autenticazione dell'utente.</span><span class="sxs-lookup"><span data-stu-id="43d4a-105">Some network access server (NAS) devices change the VLAN after a user authenticates.</span></span> <span data-ttu-id="43d4a-106">Quando userBasedVirtualLan è TRUE, il NAS può modificare la VLAN di un dispositivo dopo l'autenticazione dell'utente.</span><span class="sxs-lookup"><span data-stu-id="43d4a-106">When userBasedVirtualLan is TRUE, the NAS may change a device's VLAN after a user authenticates.</span></span>

<span data-ttu-id="43d4a-107">Questo elemento è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="43d4a-107">This element is optional.</span></span> <span data-ttu-id="43d4a-108">Quando userBasedVirtualLan non viene specificato in un profilo, viene usato il valore FALSE.</span><span class="sxs-lookup"><span data-stu-id="43d4a-108">When userBasedVirtualLan is not specified in a profile, a value of FALSE is used.</span></span>

<span data-ttu-id="43d4a-109">**Windows XP con SP3 e l'API LAN wireless per Windows XP con SP2:** Questo elemento verrà ignorato se è presente in un profilo.</span><span class="sxs-lookup"><span data-stu-id="43d4a-109">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element will be ignored if it is present in a profile.</span></span>

``` syntax
<xs:element name="userBasedVirtualLan"
    type="boolean"
    minOccurs="0"
 />
```

<span data-ttu-id="43d4a-110">L'elemento **userBasedVirtualLan** è definito dall'elemento [**singleSignOn**](onexschema-singlesignon-onex-element.md) .</span><span class="sxs-lookup"><span data-stu-id="43d4a-110">The **userBasedVirtualLan** element is defined by the [**singleSignOn**](onexschema-singlesignon-onex-element.md) element.</span></span>

## <a name="remarks"></a><span data-ttu-id="43d4a-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="43d4a-111">Remarks</span></span>

<span data-ttu-id="43d4a-112">Questo parametro può essere impostato dalla riga di comando tramite il comando **netsh wlan set profileparameter** .</span><span class="sxs-lookup"><span data-stu-id="43d4a-112">This parameter can be set at the command line using the **netsh wlan set profileparameter** command.</span></span> <span data-ttu-id="43d4a-113">Per ulteriori informazioni, vedere [comandi Netsh per WLAN (wireless local area network)](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc755301(v=ws.10)).</span><span class="sxs-lookup"><span data-stu-id="43d4a-113">For more information, see [Netsh Commands for Wireless Local Area Network (wlan)](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc755301(v=ws.10)).</span></span>

## <a name="requirements"></a><span data-ttu-id="43d4a-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="43d4a-114">Requirements</span></span>



| <span data-ttu-id="43d4a-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="43d4a-115">Requirement</span></span> | <span data-ttu-id="43d4a-116">Valore</span><span class="sxs-lookup"><span data-stu-id="43d4a-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="43d4a-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="43d4a-117">Minimum supported client</span></span><br/> | <span data-ttu-id="43d4a-118">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="43d4a-118">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="43d4a-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="43d4a-119">Minimum supported server</span></span><br/> | <span data-ttu-id="43d4a-120">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="43d4a-120">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="43d4a-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="43d4a-121">See also</span></span>

<dl> <dt>

<span data-ttu-id="43d4a-122">**Contesto di definizione dell'elemento nello schema**</span><span class="sxs-lookup"><span data-stu-id="43d4a-122">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="43d4a-123">**singleSignOn**</span><span class="sxs-lookup"><span data-stu-id="43d4a-123">**singleSignOn**</span></span>](onexschema-singlesignon-onex-element.md)
</dt> <dt>

<span data-ttu-id="43d4a-124">**Possibile elemento padre immediato nell'istanza dello schema**</span><span class="sxs-lookup"><span data-stu-id="43d4a-124">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="43d4a-125">**singleSignOn (OneX)**</span><span class="sxs-lookup"><span data-stu-id="43d4a-125">**singleSignOn (OneX)**</span></span>](onexschema-singlesignon-onex-element.md)
</dt> </dl>

 

 
