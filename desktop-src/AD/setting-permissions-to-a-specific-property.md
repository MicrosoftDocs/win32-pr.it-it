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
# <a name="setting-permissions-to-a-specific-property"></a>Impostazione delle autorizzazioni per una proprietà specifica

Le autorizzazioni possono essere impostate per applicare a una proprietà specifica di un oggetto.

**Per impostare le autorizzazioni che si applicano a una proprietà specifica di un oggetto**

1.  Impostare la proprietà [**IADsAccessControlEntry. AccessMask**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) su **Ads \_ Rights \_ DS \_ Read \_ prop** e/o **Ads \_ Rights \_ DS \_ Write \_ prop**.
2.  Impostare la proprietà [**IADsAccessControlEntry. AceType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) su **Ads \_ AceType \_ accesso \_ a \_ oggetti consentiti** o **Ads \_ AceType \_ accesso \_ negato \_**.
3.  Impostare la proprietà [**IADsAccessControlEntry. ObjectType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) su **schemaIDGUID** della proprietà. Si tratta del **schemaIDGUID** dell'oggetto **attributeSchema** che definisce la proprietà nello schema. Il GUID deve essere specificato come una stringa del formato prodotto dalla funzione [**StringFromGUID2**](/windows/win32/api/combaseapi/nf-combaseapi-stringfromguid2) nella libreria com.
4.  Impostare [**IADsAccessControlEntry. Flags**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) sul **\_ tipo di oggetto flag Ads \_ \_ \_ presente**.

Per ulteriori informazioni sull' **schemaIDGUID** di un attributo predefinito, vedere [Active Directory Domain Services Reference](active-directory-domain-services-reference.md).

Per ulteriori informazioni e un esempio di codice che può essere utilizzato per recuperare un schemaIDGUID, vedere [lettura di oggetti attributeSchema e classSchema](reading-attributeschema-and-classschema-objects.md).

Per ulteriori informazioni su come creare una voce ACE, vedere [impostazione dei diritti di accesso per un oggetto](setting-access-rights-on-an-object.md).

Per ulteriori informazioni e un esempio di codice che può essere utilizzato per impostare una voce ACE specifica della proprietà, vedere [codice di esempio per l'impostazione di una voce ACE in un oggetto directory](example-code-for-setting-an-ace-on-a-directory-object.md).

 

 