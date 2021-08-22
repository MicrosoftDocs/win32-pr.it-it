---
title: Impostazione dei diritti su proprietà specifiche di tipi specifici di oggetti
description: Le autorizzazioni specifiche della proprietà possono essere usate in combinazione con l'ereditarietà specifica dell'oggetto per fornire la delega potente e dettagliata dell'amministrazione.
ms.assetid: d2ebbe3a-78f7-4bb5-bac0-13236031b7b1
ms.tgt_platform: multiple
keywords:
- impostazione dei diritti su proprietà specifiche di tipi specifici di oggetti AD
- Active Directory, uso, sicurezza, impostazione dei diritti su proprietà specifiche
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86c01070b5c5b23e7524bd3b54293576e578861e0120b431e6dc95b7a5b4cc4b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119024739"
---
# <a name="setting-rights-to-specific-properties-of-specific-types-of-objects"></a>Impostazione dei diritti su proprietà specifiche di tipi specifici di oggetti

Le autorizzazioni specifiche della proprietà possono essere usate in combinazione con l'ereditarietà specifica dell'oggetto per fornire la delega potente e dettagliata dell'amministrazione. È possibile impostare una ACE ereditabile da un oggetto specifico della proprietà per consentire a un utente o a un gruppo specificato di leggere e/o scrivere un attributo specifico in una classe specificata di oggetti figlio in un contenitore. Ad esempio, è possibile impostare una voce ACE in un'unità organizzativa (OU) per consentire a un gruppo di leggere e scrivere l'attributo del numero di telefono di tutti gli oggetti utente nell'unità organizzativa.

**Per impostare ACE ereditabili da oggetti specifiche della proprietà**

1.  Impostare [**IADsAccessControlEntry.AceType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) su **ADS \_ ACETYPE \_ ACCESS ALLOWED \_ \_ OBJECT** o **ADS \_ ACETYPE \_ ACCESS \_ DENIED \_ OBJECT**.
2.  Impostare [**IADsAccessControlEntry.ObjectType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) sullo **schemaIDGUID** dell'attributo. Ad esempio, **lo schemaIDGUID** dell'attributo **telephoneNumber** è {bf967a49-0de6-11d0-a285-00aa003049e2}.
3.  Impostare [**IADsAccessControlEntry.AceFlags**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) su **ADS \_ ACEFLAG \_ INHERIT \_ ACE**.
4.  Impostare [**IADsAccessControlEntry.InheritedObjectType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) sullo **schemaIDGUID** della classe di oggetti che può ereditare la voce ACE. Ad esempio, **schemaIDGUID** della classe **utente** è {bf967aba-0de6-11d0-a285-00aa003049e2}.
5.  Impostare [**IADsAccessControlEntry.Flags**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) **su ADS FLAG OBJECT TYPE \_ \_ \_ \_ PRESENT** e **ADS FLAG \_ \_ INHERITED OBJECT TYPE \_ \_ \_ PRESENT**.

> [!IMPORTANT]
> Impostare ADS \_ ACEFLAG INHERIT ACE per fare in modo che la \_ \_ ACE sia ereditata. Inoltre, impostare ADS ACEFLAG INHERIT ONLY ACE se il tipo di oggetto a cui si applica questa ACE non corrisponde al tipo di oggetto del contenitore in cui è specificata \_ \_ la \_ \_ ACE. Se questa operazione non viene eseguita, la ACE diventerà effettiva anche nel contenitore e potrà concedere diritti imprevisti.

 

Per altre informazioni ed esempi di codice che possono essere usati per impostare questo tipo di ACE, vedere Codice di esempio per l'impostazione di una [ACE in un oggetto directory.](example-code-for-setting-an-ace-on-a-directory-object.md)

 

 