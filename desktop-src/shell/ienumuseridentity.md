---
description: IEnumUserIdentity non è supportato e può essere modificato o non disponibile in futuro. Usare invece gli account utente con cambio rapido utente e Desktop remoto.
ms.assetid: df4b6235-e66a-4187-b1f9-33c042cae2f2
title: Interfaccia IEnumUserIdentity (Msident. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumUserIdentity
api_type:
- COM
api_location:
- Msident.dll
ms.openlocfilehash: 48abf182942f90ecd477a241be3bf45323bdbdf3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104979503"
---
# <a name="ienumuseridentity-interface"></a><span data-ttu-id="93ecc-104">Interfaccia IEnumUserIdentity</span><span class="sxs-lookup"><span data-stu-id="93ecc-104">IEnumUserIdentity interface</span></span>

<span data-ttu-id="93ecc-105">\[**IEnumUserIdentity** non è supportato e può essere modificato o non disponibile in futuro.</span><span class="sxs-lookup"><span data-stu-id="93ecc-105">\[**IEnumUserIdentity** is not supported and may be altered or unavailable in the future.</span></span> <span data-ttu-id="93ecc-106">Usare invece gli [account utente con cambio rapido utente e desktop remoto](fastuserswitching.md).\]</span><span class="sxs-lookup"><span data-stu-id="93ecc-106">Instead, use [User Accounts with Fast User Switching and Remote Desktop](fastuserswitching.md).\]</span></span>

<span data-ttu-id="93ecc-107">Fornisce l'enumerazione di tutte le identità utente presenti nel sistema.</span><span class="sxs-lookup"><span data-stu-id="93ecc-107">Provides enumeration of all user identities present on the system.</span></span>

## <a name="members"></a><span data-ttu-id="93ecc-108">Membri</span><span class="sxs-lookup"><span data-stu-id="93ecc-108">Members</span></span>

<span data-ttu-id="93ecc-109">L'interfaccia **IEnumUserIdentity** eredita dall'interfaccia [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="93ecc-109">The **IEnumUserIdentity** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="93ecc-110">**IEnumUserIdentity** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="93ecc-110">**IEnumUserIdentity** also has these types of members:</span></span>

-   [<span data-ttu-id="93ecc-111">Metodi</span><span class="sxs-lookup"><span data-stu-id="93ecc-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="93ecc-112">Metodi</span><span class="sxs-lookup"><span data-stu-id="93ecc-112">Methods</span></span>

<span data-ttu-id="93ecc-113">L'interfaccia **IEnumUserIdentity** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="93ecc-113">The **IEnumUserIdentity** interface has these methods.</span></span>



| <span data-ttu-id="93ecc-114">Metodo</span><span class="sxs-lookup"><span data-stu-id="93ecc-114">Method</span></span>                                         | <span data-ttu-id="93ecc-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="93ecc-115">Description</span></span>                                                                                                                  |
|:-----------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="93ecc-116">**Clone**</span><span class="sxs-lookup"><span data-stu-id="93ecc-116">**Clone**</span></span>](ienumuseridentity-clone.md)       | <span data-ttu-id="93ecc-117">Deprecato.</span><span class="sxs-lookup"><span data-stu-id="93ecc-117">Deprecated.</span></span> <span data-ttu-id="93ecc-118">Ottiene una copia dell'enumerazione corrente.</span><span class="sxs-lookup"><span data-stu-id="93ecc-118">Gets a copy of the current enumeration.</span></span><br/>                                                               |
| [<span data-ttu-id="93ecc-119">**GetCount**</span><span class="sxs-lookup"><span data-stu-id="93ecc-119">**GetCount**</span></span>](ienumuseridentity-getcount.md) | <span data-ttu-id="93ecc-120">Deprecato.</span><span class="sxs-lookup"><span data-stu-id="93ecc-120">Deprecated.</span></span> <span data-ttu-id="93ecc-121">Ottiene il numero di identità utente attualmente presenti nel sistema.</span><span class="sxs-lookup"><span data-stu-id="93ecc-121">Gets the count of user identities currently on the system.</span></span><br/>                                            |
| [<span data-ttu-id="93ecc-122">**Avanti**</span><span class="sxs-lookup"><span data-stu-id="93ecc-122">**Next**</span></span>](ienumuseridentity-next.md)         | <span data-ttu-id="93ecc-123">Deprecato.</span><span class="sxs-lookup"><span data-stu-id="93ecc-123">Deprecated.</span></span> <span data-ttu-id="93ecc-124">Recupera una matrice di interfacce di identità utente dall'enumerazione.</span><span class="sxs-lookup"><span data-stu-id="93ecc-124">Retrieves an array of user identity interfaces from the enumeration.</span></span><br/>                                  |
| [<span data-ttu-id="93ecc-125">**Reset**</span><span class="sxs-lookup"><span data-stu-id="93ecc-125">**Reset**</span></span>](ienumuseridentity-reset.md)       | <span data-ttu-id="93ecc-126">Deprecato.</span><span class="sxs-lookup"><span data-stu-id="93ecc-126">Deprecated.</span></span> <span data-ttu-id="93ecc-127">Reimposta il numero interno di interfacce recuperate nell'enumerazione.</span><span class="sxs-lookup"><span data-stu-id="93ecc-127">Resets the internal count of retrieved interfaces in the enumeration.</span></span><br/>                                 |
| [<span data-ttu-id="93ecc-128">**Ignora**</span><span class="sxs-lookup"><span data-stu-id="93ecc-128">**Skip**</span></span>](ienumuseridentity-skip.md)         | <span data-ttu-id="93ecc-129">Deprecato.</span><span class="sxs-lookup"><span data-stu-id="93ecc-129">Deprecated.</span></span> <span data-ttu-id="93ecc-130">Ignora un determinato numero di interfacce di identità utente nell'enumerazione.</span><span class="sxs-lookup"><span data-stu-id="93ecc-130">Skips a given number of user identity interfaces in the enumeration.</span></span> <span data-ttu-id="93ecc-131">Utilizzato durante il recupero delle interfacce.</span><span class="sxs-lookup"><span data-stu-id="93ecc-131">Used when retrieving interfaces.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="93ecc-132">Commenti</span><span class="sxs-lookup"><span data-stu-id="93ecc-132">Remarks</span></span>

<span data-ttu-id="93ecc-133">Per recuperare informazioni sulle identità utente presenti nel sistema, è possibile usare questa interfaccia.</span><span class="sxs-lookup"><span data-stu-id="93ecc-133">To retrieve information about user identities present on the system, you can use this interface.</span></span> <span data-ttu-id="93ecc-134">Da un'interfaccia [**IUserIdentityManager**](iuseridentitymanager.md) è possibile chiamare [**IUserIdentityManager:: EnumIdentities**](iuseridentitymanager-enumidentities.md) per recuperare questa interfaccia.</span><span class="sxs-lookup"><span data-stu-id="93ecc-134">From a [**IUserIdentityManager**](iuseridentitymanager.md) interface, you can call [**IUserIdentityManager::EnumIdentities**](iuseridentitymanager-enumidentities.md) to retrieve this interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="93ecc-135">Requisiti</span><span class="sxs-lookup"><span data-stu-id="93ecc-135">Requirements</span></span>



| <span data-ttu-id="93ecc-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="93ecc-136">Requirement</span></span> | <span data-ttu-id="93ecc-137">Valore</span><span class="sxs-lookup"><span data-stu-id="93ecc-137">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="93ecc-138">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="93ecc-138">Minimum supported client</span></span><br/> | <span data-ttu-id="93ecc-139">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="93ecc-139">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="93ecc-140">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="93ecc-140">Minimum supported server</span></span><br/> | <span data-ttu-id="93ecc-141">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="93ecc-141">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="93ecc-142">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="93ecc-142">End of client support</span></span><br/>    | <span data-ttu-id="93ecc-143">Windows XP</span><span class="sxs-lookup"><span data-stu-id="93ecc-143">Windows XP</span></span><br/>                                                                  |
| <span data-ttu-id="93ecc-144">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="93ecc-144">End of server support</span></span><br/>    | <span data-ttu-id="93ecc-145">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="93ecc-145">Windows Server 2003</span></span><br/>                                                         |
| <span data-ttu-id="93ecc-146">Intestazione</span><span class="sxs-lookup"><span data-stu-id="93ecc-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="93ecc-147"><dt>Msident. h</dt></span><span class="sxs-lookup"><span data-stu-id="93ecc-147"><dt>Msident.h</dt></span></span> </dl>   |
| <span data-ttu-id="93ecc-148">IDL</span><span class="sxs-lookup"><span data-stu-id="93ecc-148">IDL</span></span><br/>                      | <dl> <span data-ttu-id="93ecc-149"><dt>Msident. idl</dt></span><span class="sxs-lookup"><span data-stu-id="93ecc-149"><dt>Msident.idl</dt></span></span> </dl> |
| <span data-ttu-id="93ecc-150">DLL</span><span class="sxs-lookup"><span data-stu-id="93ecc-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="93ecc-151"><dt>Msident.dll</dt></span><span class="sxs-lookup"><span data-stu-id="93ecc-151"><dt>Msident.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="93ecc-152">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="93ecc-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="93ecc-153">**IUserIdentityManager**</span><span class="sxs-lookup"><span data-stu-id="93ecc-153">**IUserIdentityManager**</span></span>](iuseridentitymanager.md)
</dt> </dl>

 

 
