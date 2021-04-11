---
title: Recupero del SACL di un oggetto
description: Il descrittore di sicurezza di un oggetto in Active Directory Domain Services può contenere un elenco di controllo di accesso di sistema (SACL).
ms.assetid: b1da91a2-d9b0-48a3-9de5-1e588209032d
ms.tgt_platform: multiple
keywords:
- AD SACL
- SACL AD, recupero del SACL di un oggetto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 537846f2080aecdab8e22f5fce5bdfa36298fb74
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/17/2020
ms.locfileid: "104336775"
---
# <a name="retrieving-an-objects-sacl"></a>Recupero del SACL di un oggetto

Il descrittore di sicurezza di un oggetto in Active Directory Domain Services può contenere un elenco di controllo di accesso di sistema (SACL). Un SACL contiene voci di controllo di accesso (ACE) che specificano i tipi di tentativi di accesso che generano record di controllo nel registro eventi di protezione di un controller di dominio. Tenere presente che un SACL genera voci di log solo sul controller di dominio in cui si è verificato il tentativo di accesso, non su ogni controller di dominio che contiene una replica dell'oggetto.

Per impostare o ottenere l'elenco SACL dal descrittore di sicurezza di un oggetto, il privilegio di **\_ sicurezza del \_ nome se** deve essere abilitato nel token di accesso del thread richiedente. Il gruppo Administrators dispone di questo privilegio per impostazione predefinita e può essere assegnato ad altri utenti o gruppi. Per ulteriori informazioni, vedere il [diritto di accesso SACL](/windows/desktop/SecAuthZ/sacl-access-right).

Per ottenere e impostare l'elenco SACL di un oggetto directory, usare l'interfaccia [**IADsSecurityDescriptor**](/windows/desktop/api/iads/nn-iads-iadssecuritydescriptor) . Con C++, il metodo [**IADsSecurityDescriptor:: Get \_ SystemAcl**](/windows/desktop/ADSI/iadssecuritydescriptor-property-methods) restituisce un puntatore [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . Chiamare **QueryInterface** su tale puntatore **IDispatch** per ottenere un'interfaccia [**IADsAccessControlList**](/windows/desktop/api/iads/nn-iads-iadsaccesscontrollist) e usare i metodi su tale interfaccia per accedere alle singole voci ACE nell'elenco SACL. Per ulteriori informazioni sulla procedura per la modifica di un SACL, che è simile a quello per la modifica di un DACL, vedere [impostazione dei diritti di accesso per un oggetto](setting-access-rights-on-an-object.md).

Per enumerare le voci ACE in un SACL, usare il metodo [**IADsAccessControlList:: Get \_ \_ NewEnum**](/windows/desktop/api/iads/nf-iads-iadsaccesscontrollist-get__newenum) , che restituisce un puntatore [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . Chiamare **QueryInterface** su quel puntatore **IUnknown** per ottenere un'interfaccia [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) . Usare il metodo [**IEnumVARIANT:: Next**](/windows/win32/api/oaidl/nf-oaidl-ienumvariant-next) per enumerare le voci ACE nell'ACL. Ogni voce ACE viene restituita come **variante** che contiene un puntatore [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) ; tenere presente che il membro **VT** è **VT \_ Dispatch**. Chiamare **QueryInterface** su tale puntatore **IDispatch** per ottenere un'interfaccia [**IADsAccessControlEntry**](/windows/desktop/api/iads/nn-iads-iadsaccesscontrolentry) per la voce ACE. Usare i metodi dell'interfaccia **IADsAccessControlEntry** per impostare o ottenere i componenti di una voce ACE.

Per ulteriori informazioni sui SACL, vedere:

-   [Elenchi di controllo di accesso (ACL)](/windows/desktop/SecAuthZ/access-control-lists)
-   [Generazione di controllo](/windows/desktop/SecAuthZ/audit-generation)

 

 