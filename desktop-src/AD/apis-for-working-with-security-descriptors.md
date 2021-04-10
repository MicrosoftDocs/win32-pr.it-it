---
title: API per l'uso dei descrittori di sicurezza
description: API per l'uso dei descrittori di sicurezza
ms.assetid: eb5ee183-949c-41f5-9f74-f9c418fdf0a2
ms.tgt_platform: multiple
keywords:
- Active Directory descrittori di sicurezza
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfb798e036d5e30ba58a83499b92340bf30ee3cb
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/17/2020
ms.locfileid: "103956349"
---
# <a name="apis-for-working-with-security-descriptors"></a>API per l'uso dei descrittori di sicurezza

Ogni oggetto in Active Directory Domain Services dispone di un attributo **ntSecurityDescriptor** che contiene il descrittore di sicurezza dell'oggetto. Esistono due modi principali per leggere e modificare il descrittore di sicurezza di un oggetto directory:

-   Usare il metodo [**IADs:: Get**](/windows/desktop/api/iads/nf-iads-iads-get) per recuperare il descrittore di sicurezza come oggetto ADSI com con un'interfaccia [**IADsSecurityDescriptor**](/windows/desktop/api/iads/nn-iads-iadssecuritydescriptor) . Le interfacce **IADsSecurityDescriptor**, [**IADsAccessControlList**](/windows/desktop/api/iads/nn-iads-iadsaccesscontrollist)e [**IADsAccessControlEntry**](/windows/desktop/api/iads/nn-iads-iadsaccesscontrolentry) possono essere usate per gestire il descrittore di sicurezza e i relativi componenti (ACL, ACE e così via). Per ulteriori informazioni e un esempio di codice, vedere [utilizzo di IADs per ottenere un descrittore di sicurezza](using-iads-to-get-a-security-descriptor.md).
-   Usare il metodo [**IDirectoryObject:: GetObjectAttributes**](/windows/desktop/api/iads/nf-iads-idirectoryobject-getobjectattributes) per recuperare il descrittore di sicurezza di un oggetto come puntatore a una struttura di [**\_ descrittori di sicurezza**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) . Utilizzare questo puntatore con una funzione di controllo di accesso Win32, ad esempio [**AccessCheck**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-accesscheck) o [**BuildSecurityDescriptor**](/windows/desktop/api/aclapi/nf-aclapi-buildsecuritydescriptora). Per ulteriori informazioni e un esempio di codice, vedere [utilizzo di IDirectoryObject per ottenere un descrittore di sicurezza](using-idirectoryobject-to-get-a-security-descriptor.md).

La tecnica consigliata, e quella usata dalla maggior parte degli esempi di codice in questa guida, consiste nell'usare le interfacce **IADs \*** perché semplificano la gestione di descrittori di sicurezza, ACL e ACE. Per i programmatori Visual Basic, le interfacce **IADs \*** rappresentano il modo più efficiente per gestire i descrittori di sicurezza.

La tecnica [**IDirectoryObject**](/windows/desktop/api/iads/nn-iads-idirectoryobject) è utile quando è richiesta una struttura di [**\_ descrittori di sicurezza**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) . Ad esempio, l'esempio di codice in [controllo di un diritto di accesso a un controllo nell'elenco ACL di un oggetto](checking-a-control-access-right-in-an-objectampaposs-acl.md) usa questo metodo per recuperare un descrittore di sicurezza da passare alla funzione [**AccessCheckByTypeResultList**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-accesscheckbytyperesultlist) .

Per altre informazioni, vedere:

-   [Uso di IADs per ottenere un descrittore di sicurezza](using-iads-to-get-a-security-descriptor.md)
-   [Uso di IDirectoryObject per ottenere un descrittore di sicurezza](using-idirectoryobject-to-get-a-security-descriptor.md)
-   [Componenti del descrittore di sicurezza](security-descriptor-components.md)
-   [Recupero del DACL di un oggetto](retrieving-an-objectampaposs-dacl.md)
-   [Recupero del SACL di un oggetto](retrieving-an-objectampaposs-sacl.md)
-   [Lettura del descrittore di sicurezza di un oggetto](reading-an-objectampaposs-security-descriptor.md)
-   [Codice di esempio per creare un descrittore di sicurezza](example-code-for-creating-a-security-descriptor.md)
-   [Codice di esempio per l'enumerazione dell'ACL di un oggetto in Active Directory Domain Services](example-code-for-enumerating-the-acl-of-an-active-directory-object.md)

 

 