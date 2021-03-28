---
description: Deprecato. Fornisce la notifica delle modifiche alle identità utente nel sistema, nonché le richieste degli utenti per cambiare l'identità dell'utente corrente.
ms.assetid: 09903aa6-62bf-4820-9a09-79956d775441
title: Interfaccia IIdentityChangeNotify (Msident. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IIdentityChangeNotify
api_type:
- COM
api_location:
- Msoe.dll
ms.openlocfilehash: 4a217b2cfb046bfb9ae5546e015264f74d00b1d0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104227425"
---
# <a name="iidentitychangenotify-interface"></a><span data-ttu-id="c79ab-104">Interfaccia IIdentityChangeNotify</span><span class="sxs-lookup"><span data-stu-id="c79ab-104">IIdentityChangeNotify interface</span></span>

<span data-ttu-id="c79ab-105">\[L'interfaccia **IIdentityChangeNotify** è disponibile per l'uso in Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="c79ab-105">\[The **IIdentityChangeNotify** interface is available for use in Windows 2000.</span></span> <span data-ttu-id="c79ab-106">In Windows XP questa funzionalità è stata sostituita dagli [account utente con cambio rapido utente e desktop remoto](fastuserswitching.md)e potrebbe essere modificata o non disponibile nelle versioni successive.\]</span><span class="sxs-lookup"><span data-stu-id="c79ab-106">In Windows XP, this functionality has been superseded by [User Accounts with Fast User Switching and Remote Desktop](fastuserswitching.md), and might be altered or unavailable in subsequent versions.\]</span></span>

<span data-ttu-id="c79ab-107">Deprecato.</span><span class="sxs-lookup"><span data-stu-id="c79ab-107">Deprecated.</span></span> <span data-ttu-id="c79ab-108">Fornisce la notifica delle modifiche alle identità utente nel sistema, nonché le richieste degli utenti per cambiare l'identità dell'utente corrente.</span><span class="sxs-lookup"><span data-stu-id="c79ab-108">Provides notification of modifications to user identities on the system, as well as user requests to switch the current user identity.</span></span>

## <a name="members"></a><span data-ttu-id="c79ab-109">Membri</span><span class="sxs-lookup"><span data-stu-id="c79ab-109">Members</span></span>

<span data-ttu-id="c79ab-110">L'interfaccia **IIdentityChangeNotify** eredita dall'interfaccia [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="c79ab-110">The **IIdentityChangeNotify** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="c79ab-111">**IIdentityChangeNotify** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="c79ab-111">**IIdentityChangeNotify** also has these types of members:</span></span>

-   [<span data-ttu-id="c79ab-112">Metodi</span><span class="sxs-lookup"><span data-stu-id="c79ab-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="c79ab-113">Metodi</span><span class="sxs-lookup"><span data-stu-id="c79ab-113">Methods</span></span>

<span data-ttu-id="c79ab-114">L'interfaccia **IIdentityChangeNotify** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="c79ab-114">The **IIdentityChangeNotify** interface has these methods.</span></span>



| <span data-ttu-id="c79ab-115">Metodo</span><span class="sxs-lookup"><span data-stu-id="c79ab-115">Method</span></span>                                                                                 | <span data-ttu-id="c79ab-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c79ab-116">Description</span></span>                                                                                                                           |
|:---------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c79ab-117">**IdentityInformationChanged**</span><span class="sxs-lookup"><span data-stu-id="c79ab-117">**IdentityInformationChanged**</span></span>](iidentitychangenotify-identityinformationchanged.md) | <span data-ttu-id="c79ab-118">Deprecato.</span><span class="sxs-lookup"><span data-stu-id="c79ab-118">Deprecated.</span></span> <span data-ttu-id="c79ab-119">Chiamato quando le informazioni relative a un'identità utente sono state modificate o quando un'identità utente è stata aggiunta o eliminata.</span><span class="sxs-lookup"><span data-stu-id="c79ab-119">Called when information about a user identity has changed, or when a user identity has been added or deleted.</span></span><br/>  |
| [<span data-ttu-id="c79ab-120">**QuerySwitchIdentities**</span><span class="sxs-lookup"><span data-stu-id="c79ab-120">**QuerySwitchIdentities**</span></span>](iidentitychangenotify-queryswitchidentities.md)           | <span data-ttu-id="c79ab-121">Deprecato.</span><span class="sxs-lookup"><span data-stu-id="c79ab-121">Deprecated.</span></span> <span data-ttu-id="c79ab-122">Viene chiamato quando l'utente corrente ha richiesto la commutazione dell'identità utente, ma prima che si verifichi l'opzione.</span><span class="sxs-lookup"><span data-stu-id="c79ab-122">Called when the current user has requested that their user identity be switched, but before the switch occurs.</span></span><br/> |
| [<span data-ttu-id="c79ab-123">**SwitchIdentities**</span><span class="sxs-lookup"><span data-stu-id="c79ab-123">**SwitchIdentities**</span></span>](iidentitychangenotify-switchidentities.md)                     | <span data-ttu-id="c79ab-124">Deprecato.</span><span class="sxs-lookup"><span data-stu-id="c79ab-124">Deprecated.</span></span> <span data-ttu-id="c79ab-125">Chiamato quando le identità utente sono cambiate.</span><span class="sxs-lookup"><span data-stu-id="c79ab-125">Called when user identities are switched.</span></span><br/>                                                                      |



 

## <a name="remarks"></a><span data-ttu-id="c79ab-126">Commenti</span><span class="sxs-lookup"><span data-stu-id="c79ab-126">Remarks</span></span>

<span data-ttu-id="c79ab-127">Per implementare le notifiche, un'interfaccia derivata deve connettersi a [**IUserIdentityManager**](iuseridentitymanager.md) chiamando [**IConnectionPoint:: Advise**](/windows/win32/api/ocidl/nf-ocidl-iconnectionpoint-advise) e passando un puntatore all'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="c79ab-127">To implement notifications, a derived interface must connect to the [**IUserIdentityManager**](iuseridentitymanager.md) by calling [**IConnectionPoint::Advise**](/windows/win32/api/ocidl/nf-ocidl-iconnectionpoint-advise) and by passing a pointer to the interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="c79ab-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c79ab-128">Requirements</span></span>



| <span data-ttu-id="c79ab-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="c79ab-129">Requirement</span></span> | <span data-ttu-id="c79ab-130">Valore</span><span class="sxs-lookup"><span data-stu-id="c79ab-130">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c79ab-131">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c79ab-131">Minimum supported client</span></span><br/> | <span data-ttu-id="c79ab-132">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="c79ab-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="c79ab-133">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c79ab-133">Minimum supported server</span></span><br/> | <span data-ttu-id="c79ab-134">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="c79ab-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="c79ab-135">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c79ab-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="c79ab-136"><dt>Msident. h</dt></span><span class="sxs-lookup"><span data-stu-id="c79ab-136"><dt>Msident.h</dt></span></span> </dl>   |
| <span data-ttu-id="c79ab-137">IDL</span><span class="sxs-lookup"><span data-stu-id="c79ab-137">IDL</span></span><br/>                      | <dl> <span data-ttu-id="c79ab-138"><dt>Msident. idl</dt></span><span class="sxs-lookup"><span data-stu-id="c79ab-138"><dt>Msident.idl</dt></span></span> </dl> |
| <span data-ttu-id="c79ab-139">DLL</span><span class="sxs-lookup"><span data-stu-id="c79ab-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c79ab-140"><dt>Msoe.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c79ab-140"><dt>Msoe.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="c79ab-141">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c79ab-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c79ab-142">**IUserIdentityManager**</span><span class="sxs-lookup"><span data-stu-id="c79ab-142">**IUserIdentityManager**</span></span>](iuseridentitymanager.md)
</dt> <dt>

[<span data-ttu-id="c79ab-143">**IConnectionPoint**</span><span class="sxs-lookup"><span data-stu-id="c79ab-143">**IConnectionPoint**</span></span>](/windows/win32/api/ocidl/nn-ocidl-iconnectionpoint)
</dt> </dl>

 

 
