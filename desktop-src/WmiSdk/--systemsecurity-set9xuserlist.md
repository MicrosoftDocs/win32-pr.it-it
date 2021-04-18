---
description: Consente di impostare i diritti di accesso remoto per un elenco di singoli utenti nei computer che eseguono versioni obsolete di Windows, in cui il controllo dell'accesso tramite descrittori di sicurezza di Windows non è disponibile.
ms.assetid: f6da65d3-86dd-4fc8-b4c0-f7ddc8536d4e
ms.tgt_platform: multiple
title: 'Metodo __SystemSecurity:: Set9XUserList'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __SystemSecurity.Set9XUserList
api_type:
- COM
api_location:
- all
ms.openlocfilehash: dd377da3adf55aef6a78576e1c978196f349f619
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316994"
---
# <a name="__systemsecurityset9xuserlist-method"></a><span data-ttu-id="6a697-103">\_\_Metodo SystemSecurity:: Set9XUserList</span><span class="sxs-lookup"><span data-stu-id="6a697-103">\_\_SystemSecurity::Set9XUserList method</span></span>

<span data-ttu-id="6a697-104">Il metodo **\_ \_ SystemSecurity:: Set9XUserList** imposta i diritti di accesso remoto per un elenco di singoli utenti nei computer che eseguono versioni obsolete di Windows, in cui il controllo dell'accesso tramite i descrittori di sicurezza di Windows non è disponibile.</span><span class="sxs-lookup"><span data-stu-id="6a697-104">The **\_\_SystemSecurity::Set9XUserList** method sets the remote access rights for a list of individual users on computers running obsolete versions of Windows, where access control through Windows security descriptors is not available.</span></span>

<span data-ttu-id="6a697-105">L'elenco viene specificato come una matrice di oggetti incorporati in cui ogni oggetto è un'istanza della classe [**\_ \_ NTLMUser9X**](--ntlmuser9x.md) .</span><span class="sxs-lookup"><span data-stu-id="6a697-105">The list is specified as an array of embedded objects where each object is an instance of the [**\_\_NTLMUser9X**](--ntlmuser9x.md) class.</span></span> <span data-ttu-id="6a697-106">Questa funzione è simile a quella del descrittore di sicurezza, ma è più limitata.</span><span class="sxs-lookup"><span data-stu-id="6a697-106">This functions similar to the security descriptor, but it is more limited.</span></span> <span data-ttu-id="6a697-107">I gruppi non sono supportati e non è possibile controllare l'accesso locale perché l'utente locale ha sempre accesso completo.</span><span class="sxs-lookup"><span data-stu-id="6a697-107">Groups are not supported and there is no control over local access, because the local user always has full access.</span></span> <span data-ttu-id="6a697-108">Sono consentite sia le voci di controllo di accesso sia Deny che Allow (ACE). per questo motivo, l'ordine ACE è importante nell'elenco di controllo di accesso discrezionale (DACL).</span><span class="sxs-lookup"><span data-stu-id="6a697-108">Both deny and allow access control entries (ACE) are permitted, and because of this, the ACE order is important in the discretionary access control list (DACL).</span></span> <span data-ttu-id="6a697-109">Per ulteriori informazioni, vedere [Order of ACE in a DACL](/windows/desktop/SecAuthZ/order-of-aces-in-a-dacl).</span><span class="sxs-lookup"><span data-stu-id="6a697-109">For more information, see [Order of ACEs in a DACL](/windows/desktop/SecAuthZ/order-of-aces-in-a-dacl).</span></span>

## <a name="syntax"></a><span data-ttu-id="6a697-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6a697-110">Syntax</span></span>


```C++
HRESULT Set9XUserList(
  [in] __NTLMUser9X ul[]
);
```



## <a name="parameters"></a><span data-ttu-id="6a697-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="6a697-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6a697-112">*ul* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6a697-112">*ul* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6a697-113">Matrice di utenti.</span><span class="sxs-lookup"><span data-stu-id="6a697-113">Array of users.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6a697-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="6a697-114">Return value</span></span>

<span data-ttu-id="6a697-115">Questo metodo restituisce un valore **HRESULT** che indica lo stato della chiamata al metodo.</span><span class="sxs-lookup"><span data-stu-id="6a697-115">This method returns an **HRESULT** that indicates the status of the method call.</span></span> <span data-ttu-id="6a697-116">Nell'elenco seguente sono elencati i valori restituiti significativi per **Set9XUserList**.</span><span class="sxs-lookup"><span data-stu-id="6a697-116">The following list lists the return values that are of significance to **Set9XUserList**.</span></span> <span data-ttu-id="6a697-117">Per gli script e le applicazioni Visual Basic, il risultato può essere ottenuto da [OutParameters. returnValue](parsing-outparameters-objects.md).</span><span class="sxs-lookup"><span data-stu-id="6a697-117">For scripting and Visual Basic applications, the result can be obtained from [OutParameters.ReturnValue](parsing-outparameters-objects.md).</span></span> <span data-ttu-id="6a697-118">Per altre informazioni, vedere [creazione di oggetti InParameters e analisi di oggetti OutParameters](constructing-inparameters-objects-and-parsing-outparameters-objects.md).</span><span class="sxs-lookup"><span data-stu-id="6a697-118">For more information, see [Constructing InParameters Objects and Parsing OutParameters Objects](constructing-inparameters-objects-and-parsing-outparameters-objects.md).</span></span>

<dl> <dt>

<span data-ttu-id="6a697-119">**WBEM \_ E \_ metodo \_ disabilitato**</span><span class="sxs-lookup"><span data-stu-id="6a697-119">**WBEM\_E\_METHOD\_DISABLED**</span></span>
</dt> <dd>

<span data-ttu-id="6a697-120">Questo metodo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="6a697-120">This method is not supported.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6a697-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6a697-121">Requirements</span></span>



| <span data-ttu-id="6a697-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="6a697-122">Requirement</span></span> | <span data-ttu-id="6a697-123">Valore</span><span class="sxs-lookup"><span data-stu-id="6a697-123">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="6a697-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6a697-124">Minimum supported client</span></span><br/> | <span data-ttu-id="6a697-125">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6a697-125">Windows Vista</span></span><br/>       |
| <span data-ttu-id="6a697-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6a697-126">Minimum supported server</span></span><br/> | <span data-ttu-id="6a697-127">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6a697-127">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="6a697-128">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="6a697-128">Namespace</span></span><br/>                | <span data-ttu-id="6a697-129">tutti gli spazi dei nomi WMI</span><span class="sxs-lookup"><span data-stu-id="6a697-129">all WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="6a697-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6a697-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6a697-131">Classi di sistema WMI</span><span class="sxs-lookup"><span data-stu-id="6a697-131">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> <dt>

[<span data-ttu-id="6a697-132">**\_\_SystemSecurity**</span><span class="sxs-lookup"><span data-stu-id="6a697-132">**\_\_SystemSecurity**</span></span>](--systemsecurity.md)
</dt> <dt>

[<span data-ttu-id="6a697-133">**\_\_SystemSecurity:: GetSd**</span><span class="sxs-lookup"><span data-stu-id="6a697-133">**\_\_SystemSecurity::GetSD**</span></span>](--systemsecurity-getsd.md)
</dt> <dt>

[<span data-ttu-id="6a697-134">**\_\_SystemSecurity:: SetD**</span><span class="sxs-lookup"><span data-stu-id="6a697-134">**\_\_SystemSecurity::SetSD**</span></span>](--systemsecurity-setsd.md)
</dt> <dt>

[<span data-ttu-id="6a697-135">**\_ACE Win32**</span><span class="sxs-lookup"><span data-stu-id="6a697-135">**Win32\_ACE**</span></span>](/previous-versions/windows/desktop/secrcw32prov/win32-ace)
</dt> <dt>

[<span data-ttu-id="6a697-136">**\_SecurityDescriptor Win32**</span><span class="sxs-lookup"><span data-stu-id="6a697-136">**Win32\_SecurityDescriptor**</span></span>](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor)
</dt> <dt>

[<span data-ttu-id="6a697-137">Sicurezza degli spazi dei nomi WMI</span><span class="sxs-lookup"><span data-stu-id="6a697-137">Securing WMI Namespaces</span></span>](securing-wmi-namespaces.md)
</dt> <dt>

[<span data-ttu-id="6a697-138">Costanti di sicurezza WMI</span><span class="sxs-lookup"><span data-stu-id="6a697-138">WMI Security Constants</span></span>](wmi-security-constants.md)
</dt> </dl>

 

