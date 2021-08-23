---
title: Impostazione di una ACE del diritto di accesso di controllo nell'elenco di controllo di accesso di un oggetto
description: Usando ADSI, si imposta una voce ACE del diritto di accesso di controllo esattamente come si farebbe con una voce ACE specifica della proprietà, ad eccezione del fatto che la proprietà IADsAccessControlEntry.ObjectType è il rightsGUID del diritto di accesso del controllo.
ms.assetid: 454dc372-47b0-457d-8660-644fcfa59be8
ms.tgt_platform: multiple
keywords:
- Impostazione di una ACE del diritto di accesso di controllo nell'elenco di controllo di accesso di un oggetto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 09f4a4406bfa3d16a3e3be228bf4a0f131d77ad68cb99a6b9b2a8d328f15215e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119024809"
---
# <a name="setting-a-control-access-right-ace-in-an-objects-acl"></a>Impostazione di una ACE del diritto di accesso di controllo nell'elenco di controllo di accesso di un oggetto

Usando ADSI, si imposta una voce ACE del diritto di accesso di controllo esattamente come si farebbe con una voce ACE specifica della proprietà, ad eccezione del fatto che la proprietà [**IADsAccessControlEntry.ObjectType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) è il **rightsGUID** del diritto di accesso del controllo. Tenere presente che è anche possibile usare le API di sicurezza Win32 per impostare gli ACL sugli oggetti directory.

Nella tabella seguente sono elencate [**le proprietà IADsAccessControlEntry**](/windows/desktop/api/iads/nn-iads-iadsaccesscontrolentry) per il controllo dei diritti di accesso che possono essere usate per impostare le proprietà per una voce ACE.



| Proprietà                                                       | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|----------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Accessmask**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) | Per controllare i diritti di accesso che controllano l'accesso con diritti estesi a operazioni speciali, AccessMask deve contenere il flag **ADS \_ RIGHT \_ DS \_ CONTROL \_ ACCESS.** Per controllare i diritti di accesso che definiscono un set di proprietà, AccessMask contiene **ADS \_ RIGHT \_ DS \_ READ \_ PROP** e/o **ADS RIGHT \_ \_ DS WRITE \_ \_ PROP**.<br/> Per controllare i diritti di accesso che controllano le scritture convalidate, [**AccessMask**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) contiene **ADS \_ RIGHT \_ DS \_ SELF.**<br/> |
| [**Bandiere**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods)      | Questo valore deve includere il flag **ADS \_ FLAG OBJECT \_ TYPE \_ \_ PRESENT.**                                                                                                                                                                                                                                                                                                                                                                                                                       |
| [**ObjectType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) | Questo valore deve essere il [**formato StringFromGUID2**](/windows/win32/api/combaseapi/nf-combaseapi-stringfromguid2) dell'attributo **rightsGUID** del diritto di accesso di controllo. Tenere presente che, in una ACE, la stringa GUID deve includere le parentesi graffe iniziale e di terminazione anche se l'attributo **rightsGUID** dell'oggetto **controlAccessRight** non include le parentesi graffe.                                                                                                                                     |
| [**AceType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods)    | **ADS \_ ACETYPE \_ ACCESS \_ ALLOWED \_ OBJECT** per concedere al trustee il diritto di controllo di accesso o **ADS \_ ACETYPE \_ ACCESS \_ DENIED \_ OBJECT** per negare al trustee il diritto di accesso di controllo.                                                                                                                                                                                                                                                                                                     |
| [**Fiduciario**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods)    | Entità di sicurezza, ad esempio utente, gruppo, computer e così via, a cui si applica la ACE.                                                                                                                                                                                                                                                                                                                                                                                              |



 

Per altre informazioni sulla creazione di una ACE, vedere [Impostazione dei diritti di accesso per un oggetto](setting-access-rights-on-an-object.md).

Per altre informazioni e un esempio di codice per l'impostazione di una ACE, vedere Codice di esempio per l'impostazione di una [ACE in un oggetto directory](example-code-for-setting-an-ace-on-a-directory-object.md).

 

