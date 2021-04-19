---
description: Specifica il tipo di credenziali utilizzate per l'autenticazione.
ms.assetid: a56ce888-ec07-4ce8-a540-6d1890cb338d
title: Elemento authMode (OneX)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- authMode
api_type:
- Schema
api_location: ''
ms.openlocfilehash: d699b27746226c3eb1550cfd9250e229b40a22e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311676"
---
# <a name="authmode-onex-element"></a><span data-ttu-id="c2f29-103">Elemento authMode (OneX)</span><span class="sxs-lookup"><span data-stu-id="c2f29-103">authMode (OneX) Element</span></span>

<span data-ttu-id="c2f29-104">L'elemento authMode (OneX) specifica il tipo di credenziali usate per l'autenticazione.</span><span class="sxs-lookup"><span data-stu-id="c2f29-104">The authMode (OneX) element specifies the type of credentials used for authentication.</span></span> <span data-ttu-id="c2f29-105">Nella tabella seguente sono descritti i valori possibili.</span><span class="sxs-lookup"><span data-stu-id="c2f29-105">The following table describes the possible values.</span></span>



| <span data-ttu-id="c2f29-106">Valore</span><span class="sxs-lookup"><span data-stu-id="c2f29-106">Value</span></span>         | <span data-ttu-id="c2f29-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c2f29-107">Description</span></span>                                                                                                                                                             |
|---------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c2f29-108">machineOrUser</span><span class="sxs-lookup"><span data-stu-id="c2f29-108">machineOrUser</span></span> | <span data-ttu-id="c2f29-109">Usare le credenziali del computer o dell'utente.</span><span class="sxs-lookup"><span data-stu-id="c2f29-109">Use machine or user credentials.</span></span> <span data-ttu-id="c2f29-110">Quando un utente è connesso, le credenziali dell'utente vengono usate per l'autenticazione.</span><span class="sxs-lookup"><span data-stu-id="c2f29-110">When a user is logged on, the user's credentials are used for authentication.</span></span> <span data-ttu-id="c2f29-111">Quando nessun utente è connesso, vengono usate le credenziali del computer.</span><span class="sxs-lookup"><span data-stu-id="c2f29-111">When no user is logged on, machine credentials are used.</span></span> |
| <span data-ttu-id="c2f29-112">computer</span><span class="sxs-lookup"><span data-stu-id="c2f29-112">machine</span></span>       | <span data-ttu-id="c2f29-113">Usare solo le credenziali del computer.</span><span class="sxs-lookup"><span data-stu-id="c2f29-113">Use machine credentials only.</span></span>                                                                                                                                           |
| <span data-ttu-id="c2f29-114">utente</span><span class="sxs-lookup"><span data-stu-id="c2f29-114">user</span></span>          | <span data-ttu-id="c2f29-115">Usare solo le credenziali utente.</span><span class="sxs-lookup"><span data-stu-id="c2f29-115">Use user credentials only.</span></span>                                                                                                                                              |
| <span data-ttu-id="c2f29-116">guest</span><span class="sxs-lookup"><span data-stu-id="c2f29-116">guest</span></span>         | <span data-ttu-id="c2f29-117">Utilizzare solo le credenziali Guest (vuote).</span><span class="sxs-lookup"><span data-stu-id="c2f29-117">Use guest (empty) credentials only.</span></span>                                                                                                                                     |



 

<span data-ttu-id="c2f29-118">Questo elemento è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="c2f29-118">This element is optional.</span></span> <span data-ttu-id="c2f29-119">Quando authMode non viene specificato in un profilo, viene utilizzato un valore di `machineOrUser` .</span><span class="sxs-lookup"><span data-stu-id="c2f29-119">When authMode is not specified in a profile, a value of `machineOrUser` is used.</span></span>

<span data-ttu-id="c2f29-120">**Windows XP con SP3 e l'API LAN wireless per Windows XP con SP2:** Questo elemento verrà ignorato se è presente in un profilo.</span><span class="sxs-lookup"><span data-stu-id="c2f29-120">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element will be ignored if it is present in a profile.</span></span>

``` syntax
<xs:element name="authMode">
    <xs:simpleType>
        <xs:restriction
            base="string"
        >
            <xs:enumeration
                value="machineOrUser"
             />
            <xs:enumeration
                value="machine"
             />
            <xs:enumeration
                value="user"
             />
            <xs:enumeration
                value="guest"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

<span data-ttu-id="c2f29-121">L'elemento **AuthMode** è definito dall'elemento [**Onex**](onexschema-onex-element.md) .</span><span class="sxs-lookup"><span data-stu-id="c2f29-121">The **authMode** element is defined by the [**OneX**](onexschema-onex-element.md) element.</span></span>

## <a name="remarks"></a><span data-ttu-id="c2f29-122">Commenti</span><span class="sxs-lookup"><span data-stu-id="c2f29-122">Remarks</span></span>

<span data-ttu-id="c2f29-123">Questo parametro può essere impostato dalla riga di comando tramite il comando **netsh wlan set profileparameter** .</span><span class="sxs-lookup"><span data-stu-id="c2f29-123">This parameter can be set at the command line using the **netsh wlan set profileparameter** command.</span></span> <span data-ttu-id="c2f29-124">Per ulteriori informazioni, vedere [comandi Netsh per WLAN (wireless local area network)](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc755301(v=ws.10)).</span><span class="sxs-lookup"><span data-stu-id="c2f29-124">For more information, see [Netsh Commands for Wireless Local Area Network (wlan)](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc755301(v=ws.10)).</span></span>

## <a name="requirements"></a><span data-ttu-id="c2f29-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c2f29-125">Requirements</span></span>



| <span data-ttu-id="c2f29-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="c2f29-126">Requirement</span></span> | <span data-ttu-id="c2f29-127">Valore</span><span class="sxs-lookup"><span data-stu-id="c2f29-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="c2f29-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c2f29-128">Minimum supported client</span></span><br/> | <span data-ttu-id="c2f29-129">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c2f29-129">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="c2f29-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c2f29-130">Minimum supported server</span></span><br/> | <span data-ttu-id="c2f29-131">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="c2f29-131">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c2f29-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c2f29-132">See also</span></span>

<dl> <dt>

<span data-ttu-id="c2f29-133">**Contesto di definizione dell'elemento nello schema**</span><span class="sxs-lookup"><span data-stu-id="c2f29-133">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="c2f29-134">**OneX**</span><span class="sxs-lookup"><span data-stu-id="c2f29-134">**OneX**</span></span>](onexschema-onex-element.md)
</dt> <dt>

<span data-ttu-id="c2f29-135">**Possibile elemento padre immediato nell'istanza dello schema**</span><span class="sxs-lookup"><span data-stu-id="c2f29-135">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="c2f29-136">**OneX**</span><span class="sxs-lookup"><span data-stu-id="c2f29-136">**OneX**</span></span>](onexschema-onex-element.md)
</dt> </dl>

 

 
