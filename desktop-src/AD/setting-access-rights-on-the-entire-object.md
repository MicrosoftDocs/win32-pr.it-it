---
title: Impostazione dei diritti di accesso per l'intero oggetto
description: Alcune autorizzazioni possono essere impostate solo per un intero oggetto, ad esempio Elimina ed Elenca contenuto. Le autorizzazioni specifiche dell'operazione, ad esempio l'autorizzazione Lettura, possono essere impostate anche per l'intero oggetto, in modo che siano applicate a un intero oggetto.
ms.assetid: 786357f4-146e-4638-8bd6-82bc1a6640a1
ms.tgt_platform: multiple
keywords:
- Impostazione dei diritti di accesso per l'intero oggetto AD
- oggetti AD, impostazione dei diritti di accesso su
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cde06726b7333865fe2f4b87b87bec4383a3aeb1799ad6b8772142d5b9fd6eeb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119024779"
---
# <a name="setting-access-rights-on-the-entire-object"></a>Impostazione dei diritti di accesso per l'intero oggetto

Alcune autorizzazioni possono essere impostate solo per un intero oggetto, ad esempio Elimina ed Elenca contenuto. Le autorizzazioni specifiche dell'operazione, ad esempio l'autorizzazione Lettura, possono essere impostate anche per l'intero oggetto, in modo che siano applicate a un intero oggetto.

La procedura seguente può essere usata per impostare le autorizzazioni per un intero oggetto.

**Per impostare le autorizzazioni per un intero oggetto**

1.  Impostare [**IADsAccessControlEntry.AceType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) su **ADS \_ ACETYPE \_ ACCESS \_ ALLOWED** o **ADS \_ ACETYPE \_ ACCESS \_ DENIED**.
2.  Impostare [**IADsAccessControlEntry.ObjectType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) e **IADsAccessControlEntry.InheritedObjectType** su **NULL.**

Per altre informazioni su come creare una ACE, vedere [Impostazione dei diritti di accesso per un oggetto](setting-access-rights-on-an-object.md).

Per altre informazioni e un esempio di codice che può essere usato per impostare una ACE, vedere Codice di esempio per l'impostazione di una [ACE in un oggetto directory.](example-code-for-setting-an-ace-on-a-directory-object.md)

 

 