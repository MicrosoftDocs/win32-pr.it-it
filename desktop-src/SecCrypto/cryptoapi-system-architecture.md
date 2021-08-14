---
description: Viene illustrata l'architettura di sistema CryptoAPI.
ms.assetid: 244329bb-fc71-4ab9-8831-a9478108ffa3
title: Architettura di sistema CryptoAPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 791ed0ebfc82df1dc7b6e9600d4e0455ae60df3da35cfe3f8fd613f7b230ebd7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117768808"
---
# <a name="cryptoapi-system-architecture"></a>Architettura di sistema CryptoAPI

L'architettura di sistema CryptoAPI è costituita da cinque aree funzionali principali:

-   [Funzioni di crittografia di base](#base-cryptographic-functions)
-   [Funzioni di codifica/decodifica dei certificati](#certificate-encodedecode-functions)
-   [Funzioni dell'archivio certificati](#certificate-store-functions)
-   [Funzioni dei messaggi semplificate](#simplified-message-functions)
-   [Funzioni di messaggi di basso livello](#low-level-message-functions)

## <a name="base-cryptographic-functions"></a>Funzioni di crittografia di base

-   *Funzioni di contesto* usate per connettersi a un provider di servizi di configurazione. Queste funzioni consentono alle applicazioni di scegliere un CSP specifico in base al nome o di scegliere un CSP specifico in grado di fornire una classe di funzionalità necessaria.
-   [*Funzioni di generazione delle*](../secgloss/k-gly.md) chiavi usate per generare e archiviare [*chiavi crittografiche.*](../secgloss/c-gly.md) Il supporto completo è incluso per la modifica [*delle modalità di concatenamento,*](../secgloss/c-gly.md) [*dei vettori di inizializzazione*](../secgloss/i-gly.md)e di altre funzionalità di crittografia. Per altre informazioni, vedere [Key Generation and Exchange Functions](cryptography-functions.md).
-   *Funzioni di scambio delle chiavi* usate per scambiare o trasmettere chiavi. Per altre informazioni, vedere [Cryptographic Key Archiviazione and Exchange](cryptographic-key-storage-and-exchange.md) and Key Generation and Exchange [Functions](cryptography-functions.md).

## <a name="certificate-encodedecode-functions"></a>Funzioni di codifica/decodifica dei certificati

-   Funzioni usate per crittografare o decrittografare i dati. È incluso anche il supporto per [*l'hashing dei*](../secgloss/h-gly.md) dati. Per altre informazioni, vedere Funzioni di crittografia [e decrittografia dei dati](cryptography-functions.md) e Crittografia e [decrittografia dei dati](data-encryption-and-decryption.md).

## <a name="certificate-store-functions"></a>Funzioni dell'archivio certificati

-   Funzioni usate per gestire raccolte di certificati digitali. Per altre informazioni, vedere [Certificati digitali e](digital-certificates.md) Funzioni [dell'archivio certificati](cryptography-functions.md).

## <a name="simplified-message-functions"></a>Funzioni dei messaggi semplificate

-   Funzioni usate per crittografare e decrittografare messaggi e dati.
-   Funzioni usate per firmare messaggi e dati.
-   Funzioni usate per verificare l'autenticità delle firme nei messaggi ricevuti e nei dati correlati.

Per altre informazioni, vedere [Messaggi semplificati](simplified-messages.md) e [Funzioni semplificate dei messaggi](cryptography-functions.md).

## <a name="low-level-message-functions"></a>Funzioni di messaggi di basso livello

-   Funzioni usate per eseguire tutte le attività eseguite dalle funzioni di messaggio semplificate. Le funzioni di messaggi di basso livello offrono maggiore flessibilità rispetto alle funzioni di messaggio semplificate, ma richiedono più chiamate di funzione. Per altre informazioni, vedere [Messaggi di basso livello e](low-level-messages.md) Funzioni dei messaggi di basso [livello.](cryptography-functions.md)

![Architettura cryptoapi](images/cryparch.png)

Ognuna delle aree funzionali ha una parola chiave nel nome della funzione che ne indica l'area funzionale.



| Area funzionale              | Convenzione del nome di funzione |
|------------------------------|--------------------------|
| Funzioni di crittografia di base | Cripta                    |
| Funzioni di codifica/decodifica  | Cripta                    |
| Funzioni dell'archivio certificati  | Archiviazione                    |
| Funzioni dei messaggi semplificate | Message                  |
| Funzioni di messaggi di basso livello  | Msg                      |



 

Le applicazioni usano funzioni in tutte queste aree. Queste funzioni, riunite, costituiscono CryptoAPI. Le [*funzioni di crittografia di base*](../secgloss/b-gly.md) usano i CSP per gli algoritmi di crittografia necessari e per la generazione e l'archiviazione sicura delle chiavi [crittografiche](cryptographic-keys.md).

Vengono usati due tipi diversi [](../secgloss/s-gly.md)di chiavi crittografiche: le chiavi di sessione , usate per una singola crittografia/decrittografia, e le coppie di chiavi [*pubblica/privata*](../secgloss/p-gly.md), che vengono usate in modo più permanente.

> [!Note]  
> Anche se un'applicazione può comunicare direttamente con una delle cinque aree funzionali, non può comunicare direttamente con un CSP. Tutte le comunicazioni da applicazione a CSP si verificano tramite le [*funzioni di crittografia di base*](../secgloss/b-gly.md). Le funzioni di crittografia di base hanno un parametro che specifica quale provider di servizi di crittografia usare. Questo parametro può essere impostato su **NULL per** selezionare un provider di servizi di configurazione predefinito.

 

 

 
