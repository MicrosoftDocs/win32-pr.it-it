---
description: Sono disponibili diverse tecniche per la mitigazione delle minacce che è possibile usare per migliorare la protezione delle password.
ms.assetid: b2442579-e559-4053-869f-9d96e4db202e
title: Tecniche di mitigazione delle minacce
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 435ec2b8db3a634ea93ce77d585038909056c7d8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103884445"
---
# <a name="threat-mitigation-techniques"></a>Tecniche di mitigazione delle minacce

Sono disponibili diverse tecniche per la mitigazione delle minacce che è possibile usare per migliorare la protezione delle password. Queste tecniche vengono implementate utilizzando una o più delle quattro tecnologie primarie seguenti.



| Tecnologia                      | Descrizione                                                                                                                                                                                                                                                                                                                                                                |
|---------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CryptoAPI                       | CryptoAPI fornisce un set di funzioni che consentono di applicare le routine di crittografia alle entità di destinazione. CryptoAPI può fornire hash, digest, crittografia e decrittografia per menzionare le funzionalità principali. CryptoAPI dispone anche di altre funzionalità. Per informazioni sulla crittografia e sulla CryptoAPI, vedere [Cryptography Essentials](/windows/desktop/SecCrypto/cryptography-essentials).           |
| Elenchi di controllo di accesso            | Un [*elenco di controllo di accesso*](/windows/desktop/SecGloss/a-gly) (ACL) è un elenco di protezioni di sicurezza che si applicano a un oggetto. Un oggetto può essere un file, un processo, un evento o qualsiasi altro elemento che disponga di un descrittore di sicurezza. Per ulteriori informazioni sugli ACL, vedere [elenchi di controllo di accesso](/windows/desktop/SecAuthZ/access-control-lists) (ACL). |
| API per la protezione dei dati             | Data Protection API (DPAPI) fornisce le quattro funzioni seguenti che è possibile usare per crittografare e decrittografare i dati sensibili: [**CryptProtectData**](/windows/desktop/api/dpapi/nf-dpapi-cryptprotectdata), [**CryptUnprotectData**](/windows/desktop/api/dpapi/nf-dpapi-cryptunprotectdata), [**CryptProtectMemory**](/windows/desktop/api/dpapi/nf-dpapi-cryptprotectmemory)e [**CryptUnprotectMemory**](/windows/desktop/api/dpapi/nf-dpapi-cryptunprotectmemory).                  |
| Nomi utente e password archiviati | Funzionalità di archiviazione che consente di gestire le password degli utenti e altre credenziali, ad esempio le chiavi private, più semplici, coerenti e sicure. Per ulteriori informazioni su questa funzionalità, vedere [**CredUIPromptForCredentials**](/windows/desktop/api/wincred/nf-wincred-creduipromptforcredentialsa).                                                                                                         |



 

Queste tecnologie non sono disponibili in tutti i sistemi operativi. Di conseguenza, la misura in cui è possibile migliorare la sicurezza dipende da quali sistemi operativi sono interessati. Di seguito sono riportate le tecnologie disponibili in ogni sistema operativo.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Sistema operativo</th>
<th>Tecnologia</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Windows Server 2003 e Windows XP</td>
<td><ul>
<li>CryptoAPI</li>
<li>Elenchi di controllo di accesso</li>
<li>API per la protezione dei dati</li>
<li>Nomi utente e password archiviati</li>
</ul></td>
</tr>
<tr class="even">
<td>Windows 2000</td>
<td><ul>
<li>CryptoAPI</li>
<li>Elenchi di controllo di accesso</li>
<li><a href="/windows/desktop/api/dpapi/nf-dpapi-cryptprotectdata"><strong>CryptProtectData</strong></a></li>
<li><a href="/windows/desktop/api/dpapi/nf-dpapi-cryptunprotectdata"><strong>CryptUnprotectData</strong></a></li>
</ul></td>
</tr>
</tbody>
</table>



 

Le tecniche di mitigazione delle minacce seguenti usano una o più delle quattro tecnologie. Non è possibile usare tecniche che richiedono l'uso di tecnologie non incluse nel sistema operativo.

## <a name="getting-passwords-from-the-user"></a>Recupero di password dall'utente

Quando si consente all'utente di impostare una password, forzare l'utilizzo di password complesse. Ad esempio, è necessario che le password abbiano una lunghezza minima, ad esempio otto o più caratteri. È necessario inoltre che vengano richieste le password per includere lettere maiuscole e minuscole, numeri e altri caratteri della tastiera, ad esempio il simbolo del dollaro ($), il punto esclamativo (!) o maggiore di (>).

Dopo avere ottenuto una password, usarla rapidamente (usando il minor codice possibile), quindi cancellare tutte le vestigia della password. Questo consente di ridurre al minimo il tempo disponibile a un intruso per "intercettare" la password. Il compromesso con questa tecnica è la frequenza con cui la password deve essere recuperata dall'utente. il principio, tuttavia, deve essere utilizzato laddove possibile. Per informazioni su come ottenere correttamente le password, vedere [richiesta di credenziali all'utente](asking-the-user-for-credentials.md).

Evitare di fornire le opzioni dell'interfaccia utente "Memorizza password". Spesso, gli utenti avranno la necessità di avere questa opzione. Se è necessario fornirlo, almeno, assicurarsi che la password venga salvata in modo sicuro. Per informazioni, vedere la sezione archiviazione delle password, più avanti in questo argomento.

Numero massimo di tentativi di immissione della password. Dopo un certo numero di tentativi senza esito positivo, bloccare l'utente per un determinato periodo di tempo. Facoltativamente, estendere il tempo di risposta per ogni tentativo per un massimo di. Questa tecnica è finalizzata a sconfiggere un attacco a indovinare.

## <a name="storing-passwords"></a>Archiviazione delle password

Non archiviare mai le password in testo normale (non crittografato). La crittografia delle password aumenta significativamente la loro sicurezza. Per informazioni sull'archiviazione delle password crittografate, vedere [**CryptProtectData**](/windows/desktop/api/dpapi/nf-dpapi-cryptprotectdata). Per informazioni sulla crittografia delle password in memoria, vedere [**CryptProtectMemory**](/windows/desktop/api/dpapi/nf-dpapi-cryptprotectmemory). Archiviare le password nel minor numero possibile di posizioni. Maggiore è la posizione in cui viene archiviata una password, maggiori sono le probabilità che un intruso possa trovarlo. Non archiviare mai le password in una pagina Web o in un file basato sul Web. L'archiviazione delle password in una pagina Web o in un file basato sul Web consente loro di essere facilmente compromessi.

Dopo aver crittografato e archiviato una password, usare ACL protetti per limitare l'accesso al file. In alternativa, è possibile archiviare le password e le chiavi di crittografia nei dispositivi rimovibili. L'archiviazione delle password e delle chiavi di crittografia in un supporto rimovibile, ad esempio una smart card, consente di creare un sistema più sicuro. Una volta recuperata una password per una determinata sessione, la scheda può essere rimossa, eliminando in tal modo la possibilità che un intruso possa accedervi.

 

 
