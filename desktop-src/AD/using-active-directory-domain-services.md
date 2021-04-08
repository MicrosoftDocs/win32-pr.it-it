---
title: Uso di Active Directory Domain Services
description: In questa sezione vengono fornite le linee guida per la scrittura di applicazioni che utilizzano o pubblicano dati in un servizio directory Active Directory.
ms.assetid: 2ae20169-08a5-4e15-8430-ea99a917725f
ms.tgt_platform: multiple
keywords:
- Active Directory Active Directory utilizzando
- Active Directory Domain Services Active Directory utilizzando
- Esempi di Active Directory Active Directory
- Esempi di Active Directory Domain Services Active Directory
- esempi Active Directory
- Active Directory Active Directory, esempi vedere Active Directory Domain Services esempi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 540b9004311db320decbd15c4f0a29e52ec1302a
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/09/2020
ms.locfileid: "103734546"
---
# <a name="using-active-directory-domain-services"></a>Uso di Active Directory Domain Services

In questa sezione vengono fornite le linee guida per la scrittura di applicazioni che utilizzano o pubblicano dati in un servizio directory Active Directory.

> [!Note]  
> La documentazione seguente è destinata ai programmatori di computer. Se si sta tentando di risolvere un errore di stampa della Home Active Directory, vedere il [seguente suggerimento](https://answers.microsoft.com/windows/forum/all/clicking-find-printer-shows-error-the-active/52bfd961-ff62-4397-b8cf-a0708f0cb3d2) dalle pagine della community Microsoft. Se ciò non è utile, provare questi consigli da [TechNet](https://social.technet.microsoft.com/Forums/windowsserver/d6212275-24d6-4168-830a-9441f861cb76/error-message-when-attempting-to-print-active-directory-domain-service-is-currently-unavailable?forum=winserverprint).

 

Active Directory Domain Services sono conformi al protocollo Lightweight Directory Access Protocol 3,0, definito da RFC 2251 e altre RFC. È possibile usare uno dei set di API seguenti per accedere a Active Directory Domain Services. Ogni set di API presenta vantaggi e svantaggi che dipendono dal linguaggio di programmazione, dall'ambiente di programmazione e dal metodo di esecuzione previsto. La maggior parte degli esempi in questa guida utilizza ADSI, supportato da linguaggi quali C e C++, nonché linguaggi conformi all'automazione come Microsoft Visual Basic e Visual Basic Scripting Edition.

Per ulteriori informazioni sulle tecnologie Active Directory Domain Services specifiche, vedere:

-   [Lightweight Directory Access Protocol](/previous-versions/windows/desktop/ldap/lightweight-directory-access-protocol-ldap-api)
-   [Interfacce di servizio Active Directory](../adsi/active-directory-service-interfaces-adsi.md)
-   [System.DirectoryServices](/dotnet/api/system.directoryservices)

In questa sezione vengono illustrati gli argomenti seguenti:

-   [Binding a Active Directory Domain Services](binding-to-active-directory-domain-services.md)
-   [Ricerca in Active Directory Domain Services](searching-in-active-directory-domain-services.md)
-   [Creazione ed eliminazione di oggetti in Active Directory Domain Services](creating-and-deleting-objects-in-active-directory-domain-services.md)
-   [Trasferimento di oggetti](moving-objects.md)
-   [Lettura e scrittura degli attributi degli oggetti in Active Directory Domain Services](reading-and-writing-attributes-of-objects-in-active-directory-domain-services.md)
-   [Controllo dell'accesso agli oggetti in Active Directory Domain Services](controlling-access-to-objects-in-active-directory-domain-services.md)
-   [Estensione dello schema](extending-the-schema.md)
-   [Estensione dell'interfaccia utente per gli oggetti directory](extending-the-user-interface-for-directory-objects.md)
-   [Gestione degli utenti](managing-users.md)
-   [Gestione dei gruppi](managing-groups.md)
-   [Rilevamento delle modifiche](tracking-changes.md)
-   [Pubblicazione di un servizio](service-publication.md)
-   [Account di accesso al servizio](service-logon-accounts.md)
-   [Autenticazione reciproca tramite Kerberos](mutual-authentication-using-kerberos.md)
-   [Backup e ripristino Active Directory](backing-up-and-restoring-an-active-directory-server.md)
-   [Archiviazione Dynamic Data](storing-dynamic-data.md)
-   [Partizioni di directory applicative](application-directory-partitions.md)
-   [Rilevamento della modalità operativa di un dominio](detecting-the-operation-mode-of-a-domain.md)

 

 