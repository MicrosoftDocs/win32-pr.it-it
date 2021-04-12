---
title: Scelta della tecnologia di ricerca
description: Questo argomento include un elenco delle tecnologie usate per la ricerca Active Directory.
ms.assetid: c9e887e3-7de4-4461-bc32-03db71c3e272
ms.tgt_platform: multiple
keywords:
- tecnologie di ricerca in Active Directory Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c6edba5c87ed438bc0047e0381d7e366cd6cc865
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/17/2020
ms.locfileid: "104472667"
---
# <a name="choosing-the-search-technology"></a>Scelta della tecnologia di ricerca

Le tecnologie, elencate nella tabella seguente, possono essere usate per la ricerca in Active Directory Domain Services.



| Tecnologia                                                                     | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|--------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [DirectorySearcher](/dotnet/api/system.directoryservices.directorysearcher?view=dotnet-plat-ext-3.1)<br/> | La classe [DirectorySearcher](/dotnet/api/system.directoryservices.directorysearcher?view=dotnet-plat-ext-3.1) viene fornita dallo spazio dei nomi [System. DirectoryServices](/dotnet/api/system.directoryservices?view=dotnet-plat-ext-3.1) per consentire la ricerca all'interno Active Directory Domain Services con .NET Framework. Per ulteriori informazioni, vedere [la pagina relativa alla ricerca nella directory](/previous-versions/ms180879(v=vs.90)).<br/>                                                                                                                                  |
| [**IDirectorySearch**](/windows/desktop/api/iads/nn-iads-idirectorysearch)<br/>                       | ADSI fornisce l'interfaccia [**IDirectorySearch**](/windows/desktop/api/iads/nn-iads-idirectorysearch) per eseguire una query su un server Active Directory, oltre ad altri servizi directory, ad esempio NDS, usando LDAP. **IDirectorySearch** è un'interfaccia com che restituisce dati fortemente tipizzati, ad esempio Integer, stringa ottetto, stringa, descrittore di sicurezza, ora UTC, numero intero grande o valore booleano. Per ulteriori informazioni sull'utilizzo di **IDirectorySearch**, vedere [ricerca con l'interfaccia IDirectorySearch](/windows/desktop/ADSI/searching-with-idirectorysearch).<br/> |
| OLE DB<br/>                                                              | OLE DB è un set di interfacce COM che consentono alle applicazioni di accedere in modo uniforme ai dati archiviati in diverse origini dati, indipendentemente dalla posizione o dal tipo. ADSI fornisce inoltre un provider OLE DB per ADSI che consente alle applicazioni di utilizzare OLE DB per accedere Active Directory Domain Services. Il provider di OLE DB ADSI utilizza le interfacce [**IDirectorySearch**](/windows/desktop/api/iads/nn-iads-idirectorysearch) per inviare query al Active Directory Domain Services e raccogliere i risultati.<br/>                                     |
| ADO e altre tecnologie di accesso ai dati basate su OLE DB<br/>                 | Il provider OLE DB ADSI consente qualsiasi tecnologia di accesso ai dati basata su OLE DB, ad esempio ADO, per la ricerca all'interno Active Directory Domain Services.<br/>                                                                                                                                                                                                                                                                                                                                                                |
| API LDAP<br/>                                                            | I controller di dominio Windows 2000 sono server di directory conformi a LDAP versione 3. L'API LDAP è una libreria di funzioni di tipo C. Le applicazioni possono usare l'API LDAP per eseguire la ricerca all'interno Active Directory Domain Services.<br/>                                                                                                                                                                                                                                                                              |



 

Quando si sceglie una tecnologia, tenere presente quanto segue:

-   Per Microsoft Visual Basic e Visual Basic Scripting Edition (VBScript), è consigliabile usare ADO.
-   Per C/C++, è possibile scegliere una qualsiasi delle tecnologie.
-   Se l'applicazione usa in modo esteso ADSI, potrebbe essere più semplice usare [**IDirectorySearch**](/windows/desktop/api/iads/nn-iads-idirectorysearch). Se si utilizza [**IDirectoryObject**](/windows/desktop/api/iads/nn-iads-idirectoryobject) per gestire gli oggetti in Active Directory Domain Services, utilizzare **IDirectorySearch** per rendere più semplice la gestione delle proprietà restituite dalla ricerca. **IDirectorySearch** usa le stesse strutture [**ADSVALUE**](/windows/desktop/api/iads/ns-iads-adsvalue) di **IDirectoryObject** per rappresentare le proprietà. Inoltre, **IDirectorySearch** è esposto in quasi tutti gli oggetti ADSI com. Se è presente un puntatore a un oggetto ADSI COM, è possibile chiamare **QueryInterface** per ottenere un puntatore **IDirectorySearch** che può essere usato per eseguire una ricerca a partire dall'oggetto directory rappresentato dall'oggetto com ADSI.
-   Se l'applicazione usa già OLE DB, ADO o l'API LDAP, è possibile continuare a usare tali tecnologie per eseguire la ricerca all'interno di Active Directory Domain Services.
-   Se l'applicazione deve aggiungere dati da un servizio Dominio di Active Directory e da un database SQL Server 7, utilizzare OLE DB. Utilizzando OLE DB, l'applicazione è in grado di eseguire query distribuite che fanno riferimento a Active Directory Domain Services e tabelle e set di righe da uno o più database Microsoft SQL Server 7.

 

