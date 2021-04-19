---
description: Nell'elenco seguente sono elencati i valori possibili del campo Flags in una voce di controllo di accesso (ACE) WMI.
ms.assetid: bd09691d-e285-40e0-8686-edd5a132a06e
ms.tgt_platform: multiple
title: Costanti del flag ACE dello spazio dei nomi (Winnt. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OBJECT_INHERIT_ACE
- CONTAINER_INHERIT_ACE
- NO_PROPAGATE_INHERIT_ACE
- INHERIT_ONLY_ACE
- INHERITED_ACE
api_type:
- HeaderDef
api_location:
- Winnt.h
ms.openlocfilehash: 053d4166882b6254dec313cb10fbf10588ba0071
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331844"
---
# <a name="namespace-ace-flag-constants"></a><span data-ttu-id="21978-103">Costanti del flag ACE dello spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="21978-103">Namespace ACE Flag Constants</span></span>

<span data-ttu-id="21978-104">Nell'elenco seguente sono elencati i valori possibili del campo **Flags** in una voce di controllo di accesso (ACE) WMI.</span><span class="sxs-lookup"><span data-stu-id="21978-104">The following list lists the possible values of the **Flags** field in a WMI Access Control Entry (ACE).</span></span>

<dl> <dt>

<span data-ttu-id="21978-105"><span id="OBJECT_INHERIT_ACE"></span><span id="object_inherit_ace"></span>**OGGETTO che \_ eredita \_ ACE**</span><span class="sxs-lookup"><span data-stu-id="21978-105"><span id="OBJECT_INHERIT_ACE"></span><span id="object_inherit_ace"></span>**OBJECT\_INHERIT\_ACE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="21978-106">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="21978-106">1 (0x1)</span></span>
</dt> <dt>



<span data-ttu-id="21978-107">Gli oggetti figlio non contenitore ereditano la voce ACE come una voce ACE efficace.</span><span class="sxs-lookup"><span data-stu-id="21978-107">Non-container child objects inherit the ACE as an effective ACE.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="21978-108"><span id="CONTAINER_INHERIT_ACE"></span><span id="container_inherit_ace"></span>**il contenitore \_ eredita \_ ACE**</span><span class="sxs-lookup"><span data-stu-id="21978-108"><span id="CONTAINER_INHERIT_ACE"></span><span id="container_inherit_ace"></span>**CONTAINER\_INHERIT\_ACE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="21978-109">2 (0x2)</span><span class="sxs-lookup"><span data-stu-id="21978-109">2 (0x2)</span></span>
</dt> <dt>



<span data-ttu-id="21978-110">La voce ACE ha un effetto sugli spazi dei nomi figlio e sullo spazio dei nomi corrente.</span><span class="sxs-lookup"><span data-stu-id="21978-110">The ACE has an effect on child namespaces as well as the current namespace.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="21978-111"><span id="NO_PROPAGATE_INHERIT_ACE"></span><span id="no_propagate_inherit_ace"></span>**Nessuna \_ propagazione \_ eredita \_ ACE**</span><span class="sxs-lookup"><span data-stu-id="21978-111"><span id="NO_PROPAGATE_INHERIT_ACE"></span><span id="no_propagate_inherit_ace"></span>**NO\_PROPAGATE\_INHERIT\_ACE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="21978-112">4 (0x4)</span><span class="sxs-lookup"><span data-stu-id="21978-112">4 (0x4)</span></span>
</dt> <dt>



<span data-ttu-id="21978-113">La voce ACE si applica solo allo spazio dei nomi corrente e agli elementi figlio immediati.</span><span class="sxs-lookup"><span data-stu-id="21978-113">The ACE applies only to the current namespace and immediate children .</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="21978-114"><span id="INHERIT_ONLY_ACE"></span><span id="inherit_only_ace"></span>**EREDITA \_ solo \_ ACE**</span><span class="sxs-lookup"><span data-stu-id="21978-114"><span id="INHERIT_ONLY_ACE"></span><span id="inherit_only_ace"></span>**INHERIT\_ONLY\_ACE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="21978-115">8 (0x8)</span><span class="sxs-lookup"><span data-stu-id="21978-115">8 (0x8)</span></span>
</dt> <dt>



<span data-ttu-id="21978-116">La voce ACE si applica solo agli spazi dei nomi figlio.</span><span class="sxs-lookup"><span data-stu-id="21978-116">The ACE applies only to child namespaces.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="21978-117"><span id="INHERITED_ACE"></span><span id="inherited_ace"></span>**Ace EREDITAta \_**</span><span class="sxs-lookup"><span data-stu-id="21978-117"><span id="INHERITED_ACE"></span><span id="inherited_ace"></span>**INHERITED\_ACE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="21978-118">16 (0x10)</span><span class="sxs-lookup"><span data-stu-id="21978-118">16 (0x10)</span></span>
</dt> <dt>



<span data-ttu-id="21978-119">Questa impostazione non viene impostata dai client, ma viene segnalata ai client quando l'origine di una voce ACE è uno spazio dei nomi padre.</span><span class="sxs-lookup"><span data-stu-id="21978-119">This is not set by clients, but is reported to clients when the source of an ACE is a parent namespace.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="21978-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="21978-120">Requirements</span></span>



| <span data-ttu-id="21978-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="21978-121">Requirement</span></span> | <span data-ttu-id="21978-122">Valore</span><span class="sxs-lookup"><span data-stu-id="21978-122">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="21978-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="21978-123">Header</span></span><br/> | <dl> <span data-ttu-id="21978-124"><dt>Winnt. h</dt></span><span class="sxs-lookup"><span data-stu-id="21978-124"><dt>Winnt.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="21978-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="21978-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="21978-126">Costanti di sicurezza WMI</span><span class="sxs-lookup"><span data-stu-id="21978-126">WMI Security Constants</span></span>](wmi-security-constants.md)
</dt> <dt>

[<span data-ttu-id="21978-127">Impostazione di descrittori di sicurezza spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="21978-127">Setting Namepace Security Descriptors</span></span>](setting-namespace-security-descriptors.md)
</dt> <dt>

[<span data-ttu-id="21978-128">Definizione dell'ereditarietà della sicurezza dello spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="21978-128">Establishing Inheritance of Namespace Security</span></span>](establishing-inheritance-of-namespace-security.md)
</dt> <dt>

[<span data-ttu-id="21978-129">**\_\_SystemSecurity**</span><span class="sxs-lookup"><span data-stu-id="21978-129">**\_\_SystemSecurity**</span></span>](--systemsecurity.md)
</dt> </dl>

 

 




