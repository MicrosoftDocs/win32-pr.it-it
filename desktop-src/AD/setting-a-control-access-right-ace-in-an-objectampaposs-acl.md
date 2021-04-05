---
title: Impostazione di un controllo ACE destro per l'accesso a un controllo nell'ACL di un oggetto
description: Con ADSI è possibile impostare un controllo ACE Rights Access Right come si farebbe con una voce ACE specifica della proprietà, ad eccezione del fatto che la proprietà IADsAccessControlEntry. ObjectType è il rightsGUID del diritto di accesso del controllo.
ms.assetid: 454dc372-47b0-457d-8660-644fcfa59be8
ms.tgt_platform: multiple
keywords:
- Impostazione di un controllo ACE destro per l'accesso a un controllo nell'ACL di un oggetto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f41b870ad3ed5432060fb51fe14c29a81ce4665
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/17/2020
ms.locfileid: "103956303"
---
# <a name="setting-a-control-access-right-ace-in-an-objects-acl"></a>Impostazione di un controllo ACE destro per l'accesso a un controllo nell'ACL di un oggetto

Con ADSI è possibile impostare un controllo ACE Rights Access Right come si farebbe con una voce ACE specifica della proprietà, ad eccezione del fatto che la proprietà [**IADsAccessControlEntry. ObjectType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) è il **rightsGuid** del diritto di accesso del controllo. Tenere presente che è inoltre possibile utilizzare le API di sicurezza Win32 per impostare gli ACL sugli oggetti directory.

Nella tabella seguente sono elencate le proprietà di [**IADsAccessControlEntry**](/windows/desktop/api/iads/nn-iads-iadsaccesscontrolentry) per i diritti di accesso di controllo che possono essere utilizzati per impostare le proprietà di una voce ACE.



| Proprietà                                                       | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|----------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AccessMask**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) | Per i diritti di accesso di controllo che controllano l'accesso ai diritti estesi alle operazioni speciali, AccessMask deve contenere il flag di **\_ \_ \_ \_ accesso di controllo DS Rights ADS** . Per i diritti di accesso di controllo che definiscono un set di proprietà, AccessMask contiene **Ads \_ Rights \_ DS \_ Read \_ prop** e/o **Ads \_ Rights DS \_ \_ Write \_ prop**.<br/> Per i diritti di accesso di controllo che controllano le scritture convalidate, [**accessMask**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) contiene **Ads \_ right \_ DS \_ self**.<br/> |
| [**Bandiere**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods)      | Questo valore deve includere il flag di **\_ \_ \_ tipo oggetto \_ flag ADS** .                                                                                                                                                                                                                                                                                                                                                                                                                       |
| [**ObjectType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) | Questo valore deve essere il formato [**StringFromGUID2**](/windows/win32/api/combaseapi/nf-combaseapi-stringfromguid2) dell'attributo **rightsGuid** del diritto di accesso del controllo. Tenere presente che, in una voce ACE, la stringa GUID deve includere le parentesi graffe iniziale e terminante anche se l'attributo **rightsGuid** dell'oggetto **controlAccessRight** non include le parentesi graffe.                                                                                                                                     |
| [**AceType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods)    | **Ads \_ ACETYPE \_ accesso consentito all' \_ \_ oggetto** per concedere al trustee il diritto di controllo di accesso o **Ads \_ ACETYPE \_ accesso \_ negato \_** per negare al trustee il diritto di accesso al controllo.                                                                                                                                                                                                                                                                                                     |
| [**Fiduciario**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods)    | Entità di sicurezza, ad esempio utente, gruppo, computer e così via, a cui si applica la voce ACE.                                                                                                                                                                                                                                                                                                                                                                                              |



 

Per ulteriori informazioni sulla creazione di una voce ACE, vedere [impostazione dei diritti di accesso per un oggetto](setting-access-rights-on-an-object.md).

Per ulteriori informazioni e un esempio di codice per l'impostazione di una voce ACE, vedere [il codice di esempio per l'impostazione di una voce ACE in un oggetto directory](example-code-for-setting-an-ace-on-a-directory-object.md).

 

