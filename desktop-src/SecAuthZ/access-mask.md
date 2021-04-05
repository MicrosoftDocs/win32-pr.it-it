---
description: Definisce diritti standard, specifici e generici. Questi diritti vengono usati nelle voci di controllo di accesso (ACE) e rappresentano il metodo principale per specificare l'accesso richiesto o concesso a un oggetto.
ms.assetid: f115ee54-3333-4109-8004-d71904a7a943
title: ACCESS_MASK (Winnt. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d10d9e8db246c2705911cc57221400f40da014d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131450"
---
# <a name="access_mask"></a><span data-ttu-id="b357e-104">maschera di accesso \_</span><span class="sxs-lookup"><span data-stu-id="b357e-104">ACCESS\_MASK</span></span>

<span data-ttu-id="b357e-105">Il tipo di dati di **Access \_ mask** è un valore **DWORD** che definisce diritti standard, specifici e generici.</span><span class="sxs-lookup"><span data-stu-id="b357e-105">The **ACCESS\_MASK** data type is a **DWORD** value that defines standard, specific, and generic rights.</span></span> <span data-ttu-id="b357e-106">Questi diritti vengono usati nelle [*voci di controllo di accesso*](/windows/desktop/SecGloss/a-gly) (ACE) e rappresentano il metodo principale per specificare l'accesso richiesto o concesso a un oggetto.</span><span class="sxs-lookup"><span data-stu-id="b357e-106">These rights are used in [*access control entries*](/windows/desktop/SecGloss/a-gly) (ACEs) and are the primary means of specifying the requested or granted access to an object.</span></span>


```C++
typedef DWORD ACCESS_MASK;
typedef ACCESS_MASK* PACCESS_MASK;
```



## <a name="remarks"></a><span data-ttu-id="b357e-107">Commenti</span><span class="sxs-lookup"><span data-stu-id="b357e-107">Remarks</span></span>

<span data-ttu-id="b357e-108">I bit in questo valore vengono allocati come indicato di seguito.</span><span class="sxs-lookup"><span data-stu-id="b357e-108">The bits in this value are allocated as follows.</span></span>



| <span data-ttu-id="b357e-109">BITS</span><span class="sxs-lookup"><span data-stu-id="b357e-109">Bits</span></span>             | <span data-ttu-id="b357e-110">Significato</span><span class="sxs-lookup"><span data-stu-id="b357e-110">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b357e-111">0 15</span><span class="sxs-lookup"><span data-stu-id="b357e-111">0 15</span></span><br/>  | <span data-ttu-id="b357e-112">Diritti specifici.</span><span class="sxs-lookup"><span data-stu-id="b357e-112">Specific rights.</span></span> <span data-ttu-id="b357e-113">Contiene la maschera di accesso specifica per il tipo di oggetto associato alla maschera.</span><span class="sxs-lookup"><span data-stu-id="b357e-113">Contains the access mask specific to the object type associated with the mask.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="b357e-114">16 23</span><span class="sxs-lookup"><span data-stu-id="b357e-114">16 23</span></span><br/> | <span data-ttu-id="b357e-115">Diritti standard.</span><span class="sxs-lookup"><span data-stu-id="b357e-115">Standard rights.</span></span> <span data-ttu-id="b357e-116">Contiene i diritti di accesso standard dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="b357e-116">Contains the object's standard access rights.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="b357e-117">24</span><span class="sxs-lookup"><span data-stu-id="b357e-117">24</span></span><br/>    | <span data-ttu-id="b357e-118">Accesso alla sicurezza del sistema (**accesso alla \_ \_ sicurezza del sistema**).</span><span class="sxs-lookup"><span data-stu-id="b357e-118">Access system security (**ACCESS\_SYSTEM\_SECURITY**).</span></span> <span data-ttu-id="b357e-119">Viene usato per indicare l'accesso a un [*elenco di controllo di accesso di sistema*](/windows/desktop/SecGloss/s-gly) (SACL).</span><span class="sxs-lookup"><span data-stu-id="b357e-119">It is used to indicate access to a [*system access control list*](/windows/desktop/SecGloss/s-gly) (SACL).</span></span> <span data-ttu-id="b357e-120">Questo tipo di accesso richiede che il processo chiamante disponga del **privilegio \_ \_ nome sicurezza se** (gestione registro di controllo e di sicurezza).</span><span class="sxs-lookup"><span data-stu-id="b357e-120">This type of access requires the calling process to have the **SE\_SECURITY\_NAME** (Manage auditing and security log) privilege.</span></span> <span data-ttu-id="b357e-121">Se questo flag è impostato nella maschera di accesso di una voce di controllo di accesso ACE (accesso con esito positivo o negativo), l'accesso al SACL verrà controllato.</span><span class="sxs-lookup"><span data-stu-id="b357e-121">If this flag is set in the access mask of an audit access ACE (successful or unsuccessful access), the SACL access will be audited.</span></span><br/> |
| <span data-ttu-id="b357e-122">25</span><span class="sxs-lookup"><span data-stu-id="b357e-122">25</span></span><br/>    | <span data-ttu-id="b357e-123">Massimo consentito (**massimo \_ consentito**).</span><span class="sxs-lookup"><span data-stu-id="b357e-123">Maximum allowed (**MAXIMUM\_ALLOWED**).</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="b357e-124">26 27</span><span class="sxs-lookup"><span data-stu-id="b357e-124">26 27</span></span><br/> | <span data-ttu-id="b357e-125">Riservato.</span><span class="sxs-lookup"><span data-stu-id="b357e-125">Reserved.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| <span data-ttu-id="b357e-126">28</span><span class="sxs-lookup"><span data-stu-id="b357e-126">28</span></span><br/>    | <span data-ttu-id="b357e-127">Generic All (**generico \_ All**).</span><span class="sxs-lookup"><span data-stu-id="b357e-127">Generic all (**GENERIC\_ALL**).</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="b357e-128">29</span><span class="sxs-lookup"><span data-stu-id="b357e-128">29</span></span><br/>    | <span data-ttu-id="b357e-129">Esecuzione generica **( \_ esecuzione generica**).</span><span class="sxs-lookup"><span data-stu-id="b357e-129">Generic execute (**GENERIC\_EXECUTE**).</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="b357e-130">30</span><span class="sxs-lookup"><span data-stu-id="b357e-130">30</span></span><br/>    | <span data-ttu-id="b357e-131">Scrittura generica **( \_ scrittura generica**).</span><span class="sxs-lookup"><span data-stu-id="b357e-131">Generic write (**GENERIC\_WRITE**).</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="b357e-132">31</span><span class="sxs-lookup"><span data-stu-id="b357e-132">31</span></span><br/>    | <span data-ttu-id="b357e-133">Lettura generica **( \_ lettura generica**).</span><span class="sxs-lookup"><span data-stu-id="b357e-133">Generic read (**GENERIC\_READ**).</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |



 

<span data-ttu-id="b357e-134">I bit dei diritti standard, da 16 a 23, contengono i diritti di accesso standard dell'oggetto e possono essere costituiti da una combinazione dei flag predefiniti seguenti.</span><span class="sxs-lookup"><span data-stu-id="b357e-134">Standard rights bits, 16 to 23, contain the object's standard access rights and can be a combination of the following predefined flags.</span></span>



| <span data-ttu-id="b357e-135">bit</span><span class="sxs-lookup"><span data-stu-id="b357e-135">Bit</span></span>           | <span data-ttu-id="b357e-136">Contrassegno</span><span class="sxs-lookup"><span data-stu-id="b357e-136">Flag</span></span>                         | <span data-ttu-id="b357e-137">Significato</span><span class="sxs-lookup"><span data-stu-id="b357e-137">Meaning</span></span>                                                                                                                                                                                                                                  |
|---------------|------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b357e-138">16</span><span class="sxs-lookup"><span data-stu-id="b357e-138">16</span></span><br/> | <span data-ttu-id="b357e-139">**DELETE**</span><span class="sxs-lookup"><span data-stu-id="b357e-139">**DELETE**</span></span><br/>        | <span data-ttu-id="b357e-140">Elimina accesso.</span><span class="sxs-lookup"><span data-stu-id="b357e-140">Delete access.</span></span><br/>                                                                                                                                                                                                                |
| <span data-ttu-id="b357e-141">17</span><span class="sxs-lookup"><span data-stu-id="b357e-141">17</span></span><br/> | <span data-ttu-id="b357e-142">**controllo di lettura \_**</span><span class="sxs-lookup"><span data-stu-id="b357e-142">**READ\_CONTROL**</span></span><br/> | <span data-ttu-id="b357e-143">Accesso in lettura al proprietario, al gruppo e all' [*elenco di controllo di accesso discrezionale*](/windows/desktop/SecGloss/d-gly) (DACL) del descrittore di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="b357e-143">Read access to the owner, group, and [*discretionary access control list*](/windows/desktop/SecGloss/d-gly) (DACL) of the security descriptor.</span></span><br/> |
| <span data-ttu-id="b357e-144">18</span><span class="sxs-lookup"><span data-stu-id="b357e-144">18</span></span><br/> | <span data-ttu-id="b357e-145">**Scrivi \_ DAC**</span><span class="sxs-lookup"><span data-stu-id="b357e-145">**WRITE\_DAC**</span></span><br/>    | <span data-ttu-id="b357e-146">Accesso in scrittura all'elenco DACL.</span><span class="sxs-lookup"><span data-stu-id="b357e-146">Write access to the DACL.</span></span><br/>                                                                                                                                                                                                     |
| <span data-ttu-id="b357e-147">19</span><span class="sxs-lookup"><span data-stu-id="b357e-147">19</span></span><br/> | <span data-ttu-id="b357e-148">**Scrivi \_ proprietario**</span><span class="sxs-lookup"><span data-stu-id="b357e-148">**WRITE\_OWNER**</span></span><br/>  | <span data-ttu-id="b357e-149">Accesso in scrittura al proprietario.</span><span class="sxs-lookup"><span data-stu-id="b357e-149">Write access to owner.</span></span><br/>                                                                                                                                                                                                        |
| <span data-ttu-id="b357e-150">20</span><span class="sxs-lookup"><span data-stu-id="b357e-150">20</span></span><br/> | <span data-ttu-id="b357e-151">**SINCRONIZZARE**</span><span class="sxs-lookup"><span data-stu-id="b357e-151">**SYNCHRONIZE**</span></span><br/>   | <span data-ttu-id="b357e-152">Sincronizzare l'accesso.</span><span class="sxs-lookup"><span data-stu-id="b357e-152">Synchronize access.</span></span><br/>                                                                                                                                                                                                           |



 

<span data-ttu-id="b357e-153">Le costanti seguenti definite in Winnt. h rappresentano i diritti di accesso specifici e standard.</span><span class="sxs-lookup"><span data-stu-id="b357e-153">The following constants defined in Winnt.h represent the specific and standard access rights.</span></span>


```C++
#define DELETE                           (0x00010000L)
#define READ_CONTROL                     (0x00020000L)
#define WRITE_DAC                        (0x00040000L)
#define WRITE_OWNER                      (0x00080000L)
#define SYNCHRONIZE                      (0x00100000L)

#define STANDARD_RIGHTS_REQUIRED         (0x000F0000L)

#define STANDARD_RIGHTS_READ             (READ_CONTROL)
#define STANDARD_RIGHTS_WRITE            (READ_CONTROL)
#define STANDARD_RIGHTS_EXECUTE          (READ_CONTROL)

#define STANDARD_RIGHTS_ALL              (0x001F0000L)

#define SPECIFIC_RIGHTS_ALL              (0x0000FFFFL)
```



## <a name="requirements"></a><span data-ttu-id="b357e-154">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b357e-154">Requirements</span></span>



| <span data-ttu-id="b357e-155">Requisito</span><span class="sxs-lookup"><span data-stu-id="b357e-155">Requirement</span></span> | <span data-ttu-id="b357e-156">Valore</span><span class="sxs-lookup"><span data-stu-id="b357e-156">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b357e-157">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b357e-157">Minimum supported client</span></span><br/> | <span data-ttu-id="b357e-158">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="b357e-158">Windows XP \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="b357e-159">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b357e-159">Minimum supported server</span></span><br/> | <span data-ttu-id="b357e-160">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="b357e-160">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="b357e-161">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b357e-161">Header</span></span><br/>                   | <dl> <span data-ttu-id="b357e-162"><dt>Winnt. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b357e-162"><dt>Winnt.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b357e-163">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b357e-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b357e-164">Controllo di accesso</span><span class="sxs-lookup"><span data-stu-id="b357e-164">Access Control</span></span>](access-control.md)
</dt> <dt>

[<span data-ttu-id="b357e-165">Strutture di controllo di accesso di base</span><span class="sxs-lookup"><span data-stu-id="b357e-165">Basic Access Control Structures</span></span>](authorization-structures.md)
</dt> <dt>

[<span data-ttu-id="b357e-166">Maschere di accesso e diritti di accesso</span><span class="sxs-lookup"><span data-stu-id="b357e-166">Access Rights and Access Masks</span></span>](access-rights-and-access-masks.md)
</dt> <dt>

[<span data-ttu-id="b357e-167">**\_Mapping generico**</span><span class="sxs-lookup"><span data-stu-id="b357e-167">**GENERIC\_MAPPING**</span></span>](/windows/desktop/api/Winnt/ns-winnt-generic_mapping)
</dt> </dl>

 

