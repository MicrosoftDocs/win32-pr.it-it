---
title: Informazioni Active Directory Domain Services
description: Questa guida fornisce informazioni essenziali per l'integrazione di Microsoft Active Directory in applicazioni distribuite progettate per sistemi operativi che supportano Active Directory.
ms.assetid: cc6c63dd-ae22-40a7-8312-0a4648bb92bd
ms.tgt_platform: multiple
keywords:
- Active Directory Active Directory , informazioni su
- Active Directory Domain Services Active Directory , informazioni su
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e4ef886409b435e1687d8ca6cf530b940852f3569818bb3afab69f57ab6b97c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117841075"
---
# <a name="about-active-directory-domain-services"></a>Informazioni Active Directory Domain Services

## <a name="writing-powerful-applications-that-use-active-directory-domain-services"></a>Scrittura di applicazioni potenti che usano Active Directory Domain Services

Questa guida fornisce informazioni essenziali per l'integrazione di Active Directory Domain Services in applicazioni distribuite progettate per sistemi operativi che supportano Active Directory Domain Services, tra cui:

-   Windows Server 2008
-   Windows Server 2008 R2
-   Windows Server 2012
-   R2 per Windows Server 2012
-   Windows Server 2016

> [!Note]  
> Questi argomenti sono per sviluppatori di software. Per i problemi di supporto, [vedere Supporto tecnico Microsoft](https://windows.microsoft.com/windows/support#1tc). Per informazioni sull'amministrazione di Active Directory, [vedere](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc770946(v=ws.10)) Active Directory Domain Services su TechNet.

 

## <a name="fundamental-directory-features"></a>Funzionalità fondamentali della directory

Un servizio directory è un servizio fondamentale per le applicazioni distribuite. Un servizio directory deve fornire le funzionalità elencate nella tabella seguente.



| Funzionalità               | Descrizione                                                                                         |
|-----------------------|-----------------------------------------------------------------------------------------------------|
| Trasparenza della posizione | In grado di trovare dati utente, gruppo, servizio in rete o risorsa senza l'indirizzo dell'oggetto           |
| Dati di oggetti           | Possibilità di archiviare i dati di utenti, gruppi, organizzazioni e servizi in un albero gerarchico                    |
| Query rtf            | In grado di individuare un oggetto tramite query per le proprietà dell'oggetto                                          |
| Disponibilità elevata     | In grado di individuare una replica della directory in un percorso efficiente per le operazioni di lettura/scrittura |



 

## <a name="advanced-features-of-active-directory-domain-services"></a>Funzionalità avanzate di Active Directory Domain Services

Active Directory Domain Services fornisce le funzionalità elencate nella tabella seguente.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Funzionalità</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Supporto per gli standard Internet</td>
<td>Active Directory Domain Services le funzionalità in base agli standard Internet pubblicati, ad esempio LDAP e DNS.</td>
</tr>
<tr class="even">
<td>Sicurezza strettamente integrata e flessibile</td>
<td>Alcuni vantaggi:<br/>
<ul>
<li>Scelta dei pacchetti di autenticazione. Kerberos, Secure Sockets Layer (SSL) o una combinazione; ad esempio stabilire un canale SSL per la crittografia e quindi usare Kerberos per l'autenticazione.</li>
<li>Gestione centralizzata dell'accesso a servizi e risorse usando gli utenti e i gruppi in Active Directory Domain Services.</li>
<li>Delega dell'amministrazione in modo che gli amministratori centrali possano delegare attività amministrative, ad esempio la modifica della password o la creazione e l'eliminazione di oggetti specifici.</li>
<li>Il server Active Directory usa gli stessi meccanismi di controllo di accesso usati nei file system Windows sistemi operativi. Di conseguenza, gli stessi strumenti che gestiscono il controllo di accesso in file system lavoro per Active Directory Domain Services.</li>
<li>Infrastruttura a chiave pubblica completa. Il supporto di Microsoft Certificate Server e smart card è integrato con Active Directory Domain Services per fornire l'accesso con smart card e la gestione dei certificati.</li>
</ul></td>
</tr>
<tr class="odd">
<td>Facilmente programmabile</td>
<td>È possibile accedere e amministrare il server Active Directory a livello di codice usando l'API <a href="/windows/desktop/ADSI/active-directory-service-interfaces-adsi">Active Directory Service Interfaces,</a> <a href="/previous-versions/windows/desktop/ldap/lightweight-directory-access-protocol-ldap-api">Lightweight Directory Access Protocol</a> API o lo spazio dei nomi <a href="/dotnet/api/system.directoryservices">System.DirectoryServices.</a></td>
</tr>
<tr class="even">
<td>Servizi di sistema abilitati per la directory</td>
<td>L'applicazione client può essere facilmente distribuita nei desktop distribuiti creando un pacchetto del programma di installazione di Windows e usando la funzionalità di distribuzione dell'applicazione disponibile nei Windows operativi.</td>
</tr>
<tr class="odd">
<td>Integrazione dell'applicazione chiave</td>
<td>Le principali applicazioni distribuite, ad esempio Exchange, sono integrate con Active Directory Domain Services. Di conseguenza, le aziende possono ridurre il numero di servizi directory da gestire.</td>
</tr>
<tr class="even">
<td>Schema esteso ed estendibile</td>
<td>Lo schema definisce quali oggetti e proprietà possono essere scritti e letti da un servizio directory. Lo schema di Active Directory è ricco. La maggior parte degli oggetti e delle proprietà necessari per un servizio è disponibile. In caso contrario, un'applicazione distribuita può estendere lo schema per supportare i requisiti dell'applicazione.</td>
</tr>
</tbody>
</table>



 

Per altre informazioni sui Active Directory Domain Services, vedere:

-   [Concetti di base di Active Directory Domain Services](core-concepts-of-active-directory-domain-services.md)
-   [Architettura di Active Directory](active-directory-domain-services-architecture.md)
-   [Schema di Active Directory](active-directory-schema.md)

