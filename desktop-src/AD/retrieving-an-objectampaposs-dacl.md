---
title: Recupero dell'elenco DACL di un oggetto
description: Il descrittore di sicurezza di un oggetto può contenere un elenco di controllo di accesso discrezionale (DACL).
ms.assetid: 93b16094-9923-4886-804f-4e989fbf6977
ms.tgt_platform: multiple
keywords:
- DACL AD
- DACL AD, recupero dell'elenco DACL di un oggetto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b515e6c5d28be7003734510300fc7f6d2de776b479b56e62ad521567c76dce4c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119025109"
---
# <a name="retrieving-an-objects-dacl"></a>Recupero dell'elenco DACL di un oggetto

Il descrittore di sicurezza di un oggetto può contenere un elenco di controllo di accesso discrezionale (DACL). Un DACL contiene zero o più voci di controllo di accesso (ACE) che identificano gli utenti e i gruppi che possono accedere all'oggetto. Se un DACL è vuoto,ovvero contiene zero ACE, non viene concesso in modo esplicito alcun accesso, pertanto l'accesso viene negato in modo implicito. Tuttavia, se il descrittore di sicurezza di un oggetto non dispone di un elenco DACL, l'oggetto non è protetto e tutti gli utenti hanno accesso completo.

Per recuperare l'elenco DACL di un oggetto, è necessario essere il proprietario dell'oggetto o disporre dell'accesso **READ \_ CONTROL** all'oggetto.

Per ottenere e impostare l'elenco DACL di un oggetto directory, usare [**l'interfaccia IADsSecurityDescriptor.**](/windows/desktop/api/iads/nn-iads-iadssecuritydescriptor) Usando C++, il [**metodo IADsSecurityDescriptor::get \_ DiscretionaryAcl**](/windows/desktop/ADSI/iadssecuritydescriptor-property-methods) restituisce un [**puntatore IDispatch.**](/windows/win32/api/oaidl/nn-oaidl-idispatch) Chiamare **QueryInterface** sul puntatore **IDispatch** per ottenere un'interfaccia [**IADsAccessControlList**](/windows/desktop/api/iads/nn-iads-iadsaccesscontrollist) e usare i metodi su tale interfaccia per accedere alle singole voci ACE nell'elenco DACL. La procedura per la modifica di un DACL è descritta in [Impostazione dei diritti di accesso per un oggetto](setting-access-rights-on-an-object.md).

Per enumerare le voci ACE, usare [**il metodo IADsAccessControlList::get \_ \_ NewEnum.**](/windows/desktop/api/iads/nf-iads-iadsaccesscontrollist-get__newenum) Il metodo restituisce un [**puntatore IUnknown.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) Chiamare **QueryInterface** sul **puntatore IUnknown** per ottenere [**un'interfaccia IEnumVARIANT.**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) Usare il [**metodo IEnumVARIANT::Next**](/windows/win32/api/oaidl/nf-oaidl-ienumvariant-next) per enumerare le voci ACE nell'ACL. Ogni ACE viene restituita come **VARIANT contenente** un [**puntatore IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) (il **membro vt** è **VT \_ DISPATCH).** Chiamare **QueryInterface sul** puntatore **IDispatch** per ottenere [**un'interfaccia IADsAccessControlEntry**](/windows/desktop/api/iads/nn-iads-iadsaccesscontrolentry) per la voce ACE. È possibile usare i metodi **dell'interfaccia IADsAccessControlEntry** per impostare o recuperare i componenti di una voce ACE.

Per altre informazioni sui daCL e sulle voci ACE, vedere gli argomenti seguenti in Platform Software Development Kit (SDK).

-   [Elenchi di controllo di accesso (ACL)](/windows/desktop/SecAuthZ/access-control-lists)
-   [Voci di controllo di accesso (ACE)](/windows/desktop/SecAuthZ/access-control-entries)

 

 