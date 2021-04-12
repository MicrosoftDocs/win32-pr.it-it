---
title: Impostazione dei diritti per proprietà specifiche di tipi specifici di oggetti
description: Le autorizzazioni specifiche della proprietà possono essere utilizzate in combinazione con l'ereditarietà specifica dell'oggetto per fornire la delega avanzata e dettagliata dell'amministrazione.
ms.assetid: d2ebbe3a-78f7-4bb5-bac0-13236031b7b1
ms.tgt_platform: multiple
keywords:
- impostazione dei diritti per proprietà specifiche di tipi specifici di oggetti AD
- Active Directory, utilizzo, sicurezza, impostazione dei diritti per proprietà specifiche
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 79bfa24b574639e64fbb17c33fabee1185cc014c
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/17/2020
ms.locfileid: "104472459"
---
# <a name="setting-rights-to-specific-properties-of-specific-types-of-objects"></a><span data-ttu-id="b2704-105">Impostazione dei diritti per proprietà specifiche di tipi specifici di oggetti</span><span class="sxs-lookup"><span data-stu-id="b2704-105">Setting Rights to Specific Properties of Specific Types of Objects</span></span>

<span data-ttu-id="b2704-106">Le autorizzazioni specifiche della proprietà possono essere utilizzate in combinazione con l'ereditarietà specifica dell'oggetto per fornire la delega avanzata e dettagliata dell'amministrazione.</span><span class="sxs-lookup"><span data-stu-id="b2704-106">Property-specific permissions can be used in combination with object specific inheritance to provide the powerful and detailed delegation of administration.</span></span> <span data-ttu-id="b2704-107">È possibile impostare una voce ACE ereditabile da un oggetto specifico della proprietà per consentire a un utente o a un gruppo specificato di leggere e/o scrivere un attributo specifico in una classe specificata di oggetti figlio in un contenitore.</span><span class="sxs-lookup"><span data-stu-id="b2704-107">You can set a property-specific object-inheritable ACE to allow a specified user or group to read and/or write a specific attribute on a specified class of child objects in a container.</span></span> <span data-ttu-id="b2704-108">Ad esempio, è possibile impostare una voce ACE in un'unità organizzativa (OU) per consentire a un gruppo di leggere e scrivere l'attributo del numero di telefono di tutti gli oggetti utente nell'unità organizzativa.</span><span class="sxs-lookup"><span data-stu-id="b2704-108">For example, you can set an ACE on an organizational unit (OU) to enable a group to read and write the telephone number attribute of all user objects in the OU.</span></span>

<span data-ttu-id="b2704-109">**Per impostare ACE ereditabili da oggetti specifici della proprietà**</span><span class="sxs-lookup"><span data-stu-id="b2704-109">**To set property-specific object-inheritable ACEs**</span></span>

1.  <span data-ttu-id="b2704-110">Impostare [**IADsAccessControlEntry. AceType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) su **Ads \_ AceType \_ accesso \_ a \_ oggetti consentiti** o **Ads \_ AceType \_ accesso \_ negato \_**.</span><span class="sxs-lookup"><span data-stu-id="b2704-110">Set [**IADsAccessControlEntry.AceType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) to **ADS\_ACETYPE\_ACCESS\_ALLOWED\_OBJECT** or **ADS\_ACETYPE\_ACCESS\_DENIED\_OBJECT**.</span></span>
2.  <span data-ttu-id="b2704-111">Impostare [**IADsAccessControlEntry. ObjectType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) su **schemaIDGUID** dell'attributo.</span><span class="sxs-lookup"><span data-stu-id="b2704-111">Set [**IADsAccessControlEntry.ObjectType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) to the **schemaIDGUID** of the attribute.</span></span> <span data-ttu-id="b2704-112">Ad esempio, il **schemaIDGUID** dell'attributo **telephoneNumber** è {bf967a49-0de6-11D0-A285-00aa003049e2}.</span><span class="sxs-lookup"><span data-stu-id="b2704-112">For example, the **schemaIDGUID** of the **telephoneNumber** attribute is {bf967a49-0de6-11d0-a285-00aa003049e2}.</span></span>
3.  <span data-ttu-id="b2704-113">Impostare [**IADsAccessControlEntry. AceFlags**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) su **Ads \_ ACEFLAG \_ ereditare \_ ACE**.</span><span class="sxs-lookup"><span data-stu-id="b2704-113">Set [**IADsAccessControlEntry.AceFlags**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) to **ADS\_ACEFLAG\_INHERIT\_ACE**.</span></span>
4.  <span data-ttu-id="b2704-114">Impostare [**IADsAccessControlEntry. InheritedObjectType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) su **schemaIDGUID** della classe dell'oggetto che può ereditare la voce ACE.</span><span class="sxs-lookup"><span data-stu-id="b2704-114">Set [**IADsAccessControlEntry.InheritedObjectType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) to the **schemaIDGUID** of the object class that can inherit the ACE.</span></span> <span data-ttu-id="b2704-115">Ad esempio, il **schemaIDGUID** della classe **utente** è {bf967aba-0de6-11D0-A285-00aa003049e2}.</span><span class="sxs-lookup"><span data-stu-id="b2704-115">For example, the **schemaIDGUID** of the **user** class is {bf967aba-0de6-11d0-a285-00aa003049e2}.</span></span>
5.  <span data-ttu-id="b2704-116">Impostare [**IADsAccessControlEntry. Flags**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) sul **\_ tipo di oggetto flag Ads \_ \_ \_ presente** e il **\_ flag ADS ereditato il tipo di \_ \_ oggetto \_ \_ presente**.</span><span class="sxs-lookup"><span data-stu-id="b2704-116">Set [**IADsAccessControlEntry.Flags**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) to **ADS\_FLAG\_OBJECT\_TYPE\_PRESENT** and **ADS\_FLAG\_INHERITED\_OBJECT\_TYPE\_PRESENT**.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b2704-117">Set ADS \_ ACEFLAG \_ eredita \_ ACE per provocare l'ereditarietà della voce ACE.</span><span class="sxs-lookup"><span data-stu-id="b2704-117">Set ADS\_ACEFLAG\_INHERIT\_ACE to cause the ACE to be inherited.</span></span> <span data-ttu-id="b2704-118">Inoltre, set ADS \_ ACEFLAG \_ eredita \_ solo \_ ACE se il tipo di oggetto a cui si applica questa voce ACE non corrisponde al tipo di oggetto del contenitore in cui è specificata la voce ACE.</span><span class="sxs-lookup"><span data-stu-id="b2704-118">In addition, set ADS\_ACEFLAG\_INHERIT\_ONLY\_ACE if the object type this ACE applies to does not match the object type of the container where the ACE is specified.</span></span> <span data-ttu-id="b2704-119">Se questa operazione non viene eseguita, la voce ACE diventerà effettiva anche sul contenitore e potrà concedere diritti imprevisti.</span><span class="sxs-lookup"><span data-stu-id="b2704-119">If this is not done, the ACE will also become effective on the container and can grant unexpected rights.</span></span>

 

<span data-ttu-id="b2704-120">Per ulteriori informazioni ed esempi di codice che possono essere utilizzati per impostare questo tipo di voce ACE, vedere [codice di esempio per l'impostazione di una voce ACE in un oggetto directory](example-code-for-setting-an-ace-on-a-directory-object.md).</span><span class="sxs-lookup"><span data-stu-id="b2704-120">For more information and code examples that can be used to set this kind of ACE, see [Example Code for Setting an ACE on a Directory Object](example-code-for-setting-an-ace-on-a-directory-object.md).</span></span>

 

 