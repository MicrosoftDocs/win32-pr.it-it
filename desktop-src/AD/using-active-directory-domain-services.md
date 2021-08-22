---
title: Uso di Active Directory Domain Services
description: Questa sezione fornisce linee guida per la scrittura di applicazioni che usano o pubblicano dati in un servizio directory Active Directory.
ms.assetid: 2ae20169-08a5-4e15-8430-ea99a917725f
ms.tgt_platform: multiple
keywords:
- Active Directory Active Directory , tramite
- Active Directory Domain Services Active Directory , usando
- Esempi di Active Directory Active Directory
- Active Directory Domain Services esempi di Active Directory
- esempi di Active Directory
- Active Directory Active Directory, esempi vedere Active Directory Domain Services esempi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e1ef5428242e6d83fcb0c517c91abaee24de8181689a3aa1922eafea4d76703
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119024539"
---
# <a name="using-active-directory-domain-services"></a>Uso di Active Directory Domain Services

Questa sezione fornisce linee guida per la scrittura di applicazioni che usano o pubblicano dati in un servizio directory Active Directory.

> [!Note]  
> La documentazione seguente è per programmatori di computer. Se si sta tentando di risolvere un errore di stampa nella home page di Active Directory, vedere il [suggerimento seguente](https://answers.microsoft.com/windows/forum/all/clicking-find-printer-shows-error-the-active/52bfd961-ff62-4397-b8cf-a0708f0cb3d2) nelle pagine della community Microsoft. In caso contrario, provare queste raccomandazioni di [TechNet.](https://social.technet.microsoft.com/Forums/windowsserver/d6212275-24d6-4168-830a-9441f861cb76/error-message-when-attempting-to-print-active-directory-domain-service-is-currently-unavailable?forum=winserverprint)

 

Active Directory Domain Services conformi a Lightweight Directory Access Protocol 3.0, definito da RFC 2251 e da altre RFC. È possibile usare uno dei set di API seguenti per accedere Active Directory Domain Services. Ogni set di API presenta vantaggi e svantaggi che dipendono dal linguaggio di programmazione, dall'ambiente di programmazione e dal metodo di esecuzione previsto. La maggior parte degli esempi in questa guida usa ADSI, supportato da linguaggi come C e C++, nonché linguaggi conformi all'automazione come Microsoft Visual Basic e Visual Basic Scripting Edition.

Per altre informazioni su tecnologie Active Directory Domain Services, vedere:

-   [Lightweight Directory Access Protocol](/previous-versions/windows/desktop/ldap/lightweight-directory-access-protocol-ldap-api)
-   [Interfacce di servizio Active Directory](../adsi/active-directory-service-interfaces-adsi.md)
-   [System.DirectoryServices](/dotnet/api/system.directoryservices)

In questa sezione vengono illustrati gli argomenti seguenti:

-   [Associazione a Active Directory Domain Services](binding-to-active-directory-domain-services.md)
-   [Ricerca in Active Directory Domain Services](searching-in-active-directory-domain-services.md)
-   [Creazione ed eliminazione di oggetti in Active Directory Domain Services](creating-and-deleting-objects-in-active-directory-domain-services.md)
-   [Spostamento di oggetti](moving-objects.md)
-   [Lettura e scrittura di attributi di oggetti in Active Directory Domain Services](reading-and-writing-attributes-of-objects-in-active-directory-domain-services.md)
-   [Controllo dell'accesso agli oggetti in Active Directory Domain Services](controlling-access-to-objects-in-active-directory-domain-services.md)
-   [Estensione dello schema](extending-the-schema.md)
-   [Estensione del Interfaccia utente per gli oggetti directory](extending-the-user-interface-for-directory-objects.md)
-   [Gestione degli utenti](managing-users.md)
-   [Gestione dei gruppi](managing-groups.md)
-   [Rilevamento delle modifiche](tracking-changes.md)
-   [Pubblicazione di un servizio](service-publication.md)
-   [Account di accesso al servizio](service-logon-accounts.md)
-   [Autenticazione reciproca tramite Kerberos](mutual-authentication-using-kerberos.md)
-   [Backup e ripristino di Active Directory](backing-up-and-restoring-an-active-directory-server.md)
-   [Archiviazione Dynamic Data](storing-dynamic-data.md)
-   [Partizioni di directory applicative](application-directory-partitions.md)
-   [Rilevamento della modalità di funzionamento di un dominio](detecting-the-operation-mode-of-a-domain.md)

 

 