---
title: Creazione di descrittori di sicurezza per i nuovi oggetti directory
description: È possibile utilizzare ADSI per creare un descrittore di sicurezza e impostarlo come proprietà nTSecurityDescriptor di un nuovo oggetto o utilizzarlo per sostituire la proprietà nTSecurityDescriptor di un oggetto esistente.
ms.assetid: b9ff626f-17f1-4fc1-9d6e-4f47e29a5aeb
ms.tgt_platform: multiple
keywords:
- Creazione di un descrittore di sicurezza per un nuovo oggetto directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78265d27c52023d669e27fc9890fd2d5273e2ffd
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/17/2020
ms.locfileid: "104472627"
---
# <a name="creating-security-descriptors-for-new-directory-objects"></a>Creazione di descrittori di sicurezza per i nuovi oggetti directory

È possibile utilizzare ADSI per creare un descrittore di sicurezza e impostarlo come proprietà **ntSecurityDescriptor** di un nuovo oggetto o utilizzarlo per sostituire la proprietà **ntSecurityDescriptor** di un oggetto esistente.

Per creare un descrittore di sicurezza per un oggetto:

1.  Utilizzare [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) per creare l'oggetto ADSI com per il nuovo descrittore di sicurezza e ottenere un puntatore di interfaccia [**IADsSecurityDescriptor**](/windows/desktop/api/iads/nn-iads-iadssecuritydescriptor) a tale oggetto. Tenere presente che l'ID di classe è **CLSID \_ securityDescriptor**.
2.  Usare il metodo [**IADsSecurityDescriptor::p UT \_ owner**](/windows/desktop/ADSI/iadssecuritydescriptor-property-methods) per impostare il proprietario dell'oggetto. Il fiduciario è un utente, un gruppo o un'altra entità di sicurezza. Un'applicazione deve usare il valore della proprietà appropriata dall'oggetto utente o gruppo del trustee a cui applicare la voce ACE.
3.  Usare il metodo [**IADsSecurityDescriptor::p UT \_ Control**](/windows/desktop/ADSI/iadssecuritydescriptor-property-methods) per controllare se i DACL e i SACL vengono ereditati dall'oggetto dal relativo contenitore padre.
4.  Utilizzare [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) per creare l'oggetto ADSI com per l'elenco DACL per il nuovo descrittore di sicurezza e ottenere un puntatore di interfaccia [**IADsAccessControlList**](/windows/desktop/api/iads/nn-iads-iadsaccesscontrollist) a tale oggetto. Tenere presente che l'ID di classe è **CLSID \_ AccessControlList**.
5.  Per ogni voce ACE da aggiungere all'elenco DACL, utilizzare [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) per creare l'oggetto ADSI com per la nuova voce ACE e ottenere un puntatore di interfaccia [**IADsAccessControlEntry**](/windows/desktop/api/iads/nn-iads-iadsaccesscontrolentry) a tale oggetto. Tenere presente che l'ID di classe è CLSID \_ AccessControlEntry.
6.  Per ogni voce ACE da aggiungere all'elenco DACL, impostare le proprietà della voce ACE usando i metodi della proprietà dell'oggetto [**IADsAccessControlEntry**](/windows/desktop/api/iads/nn-iads-iadsaccesscontrolentry) della voce ACE. Per ulteriori informazioni sulle proprietà da impostare in una voce ACE, vedere [impostazione dei diritti di accesso per un oggetto](setting-access-rights-on-an-object.md).
7.  Per ogni voce ACE da aggiungere all'elenco DACL, usare il metodo **QueryInterface** sull'oggetto [**IADsAccessControlEntry**](/windows/desktop/api/iads/nn-iads-iadsaccesscontrolentry) per ottenere un puntatore [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . Il metodo [**IADsAccessControlList:: AddAce**](/windows/desktop/api/iads/nf-iads-iadsaccesscontrollist-addace) richiede un puntatore di interfaccia **IDispatch** alla voce ACE.
8.  Per ogni voce ACE da aggiungere all'elenco DACL, utilizzare [**IADsAccessControlList:: AddAce**](/windows/desktop/api/iads/nf-iads-iadsaccesscontrollist-addace) per aggiungere la nuova voce ACE all'elenco DACL. Tenere presente che l'ordine delle voci ACE nell'ACL può influire sulla valutazione dell'accesso all'oggetto. Per accedere correttamente all'oggetto, potrebbe essere necessario creare un nuovo ACL, aggiungere le voci ACE dall'ACL esistente nell'ordine corretto al nuovo ACL, quindi sostituire l'ACL esistente nel descrittore di sicurezza con il nuovo ACL. Per ulteriori informazioni, vedere [Order of ACE in a DACL](/windows/desktop/SecAuthZ/order-of-aces-in-a-dacl).
9.  Seguire i passaggi 4-8 per creare il SACL per il nuovo descrittore di sicurezza.
10. Usare il metodo [**IADsSecurityDescriptor::p UT \_ DiscretionaryAcl**](/windows/desktop/ADSI/iadssecuritydescriptor-property-methods) per impostare l'elenco DACL. Per ulteriori informazioni sugli elenchi DACL, vedere [DACL null e elenchi DACL vuoti](null-dacls-and-empty-dacls.md).
11. Usare il metodo [**IADsSecurityDescriptor::p UT \_ SystemAcl**](/windows/desktop/ADSI/iadssecuritydescriptor-property-methods) per impostare il SACL.
12. Convertire l'oggetto [**IADsSecurityDescriptor**](/windows/desktop/api/iads/nn-iads-iadssecuritydescriptor) in una [**variante**](/windows/win32/api/oaidl/ns-oaidl-variant) usando il metodo **QueryInterface** dell'oggetto **IADsSecurityDescriptor** per ottenere un'interfaccia [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . Impostare quindi il membro **VT** della **variante** su **VT \_ Dispatch** e impostare il membro **pdispVal** della **variante** uguale al puntatore **IDispatch** .
13. Ottenere un puntatore di interfaccia [**IADs**](/windows/desktop/api/iads/nn-iads-iads) all'oggetto.
14. Usare il metodo [**IADs::P UT**](/windows/desktop/api/iads/nf-iads-iads-put) con "ntSecurityDescriptor" e la [**variante**](/windows/win32/api/oaidl/ns-oaidl-variant) creata in precedenza per scrivere il nuovo descrittore di sicurezza nella cache delle proprietà.
15. Usare il metodo [**IADs:: SetInfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo) per aggiornare la proprietà nell'oggetto nella directory.

 

 