---
description: IUserIdentity non è supportato e può essere modificato o non disponibile in futuro. Usare invece gli account utente con cambio rapido utente e Desktop remoto.
ms.assetid: c2f11f8b-f944-445b-b4fc-ac57b0fe3a74
title: Interfaccia IUserIdentity (Msident. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUserIdentity
api_type:
- COM
api_location:
- Msident.dll
ms.openlocfilehash: 068d806086aff44db172a4a7b09f55b600204478
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104979482"
---
# <a name="iuseridentity-interface"></a><span data-ttu-id="a28a2-104">Interfaccia IUserIdentity</span><span class="sxs-lookup"><span data-stu-id="a28a2-104">IUserIdentity interface</span></span>

<span data-ttu-id="a28a2-105">\[**IUserIdentity** non è supportato e può essere modificato o non disponibile in futuro.</span><span class="sxs-lookup"><span data-stu-id="a28a2-105">\[**IUserIdentity** is not supported and may be altered or unavailable in the future.</span></span> <span data-ttu-id="a28a2-106">Usare invece gli [account utente con cambio rapido utente e desktop remoto](fastuserswitching.md).\]</span><span class="sxs-lookup"><span data-stu-id="a28a2-106">Instead, use [User Accounts with Fast User Switching and Remote Desktop](fastuserswitching.md).\]</span></span>

<span data-ttu-id="a28a2-107">Espone i metodi che forniscono i dati di identificazione, registro di sistema e cartella per un'identità utente specifica.</span><span class="sxs-lookup"><span data-stu-id="a28a2-107">Exposes methods that provide identification, registry, and folder data for a specific user identity.</span></span>

## <a name="members"></a><span data-ttu-id="a28a2-108">Membri</span><span class="sxs-lookup"><span data-stu-id="a28a2-108">Members</span></span>

<span data-ttu-id="a28a2-109">L'interfaccia **IUserIdentity** eredita dall'interfaccia [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="a28a2-109">The **IUserIdentity** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="a28a2-110">**IUserIdentity** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="a28a2-110">**IUserIdentity** also has these types of members:</span></span>

-   [<span data-ttu-id="a28a2-111">Metodi</span><span class="sxs-lookup"><span data-stu-id="a28a2-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="a28a2-112">Metodi</span><span class="sxs-lookup"><span data-stu-id="a28a2-112">Methods</span></span>

<span data-ttu-id="a28a2-113">L'interfaccia **IUserIdentity** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="a28a2-113">The **IUserIdentity** interface has these methods.</span></span>



| <span data-ttu-id="a28a2-114">Metodo</span><span class="sxs-lookup"><span data-stu-id="a28a2-114">Method</span></span>                                                         | <span data-ttu-id="a28a2-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a28a2-115">Description</span></span>                                                                                      |
|:---------------------------------------------------------------|:-------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a28a2-116">**GetCookie**</span><span class="sxs-lookup"><span data-stu-id="a28a2-116">**GetCookie**</span></span>](iuseridentity-getcookie.md)                   | <span data-ttu-id="a28a2-117">Deprecato.</span><span class="sxs-lookup"><span data-stu-id="a28a2-117">Deprecated.</span></span> <span data-ttu-id="a28a2-118">Ottiene il cookie utilizzato per identificare in modo univoco l'identità dell'utente.</span><span class="sxs-lookup"><span data-stu-id="a28a2-118">Gets the cookie used to uniquely identify this user identity.</span></span><br/>             |
| [<span data-ttu-id="a28a2-119">**GetIdentityFolder**</span><span class="sxs-lookup"><span data-stu-id="a28a2-119">**GetIdentityFolder**</span></span>](iuseridentity-getidentityfolder.md)   | <span data-ttu-id="a28a2-120">Deprecato.</span><span class="sxs-lookup"><span data-stu-id="a28a2-120">Deprecated.</span></span> <span data-ttu-id="a28a2-121">Ottiene la cartella di file associata a questa identità.</span><span class="sxs-lookup"><span data-stu-id="a28a2-121">Gets the file folder associated with this identity.</span></span><br/>                       |
| [<span data-ttu-id="a28a2-122">**GetName**</span><span class="sxs-lookup"><span data-stu-id="a28a2-122">**GetName**</span></span>](iuseridentity-getname.md)                       | <span data-ttu-id="a28a2-123">Deprecato.</span><span class="sxs-lookup"><span data-stu-id="a28a2-123">Deprecated.</span></span> <span data-ttu-id="a28a2-124">Ottiene il nome associato a questa identità utente.</span><span class="sxs-lookup"><span data-stu-id="a28a2-124">Gets the name associated with this user identity.</span></span><br/>                         |
| [<span data-ttu-id="a28a2-125">**OpenIdentityRegKey**</span><span class="sxs-lookup"><span data-stu-id="a28a2-125">**OpenIdentityRegKey**</span></span>](iuseridentity-openidentityregkey.md) | <span data-ttu-id="a28a2-126">Deprecato.</span><span class="sxs-lookup"><span data-stu-id="a28a2-126">Deprecated.</span></span> <span data-ttu-id="a28a2-127">Recupera la chiave nel registro di sistema che corrisponde a questa identità utente.</span><span class="sxs-lookup"><span data-stu-id="a28a2-127">Retrieves the key in the registry that corresponds to this user identity.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="a28a2-128">Commenti</span><span class="sxs-lookup"><span data-stu-id="a28a2-128">Remarks</span></span>

<span data-ttu-id="a28a2-129">Questa interfaccia fornisce informazioni che corrispondono a una specifica identità utente presente nel sistema.</span><span class="sxs-lookup"><span data-stu-id="a28a2-129">This interface provides information that corresponds to a specific user identity present on the system.</span></span> <span data-ttu-id="a28a2-130">È possibile accedere alla cartella Identity dell'identità utente, alla relativa chiave del registro di sistema e al relativo cookie di identificazione, nonché recuperare il nome associato all'identità utente.</span><span class="sxs-lookup"><span data-stu-id="a28a2-130">You can access this user identity's identity folder, its registry key, and its identification cookie, as well as retrieve the name associated with the user identity.</span></span>

## <a name="requirements"></a><span data-ttu-id="a28a2-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a28a2-131">Requirements</span></span>



| <span data-ttu-id="a28a2-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="a28a2-132">Requirement</span></span> | <span data-ttu-id="a28a2-133">Valore</span><span class="sxs-lookup"><span data-stu-id="a28a2-133">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a28a2-134">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a28a2-134">Minimum supported client</span></span><br/> | <span data-ttu-id="a28a2-135">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="a28a2-135">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="a28a2-136">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a28a2-136">Minimum supported server</span></span><br/> | <span data-ttu-id="a28a2-137">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="a28a2-137">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="a28a2-138">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="a28a2-138">End of client support</span></span><br/>    | <span data-ttu-id="a28a2-139">Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="a28a2-139">Windows 2000 Professional</span></span><br/>                                                   |
| <span data-ttu-id="a28a2-140">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="a28a2-140">End of server support</span></span><br/>    | <span data-ttu-id="a28a2-141">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="a28a2-141">Windows 2000 Server</span></span><br/>                                                         |
| <span data-ttu-id="a28a2-142">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a28a2-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="a28a2-143"><dt>Msident. h</dt></span><span class="sxs-lookup"><span data-stu-id="a28a2-143"><dt>Msident.h</dt></span></span> </dl>   |
| <span data-ttu-id="a28a2-144">IDL</span><span class="sxs-lookup"><span data-stu-id="a28a2-144">IDL</span></span><br/>                      | <dl> <span data-ttu-id="a28a2-145"><dt>Msident. idl</dt></span><span class="sxs-lookup"><span data-stu-id="a28a2-145"><dt>Msident.idl</dt></span></span> </dl> |
| <span data-ttu-id="a28a2-146">DLL</span><span class="sxs-lookup"><span data-stu-id="a28a2-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a28a2-147"><dt>Msident.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a28a2-147"><dt>Msident.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a28a2-148">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a28a2-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a28a2-149">**IUserIdentity2**</span><span class="sxs-lookup"><span data-stu-id="a28a2-149">**IUserIdentity2**</span></span>](iuseridentity2.md)
</dt> <dt>

[<span data-ttu-id="a28a2-150">**IUserIdentityManager**</span><span class="sxs-lookup"><span data-stu-id="a28a2-150">**IUserIdentityManager**</span></span>](iuseridentitymanager.md)
</dt> <dt>

[<span data-ttu-id="a28a2-151">**IEnumUserIdentity**</span><span class="sxs-lookup"><span data-stu-id="a28a2-151">**IEnumUserIdentity**</span></span>](ienumuseridentity.md)
</dt> </dl>

 

 
