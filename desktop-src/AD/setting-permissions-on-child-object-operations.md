---
title: Impostazione delle autorizzazioni per le operazioni sugli oggetti figlio
description: Le autorizzazioni, ad esempio Create Child e Delete Child, possono anche essere concesse o negate per le operazioni su tutti i sottooggetti o i sottooggetti di una classe specifica.
ms.assetid: fe2f8939-7562-4c03-a7a9-3ac5fc3e81bb
ms.tgt_platform: multiple
keywords:
- Impostazione delle autorizzazioni per le operazioni sugli oggetti figlio AD
- oggetti AD, figlio, impostazione delle autorizzazioni per le operazioni sugli oggetti figlio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f136119d5e61ea312748d5cd64cabb8c0aee0b651d8b192519dc2d74e2045cd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119024769"
---
# <a name="setting-permissions-on-child-object-operations"></a>Impostazione delle autorizzazioni per le operazioni sugli oggetti figlio

Le autorizzazioni, ad esempio Create Child e Delete Child, possono anche essere concesse o negate per le operazioni su tutti i sottooggetti o i sottooggetti di una classe specifica.

La procedura seguente consente di impostare le autorizzazioni per un tipo di oggetto secondario specifico.

**Per impostare le autorizzazioni per un tipo di oggetto secondario specifico**

1.  Impostare la [**proprietà IADsAccessControlEntry.AceType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) su **ADS \_ ACETYPE \_ ACCESS ALLOWED \_ \_ OBJECT** o **ADS \_ ACETYPE \_ ACCESS \_ DENIED \_ OBJECT.**
2.  Impostare la [**proprietà IADsAccessControlEntry.ObjectType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) sul GUID per la classe di oggetti. Si tratta della **proprietà schemaIDGUID** dell'oggetto classSchema che definisce la classe dell'oggetto. Se la **proprietà ObjectType** è **NULL,** la ACE si applica agli oggetti secondari di qualsiasi classe.
3.  Impostare la [**proprietà IADsAccessControlEntry.Flags**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) su **ADS \_ FLAG OBJECT \_ TYPE \_ \_ PRESENT**.

Per altre informazioni e per una procedura per la creazione di una ACE, vedere [Impostazione dei diritti di accesso per un oggetto](setting-access-rights-on-an-object.md).

Per altre informazioni e un esempio di codice che può essere usato per impostare una ACE che controlla le operazioni sugli oggetti figlio, vedere Codice di esempio per l'impostazione di una [ACE](example-code-for-setting-an-ace-on-a-directory-object.md)in un oggetto directory .

 

 