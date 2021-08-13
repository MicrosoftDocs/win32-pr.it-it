---
description: L'API CNG implementa un modello di provider estendibile che consente di caricare un provider specificando l'algoritmo di crittografia richiesto anziché un provider specifico.
ms.assetid: a88a089b-4afe-4201-96f7-97f19bce18a1
title: Programmazione CNG tipica
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1cd45c68d7c34c3815008690b49cabfefff437222b29512abbf858cf3b370f1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118905522"
---
# <a name="typical-cng-programming"></a>Programmazione CNG tipica

L'API CNG implementa un modello di provider estendibile che consente di caricare un provider specificando l'algoritmo di crittografia richiesto anziché un provider specifico. Il vantaggio è che un provider di algoritmi può essere sostituito o aggiornato e non sarà necessario modificare il codice in alcun modo per usare il nuovo provider. Inoltre, se un algoritmo viene determinato come non sicuro in futuro, è possibile installare una versione più sicura di tale algoritmo senza influire sul codice. La maggior parte delle API CNG richiede un provider o un oggetto creato da un provider.

I passaggi tipici dell'uso dell'API CNG per le operazioni primitive crittografiche sono i seguenti:

1.  Apertura del provider dell'algoritmo
2.  Recupero o impostazione delle proprietà dell'algoritmo
3.  Creazione o importazione di una chiave
4.  Esecuzione di operazioni di crittografia
5.  Chiusura del provider di algoritmi

Per altre informazioni, vedere Esempi di programmazione.

## <a name="opening-the-algorithm-provider"></a>Apertura del provider dell'algoritmo

La [**funzione BCryptOpenAlgorithmProvider**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptopenalgorithmprovider) fornisce un handle del provider di algoritmi usato nelle API CNG successive, ad esempio [**BCryptCreateHash**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptcreatehash) o [**BCryptGenerateKeyPair.**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptgeneratekeypair)

## <a name="getting-or-setting-algorithm-properties"></a>Recupero o impostazione delle proprietà dell'algoritmo

È possibile utilizzare l'handle del provider dell'algoritmo per ottenere i dettagli di implementazione per l'algoritmo, ad esempio le dimensioni della chiave o la modalità di funzionamento corrente. Usare la [**funzione BCryptGetProperty**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptgetproperty) per ottenere proprietà specifiche.

È anche possibile modificare le proprietà dell'algoritmo. Ad esempio, se si vuole usare il concatenamento di crittografia a blocchi DIAS con AES, si imposta la proprietà **BCRYPT \_ CHAINING \_ MODE** di un algoritmo AES su **BCRYPT \_ CHAIN MODE PIÙ \_ \_ CHE** LA PROPRIETÀ viene assegnata a tutte le chiavi AES create usando questo handle di algoritmo, senza la necessità di configurare ogni chiave AES. Usare la [**funzione BCryptSetProperty**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptsetproperty) per modificare queste proprietà.

## <a name="creating-or-importing-a-key"></a>Creazione o importazione di una chiave

A seconda del tipo di algoritmo utilizzato, potrebbe essere necessario creare o caricare una chiave. Ad esempio, la [**funzione BCryptEncrypt**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptencrypt) accetta un handle di chiave per il primo parametro. Se si desidera che tale funzione crittografi i dati con un algoritmo di crittografia simmetrica, ad esempio AES, è prima necessario ottenere una chiave. La modalità di recupero della chiave dipende dal tipo di algoritmo usato e dall'origine della chiave.

È possibile creare chiavi effimere con [**le funzioni BCryptGenerateSymmetricKey**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptgeneratesymmetrickey) e [**BCryptGenerateKeyPair.**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptgeneratekeypair) È anche possibile importare chiavi effimere da un BLOB di memoria con le funzioni [**BCryptImportKey**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptimportkey) e [**BCryptImportKeyPair.**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptimportkeypair)

Per le chiavi persistenti, usare le funzioni di archiviazione delle chiavi per caricare un provider di archiviazione chiavi e quindi creare o caricare le chiavi. È anche possibile usare queste funzioni per creare o caricare chiavi effimere passando **NULL per** i nomi dei contenitori. Per altre informazioni sulle funzioni di archiviazione delle chiavi, vedere [Funzioni di Archiviazione CNG.](cng-key-storage-functions.md)

## <a name="performing-cryptographic-operations"></a>Esecuzione di operazioni di crittografia

È ora possibile eseguire l'operazione di crittografia, ad esempio crittografare o decrittografare i dati usando rispettivamente le funzioni [**BCryptEncrypt**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptencrypt) o [**BCryptDecrypt.**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptdecrypt)

## <a name="closing-the-algorithm-provider"></a>Chiusura del provider di algoritmi

Quando il provider non è più necessario, è necessario passare l'handle alla [**funzione BCryptCloseAlgorithmProvider**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptclosealgorithmprovider) per chiudere il provider. In questo modo il provider rilascia tutte le risorse allocate per l'istanza del provider dell'algoritmo. Dopo la chiusura, un handle del provider non può essere riutilizzato.

Il caricamento di un provider può essere un processo che richiede molto tempo. È quindi consigliabile memorizzare nella cache tutti gli handle di provider a cui si farà riferimento più volte durante la durata dell'applicazione.

## <a name="programming-examples"></a>Esempi di programmazione

Gli esempi seguenti descrivono come eseguire operazioni di crittografia specifiche usando CNG.

-   [Creazione di un hash con CNG](creating-a-hash-with-cng.md)
-   [Firma dei dati con CNG](signing-data-with-cng.md)
-   [Crittografia dei dati con CNG](encrypting-data-with-cng.md)

 

 



