---
description: IUserIdentityManager non è supportato e può essere modificato o non disponibile in futuro. Usare invece gli account utente con cambio rapido utente e Desktop remoto.
ms.assetid: 3d24b858-bbaf-455c-83cd-3f6f93aba2a8
title: Interfaccia IUserIdentityManager (Msident. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUserIdentityManager
api_type:
- COM
api_location:
- Msident.dll
ms.openlocfilehash: d0d00399e0ba958ef63c5e6597eb4a34387f92f9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103878426"
---
# <a name="iuseridentitymanager-interface"></a><span data-ttu-id="e7247-104">Interfaccia IUserIdentityManager</span><span class="sxs-lookup"><span data-stu-id="e7247-104">IUserIdentityManager interface</span></span>

<span data-ttu-id="e7247-105">\[**IUserIdentityManager** non è supportato e può essere modificato o non disponibile in futuro.</span><span class="sxs-lookup"><span data-stu-id="e7247-105">\[**IUserIdentityManager** is not supported and may be altered or unavailable in the future.</span></span> <span data-ttu-id="e7247-106">Usare invece gli [account utente con cambio rapido utente e desktop remoto](fastuserswitching.md).\]</span><span class="sxs-lookup"><span data-stu-id="e7247-106">Instead, use [User Accounts with Fast User Switching and Remote Desktop](fastuserswitching.md).\]</span></span>

<span data-ttu-id="e7247-107">Espone metodi che identificano, enumerano e gestiscono le identità utente nel sistema.</span><span class="sxs-lookup"><span data-stu-id="e7247-107">Exposes methods that identify, enumerate, and manage user identities on the system.</span></span>

## <a name="members"></a><span data-ttu-id="e7247-108">Membri</span><span class="sxs-lookup"><span data-stu-id="e7247-108">Members</span></span>

<span data-ttu-id="e7247-109">L'interfaccia **IUserIdentityManager** eredita dall'interfaccia [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="e7247-109">The **IUserIdentityManager** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="e7247-110">**IUserIdentityManager** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="e7247-110">**IUserIdentityManager** also has these types of members:</span></span>

-   [<span data-ttu-id="e7247-111">Metodi</span><span class="sxs-lookup"><span data-stu-id="e7247-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="e7247-112">Metodi</span><span class="sxs-lookup"><span data-stu-id="e7247-112">Methods</span></span>

<span data-ttu-id="e7247-113">L'interfaccia **IUserIdentityManager** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="e7247-113">The **IUserIdentityManager** interface has these methods.</span></span>



| <span data-ttu-id="e7247-114">Metodo</span><span class="sxs-lookup"><span data-stu-id="e7247-114">Method</span></span>                                                                  | <span data-ttu-id="e7247-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e7247-115">Description</span></span>                                                                                                                                                             |
|:------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e7247-116">**EnumIdentities**</span><span class="sxs-lookup"><span data-stu-id="e7247-116">**EnumIdentities**</span></span>](iuseridentitymanager-enumidentities.md)           | <span data-ttu-id="e7247-117">Deprecato.</span><span class="sxs-lookup"><span data-stu-id="e7247-117">Deprecated.</span></span> <span data-ttu-id="e7247-118">Ottiene un oggetto [**IEnumUserIdentity**](ienumuseridentity.md) che può essere utilizzato per enumerare le identità utente presenti nel sistema.</span><span class="sxs-lookup"><span data-stu-id="e7247-118">Gets an [**IEnumUserIdentity**](ienumuseridentity.md) object, which can be used to enumerate through the user identities present on the system.</span></span><br/> |
| [<span data-ttu-id="e7247-119">**GetIdentityByCookie**</span><span class="sxs-lookup"><span data-stu-id="e7247-119">**GetIdentityByCookie**</span></span>](iuseridentitymanager-getidentitybycookie.md) | <span data-ttu-id="e7247-120">Deprecato.</span><span class="sxs-lookup"><span data-stu-id="e7247-120">Deprecated.</span></span> <span data-ttu-id="e7247-121">Ottiene un'identità utente specifica dal cookie usato per identificarla in modo univoco.</span><span class="sxs-lookup"><span data-stu-id="e7247-121">Gets a specific user identity by the cookie used to uniquely identify it.</span></span><br/>                                                                        |
| [<span data-ttu-id="e7247-122">**Disconnessione**</span><span class="sxs-lookup"><span data-stu-id="e7247-122">**Logoff**</span></span>](iuseridentitymanager-logoff.md)                           | <span data-ttu-id="e7247-123">Deprecato.</span><span class="sxs-lookup"><span data-stu-id="e7247-123">Deprecated.</span></span> <span data-ttu-id="e7247-124">Disconnettere l'identità corrente.</span><span class="sxs-lookup"><span data-stu-id="e7247-124">Log off the current identity.</span></span><br/>                                                                                                                    |
| [<span data-ttu-id="e7247-125">**Accesso**</span><span class="sxs-lookup"><span data-stu-id="e7247-125">**Logon**</span></span>](iuseridentitymanager-logon.md)                             | <span data-ttu-id="e7247-126">Deprecato.</span><span class="sxs-lookup"><span data-stu-id="e7247-126">Deprecated.</span></span> <span data-ttu-id="e7247-127">Visualizza un'interfaccia utente per l'utente, consentendo all'utente di scegliere un'identità utente.</span><span class="sxs-lookup"><span data-stu-id="e7247-127">Displays a UI to the user, allowing the user to choose a user identity.</span></span> <span data-ttu-id="e7247-128">Se l'esito è positivo, l'identità utente verrà registrata e recuperata.</span><span class="sxs-lookup"><span data-stu-id="e7247-128">If successful, the user identity will be logged on and retrieved.</span></span><br/>        |
| [<span data-ttu-id="e7247-129">**ManageIdentities**</span><span class="sxs-lookup"><span data-stu-id="e7247-129">**ManageIdentities**</span></span>](iuseridentitymanager-manageidentities.md)       | <span data-ttu-id="e7247-130">Deprecato.</span><span class="sxs-lookup"><span data-stu-id="e7247-130">Deprecated.</span></span> <span data-ttu-id="e7247-131">Visualizza un'interfaccia utente per l'utente, consentendo all'utente di gestire le identità utente.</span><span class="sxs-lookup"><span data-stu-id="e7247-131">Displays a UI to the user, allowing the user to manage user identities.</span></span><br/>                                                                          |



 

## <a name="requirements"></a><span data-ttu-id="e7247-132">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e7247-132">Requirements</span></span>



| <span data-ttu-id="e7247-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="e7247-133">Requirement</span></span> | <span data-ttu-id="e7247-134">Valore</span><span class="sxs-lookup"><span data-stu-id="e7247-134">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e7247-135">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e7247-135">Minimum supported client</span></span><br/> | <span data-ttu-id="e7247-136">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="e7247-136">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="e7247-137">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e7247-137">Minimum supported server</span></span><br/> | <span data-ttu-id="e7247-138">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="e7247-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="e7247-139">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="e7247-139">End of client support</span></span><br/>    | <span data-ttu-id="e7247-140">Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="e7247-140">Windows 2000 Professional</span></span><br/>                                                   |
| <span data-ttu-id="e7247-141">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="e7247-141">End of server support</span></span><br/>    | <span data-ttu-id="e7247-142">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="e7247-142">Windows 2000 Server</span></span><br/>                                                         |
| <span data-ttu-id="e7247-143">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e7247-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="e7247-144"><dt>Msident. h</dt></span><span class="sxs-lookup"><span data-stu-id="e7247-144"><dt>Msident.h</dt></span></span> </dl>   |
| <span data-ttu-id="e7247-145">IDL</span><span class="sxs-lookup"><span data-stu-id="e7247-145">IDL</span></span><br/>                      | <dl> <span data-ttu-id="e7247-146"><dt>Msident. idl</dt></span><span class="sxs-lookup"><span data-stu-id="e7247-146"><dt>Msident.idl</dt></span></span> </dl> |
| <span data-ttu-id="e7247-147">DLL</span><span class="sxs-lookup"><span data-stu-id="e7247-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e7247-148"><dt>Msident.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e7247-148"><dt>Msident.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e7247-149">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e7247-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e7247-150">**IUserIdentity**</span><span class="sxs-lookup"><span data-stu-id="e7247-150">**IUserIdentity**</span></span>](iuseridentity.md)
</dt> <dt>

[<span data-ttu-id="e7247-151">**IUserIdentity2**</span><span class="sxs-lookup"><span data-stu-id="e7247-151">**IUserIdentity2**</span></span>](iuseridentity2.md)
</dt> <dt>

[<span data-ttu-id="e7247-152">**IEnumUserIdentity**</span><span class="sxs-lookup"><span data-stu-id="e7247-152">**IEnumUserIdentity**</span></span>](ienumuseridentity.md)
</dt> <dt>

[<span data-ttu-id="e7247-153">**IIdentityChangeNotify**</span><span class="sxs-lookup"><span data-stu-id="e7247-153">**IIdentityChangeNotify**</span></span>](iidentitychangenotify.md)
</dt> </dl>

 

 
