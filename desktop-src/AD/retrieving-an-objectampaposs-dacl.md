---
title: Recupero del DACL di un oggetto
description: Il descrittore di sicurezza di un oggetto può contenere un elenco di controllo di accesso discrezionale (DACL).
ms.assetid: 93b16094-9923-4886-804f-4e989fbf6977
ms.tgt_platform: multiple
keywords:
- ANNUNCIO DACL
- DACL AD, recupero del DACL di un oggetto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3db74cb235b5cb322f0edf3dc4cfb32f50b4c00c
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/17/2020
ms.locfileid: "104336774"
---
# <a name="retrieving-an-objects-dacl"></a>Recupero del DACL di un oggetto

Il descrittore di sicurezza di un oggetto può contenere un elenco di controllo di accesso discrezionale (DACL). Un DACL contiene zero o più voci di controllo di accesso (ACE) che identificano gli utenti e i gruppi che possono accedere all'oggetto. Se un DACL è vuoto (ovvero contiene zero assi), nessun accesso viene concesso in modo esplicito, quindi l'accesso viene negato in modo implicito. Tuttavia, se il descrittore di sicurezza di un oggetto non dispone di un DACL, l'oggetto non è protetto e tutti hanno accesso completo.

Per recuperare l'elenco DACL di un oggetto, è necessario essere il proprietario dell'oggetto o avere accesso in **lettura al \_ controllo** dell'oggetto.

Per ottenere e impostare l'elenco DACL di un oggetto directory, utilizzare l'interfaccia [**IADsSecurityDescriptor**](/windows/desktop/api/iads/nn-iads-iadssecuritydescriptor) . Con C++, il metodo [**IADsSecurityDescriptor:: Get \_ DiscretionaryAcl**](/windows/desktop/ADSI/iadssecuritydescriptor-property-methods) restituisce un puntatore [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . Chiamare **QueryInterface** su tale puntatore **IDispatch** per ottenere un'interfaccia [**IADsAccessControlList**](/windows/desktop/api/iads/nn-iads-iadsaccesscontrollist) e usare i metodi su tale interfaccia per accedere alle singole voci ACE nell'elenco DACL. La procedura per la modifica di un DACL è descritta in [impostazione dei diritti di accesso per un oggetto](setting-access-rights-on-an-object.md).

Per enumerare le voci ACE, usare il metodo [**IADsAccessControlList:: Get \_ \_ NewEnum**](/windows/desktop/api/iads/nf-iads-iadsaccesscontrollist-get__newenum) . Il metodo restituisce un puntatore [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . Chiamare **QueryInterface** su quel puntatore **IUnknown** per ottenere un'interfaccia [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) . Usare il metodo [**IEnumVARIANT:: Next**](/windows/win32/api/oaidl/nf-oaidl-ienumvariant-next) per enumerare le voci ACE nell'ACL. Ogni voce ACE viene restituita come **variante** contenente un puntatore [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) (il membro **VT** è **VT \_ Dispatch**). Chiamare **QueryInterface** su tale puntatore **IDispatch** per ottenere un'interfaccia [**IADsAccessControlEntry**](/windows/desktop/api/iads/nn-iads-iadsaccesscontrolentry) per la voce ACE. È possibile utilizzare i metodi dell'interfaccia **IADsAccessControlEntry** per impostare o recuperare i componenti di una voce ACE.

Per ulteriori informazioni sugli elenchi DACL e le voci ACE, vedere gli argomenti seguenti nel Software Development Kit (SDK) della piattaforma.

-   [Elenchi di controllo di accesso (ACL)](/windows/desktop/SecAuthZ/access-control-lists)
-   [Voci di controllo di accesso (ACE)](/windows/desktop/SecAuthZ/access-control-entries)

 

 