---
description: IUserIdentity2 non è supportato e può essere modificato o non disponibile in futuro. Usare invece gli account utente con cambio rapido utente e Desktop remoto.
ms.assetid: 85238574-f6bf-43d7-a41b-3ea086c45e07
title: Interfaccia IUserIdentity2 (Msident. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUserIdentity2
api_type:
- COM
api_location:
- Msident.dll
ms.openlocfilehash: 88142e462566a6afaf299096744a0b8f9ea83dfa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524442"
---
# <a name="iuseridentity2-interface"></a><span data-ttu-id="a7e33-104">Interfaccia IUserIdentity2</span><span class="sxs-lookup"><span data-stu-id="a7e33-104">IUserIdentity2 interface</span></span>

<span data-ttu-id="a7e33-105">\[**IUserIdentity2** non è supportato e può essere modificato o non disponibile in futuro.</span><span class="sxs-lookup"><span data-stu-id="a7e33-105">\[**IUserIdentity2** is not supported and may be altered or unavailable in the future.</span></span> <span data-ttu-id="a7e33-106">Usare invece gli [account utente con cambio rapido utente e desktop remoto](fastuserswitching.md).\]</span><span class="sxs-lookup"><span data-stu-id="a7e33-106">Instead, use [User Accounts with Fast User Switching and Remote Desktop](fastuserswitching.md).\]</span></span>

<span data-ttu-id="a7e33-107">Espone metodi che forniscono la denominazione, la password e il controllo ordinale per un'identità utente specifica.</span><span class="sxs-lookup"><span data-stu-id="a7e33-107">Exposes methods that provide naming, password, and ordinal control for a specific user identity.</span></span>

## <a name="members"></a><span data-ttu-id="a7e33-108">Membri</span><span class="sxs-lookup"><span data-stu-id="a7e33-108">Members</span></span>

<span data-ttu-id="a7e33-109">L'interfaccia **IUserIdentity2** eredita da [**IUserIdentity**](iuseridentity.md).</span><span class="sxs-lookup"><span data-stu-id="a7e33-109">The **IUserIdentity2** interface inherits from [**IUserIdentity**](iuseridentity.md).</span></span> <span data-ttu-id="a7e33-110">**IUserIdentity2** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="a7e33-110">**IUserIdentity2** also has these types of members:</span></span>

-   [<span data-ttu-id="a7e33-111">Metodi</span><span class="sxs-lookup"><span data-stu-id="a7e33-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="a7e33-112">Metodi</span><span class="sxs-lookup"><span data-stu-id="a7e33-112">Methods</span></span>

<span data-ttu-id="a7e33-113">L'interfaccia **IUserIdentity2** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="a7e33-113">The **IUserIdentity2** interface has these methods.</span></span>



| <span data-ttu-id="a7e33-114">Metodo</span><span class="sxs-lookup"><span data-stu-id="a7e33-114">Method</span></span>                                                  | <span data-ttu-id="a7e33-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a7e33-115">Description</span></span>                                                       |
|:--------------------------------------------------------|:------------------------------------------------------------------|
| [<span data-ttu-id="a7e33-116">**ChangePassword**</span><span class="sxs-lookup"><span data-stu-id="a7e33-116">**ChangePassword**</span></span>](iuseridentity2-changepassword.md) | <span data-ttu-id="a7e33-117">Deprecato.</span><span class="sxs-lookup"><span data-stu-id="a7e33-117">Deprecated.</span></span> <span data-ttu-id="a7e33-118">Imposta una nuova password per l'identità.</span><span class="sxs-lookup"><span data-stu-id="a7e33-118">Sets a new password for the identity.</span></span><br/>      |
| [<span data-ttu-id="a7e33-119">**GetOrdinal**</span><span class="sxs-lookup"><span data-stu-id="a7e33-119">**GetOrdinal**</span></span>](iuseridentity2-getordinal.md)         | <span data-ttu-id="a7e33-120">Deprecato.</span><span class="sxs-lookup"><span data-stu-id="a7e33-120">Deprecated.</span></span> <span data-ttu-id="a7e33-121">Ottiene il numero ordinale per l'identità.</span><span class="sxs-lookup"><span data-stu-id="a7e33-121">Gets the ordinal number for this identity.</span></span><br/> |
| [<span data-ttu-id="a7e33-122">**SetName**</span><span class="sxs-lookup"><span data-stu-id="a7e33-122">**SetName**</span></span>](iuseridentity2-setname.md)               | <span data-ttu-id="a7e33-123">Deprecato.</span><span class="sxs-lookup"><span data-stu-id="a7e33-123">Deprecated.</span></span> <span data-ttu-id="a7e33-124">Imposta il nome visualizzato dell'identità.</span><span class="sxs-lookup"><span data-stu-id="a7e33-124">Sets the display name of the identity.</span></span><br/>     |



 

## <a name="remarks"></a><span data-ttu-id="a7e33-125">Commenti</span><span class="sxs-lookup"><span data-stu-id="a7e33-125">Remarks</span></span>

<span data-ttu-id="a7e33-126">Questa interfaccia fornisce anche i metodi dell'interfaccia [**IUserIdentity**](iuseridentity.md) , da cui eredita.</span><span class="sxs-lookup"><span data-stu-id="a7e33-126">This interface also provides the methods of the [**IUserIdentity**](iuseridentity.md) interface, from which it inherits.</span></span>

## <a name="requirements"></a><span data-ttu-id="a7e33-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a7e33-127">Requirements</span></span>



| <span data-ttu-id="a7e33-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="a7e33-128">Requirement</span></span> | <span data-ttu-id="a7e33-129">Valore</span><span class="sxs-lookup"><span data-stu-id="a7e33-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a7e33-130">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a7e33-130">Minimum supported client</span></span><br/> | <span data-ttu-id="a7e33-131">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="a7e33-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="a7e33-132">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a7e33-132">Minimum supported server</span></span><br/> | <span data-ttu-id="a7e33-133">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="a7e33-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="a7e33-134">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="a7e33-134">End of client support</span></span><br/>    | <span data-ttu-id="a7e33-135">Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="a7e33-135">Windows 2000 Professional</span></span><br/>                                                   |
| <span data-ttu-id="a7e33-136">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="a7e33-136">End of server support</span></span><br/>    | <span data-ttu-id="a7e33-137">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="a7e33-137">Windows 2000 Server</span></span><br/>                                                         |
| <span data-ttu-id="a7e33-138">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a7e33-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="a7e33-139"><dt>Msident. h</dt></span><span class="sxs-lookup"><span data-stu-id="a7e33-139"><dt>Msident.h</dt></span></span> </dl>   |
| <span data-ttu-id="a7e33-140">IDL</span><span class="sxs-lookup"><span data-stu-id="a7e33-140">IDL</span></span><br/>                      | <dl> <span data-ttu-id="a7e33-141"><dt>Msident. idl</dt></span><span class="sxs-lookup"><span data-stu-id="a7e33-141"><dt>Msident.idl</dt></span></span> </dl> |
| <span data-ttu-id="a7e33-142">DLL</span><span class="sxs-lookup"><span data-stu-id="a7e33-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a7e33-143"><dt>Msident.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a7e33-143"><dt>Msident.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a7e33-144">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a7e33-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a7e33-145">**IUserIdentity**</span><span class="sxs-lookup"><span data-stu-id="a7e33-145">**IUserIdentity**</span></span>](iuseridentity.md)
</dt> </dl>

 

 




