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
# <a name="setting-rights-to-specific-properties-of-specific-types-of-objects"></a>Impostazione dei diritti per proprietà specifiche di tipi specifici di oggetti

Le autorizzazioni specifiche della proprietà possono essere utilizzate in combinazione con l'ereditarietà specifica dell'oggetto per fornire la delega avanzata e dettagliata dell'amministrazione. È possibile impostare una voce ACE ereditabile da un oggetto specifico della proprietà per consentire a un utente o a un gruppo specificato di leggere e/o scrivere un attributo specifico in una classe specificata di oggetti figlio in un contenitore. Ad esempio, è possibile impostare una voce ACE in un'unità organizzativa (OU) per consentire a un gruppo di leggere e scrivere l'attributo del numero di telefono di tutti gli oggetti utente nell'unità organizzativa.

**Per impostare ACE ereditabili da oggetti specifici della proprietà**

1.  Impostare [**IADsAccessControlEntry. AceType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) su **Ads \_ AceType \_ accesso \_ a \_ oggetti consentiti** o **Ads \_ AceType \_ accesso \_ negato \_**.
2.  Impostare [**IADsAccessControlEntry. ObjectType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) su **schemaIDGUID** dell'attributo. Ad esempio, il **schemaIDGUID** dell'attributo **telephoneNumber** è {bf967a49-0de6-11D0-A285-00aa003049e2}.
3.  Impostare [**IADsAccessControlEntry. AceFlags**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) su **Ads \_ ACEFLAG \_ ereditare \_ ACE**.
4.  Impostare [**IADsAccessControlEntry. InheritedObjectType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) su **schemaIDGUID** della classe dell'oggetto che può ereditare la voce ACE. Ad esempio, il **schemaIDGUID** della classe **utente** è {bf967aba-0de6-11D0-A285-00aa003049e2}.
5.  Impostare [**IADsAccessControlEntry. Flags**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) sul **\_ tipo di oggetto flag Ads \_ \_ \_ presente** e il **\_ flag ADS ereditato il tipo di \_ \_ oggetto \_ \_ presente**.

> [!IMPORTANT]
> Set ADS \_ ACEFLAG \_ eredita \_ ACE per provocare l'ereditarietà della voce ACE. Inoltre, set ADS \_ ACEFLAG \_ eredita \_ solo \_ ACE se il tipo di oggetto a cui si applica questa voce ACE non corrisponde al tipo di oggetto del contenitore in cui è specificata la voce ACE. Se questa operazione non viene eseguita, la voce ACE diventerà effettiva anche sul contenitore e potrà concedere diritti imprevisti.

 

Per ulteriori informazioni ed esempi di codice che possono essere utilizzati per impostare questo tipo di voce ACE, vedere [codice di esempio per l'impostazione di una voce ACE in un oggetto directory](example-code-for-setting-an-ace-on-a-directory-object.md).

 

 