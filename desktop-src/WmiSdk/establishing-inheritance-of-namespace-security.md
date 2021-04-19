---
description: È possibile controllare se uno spazio dei nomi figlio eredita il descrittore di sicurezza dello spazio dei nomi padre.
ms.assetid: d4fbd5af-69e2-4c60-907a-cb2a1506b7c9
ms.tgt_platform: multiple
title: Definizione dell'ereditarietà della sicurezza dello spazio dei nomi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74e242299b78ede3ff49679305a97823bc022358
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317554"
---
# <a name="establishing-inheritance-of-namespace-security"></a><span data-ttu-id="467c9-103">Definizione dell'ereditarietà della sicurezza dello spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="467c9-103">Establishing Inheritance of Namespace Security</span></span>

<span data-ttu-id="467c9-104">È possibile controllare se uno spazio dei nomi figlio eredita il descrittore di sicurezza dello spazio dei nomi padre.</span><span class="sxs-lookup"><span data-stu-id="467c9-104">You can control whether a child namespace inherits the security descriptor of the parent namespace.</span></span>

<span data-ttu-id="467c9-105">Gli spazi dei nomi WMI hanno descrittori di sicurezza che controllano chi può accedere allo spazio dei nomi e ai dati dello spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="467c9-105">WMI namespaces have security descriptors that control who can access the namespace and the data of the namespace.</span></span> <span data-ttu-id="467c9-106">Ogni descrittore di sicurezza dispone di un elenco di controllo di accesso discrezionale (DACL) e un elenco di controllo di accesso (SACL) di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="467c9-106">Each security descriptor has a discretionary access control list (DACL) and a security access control list (SACL).</span></span> <span data-ttu-id="467c9-107">Questi elenchi contengono voci di controllo di accesso (ACE).</span><span class="sxs-lookup"><span data-stu-id="467c9-107">These lists contain access control entries (ACE).</span></span>

<span data-ttu-id="467c9-108">A seconda delle [**costanti del flag ACE dello spazio dei nomi**](namespace-ace-flag-constants.md) impostate, le autorizzazioni applicate a uno spazio dei nomi possono essere ereditate da tutti gli spazi dei nomi figlio dello spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="467c9-108">Depending on the [**Namespace ACE Flag Constants**](namespace-ace-flag-constants.md) that are set, permissions that are applied to a namespace may be inherited by all the child namespaces of that namespace.</span></span> <span data-ttu-id="467c9-109">Uno spazio dei nomi figlio eredita il descrittore di sicurezza dello spazio dei nomi padre quando viene creato lo spazio dei nomi figlio se il **contenitore eredita il flag \_ \_ ACE** nel descrittore di sicurezza dello spazio dei nomi padre.</span><span class="sxs-lookup"><span data-stu-id="467c9-109">A child namespace inherits the security descriptor of its parent namespace when the child namespace is created if the **CONTAINER\_INHERIT\_ACE** flag is in the parent namespace security descriptor.</span></span> <span data-ttu-id="467c9-110">Se il **contenitore \_ eredita \_ ACE \| No \_ essere propagati \_ eredita \_ ACE** è impostato, solo lo spazio dei nomi figlio eredita il descrittore di sicurezza, non gli spazi dei nomi nipoti.</span><span class="sxs-lookup"><span data-stu-id="467c9-110">If **CONTAINER\_INHERIT\_ACE\|NO\_PROPOGATE\_INHERIT\_ACE** is set, then only the child namespace inherits the security descriptor, not grandchild namespaces.</span></span> <span data-ttu-id="467c9-111">Gli spazi dei nomi figlio possono eseguire l'override delle autorizzazioni di sicurezza del padre chiamando i metodi della classe [**\_ \_ SystemSecurity**](--systemsecurity.md) per scrivere un nuovo descrittore di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="467c9-111">Child namespaces can override the security permissions of their parent by calling methods of the [**\_\_SystemSecurity**](--systemsecurity.md) class to write a new security descriptor.</span></span> <span data-ttu-id="467c9-112">Non è possibile modificare le impostazioni di sicurezza predefinite.</span><span class="sxs-lookup"><span data-stu-id="467c9-112">The default security settings cannot be changed.</span></span> <span data-ttu-id="467c9-113">Per altre informazioni, vedere [impostazione dei descrittori di sicurezza spazio dei nomi](setting-namespace-security-descriptors.md). Per ulteriori informazioni sugli elenchi DACL, vedere [Access Control List (ACL)](/windows/desktop/SecAuthZ/access-control-lists) e le [**costanti di tipo ACE dello spazio dei nomi**](namespace-ace-type-constants.md).</span><span class="sxs-lookup"><span data-stu-id="467c9-113">For more information, see [Setting Namepace Security Descriptors](setting-namespace-security-descriptors.md).For more information about DACLs, see [Access Control Lists (ACL)](/windows/desktop/SecAuthZ/access-control-lists) and [**Namespace ACE Type Constants**](namespace-ace-type-constants.md).</span></span>

<span data-ttu-id="467c9-114">Si noti che le autorizzazioni predefinite non possono essere modificate.</span><span class="sxs-lookup"><span data-stu-id="467c9-114">Note that the default permissions cannot be changed.</span></span> <span data-ttu-id="467c9-115">Inoltre, l'impostazione del flag di protezione **\_ \_ DACL se** durante l'impostazione del descrittore di sicurezza (SD) non viene utilizzata per aggiungere una SD specializzata a uno spazio dei nomi figlio.</span><span class="sxs-lookup"><span data-stu-id="467c9-115">Furthermore, setting the **SE\_DACL\_PROTECTED** flag while setting the security descriptor (SD) is not used to add a specialized SD to a child namespace.</span></span> <span data-ttu-id="467c9-116">Per eseguire l'override di una SD ereditata, è sufficiente impostarne una nuova.</span><span class="sxs-lookup"><span data-stu-id="467c9-116">To override an inherited SD, simply set a new one.</span></span> <span data-ttu-id="467c9-117">Per ereditare tale SD in uno spazio dei nomi figlio, passare il **contenitore \_ ereditare \_** il flag ACE nel descrittore di sicurezza dello spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="467c9-117">To inherit that SD to a child namespace, pass the **CONTAINER\_INHERIT\_ACE** flag in the namespace security descriptor.</span></span> <span data-ttu-id="467c9-118">Per ereditare solo l'elemento figlio e non i discendenti, passare `CONTAINER_INHERIT_ACE|NO_PROPOGATE_INHERIT_ACE`</span><span class="sxs-lookup"><span data-stu-id="467c9-118">To inherit to just the child, and not the descendants, pass `CONTAINER_INHERIT_ACE|NO_PROPOGATE_INHERIT_ACE`</span></span>

<span data-ttu-id="467c9-119">.</span><span class="sxs-lookup"><span data-stu-id="467c9-119">.</span></span>

## <a name="related-topics"></a><span data-ttu-id="467c9-120">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="467c9-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="467c9-121">Impostazione di descrittori di sicurezza spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="467c9-121">Setting Namepace Security Descriptors</span></span>](setting-namespace-security-descriptors.md)
</dt> <dt>

[<span data-ttu-id="467c9-122">**\_\_SystemSecurity**</span><span class="sxs-lookup"><span data-stu-id="467c9-122">**\_\_SystemSecurity**</span></span>](--systemsecurity.md)
</dt> </dl>

 

 
