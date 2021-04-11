---
title: Impostazione delle autorizzazioni per le operazioni oggetto figlio
description: È anche possibile concedere o negare le autorizzazioni, ad esempio Create Child ed Delete Child, per le operazioni su tutti gli oggetti o sottooggetti di una classe specifica.
ms.assetid: fe2f8939-7562-4c03-a7a9-3ac5fc3e81bb
ms.tgt_platform: multiple
keywords:
- Impostazione delle autorizzazioni per le operazioni dell'oggetto figlio AD
- oggetti AD, Child, impostazione delle autorizzazioni per le operazioni di oggetti figlio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d407e9b0db865c5df8d5dab53bd97f9f1afa1497
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/17/2020
ms.locfileid: "104117530"
---
# <a name="setting-permissions-on-child-object-operations"></a><span data-ttu-id="7764c-105">Impostazione delle autorizzazioni per le operazioni oggetto figlio</span><span class="sxs-lookup"><span data-stu-id="7764c-105">Setting Permissions on Child Object Operations</span></span>

<span data-ttu-id="7764c-106">È anche possibile concedere o negare le autorizzazioni, ad esempio Create Child ed Delete Child, per le operazioni su tutti gli oggetti o sottooggetti di una classe specifica.</span><span class="sxs-lookup"><span data-stu-id="7764c-106">Permissions, such as Create Child and Delete Child, can also be granted or denied for operations on all subobjects or subobjects of a specific class.</span></span>

<span data-ttu-id="7764c-107">È possibile utilizzare la procedura seguente per impostare le autorizzazioni per un tipo di oggetto specifico.</span><span class="sxs-lookup"><span data-stu-id="7764c-107">The following procedure can be used to set permissions for a specific subobject type.</span></span>

<span data-ttu-id="7764c-108">**Per impostare le autorizzazioni per un tipo di sottooggetto specifico**</span><span class="sxs-lookup"><span data-stu-id="7764c-108">**To set permissions for a specific subobject type**</span></span>

1.  <span data-ttu-id="7764c-109">Impostare la proprietà [**IADsAccessControlEntry. AceType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) su **Ads \_ AceType \_ accesso \_ a \_ oggetti consentiti** o **Ads \_ AceType \_ accesso \_ negato \_**.</span><span class="sxs-lookup"><span data-stu-id="7764c-109">Set the [**IADsAccessControlEntry.AceType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) property to **ADS\_ACETYPE\_ACCESS\_ALLOWED\_OBJECT** or **ADS\_ACETYPE\_ACCESS\_DENIED\_OBJECT**.</span></span>
2.  <span data-ttu-id="7764c-110">Impostare la proprietà [**IADsAccessControlEntry. ObjectType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) sul GUID per la classe di oggetti.</span><span class="sxs-lookup"><span data-stu-id="7764c-110">Set the [**IADsAccessControlEntry.ObjectType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) property to the GUID for object class.</span></span> <span data-ttu-id="7764c-111">Si tratta della proprietà **schemaIDGUID** dell'oggetto classSchema che definisce la classe di oggetti.</span><span class="sxs-lookup"><span data-stu-id="7764c-111">This is the **schemaIDGUID** property of the classSchema object that defines the object class.</span></span> <span data-ttu-id="7764c-112">Se la proprietà **ObjectType** è **null**, la voce ACE si applica agli oggetti SubObject di qualsiasi classe.</span><span class="sxs-lookup"><span data-stu-id="7764c-112">If the **ObjectType** property is **NULL**, the ACE applies to subobjects of any class.</span></span>
3.  <span data-ttu-id="7764c-113">Impostare la proprietà [**IADsAccessControlEntry. Flags**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) sul **tipo di \_ oggetto flag Ads \_ \_ \_ presente**.</span><span class="sxs-lookup"><span data-stu-id="7764c-113">Set the [**IADsAccessControlEntry.Flags**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) property to **ADS\_FLAG\_OBJECT\_TYPE\_PRESENT**.</span></span>

<span data-ttu-id="7764c-114">Per ulteriori informazioni e per una procedura per la creazione di una voce ACE, vedere [impostazione dei diritti di accesso per un oggetto](setting-access-rights-on-an-object.md).</span><span class="sxs-lookup"><span data-stu-id="7764c-114">For more information and a procedure for creating an ACE, see [Setting Access Rights on an Object](setting-access-rights-on-an-object.md).</span></span>

<span data-ttu-id="7764c-115">Per ulteriori informazioni e un esempio di codice che può essere utilizzato per impostare una voce ACE che controlla le operazioni relative agli oggetti figlio, vedere [codice di esempio per l'impostazione di una voce ACE in un oggetto directory](example-code-for-setting-an-ace-on-a-directory-object.md).</span><span class="sxs-lookup"><span data-stu-id="7764c-115">For more information and a code example that can be used to set an ACE that controls child object operations, see [Example Code for Setting an ACE on a Directory Object](example-code-for-setting-an-ace-on-a-directory-object.md).</span></span>

 

 