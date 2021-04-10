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
# <a name="setting-rights-to-specific-types-of-objects"></a>Impostazione dei diritti per tipi specifici di oggetti

Nella procedura riportata di seguito viene illustrato come impostare una voce ACE che può essere ereditata solo da una classe specifica di oggetti.

 **Per impostare una voce ACE che può essere ereditata solo da una classe specifica di oggetti**

1.  Impostare la proprietà [**IADsAccessControlEntry. AceType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) su **Ads \_ AceType \_ accesso \_ a \_ oggetti consentiti** o **Ads \_ AceType \_ accesso \_ negato \_**.
2.  Impostare la proprietà [**IADsAccessControlEntry. AceFlags**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) in modo da includere \_ il \_ flag ACE ACEFLAG ereditare Ads \_ .
3.  Impostare la proprietà [**IADsAccessControlEntry. InheritedObjectType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) su **schemaIDGUID** della classe Object che può ereditare la voce ACE.
4.  Impostare la proprietà [**IADsAccessControlEntry. Flags**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) sul **flag ADS per il tipo di \_ \_ oggetto ereditato \_ \_ presente**.

> [!IMPORTANT]
> Set **Ads \_ ACEFLAG \_ eredita \_ ACE** per provocare l'ereditarietà della voce ACE. Inoltre, è necessario impostare **Ads \_ ACEFLAG \_ solo eredita \_ \_ ACE** se il tipo di oggetto a cui si applica questa voce ACE non corrisponde al tipo di oggetto del contenitore in cui è specificata la voce ACE. Se questa operazione non viene eseguita, la voce ACE diventerà effettiva anche sul contenitore e potrà concedere diritti imprevisti.

 

Per ulteriori informazioni ed esempi di codice che possono essere utilizzati per impostare questo tipo di voce ACE, vedere [codice di esempio per l'impostazione di una voce ACE in un oggetto directory](example-code-for-setting-an-ace-on-a-directory-object.md).

 

 