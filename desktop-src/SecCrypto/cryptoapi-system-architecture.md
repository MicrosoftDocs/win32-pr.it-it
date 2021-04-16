---
description: Viene illustrata l'architettura del sistema CryptoAPI.
ms.assetid: 244329bb-fc71-4ab9-8831-a9478108ffa3
title: Architettura del sistema CryptoAPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86d5dcf1756c9b581d75d4e52d57fbce089976a3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104343141"
---
# <a name="cryptoapi-system-architecture"></a>Architettura del sistema CryptoAPI

L'architettura di sistema CryptoAPI è costituita da cinque aree funzionali principali:

-   [Funzioni di crittografia di base](#base-cryptographic-functions)
-   [Funzioni codifica/decodifica certificati](#certificate-encodedecode-functions)
-   [Funzioni dell'archivio certificati](#certificate-store-functions)
-   [Funzioni di messaggio semplificate](#simplified-message-functions)
-   [Funzioni di messaggio di basso livello](#low-level-message-functions)

## <a name="base-cryptographic-functions"></a>Funzioni di crittografia di base

-   *Funzioni di contesto* utilizzate per la connessione a un CSP. Queste funzioni consentono alle applicazioni di scegliere un CSP specifico in base al nome o di scegliere un CSP specifico che può fornire una classe necessaria di funzionalità.
-   [*Funzioni di generazione*](../secgloss/k-gly.md) delle chiavi utilizzate per generare e archiviare le [*chiavi crittografiche*](../secgloss/c-gly.md). Il supporto completo è incluso per modificare le [*modalità di concatenamento*](../secgloss/c-gly.md), i [*vettori di inizializzazione*](../secgloss/i-gly.md)e altre funzionalità di crittografia. Per altre informazioni, vedere [generazione di chiavi e funzioni di Exchange](cryptography-functions.md).
-   *Funzioni di scambio* delle chiavi usate per scambiare o trasmettere chiavi. Per altre informazioni, vedere [archiviazione delle chiavi crittografiche ed Exchange](cryptographic-key-storage-and-exchange.md) e [funzioni di generazione e scambio di chiavi](cryptography-functions.md).

## <a name="certificate-encodedecode-functions"></a>Funzioni codifica/decodifica certificati

-   Funzioni usate per crittografare o decrittografare i dati. È incluso anche il supporto per l' [*hashing*](../secgloss/h-gly.md) dei dati. Per altre informazioni, vedere [funzioni di crittografia](cryptography-functions.md) e decrittografia dei dati e [crittografia e decrittografia dei dati](data-encryption-and-decryption.md).

## <a name="certificate-store-functions"></a>Funzioni dell'archivio certificati

-   Funzioni utilizzate per gestire le raccolte di certificati digitali. Per ulteriori informazioni, vedere [certificati digitali](digital-certificates.md) e [funzioni di archivio certificati](cryptography-functions.md).

## <a name="simplified-message-functions"></a>Funzioni di messaggio semplificate

-   Funzioni utilizzate per crittografare e decrittografare i messaggi e i dati.
-   Funzioni utilizzate per firmare messaggi e dati.
-   Funzioni utilizzate per verificare l'autenticità delle firme nei messaggi ricevuti e nei dati correlati.

Per ulteriori informazioni, vedere [messaggi semplificati](simplified-messages.md) e [funzioni di messaggio semplificate](cryptography-functions.md).

## <a name="low-level-message-functions"></a>Funzioni di messaggio di basso livello

-   Funzioni utilizzate per eseguire tutte le attività eseguite dalle funzioni di messaggio semplificate. Le funzioni di messaggio di basso livello offrono maggiore flessibilità rispetto alle funzioni di messaggio semplificate, ma richiedono più chiamate di funzione. Per ulteriori informazioni, vedere [messaggi di basso livello](low-level-messages.md) e [funzioni di messaggio di basso livello](cryptography-functions.md).

![architettura CryptoAPI](images/cryparch.png)

Ogni area funzionale ha una parola chiave nel nome della funzione che ne indica l'area funzionale.



| Area funzionale              | Convenzione nome funzione |
|------------------------------|--------------------------|
| Funzioni di crittografia di base | Cripta                    |
| Funzioni di codifica/decodifica  | Cripta                    |
| Funzioni dell'archivio certificati  | Archivio                    |
| Funzioni di messaggio semplificate | Message                  |
| Funzioni di messaggio di basso livello  | Msg                      |



 

Le applicazioni utilizzano funzioni in tutte queste aree. Queste funzioni, combinate, costituiscono CryptoAPI. Le [*funzioni di crittografia di base*](../secgloss/b-gly.md) utilizzano i CSP per gli algoritmi di crittografia necessari e per la generazione e l'archiviazione sicura delle [chiavi crittografiche](cryptographic-keys.md).

Vengono utilizzati due tipi diversi di chiavi crittografiche: [*chiavi di sessione*](../secgloss/s-gly.md), utilizzate per una singola crittografia/decrittografia e coppie di [*chiavi pubbliche/private*](../secgloss/p-gly.md), che vengono utilizzate in modo più permanente.

> [!Note]  
> Sebbene un'applicazione possa comunicare direttamente con una delle cinque aree funzionali, non può comunicare direttamente con un CSP. Tutte le comunicazioni da applicazione a CSP avvengono tramite le [*funzioni di crittografia di base*](../secgloss/b-gly.md). Le funzioni di crittografia di base dispongono di un parametro che specifica il CSP da usare. Questo parametro può essere impostato su **null** per selezionare un CSP predefinito.

 

 

 
