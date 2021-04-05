---
title: Impostazione delle autorizzazioni per una proprietà specifica
description: Le autorizzazioni possono essere impostate per applicare a una proprietà specifica di un oggetto.
ms.assetid: 7bafba5a-a437-4777-98a0-f478b738a8ca
ms.tgt_platform: multiple
keywords:
- Impostazione delle autorizzazioni per una proprietà specifica di Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99dbfc3dc682103166b41957a3f52206d84fe671
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/17/2020
ms.locfileid: "104046483"
---
# <a name="setting-permissions-to-a-specific-property"></a><span data-ttu-id="1887c-104">Impostazione delle autorizzazioni per una proprietà specifica</span><span class="sxs-lookup"><span data-stu-id="1887c-104">Setting Permissions to a Specific Property</span></span>

<span data-ttu-id="1887c-105">Le autorizzazioni possono essere impostate per applicare a una proprietà specifica di un oggetto.</span><span class="sxs-lookup"><span data-stu-id="1887c-105">Permissions can be set to apply to a specific property of an object.</span></span>

<span data-ttu-id="1887c-106">**Per impostare le autorizzazioni che si applicano a una proprietà specifica di un oggetto**</span><span class="sxs-lookup"><span data-stu-id="1887c-106">**To set permissions that apply to a specific property of an object**</span></span>

1.  <span data-ttu-id="1887c-107">Impostare la proprietà [**IADsAccessControlEntry. AccessMask**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) su **Ads \_ Rights \_ DS \_ Read \_ prop** e/o **Ads \_ Rights \_ DS \_ Write \_ prop**.</span><span class="sxs-lookup"><span data-stu-id="1887c-107">Set the [**IADsAccessControlEntry.AccessMask**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) property to **ADS\_RIGHT\_DS\_READ\_PROP** and/or **ADS\_RIGHT\_DS\_WRITE\_PROP**.</span></span>
2.  <span data-ttu-id="1887c-108">Impostare la proprietà [**IADsAccessControlEntry. AceType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) su **Ads \_ AceType \_ accesso \_ a \_ oggetti consentiti** o **Ads \_ AceType \_ accesso \_ negato \_**.</span><span class="sxs-lookup"><span data-stu-id="1887c-108">Set the [**IADsAccessControlEntry.AceType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) property to **ADS\_ACETYPE\_ACCESS\_ALLOWED\_OBJECT** or **ADS\_ACETYPE\_ACCESS\_DENIED\_OBJECT**.</span></span>
3.  <span data-ttu-id="1887c-109">Impostare la proprietà [**IADsAccessControlEntry. ObjectType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) su **schemaIDGUID** della proprietà.</span><span class="sxs-lookup"><span data-stu-id="1887c-109">Set the [**IADsAccessControlEntry.ObjectType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) property to the **schemaIDGUID** of the property.</span></span> <span data-ttu-id="1887c-110">Si tratta del **schemaIDGUID** dell'oggetto **attributeSchema** che definisce la proprietà nello schema.</span><span class="sxs-lookup"><span data-stu-id="1887c-110">This is the **schemaIDGUID** of the **attributeSchema** object that defines the property in the schema.</span></span> <span data-ttu-id="1887c-111">Il GUID deve essere specificato come una stringa del formato prodotto dalla funzione [**StringFromGUID2**](/windows/win32/api/combaseapi/nf-combaseapi-stringfromguid2) nella libreria com.</span><span class="sxs-lookup"><span data-stu-id="1887c-111">The GUID must be specified as a string of the form produced by the [**StringFromGUID2**](/windows/win32/api/combaseapi/nf-combaseapi-stringfromguid2) function in the COM library.</span></span>
4.  <span data-ttu-id="1887c-112">Impostare [**IADsAccessControlEntry. Flags**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) sul **\_ tipo di oggetto flag Ads \_ \_ \_ presente**.</span><span class="sxs-lookup"><span data-stu-id="1887c-112">Set [**IADsAccessControlEntry.Flags**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) to **ADS\_FLAG\_OBJECT\_TYPE\_PRESENT**.</span></span>

<span data-ttu-id="1887c-113">Per ulteriori informazioni sull' **schemaIDGUID** di un attributo predefinito, vedere [Active Directory Domain Services Reference](active-directory-domain-services-reference.md).</span><span class="sxs-lookup"><span data-stu-id="1887c-113">For more information about the **schemaIDGUID** of a predefined attribute, see [Active Directory Domain Services Reference](active-directory-domain-services-reference.md).</span></span>

<span data-ttu-id="1887c-114">Per ulteriori informazioni e un esempio di codice che può essere utilizzato per recuperare un schemaIDGUID, vedere [lettura di oggetti attributeSchema e classSchema](reading-attributeschema-and-classschema-objects.md).</span><span class="sxs-lookup"><span data-stu-id="1887c-114">For more information and a code example that can be used to retrieve a schemaIDGUID, see [Reading attributeSchema and classSchema Objects](reading-attributeschema-and-classschema-objects.md).</span></span>

<span data-ttu-id="1887c-115">Per ulteriori informazioni su come creare una voce ACE, vedere [impostazione dei diritti di accesso per un oggetto](setting-access-rights-on-an-object.md).</span><span class="sxs-lookup"><span data-stu-id="1887c-115">For more information about how to create an ACE, see [Setting Access Rights on an Object](setting-access-rights-on-an-object.md).</span></span>

<span data-ttu-id="1887c-116">Per ulteriori informazioni e un esempio di codice che può essere utilizzato per impostare una voce ACE specifica della proprietà, vedere [codice di esempio per l'impostazione di una voce ACE in un oggetto directory](example-code-for-setting-an-ace-on-a-directory-object.md).</span><span class="sxs-lookup"><span data-stu-id="1887c-116">For more information and a code example that can be used to set a property-specific ACE, see [Example Code for Setting an ACE on a Directory Object](example-code-for-setting-an-ace-on-a-directory-object.md).</span></span>

 

 