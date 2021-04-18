---
description: Ottiene i diritti di accesso remoto per un elenco di singoli utenti in computer in cui sono in esecuzione versioni obsolete di Windows, in cui il controllo degli accessi tramite descrittori di sicurezza di Windows non è disponibile.
ms.assetid: 79a596db-5f85-4664-8989-f309286eca0d
ms.tgt_platform: multiple
title: 'Metodo __SystemSecurity:: Get9XUserList'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __SystemSecurity.Get9XUserList
api_type:
- COM
api_location:
- all
ms.openlocfilehash: 521f2fe489089d486480c138293ebea39ca6f105
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315998"
---
# <a name="__systemsecurityget9xuserlist-method"></a><span data-ttu-id="41b0b-103">\_\_Metodo SystemSecurity:: Get9XUserList</span><span class="sxs-lookup"><span data-stu-id="41b0b-103">\_\_SystemSecurity::Get9XUserList method</span></span>

<span data-ttu-id="41b0b-104">Il metodo [**\_ \_ SystemSecurity:: Set9XUserList**](--systemsecurity-set9xuserlist.md) ottiene i diritti di accesso remoto per un elenco di singoli utenti nei computer che eseguono versioni obsolete di Windows, in cui il controllo dell'accesso tramite i descrittori di sicurezza di Windows non è disponibile.</span><span class="sxs-lookup"><span data-stu-id="41b0b-104">The [**\_\_SystemSecurity::Set9XUserList**](--systemsecurity-set9xuserlist.md) method gets the remote access rights for a list of individual users on computers running obsolete versions of Windows , where access control through Windows security descriptors is not available.</span></span>

<span data-ttu-id="41b0b-105">Questa funzione è simile a quella del descrittore di sicurezza, ma è più limitata.</span><span class="sxs-lookup"><span data-stu-id="41b0b-105">This functions similar to the security descriptor, but it is more limited.</span></span> <span data-ttu-id="41b0b-106">I gruppi non sono supportati e non è possibile controllare l'accesso locale perché l'utente locale ha sempre accesso completo.</span><span class="sxs-lookup"><span data-stu-id="41b0b-106">Groups are not supported and there is no control over local access, because the local user always has full access.</span></span> <span data-ttu-id="41b0b-107">Sono consentite sia le voci di controllo di accesso sia Deny che Allow (ACE). per questo motivo, l'ordine ACE è importante nell'elenco di controllo di accesso discrezionale (DACL).</span><span class="sxs-lookup"><span data-stu-id="41b0b-107">Both deny and allow access control entries (ACE) are permitted, and because of this, the ACE order is important in the discretionary access control list (DACL).</span></span> <span data-ttu-id="41b0b-108">Per ulteriori informazioni, vedere [Order of ACE in a DACL](/windows/desktop/SecAuthZ/order-of-aces-in-a-dacl).</span><span class="sxs-lookup"><span data-stu-id="41b0b-108">For more information, see [Order of ACEs in a DACL](/windows/desktop/SecAuthZ/order-of-aces-in-a-dacl).</span></span>

## <a name="syntax"></a><span data-ttu-id="41b0b-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="41b0b-109">Syntax</span></span>


```C++
HRESULT Get9XUserList(
  [out] __NTLMUser9X ul[]
);
```



## <a name="parameters"></a><span data-ttu-id="41b0b-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="41b0b-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="41b0b-111">*ul* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="41b0b-111">*ul* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="41b0b-112">Matrice di utenti.</span><span class="sxs-lookup"><span data-stu-id="41b0b-112">Array of users.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="41b0b-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="41b0b-113">Return value</span></span>

<span data-ttu-id="41b0b-114">Questo metodo restituisce un valore **HRESULT** che indica lo stato della chiamata al metodo.</span><span class="sxs-lookup"><span data-stu-id="41b0b-114">This method returns an **HRESULT** that indicates the status of the method call.</span></span> <span data-ttu-id="41b0b-115">Nell'elenco seguente sono elencati i valori restituiti significativi per **Get9XUserList**.</span><span class="sxs-lookup"><span data-stu-id="41b0b-115">The following list lists the return values that are of significance to **Get9XUserList**.</span></span> <span data-ttu-id="41b0b-116">Per gli script e le applicazioni Visual Basic, il risultato può essere [OutParameters. returnValue](parsing-outparameters-objects.md).</span><span class="sxs-lookup"><span data-stu-id="41b0b-116">For scripting and Visual Basic applications, the result can be [OutParameters.ReturnValue](parsing-outparameters-objects.md).</span></span> <span data-ttu-id="41b0b-117">Per altre informazioni, vedere [creazione di oggetti InParameters e analisi di oggetti OutParameters](constructing-inparameters-objects-and-parsing-outparameters-objects.md).</span><span class="sxs-lookup"><span data-stu-id="41b0b-117">For more information, see [Constructing InParameters Objects and Parsing OutParameters Objects](constructing-inparameters-objects-and-parsing-outparameters-objects.md).</span></span>

<dl> <dt>

<span data-ttu-id="41b0b-118">**WBEM \_ E \_ metodo \_ disabilitato**</span><span class="sxs-lookup"><span data-stu-id="41b0b-118">**WBEM\_E\_METHOD\_DISABLED**</span></span>
</dt> <dd>

<span data-ttu-id="41b0b-119">Questo metodo non è supportato nelle versioni supportate di Windows.</span><span class="sxs-lookup"><span data-stu-id="41b0b-119">This method is not supported on supported versions of Windows.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="41b0b-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="41b0b-120">Requirements</span></span>



| <span data-ttu-id="41b0b-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="41b0b-121">Requirement</span></span> | <span data-ttu-id="41b0b-122">Valore</span><span class="sxs-lookup"><span data-stu-id="41b0b-122">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="41b0b-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="41b0b-123">Minimum supported client</span></span><br/> | <span data-ttu-id="41b0b-124">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="41b0b-124">Windows Vista</span></span><br/>       |
| <span data-ttu-id="41b0b-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="41b0b-125">Minimum supported server</span></span><br/> | <span data-ttu-id="41b0b-126">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="41b0b-126">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="41b0b-127">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="41b0b-127">Namespace</span></span><br/>                | <span data-ttu-id="41b0b-128">tutti gli spazi dei nomi WMI</span><span class="sxs-lookup"><span data-stu-id="41b0b-128">all WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="41b0b-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="41b0b-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="41b0b-130">Classi di sistema WMI</span><span class="sxs-lookup"><span data-stu-id="41b0b-130">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> <dt>

[<span data-ttu-id="41b0b-131">**\_\_SystemSecurity**</span><span class="sxs-lookup"><span data-stu-id="41b0b-131">**\_\_SystemSecurity**</span></span>](--systemsecurity.md)
</dt> <dt>

[<span data-ttu-id="41b0b-132">**\_\_SystemSecurity:: GetSd**</span><span class="sxs-lookup"><span data-stu-id="41b0b-132">**\_\_SystemSecurity::GetSD**</span></span>](--systemsecurity-getsd.md)
</dt> <dt>

[<span data-ttu-id="41b0b-133">**\_\_SystemSecurity:: SetD**</span><span class="sxs-lookup"><span data-stu-id="41b0b-133">**\_\_SystemSecurity::SetSD**</span></span>](--systemsecurity-setsd.md)
</dt> <dt>

[<span data-ttu-id="41b0b-134">**\_ACE Win32**</span><span class="sxs-lookup"><span data-stu-id="41b0b-134">**Win32\_ACE**</span></span>](/previous-versions/windows/desktop/secrcw32prov/win32-ace)
</dt> <dt>

[<span data-ttu-id="41b0b-135">**\_SecurityDescriptor Win32**</span><span class="sxs-lookup"><span data-stu-id="41b0b-135">**Win32\_SecurityDescriptor**</span></span>](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor)
</dt> <dt>

[<span data-ttu-id="41b0b-136">Sicurezza degli spazi dei nomi WMI</span><span class="sxs-lookup"><span data-stu-id="41b0b-136">Securing WMI Namespaces</span></span>](securing-wmi-namespaces.md)
</dt> <dt>

[<span data-ttu-id="41b0b-137">Costanti di sicurezza WMI</span><span class="sxs-lookup"><span data-stu-id="41b0b-137">WMI Security Constants</span></span>](wmi-security-constants.md)
</dt> </dl>

 

