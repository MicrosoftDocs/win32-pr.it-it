---
title: Impostazione dei diritti di accesso per l'intero oggetto
description: Determinate autorizzazioni possono essere impostate solo per un intero oggetto, ad esempio il contenuto Delete ed List. Le autorizzazioni specifiche dell'operazione, ad esempio l'autorizzazione di lettura, possono essere impostate anche per l'intero oggetto, in modo che vengano applicate a un intero oggetto.
ms.assetid: 786357f4-146e-4638-8bd6-82bc1a6640a1
ms.tgt_platform: multiple
keywords:
- Impostazione dei diritti di accesso per l'intero oggetto AD
- oggetti AD, impostazione dei diritti di accesso per
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9a965b646de1ee3eba40757386fd243839cb35b
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/17/2020
ms.locfileid: "104472462"
---
# <a name="setting-access-rights-on-the-entire-object"></a><span data-ttu-id="21670-106">Impostazione dei diritti di accesso per l'intero oggetto</span><span class="sxs-lookup"><span data-stu-id="21670-106">Setting Access Rights on the Entire Object</span></span>

<span data-ttu-id="21670-107">Determinate autorizzazioni possono essere impostate solo per un intero oggetto, ad esempio il contenuto Delete ed List.</span><span class="sxs-lookup"><span data-stu-id="21670-107">Certain permissions can be set only for an entire object, such as Delete and List Contents.</span></span> <span data-ttu-id="21670-108">Le autorizzazioni specifiche dell'operazione, ad esempio l'autorizzazione di lettura, possono essere impostate anche per l'intero oggetto, in modo che vengano applicate a un intero oggetto.</span><span class="sxs-lookup"><span data-stu-id="21670-108">Operation-specific permissions, such as the Read permission, can also be set for entire object so that they apply to an entire object.</span></span>

<span data-ttu-id="21670-109">È possibile utilizzare la procedura seguente per impostare le autorizzazioni per un intero oggetto.</span><span class="sxs-lookup"><span data-stu-id="21670-109">The following procedure can be used to set permissions for an entire object.</span></span>

<span data-ttu-id="21670-110">**Per impostare le autorizzazioni per un intero oggetto**</span><span class="sxs-lookup"><span data-stu-id="21670-110">**To set permissions for an entire object**</span></span>

1.  <span data-ttu-id="21670-111">Impostare [**IADsAccessControlEntry. AceType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) su **Ads \_ AceType \_ accesso \_ consentito** o **Ads \_ AceType \_ accesso \_ negato**.</span><span class="sxs-lookup"><span data-stu-id="21670-111">Set [**IADsAccessControlEntry.AceType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) to **ADS\_ACETYPE\_ACCESS\_ALLOWED** or **ADS\_ACETYPE\_ACCESS\_DENIED**.</span></span>
2.  <span data-ttu-id="21670-112">Impostare [**IADsAccessControlEntry. ObjectType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) e **IADsAccessControlEntry. InheritedObjectType** su **null**.</span><span class="sxs-lookup"><span data-stu-id="21670-112">Set [**IADsAccessControlEntry.ObjectType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) and **IADsAccessControlEntry.InheritedObjectType** to **NULL**.</span></span>

<span data-ttu-id="21670-113">Per ulteriori informazioni su come creare una voce ACE, vedere [impostazione dei diritti di accesso per un oggetto](setting-access-rights-on-an-object.md).</span><span class="sxs-lookup"><span data-stu-id="21670-113">For more information about how to create an ACE, see [Setting Access Rights on an Object](setting-access-rights-on-an-object.md).</span></span>

<span data-ttu-id="21670-114">Per ulteriori informazioni e un esempio di codice che può essere utilizzato per impostare una voce ACE, vedere il [codice di esempio per l'impostazione di una voce ACE in un oggetto directory](example-code-for-setting-an-ace-on-a-directory-object.md).</span><span class="sxs-lookup"><span data-stu-id="21670-114">For more information and a code example that can be used to set an ACE, see [Example Code for Setting an ACE on a Directory Object](example-code-for-setting-an-ace-on-a-directory-object.md).</span></span>

 

 