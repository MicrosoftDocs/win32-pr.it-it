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
# <a name="setting-permissions-on-child-object-operations"></a>Impostazione delle autorizzazioni per le operazioni oggetto figlio

È anche possibile concedere o negare le autorizzazioni, ad esempio Create Child ed Delete Child, per le operazioni su tutti gli oggetti o sottooggetti di una classe specifica.

È possibile utilizzare la procedura seguente per impostare le autorizzazioni per un tipo di oggetto specifico.

**Per impostare le autorizzazioni per un tipo di sottooggetto specifico**

1.  Impostare la proprietà [**IADsAccessControlEntry. AceType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) su **Ads \_ AceType \_ accesso \_ a \_ oggetti consentiti** o **Ads \_ AceType \_ accesso \_ negato \_**.
2.  Impostare la proprietà [**IADsAccessControlEntry. ObjectType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) sul GUID per la classe di oggetti. Si tratta della proprietà **schemaIDGUID** dell'oggetto classSchema che definisce la classe di oggetti. Se la proprietà **ObjectType** è **null**, la voce ACE si applica agli oggetti SubObject di qualsiasi classe.
3.  Impostare la proprietà [**IADsAccessControlEntry. Flags**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) sul **tipo di \_ oggetto flag Ads \_ \_ \_ presente**.

Per ulteriori informazioni e per una procedura per la creazione di una voce ACE, vedere [impostazione dei diritti di accesso per un oggetto](setting-access-rights-on-an-object.md).

Per ulteriori informazioni e un esempio di codice che può essere utilizzato per impostare una voce ACE che controlla le operazioni relative agli oggetti figlio, vedere [codice di esempio per l'impostazione di una voce ACE in un oggetto directory](example-code-for-setting-an-ace-on-a-directory-object.md).

 

 