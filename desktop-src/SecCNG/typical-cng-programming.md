---
description: L'API CNG implementa un modello di provider estendibile che consente di caricare un provider specificando l'algoritmo di crittografia necessario anziché un provider specifico.
ms.assetid: a88a089b-4afe-4201-96f7-97f19bce18a1
title: Programmazione CNG tipica
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1119da63ca1ea0613444b150914c06664f36c121
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751658"
---
# <a name="typical-cng-programming"></a>Programmazione CNG tipica

L'API CNG implementa un modello di provider estendibile che consente di caricare un provider specificando l'algoritmo di crittografia necessario anziché un provider specifico. Il vantaggio è che un provider di algoritmi può essere sostituito o aggiornato e non sarà necessario modificare il codice in alcun modo per usare il nuovo provider. Inoltre, se in futuro è stato determinato un algoritmo non sicuro, è possibile installare una versione più sicura di tale algoritmo senza influire sul codice. La maggior parte delle API CNG richiede un provider o un oggetto creato da un provider.

I passaggi tipici per l'uso dell'API CNG per le operazioni primitive crittografiche sono i seguenti:

1.  Apertura del provider di algoritmi
2.  Recupero o impostazione delle proprietà degli algoritmi
3.  Creazione o importazione di una chiave
4.  Esecuzione di operazioni di crittografia
5.  Chiusura del provider di algoritmi

Per ulteriori informazioni, vedere esempi di programmazione.

## <a name="opening-the-algorithm-provider"></a>Apertura del provider di algoritmi

La funzione [**BCryptOpenAlgorithmProvider**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptopenalgorithmprovider) fornisce un handle del provider di algoritmi usato nelle API CNG successive, ad esempio [**BCryptCreateHash**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptcreatehash) o [**BCryptGenerateKeyPair**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptgeneratekeypair).

## <a name="getting-or-setting-algorithm-properties"></a>Recupero o impostazione delle proprietà degli algoritmi

È possibile usare l'handle del provider dell'algoritmo per ottenere i dettagli di implementazione per l'algoritmo, ad esempio la dimensione della chiave o la modalità operativa corrente. Usare la funzione [**BCryptGetProperty**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptgetproperty) per ottenere proprietà specifiche.

È inoltre possibile modificare le proprietà dell'algoritmo. Se, ad esempio, si vuole usare il concatenamento di crittografia a blocchi ECB con AES, impostare la proprietà **\_ \_ modalità di concatenamento di BCRYPT** di un algoritmo AES su **BCRYPT \_ Chain \_ mode \_ BCE**; la proprietà viene assegnata a tutte le chiavi AES create usando questo handle dell'algoritmo, senza la necessità di configurare ogni chiave AES. Per modificare queste proprietà, usare la funzione [**BCryptSetProperty**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptsetproperty) .

## <a name="creating-or-importing-a-key"></a>Creazione o importazione di una chiave

A seconda del tipo di algoritmo utilizzato, potrebbe essere necessario creare o caricare una chiave. Ad esempio, la funzione [**BCryptEncrypt**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptencrypt) accetta un handle di chiave per il primo parametro. Se si desidera che la funzione crittografa i dati con un algoritmo di crittografia simmetrica, ad esempio AES, è necessario innanzitutto ottenere una chiave. Il modo in cui si ottiene la chiave dipende dal tipo di algoritmo utilizzato e dall'origine della chiave.

È possibile creare chiavi effimere con le funzioni [**BCryptGenerateSymmetricKey**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptgeneratesymmetrickey) e [**BCryptGenerateKeyPair**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptgeneratekeypair) . È anche possibile importare chiavi effimere da un BLOB di memoria con le funzioni [**BCryptImportKey**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptimportkey) e [**BCryptImportKeyPair**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptimportkeypair) .

Per le chiavi salvate in modo permanente, usare le funzioni di archiviazione chiavi per caricare un provider di archiviazione chiavi e quindi creare o caricare le chiavi. È anche possibile usare queste funzioni per creare o caricare chiavi effimere passando **null** per i nomi dei contenitori. Per altre informazioni sulle funzioni di archiviazione delle chiavi, vedere [funzioni di archiviazione delle chiavi CNG](cng-key-storage-functions.md).

## <a name="performing-cryptographic-operations"></a>Esecuzione di operazioni di crittografia

A questo punto è possibile eseguire l'operazione di crittografia, ad esempio crittografare o decrittografare i dati usando rispettivamente le funzioni [**BCryptEncrypt**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptencrypt) o [**BCryptDecrypt**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptdecrypt) .

## <a name="closing-the-algorithm-provider"></a>Chiusura del provider di algoritmi

Quando il provider non è più necessario, è necessario passare l'handle alla funzione [**BCryptCloseAlgorithmProvider**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptclosealgorithmprovider) per chiudere il provider. In questo modo il provider rilascia tutte le risorse allocate per l'istanza del provider dell'algoritmo. Una volta chiuso, un handle del provider non può essere riutilizzato.

Il caricamento di un provider può essere un processo relativamente lungo. È pertanto necessario memorizzare nella cache tutti gli handle del provider a cui si fa riferimento più volte nel corso della durata dell'applicazione.

## <a name="programming-examples"></a>Esempi di programmazione

Negli esempi seguenti viene descritto come eseguire operazioni di crittografia specifiche utilizzando CNG.

-   [Creazione di un hash con CNG](creating-a-hash-with-cng.md)
-   [Firma di dati con CNG](signing-data-with-cng.md)
-   [Crittografia dei dati con CNG](encrypting-data-with-cng.md)

 

 



