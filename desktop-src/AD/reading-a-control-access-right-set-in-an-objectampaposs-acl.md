---
title: Lettura di un set di diritti di accesso di controllo nell'ACL di un oggetto
description: Le proprietà dell'interfaccia IADsAccessControlEntry vengono usate per concedere o negare i diritti di accesso del controllo.
ms.assetid: 2c6fef91-990e-4954-9aff-c9ec72d13972
ms.tgt_platform: multiple
keywords:
- Lettura di un set di diritti di accesso di controllo nell'ACL di un oggetto Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4877c96a95fc94095c79ad129e8a07b1c786abe1
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/17/2020
ms.locfileid: "104046495"
---
# <a name="reading-a-control-access-right-set-in-an-objects-acl"></a>Lettura di un set di diritti di accesso di controllo nell'ACL di un oggetto

Utilizzando ADSI, è possibile leggere un controllo ACE right Access Right come qualsiasi altra voce ACE in un ACL. Tenere presente che è inoltre possibile utilizzare le API di sicurezza Win32 per leggere gli ACL negli oggetti directory. Tuttavia, i diritti di accesso di controllo usano le proprietà dell'interfaccia [**IADsAccessControlEntry**](/windows/desktop/api/iads/nn-iads-iadsaccesscontrolentry) in modo specifico per concedere e negare i diritti di accesso di controllo:

-   [**AccessMask**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) deve contenere gli **annunci di \_ \_ controllo DS Rights \_ \_ Access**.
-   Il valore di [**Flags**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) è il **tipo di \_ oggetto flag Ads \_ \_ \_ presente**.
-   [**ObjectType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) è il formato stringa dell'attributo **rightsGuid** del diritto di accesso del controllo. Il formato della stringa del GUID è lo stesso formato della stringa della funzione della libreria COM [**StringFromGUID2**](/windows/win32/api/combaseapi/nf-combaseapi-stringfromguid2) .
-   [**AceType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) è l' **\_ oggetto AceType \_ di \_ accesso \_ consentito ADS** per concedere al trustee il diritto di accesso di controllo o l' **\_ \_ \_ \_ oggetto accesso negato di ADS AceType** per negare al trustee il diritto di accesso del controllo.
-   Il [**trustee**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) è l'entità di sicurezza. ovvero l'utente, il gruppo, il computer e così via, a cui si applica la voce ACE.

Utilizzare la seguente procedura per leggere una voce ACE per un oggetto ADSI. La procedura seguente si applica alle applicazioni C e C++.

**Per leggere una voce ACE per un oggetto ADSI**

1.  Ottiene un puntatore di interfaccia [**IADs**](/windows/desktop/api/iads/nn-iads-iads) all'oggetto.
2.  Usare il metodo [**IADs:: Get**](/windows/desktop/api/iads/nf-iads-iads-get) per ottenere il descrittore di sicurezza dell'oggetto. Il nome della proprietà che contiene il descrittore di sicurezza è "nTSecurityDescriptor". La proprietà verrà restituita come **variante** che contiene un puntatore [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . Tenere presente che il membro **VT** è **VT \_ Dispatch**. Chiamare **QueryInterface** su tale puntatore **IDispatch** per ottenere un'interfaccia [**IADsSecurityDescriptor**](/windows/desktop/api/iads/nn-iads-iadssecuritydescriptor) per usare i metodi su tale interfaccia per accedere all'ACL del descrittore di sicurezza.
3.  Usare il metodo [**IADsSecurityDescriptor:: Get \_ DiscretionaryAcl**](/windows/desktop/ADSI/iadssecuritydescriptor-property-methods) per ottenere l'ACL. Il metodo restituisce un puntatore [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . Chiamare **QueryInterface** su tale puntatore **IDispatch** per ottenere un'interfaccia [**IADsAccessControlList**](/windows/desktop/api/iads/nn-iads-iadsaccesscontrollist) per usare i metodi su tale interfaccia per accedere alle singole voci ACE nell'ACL.
4.  Usare il metodo [**IADsAccessControlList:: Get \_ \_ NewEnum**](/windows/desktop/api/iads/nf-iads-iadsaccesscontrollist-get__newenum) per enumerare le voci ACE. Il metodo restituisce un puntatore [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . Chiamare **QueryInterface** su quel puntatore **IUnknown** per ottenere un'interfaccia [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) .
5.  Usare il metodo [**IEnumVARIANT:: Next**](/windows/win32/api/oaidl/nf-oaidl-ienumvariant-next) per enumerare le voci ACE nell'ACL. La proprietà viene restituita come **variante** che contiene un puntatore [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . Tenere presente che il membro **VT** è **VT \_ Dispatch**. Chiamare **QueryInterface** su tale puntatore **IDispatch** per ottenere un'interfaccia [**IADsAccessControlEntry**](/windows/desktop/api/iads/nn-iads-iadsaccesscontrolentry) per leggere la voce ACE.
6.  Chiamare il [**Metodo IADsAccessControlEntry:: Get \_ accessMask**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) per ottenere **accessMask** e verificare che il valore di **accessMask** per il flag di **\_ \_ \_ \_ accesso di controllo DS Rights ADS** . Se dispone di questo flag, la voce ACE contiene un diritto di accesso al controllo.
7.  Chiamare il metodo [**IADsAccessControlEntry:: Get \_ Flags**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) per ottenere il flag per il tipo di oggetto.
8.  Flag [**di controllo del**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) valore per il **tipo di oggetto flag ADS del flag \_ \_ \_ \_ present** . Se **Flags** è impostato **sul \_ tipo di oggetto flag Ads \_ \_ \_ presente**, chiamare il metodo **IADsAccessControlEntry:: Get \_ ObjectType** per ottenere una stringa che contiene il RightsGUID del diritto di accesso al controllo a cui si applica la voce ACE.
9.  Chiamare il metodo [**IADsAccessControlEntry:: Get \_ AceType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) per ottenere il tipo ACE. Il tipo sarà un **oggetto Ads \_ ACETYPE \_ Access \_ allowed \_** per concedere al trustee il diritto di accesso di controllo o l' **\_ oggetto ADS ACETYPE \_ accesso \_ negato \_** per negare il diritto di accesso al controllo.
10. Chiamare il metodo [**IADsAccessControlEntry:: Get \_ trustee**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) per ottenere l'entità di sicurezza, ovvero utente, gruppo, computer e così via a cui viene applicata la voce ACE.
11. Al termine delle stringhe [**ObjectType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) e **trustee** , usare [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) per liberare la memoria per tali stringhe.
12. Al termine delle interfacce, chiamare **Release** per decrementare o rilasciare tutti i riferimenti all'interfaccia.

 

 