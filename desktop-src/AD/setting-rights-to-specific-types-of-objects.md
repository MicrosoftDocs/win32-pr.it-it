---
title: Impostazione dei diritti su tipi specifici di oggetti
description: La procedura seguente illustra come impostare una ACE che può essere ereditata solo da una classe specifica di oggetti.
ms.assetid: 42712458-69c7-4fe1-bfb3-b3fb28092a56
ms.tgt_platform: multiple
keywords:
- impostazione dei diritti per i tipi di oggetti AD
- oggetti AD, impostazione dei diritti su
- Active Directory, uso, sicurezza, impostazione dei diritti sui tipi di oggetti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d8740b4454eac5de158c826ec135a0becf6777f320e16729598187a3093f088
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118183289"
---
# <a name="setting-rights-to-specific-types-of-objects"></a>Impostazione dei diritti su tipi specifici di oggetti

La procedura seguente illustra come impostare una ACE che può essere ereditata solo da una classe specifica di oggetti.

 **Per impostare una ACE che può essere ereditata solo da una classe specifica di oggetti**

1.  Impostare la [**proprietà IADsAccessControlEntry.AceType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) su **ADS \_ ACETYPE \_ ACCESS ALLOWED \_ \_ OBJECT** o **ADS \_ ACETYPE \_ ACCESS \_ DENIED \_ OBJECT**.
2.  Impostare la [**proprietà IADsAccessControlEntry.AceFlags**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) per includere il \_ flag ACE ADS ACEFLAG \_ \_ INHERIT.
3.  Impostare la [**proprietà IADsAccessControlEntry.InheritedObjectType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) su **schemaIDGUID** della classe di oggetti che può ereditare la voce ACE.
4.  Impostare la [**proprietà IADsAccessControlEntry.Flags**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) **su ADS FLAG \_ \_ INHERITED OBJECT TYPE \_ \_ PRESENT**.

> [!IMPORTANT]
> Impostare **ADS \_ ACEFLAG \_ INHERIT \_ ACE** per fare in modo che la ACE sia ereditata. È inoltre necessario impostare **ADS \_ ACEFLAG INHERIT ONLY ACE se il tipo di oggetto a cui si applica questa \_ \_ \_ ACE** non corrisponde al tipo di oggetto del contenitore in cui è specificata la ACE. Se questa operazione non viene eseguita, la ACE diventerà effettiva anche nel contenitore e potrà concedere diritti imprevisti.

 

Per altre informazioni ed esempi di codice che possono essere usati per impostare questo tipo di ACE, vedere Codice di esempio per l'impostazione di una [ACE in un oggetto directory](example-code-for-setting-an-ace-on-a-directory-object.md).

 

 