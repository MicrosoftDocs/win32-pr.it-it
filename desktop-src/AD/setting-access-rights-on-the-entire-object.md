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
# <a name="setting-access-rights-on-the-entire-object"></a>Impostazione dei diritti di accesso per l'intero oggetto

Determinate autorizzazioni possono essere impostate solo per un intero oggetto, ad esempio il contenuto Delete ed List. Le autorizzazioni specifiche dell'operazione, ad esempio l'autorizzazione di lettura, possono essere impostate anche per l'intero oggetto, in modo che vengano applicate a un intero oggetto.

È possibile utilizzare la procedura seguente per impostare le autorizzazioni per un intero oggetto.

**Per impostare le autorizzazioni per un intero oggetto**

1.  Impostare [**IADsAccessControlEntry. AceType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) su **Ads \_ AceType \_ accesso \_ consentito** o **Ads \_ AceType \_ accesso \_ negato**.
2.  Impostare [**IADsAccessControlEntry. ObjectType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) e **IADsAccessControlEntry. InheritedObjectType** su **null**.

Per ulteriori informazioni su come creare una voce ACE, vedere [impostazione dei diritti di accesso per un oggetto](setting-access-rights-on-an-object.md).

Per ulteriori informazioni e un esempio di codice che può essere utilizzato per impostare una voce ACE, vedere il [codice di esempio per l'impostazione di una voce ACE in un oggetto directory](example-code-for-setting-an-ace-on-a-directory-object.md).

 

 