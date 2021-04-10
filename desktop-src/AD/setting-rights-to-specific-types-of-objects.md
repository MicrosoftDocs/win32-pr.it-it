---
title: Impostazione dei diritti per tipi specifici di oggetti
description: Nella procedura riportata di seguito viene illustrato come impostare una voce ACE che può essere ereditata solo da una classe specifica di oggetti.
ms.assetid: 42712458-69c7-4fe1-bfb3-b3fb28092a56
ms.tgt_platform: multiple
keywords:
- impostazione dei diritti per i tipi di oggetti AD
- oggetti AD, impostazione dei diritti su
- Active Directory, utilizzo, sicurezza, impostazione dei diritti per i tipi di oggetti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6f44cfbe753e6f92787f8269eab1f4eab4c2e98
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/17/2020
ms.locfileid: "103956300"
---
# <a name="setting-rights-to-specific-types-of-objects"></a><span data-ttu-id="9ccd8-106">Impostazione dei diritti per tipi specifici di oggetti</span><span class="sxs-lookup"><span data-stu-id="9ccd8-106">Setting Rights to Specific Types of Objects</span></span>

<span data-ttu-id="9ccd8-107">Nella procedura riportata di seguito viene illustrato come impostare una voce ACE che può essere ereditata solo da una classe specifica di oggetti.</span><span class="sxs-lookup"><span data-stu-id="9ccd8-107">The following procedure shows how to set an ACE that can be inherited only by a specific class of objects.</span></span>

 <span data-ttu-id="9ccd8-108">**Per impostare una voce ACE che può essere ereditata solo da una classe specifica di oggetti**</span><span class="sxs-lookup"><span data-stu-id="9ccd8-108">**To set an ACE that can be inherited only by a specific class of objects**</span></span>

1.  <span data-ttu-id="9ccd8-109">Impostare la proprietà [**IADsAccessControlEntry. AceType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) su **Ads \_ AceType \_ accesso \_ a \_ oggetti consentiti** o **Ads \_ AceType \_ accesso \_ negato \_**.</span><span class="sxs-lookup"><span data-stu-id="9ccd8-109">Set the [**IADsAccessControlEntry.AceType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) property to **ADS\_ACETYPE\_ACCESS\_ALLOWED\_OBJECT** or **ADS\_ACETYPE\_ACCESS\_DENIED\_OBJECT**.</span></span>
2.  <span data-ttu-id="9ccd8-110">Impostare la proprietà [**IADsAccessControlEntry. AceFlags**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) in modo da includere \_ il \_ flag ACE ACEFLAG ereditare Ads \_ .</span><span class="sxs-lookup"><span data-stu-id="9ccd8-110">Set the [**IADsAccessControlEntry.AceFlags**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) property to include the ADS\_ACEFLAG\_INHERIT\_ACE flag.</span></span>
3.  <span data-ttu-id="9ccd8-111">Impostare la proprietà [**IADsAccessControlEntry. InheritedObjectType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) su **schemaIDGUID** della classe Object che può ereditare la voce ACE.</span><span class="sxs-lookup"><span data-stu-id="9ccd8-111">Set the [**IADsAccessControlEntry.InheritedObjectType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) property to the **schemaIDGUID** of the object class that can inherit the ACE.</span></span>
4.  <span data-ttu-id="9ccd8-112">Impostare la proprietà [**IADsAccessControlEntry. Flags**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) sul **flag ADS per il tipo di \_ \_ oggetto ereditato \_ \_ presente**.</span><span class="sxs-lookup"><span data-stu-id="9ccd8-112">Set the [**IADsAccessControlEntry.Flags**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) property to **ADS\_FLAG\_INHERITED OBJECT\_TYPE\_PRESENT**.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="9ccd8-113">Set **Ads \_ ACEFLAG \_ eredita \_ ACE** per provocare l'ereditarietà della voce ACE.</span><span class="sxs-lookup"><span data-stu-id="9ccd8-113">Set **ADS\_ACEFLAG\_INHERIT\_ACE** to cause the ACE to be inherited.</span></span> <span data-ttu-id="9ccd8-114">Inoltre, è necessario impostare **Ads \_ ACEFLAG \_ solo eredita \_ \_ ACE** se il tipo di oggetto a cui si applica questa voce ACE non corrisponde al tipo di oggetto del contenitore in cui è specificata la voce ACE.</span><span class="sxs-lookup"><span data-stu-id="9ccd8-114">In addition, you must set **ADS\_ACEFLAG\_INHERIT\_ONLY\_ACE** if the object type this ACE applies to does not match the object type of the container where the ACE is specified.</span></span> <span data-ttu-id="9ccd8-115">Se questa operazione non viene eseguita, la voce ACE diventerà effettiva anche sul contenitore e potrà concedere diritti imprevisti.</span><span class="sxs-lookup"><span data-stu-id="9ccd8-115">If this is not done, the ACE will also become effective on the container and can grant unintended rights.</span></span>

 

<span data-ttu-id="9ccd8-116">Per ulteriori informazioni ed esempi di codice che possono essere utilizzati per impostare questo tipo di voce ACE, vedere [codice di esempio per l'impostazione di una voce ACE in un oggetto directory](example-code-for-setting-an-ace-on-a-directory-object.md).</span><span class="sxs-lookup"><span data-stu-id="9ccd8-116">For more information and code examples that can be used to set this type of ACE, see [Example Code for Setting an ACE on a Directory Object](example-code-for-setting-an-ace-on-a-directory-object.md).</span></span>

 

 