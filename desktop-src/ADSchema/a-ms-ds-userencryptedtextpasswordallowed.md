---
title: attributo ms-DS-user-Encrypted-text-password-allowed
description: Indica se Active Directory la password viene archiviata nel formato di crittografia reversibile.
ms.assetid: 67067cf6-60e3-4626-bf8c-a0a1264a899e
ms.tgt_platform: multiple
keywords:
- ms-DS-utente-crittografato-testo-password-schema AD attributo consentito
- Schema AD dell'attributo ms-DS-UserEncryptedTextPasswordAllowed
topic_type:
- apiref
api_name:
- ms-DS-User-Encrypted-Text-Password-Allowed
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d99ae61566ceec94336fd58951214dfc3255d2e
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "104479760"
---
# <a name="ms-ds-user-encrypted-text-password-allowed-attribute"></a><span data-ttu-id="aa9a3-105">attributo ms-DS-user-Encrypted-text-password-allowed</span><span class="sxs-lookup"><span data-stu-id="aa9a3-105">ms-DS-User-Encrypted-Text-Password-Allowed attribute</span></span>

<span data-ttu-id="aa9a3-106">Indica se Active Directory la password viene archiviata nel formato di crittografia reversibile.</span><span class="sxs-lookup"><span data-stu-id="aa9a3-106">Indicates whether Active Directory will store the password in the reversible encryption format.</span></span> <span data-ttu-id="aa9a3-107">True se la password è archiviata nel formato di crittografia reversibile; in caso contrario, false.</span><span class="sxs-lookup"><span data-stu-id="aa9a3-107">True if the password is stored in the reversible encryption format; otherwise, False.</span></span>

> [!Note]  
> <span data-ttu-id="aa9a3-108">Questo attributo non viene usato da [Active Directory Lightweight Directory Services](/previous-versions/windows/desktop/adam/active-directory-lightweight-directory-services) ed è incluso solo per la completezza e la parità con userAccountControl.</span><span class="sxs-lookup"><span data-stu-id="aa9a3-108">This attribute is not used by [Active Directory Lightweight Directory Services](/previous-versions/windows/desktop/adam/active-directory-lightweight-directory-services) and is only included for completeness/parity with userAccountControl.</span></span> <span data-ttu-id="aa9a3-109">AD LDS non archivia le password con la crittografia reversibile, indipendentemente dal valore di questo attributo per un determinato oggetto o dai criteri di sicurezza del computer che riguardano la crittografia reversibile nel computer stesso.</span><span class="sxs-lookup"><span data-stu-id="aa9a3-109">AD LDS does not store passwords with reversible encryption, regardless of this attribute's value on any given object or the computer security policy pertaining to reversible encryption on the computer itself.</span></span>

 



| <span data-ttu-id="aa9a3-110">Voce</span><span class="sxs-lookup"><span data-stu-id="aa9a3-110">Entry</span></span> | <span data-ttu-id="aa9a3-111">Valore</span><span class="sxs-lookup"><span data-stu-id="aa9a3-111">Value</span></span> |
|-------------------|--------------------------------------------|
| <span data-ttu-id="aa9a3-112">CN</span><span class="sxs-lookup"><span data-stu-id="aa9a3-112">CN</span></span>                | <span data-ttu-id="aa9a3-113">ms-DS-utente-crittografato-testo-password-consentito</span><span class="sxs-lookup"><span data-stu-id="aa9a3-113">ms-DS-User-Encrypted-Text-Password-Allowed</span></span> |
| <span data-ttu-id="aa9a3-114">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="aa9a3-114">Ldap-Display-Name</span></span> | <span data-ttu-id="aa9a3-115">ms-DS-UserEncryptedTextPasswordAllowed</span><span class="sxs-lookup"><span data-stu-id="aa9a3-115">ms-DS-UserEncryptedTextPasswordAllowed</span></span>     |
| <span data-ttu-id="aa9a3-116">Dimensione</span><span class="sxs-lookup"><span data-stu-id="aa9a3-116">Size</span></span>              | \-                                         |
| <span data-ttu-id="aa9a3-117">Privilegio aggiornamento</span><span class="sxs-lookup"><span data-stu-id="aa9a3-117">Update Privilege</span></span>  | \-                                         |
| <span data-ttu-id="aa9a3-118">Frequenza di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="aa9a3-118">Update Frequency</span></span>  | \-                                         |
| <span data-ttu-id="aa9a3-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="aa9a3-119">Attribute-Id</span></span>      | <span data-ttu-id="aa9a3-120">1.2.840.113556.1.4.1856</span><span class="sxs-lookup"><span data-stu-id="aa9a3-120">1.2.840.113556.1.4.1856</span></span>                    |
| <span data-ttu-id="aa9a3-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="aa9a3-121">System-Id-Guid</span></span>    | <span data-ttu-id="aa9a3-122">5a87c7f2-93c5-454c-a8c5-8cb09613292e</span><span class="sxs-lookup"><span data-stu-id="aa9a3-122">5a87c7f2-93c5-454c-a8c5-8cb09613292e</span></span>       |
| <span data-ttu-id="aa9a3-123">Sintassi</span><span class="sxs-lookup"><span data-stu-id="aa9a3-123">Syntax</span></span>            | [<span data-ttu-id="aa9a3-124">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="aa9a3-124">**Boolean**</span></span>](s-boolean.md)               |



## <a name="implementations"></a><span data-ttu-id="aa9a3-125">Implementazioni</span><span class="sxs-lookup"><span data-stu-id="aa9a3-125">Implementations</span></span>

-   [<span data-ttu-id="aa9a3-126">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="aa9a3-126">**ADAM**</span></span>](#adam)

## <a name="adam"></a><span data-ttu-id="aa9a3-127">ADAM</span><span class="sxs-lookup"><span data-stu-id="aa9a3-127">ADAM</span></span>



| <span data-ttu-id="aa9a3-128">Voce</span><span class="sxs-lookup"><span data-stu-id="aa9a3-128">Entry</span></span> | <span data-ttu-id="aa9a3-129">Valore</span><span class="sxs-lookup"><span data-stu-id="aa9a3-129">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="aa9a3-130">ID collegamento</span><span class="sxs-lookup"><span data-stu-id="aa9a3-130">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="aa9a3-131">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="aa9a3-131">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="aa9a3-132">System-Only</span><span class="sxs-lookup"><span data-stu-id="aa9a3-132">System-Only</span></span>            | <span data-ttu-id="aa9a3-133">Falso</span><span class="sxs-lookup"><span data-stu-id="aa9a3-133">False</span></span>                                                             |
| <span data-ttu-id="aa9a3-134">È a valore singolo</span><span class="sxs-lookup"><span data-stu-id="aa9a3-134">Is-Single-Valued</span></span>       | <span data-ttu-id="aa9a3-135">Vero</span><span class="sxs-lookup"><span data-stu-id="aa9a3-135">True</span></span>                                                              |
| <span data-ttu-id="aa9a3-136">Indicizzato</span><span class="sxs-lookup"><span data-stu-id="aa9a3-136">Is Indexed</span></span>             | <span data-ttu-id="aa9a3-137">Falso</span><span class="sxs-lookup"><span data-stu-id="aa9a3-137">False</span></span>                                                             |
| <span data-ttu-id="aa9a3-138">Nel catalogo globale</span><span class="sxs-lookup"><span data-stu-id="aa9a3-138">In Global Catalog</span></span>      | <span data-ttu-id="aa9a3-139">Falso</span><span class="sxs-lookup"><span data-stu-id="aa9a3-139">False</span></span>                                                             |
| <span data-ttu-id="aa9a3-140">NT-Security-descrittore</span><span class="sxs-lookup"><span data-stu-id="aa9a3-140">NT-Security-Descriptor</span></span> | <span data-ttu-id="aa9a3-141">O:BAG: NON VALIDO: S:</span><span class="sxs-lookup"><span data-stu-id="aa9a3-141">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="aa9a3-142">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="aa9a3-142">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="aa9a3-143">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="aa9a3-143">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="aa9a3-144">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="aa9a3-144">Search-Flags</span></span>           | <span data-ttu-id="aa9a3-145">0x00000000</span><span class="sxs-lookup"><span data-stu-id="aa9a3-145">0x00000000</span></span>                                                        |
| <span data-ttu-id="aa9a3-146">System-Flags</span><span class="sxs-lookup"><span data-stu-id="aa9a3-146">System-Flags</span></span>           | <span data-ttu-id="aa9a3-147">0x00000010</span><span class="sxs-lookup"><span data-stu-id="aa9a3-147">0x00000010</span></span>                                                        |
| <span data-ttu-id="aa9a3-148">Classi utilizzate in</span><span class="sxs-lookup"><span data-stu-id="aa9a3-148">Classes used in</span></span>        | [<span data-ttu-id="aa9a3-149">**ms-DS-associabile-oggetto**</span><span class="sxs-lookup"><span data-stu-id="aa9a3-149">**ms-DS-Bindable-Object**</span></span>](c-msds-bindableobject.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="aa9a3-150">Commenti</span><span class="sxs-lookup"><span data-stu-id="aa9a3-150">Remarks</span></span>

<span data-ttu-id="aa9a3-151">In ADAM, questo attributo sostituisce il flag [**Ads \_ UF \_ Encrypted \_ Text \_ password \_ consentita**](/windows/desktop/api/iads/ne-iads-ads_user_flag_enum) dell'attributo [**userAccountControl**](a-useraccountcontrol.md) .</span><span class="sxs-lookup"><span data-stu-id="aa9a3-151">In ADAM, this attribute replaces the [**ADS\_UF\_ENCRYPTED\_TEXT\_PASSWORD\_ALLOWED**](/windows/desktop/api/iads/ne-iads-ads_user_flag_enum) flag of the [**userAccountControl**](a-useraccountcontrol.md) attribute.</span></span>

 

