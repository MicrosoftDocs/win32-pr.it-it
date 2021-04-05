---
title: Informazioni su Active Directory Domain Services
description: Questa guida fornisce informazioni essenziali per l'integrazione di Microsoft Active Directory in applicazioni distribuite progettate per sistemi operativi che supportano Active Directory.
ms.assetid: cc6c63dd-ae22-40a7-8312-0a4648bb92bd
ms.tgt_platform: multiple
keywords:
- Active Directory Active Directory, informazioni
- Active Directory Domain Services Active Directory, informazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d8dafb89533d796f0651ad08b913eacda1d0fe9
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104046788"
---
# <a name="about-active-directory-domain-services"></a>Informazioni su Active Directory Domain Services

## <a name="writing-powerful-applications-that-use-active-directory-domain-services"></a>Scrittura di applicazioni potenti che utilizzano Active Directory Domain Services

Questa guida fornisce informazioni essenziali per l'integrazione di Active Directory Domain Services in applicazioni distribuite progettate per sistemi operativi che supportano Active Directory Domain Services, tra cui:

-   Windows Server 2008
-   Windows Server 2008 R2
-   Windows Server 2012
-   Windows Server 2012 R2
-   Windows Server 2016

> [!Note]  
> Questi argomenti sono destinati agli sviluppatori di software. Per i problemi di supporto, vedere [supporto tecnico Microsoft](https://windows.microsoft.com/windows/support#1tc). Per informazioni sull'amministrazione di Active Directory, vedere [Active Directory Domain Services](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc770946(v=ws.10)) in TechNet.

 

## <a name="fundamental-directory-features"></a>Funzionalità di directory fondamentali

Un servizio directory è un servizio fondamentale per le applicazioni distribuite. Un servizio directory deve fornire le funzionalità elencate nella tabella seguente.



| Funzionalità               | Descrizione                                                                                         |
|-----------------------|-----------------------------------------------------------------------------------------------------|
| Trasparenza della posizione | È possibile trovare dati di utenti, gruppi, servizi di rete o risorse senza l'indirizzo dell'oggetto           |
| Dati di oggetti           | In grado di archiviare dati utente, gruppo, organizzazione e servizio in un albero gerarchico                    |
| Query avanzata            | In grado di individuare un oggetto eseguendo una query per le proprietà dell'oggetto                                          |
| Disponibilità elevata     | In grado di individuare una replica della directory in una posizione efficiente per le operazioni di lettura/scrittura |



 

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
<td>Active Directory Domain Services implementa le funzionalità in base agli standard Internet pubblicati, ad esempio LDAP e DNS.</td>
</tr>
<tr class="even">
<td>Sicurezza strettamente integrata e flessibile</td>
<td>Alcuni vantaggi:<br/>
<ul>
<li>Scelta dei pacchetti di autenticazione. Kerberos, Secure Sockets Layer (SSL) o una combinazione; ad esempio, stabilire un canale SSL per la crittografia e quindi usare Kerberos per l'autenticazione.</li>
<li>Gestione centralizzata dell'accesso al servizio e alle risorse tramite utenti e gruppi in Active Directory Domain Services.</li>
<li>Delega dell'amministrazione in modo che gli amministratori centrali possano delegare attività amministrative quali la modifica della password o la creazione e l'eliminazione di oggetti specifici.</li>
<li>Il server Active Directory utilizza gli stessi meccanismi di controllo degli accessi utilizzati nei file System nei sistemi operativi Windows. Di conseguenza, gli stessi strumenti che gestiscono il controllo di accesso su un file system funzionano per Active Directory Domain Services.</li>
<li>Infrastruttura a chiave pubblica completa. Il supporto per le smart card e il server dei certificati Microsoft è integrato con Active Directory Domain Services per fornire l'accesso con smart card e la gestione dei certificati.</li>
</ul></td>
</tr>
<tr class="odd">
<td>Facilmente programmabile</td>
<td>È possibile accedere a livello di codice e amministrare il server Active Directory usando l'API <a href="/windows/desktop/ADSI/active-directory-service-interfaces-adsi">interfacce del servizio Active Directory</a> , l'API <a href="/previous-versions/windows/desktop/ldap/lightweight-directory-access-protocol-ldap-api">Lightweight Directory Access Protocol</a> o lo spazio dei nomi <a href="/dotnet/api/system.directoryservices">System. DirectoryServices</a> .</td>
</tr>
<tr class="even">
<td>Servizi di sistema abilitati per la directory</td>
<td>L'applicazione client può essere facilmente distribuita nei desktop distribuiti creando un pacchetto di Windows Installer e utilizzando la funzionalità di distribuzione delle applicazioni disponibile nei sistemi operativi Windows.</td>
</tr>
<tr class="odd">
<td>Integrazione di applicazioni chiave</td>
<td>Le applicazioni distribuite principali, ad esempio Exchange, sono integrate con Active Directory Domain Services. In questo modo, le aziende possono ridurre il numero di servizi directory da gestire.</td>
</tr>
<tr class="even">
<td>Schema completo ed estendibile</td>
<td>Lo schema definisce gli oggetti e le proprietà che possono essere scritti e letti da un servizio directory. Lo schema Active Directory è ricco. La maggior parte degli oggetti e delle proprietà richiesti da un servizio sono disponibili. In caso contrario, un'applicazione distribuita può estendere lo schema per supportare i requisiti dell'applicazione.</td>
</tr>
</tbody>
</table>



 

Per ulteriori informazioni su Active Directory Domain Services, vedere:

-   [Concetti di base di Active Directory Domain Services](core-concepts-of-active-directory-domain-services.md)
-   [Architettura Active Directory](active-directory-domain-services-architecture.md)
-   [Schema Active Directory](active-directory-schema.md)

