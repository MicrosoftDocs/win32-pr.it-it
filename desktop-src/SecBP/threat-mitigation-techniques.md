---
description: Sono disponibili diverse tecniche di mitigazione delle minacce che è possibile usare per proteggere meglio le password.
ms.assetid: b2442579-e559-4053-869f-9d96e4db202e
title: Tecniche di mitigazione delle minacce
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 315a79ec1db48a16de858d655bd1550fa1458720
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122482447"
---
# <a name="threat-mitigation-techniques"></a>Tecniche di mitigazione delle minacce

Sono disponibili diverse tecniche di mitigazione delle minacce che è possibile usare per proteggere meglio le password. Queste tecniche vengono implementate usando una o più delle quattro tecnologie principali seguenti.



| Tecnologia                      | Descrizione                                                                                                                                                                                                                                                                                                                                                                |
|---------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cryptoapi                       | CryptoAPI fornisce un set di funzioni che consentono di applicare routine crittografiche alle entità di destinazione. CryptoAPI può fornire hash, digest, crittografia e decrittografia, per menzionarne le funzionalità principali. CryptoAPI include anche altre funzionalità. Per informazioni sulla crittografia e su CryptoAPI, vedere [Cryptography Essentials](/windows/desktop/SecCrypto/cryptography-essentials).           |
| Elenchi di controllo di accesso            | Un [*elenco di controllo di*](/windows/desktop/SecGloss/a-gly) accesso (ACL) è un elenco di protezioni di sicurezza applicabili a un oggetto. Un oggetto può essere un file, un processo, un evento o qualsiasi altro elemento con un descrittore di sicurezza. Per altre informazioni sugli elenchi di controllo di accesso, vedere [Elenchi di controllo](/windows/desktop/SecAuthZ/access-control-lists) di accesso (ACL). |
| API di protezione dei dati             | L'API di protezione dei dati (DPAPI) fornisce le quattro funzioni seguenti usate per crittografare e decrittografare i dati sensibili: [**CryptProtectData,**](/windows/desktop/api/dpapi/nf-dpapi-cryptprotectdata) [**CryptUnprotectData,**](/windows/desktop/api/dpapi/nf-dpapi-cryptunprotectdata) [**CryptProtectMemory**](/windows/desktop/api/dpapi/nf-dpapi-cryptprotectmemory)e [**CryptUnprotectMemory.**](/windows/desktop/api/dpapi/nf-dpapi-cryptunprotectmemory)                  |
| Nomi utente e password archiviati | Archiviazione funzionalità che rende più semplice, coerente e sicura la gestione delle password degli utenti e di altre credenziali, ad esempio chiavi private. Per altre informazioni su questa funzionalità, vedere [**CredUIPromptForCredentials.**](/windows/desktop/api/wincred/nf-wincred-creduipromptforcredentialsa)                                                                                                         |



 

Queste tecnologie non sono disponibili in tutti i sistemi operativi. Di conseguenza, la misura in cui è possibile migliorare la sicurezza dipende dai sistemi operativi coinvolti. Ecco le tecnologie disponibili in ogni sistema operativo.


| Sistema operativo | Tecnologia | 
|------------------|------------|
| Windows Server 2003 e Windows XP | <ul><li>Cryptoapi</li><li>Elenchi di controllo di accesso</li><li>API di protezione dei dati</li><li>Nomi utente e password archiviati</li></ul> | 
| Windows 2000 | <ul><li>Cryptoapi</li><li>Elenchi di controllo di accesso</li><li><a href="/windows/desktop/api/dpapi/nf-dpapi-cryptprotectdata"><strong>CryptProtectData</strong></a></li><li><a href="/windows/desktop/api/dpapi/nf-dpapi-cryptunprotectdata"><strong>CryptUnprotectData</strong></a></li></ul> | 




 

Le tecniche di mitigazione delle minacce seguenti usano una o più delle quattro tecnologie. Non è possibile usare tecniche che richiedono l'uso di tecnologie non incluse nel sistema operativo.

## <a name="getting-passwords-from-the-user"></a>Recupero di password dall'utente

Quando si consente all'utente di configurare una password, forzare l'uso di password complesse. Ad esempio, richiedere che le password siano di lunghezza minima, ad esempio otto caratteri o più. Le password devono anche includere lettere maiuscole e minuscole, numeri e altri caratteri della tastiera, ad esempio il simbolo del dollaro ($), il punto esclamativo (!) o maggiore di (>).

Dopo aver ottenere una password, usarla rapidamente (usando il meno codice possibile) e quindi cancellare tutte le vestigia della password. Ciò riduce al minimo il tempo disponibile per un intruso per "intercettare" la password. Il compromesso con questa tecnica è la frequenza con cui la password deve essere recuperata dall'utente. Tuttavia, il principio deve essere utilizzato laddove possibile. Per informazioni su come ottenere correttamente le password, vedere [Richiesta di credenziali all'utente.](asking-the-user-for-credentials.md)

Evitare di specificare le opzioni dell'interfaccia utente "Memorizza la password". Spesso gli utenti richiedono questa opzione. Se è necessario specificarlo, assicurarsi almeno che la password venga salvata in modo sicuro. Per informazioni, vedere la sezione Archiviazione delle password più avanti in questo argomento.

Limitare i tentativi di immissione della password. Dopo un determinato numero di tentativi senza esito positivo, bloccare l'utente per un determinato periodo di tempo. Facoltativamente, è possibile allungare il tempo di risposta per ogni tentativo oltre un massimo. Questa tecnica ha lo scopo di sconfiggire un attacco di congettura.

## <a name="storing-passwords"></a>Archiviazione delle password

Non archiviare mai le password in testo non crittografato (non crittografato). La crittografia delle password aumenta significativamente la sicurezza. Per informazioni sull'archiviazione delle password crittografate, vedere [**CryptProtectData**](/windows/desktop/api/dpapi/nf-dpapi-cryptprotectdata). Per informazioni sulla crittografia delle password in memoria, vedere [**CryptProtectMemory**](/windows/desktop/api/dpapi/nf-dpapi-cryptprotectmemory). Archiviare le password in un numero di posizioni il più possibile. Maggiore è il numero di posizioni in cui viene archiviata una password, maggiore è la probabilità che venga individuata da un intruso. Non archiviare mai le password in una pagina Web o in un file basato sul Web. L'archiviazione delle password in una pagina Web o in un file basato sul Web consente di comprometterle facilmente.

Dopo aver crittografato e archiviato una password, usare gli ACL sicuri per limitare l'accesso al file. In alternativa, è possibile archiviare le password e le chiavi di crittografia nei dispositivi rimovibili. L'archiviazione di password e chiavi di crittografia in un supporto rimovibile, ad esempio smart card, consente di creare un sistema più sicuro. Dopo aver recuperato una password per una determinata sessione, la scheda può essere rimossa, eliminando così la possibilità che un intruso possa accedervi.

 

 
