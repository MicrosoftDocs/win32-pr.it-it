---
description: Diverse funzioni forniscono servizi per la gestione dello stato di un archivio certificati.
ms.assetid: bae3d693-31b3-4c1d-9a8f-0dafa8bb6897
title: Gestione dello stato di un archivio certificati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75cbbb41691b66abfa2d49d669b13ec7fd438bd4ae503bf944d9e4923f647f29
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119425671"
---
# <a name="managing-a-certificate-store-state"></a>Gestione dello stato di un archivio certificati

Diverse funzioni forniscono servizi per la gestione dello stato [*di un archivio*](../secgloss/c-gly.md) [*certificati.*](../secgloss/s-gly.md)

Per ottenere l'accesso ai certificati, l'archivio certificati in cui sono archiviati deve essere aperto tramite una chiamata a [**CertOpenStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certopenstore) o [**CertOpenSystemStore.**](/windows/desktop/api/Wincrypt/nf-wincrypt-certopensystemstorea)

In genere un archivio certificati viene aperto nella memoria memorizzata nella cache. Può trattarsi di un nuovo archivio o il relativo contenuto può essere caricato dal Registro di sistema locale, dal Registro di sistema in un computer remoto, da un file su disco, da un messaggio PKCS 7 o da \# un'altra origine.

Le funzioni dell'archivio certificati CryptoAPI consentono inoltre a un archivio di mantenere i certificati all'esterno della memoria memorizzata nella cache, ad esempio in un database esterno di certificati, ad esempio quello fornito dal database del server dei certificati Microsoft.

Uno dei parametri della funzione [**CertOpenStore,**](/windows/desktop/api/Wincrypt/nf-wincrypt-certopenstore) *lpszStoreProvider,* determina il tipo di archivio aperto e il provider usato per aprire l'archivio. Per esempi di apertura di archivi certificati con vari provider, vedere [Codice C di esempio per l'apertura di archivi certificati.](example-c-code-for-opening-certificate-stores.md)

[**CertCloseStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certclosestore) chiude un archivio certificati. Quando un archivio certificati viene chiuso, il conteggio [](../secgloss/r-gly.md) dei riferimenti di ognuno dei contesti di certificato in tale archivio viene ridotto di uno. La memoria viene liberata per i certificati il cui conteggio dei riferimenti è pari a zero.

L'impostazione di CERT CLOSE STORE FORCE FLAG con \_ \_ \_ \_ [**CertCloseStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certclosestore) chiude l'archivio certificati e libera memoria per tutti i contesti di certificato indipendentemente dal numero di riferimenti. In alcuni casi, ad esempio nei programmi multithreading, questa operazione non può essere utile. Se CERT CLOSE STORE CHECK FLAG è impostato, l'archivio viene chiuso, ma la funzione restituisce un valore di avviso se la memoria è ancora allocata per i certificati i cui conteggi dei riferimenti non sono stati ridotti \_ \_ a \_ \_ zero. Se il conteggio dei riferimenti di un certificato è maggiore di zero, non è stato liberato un duplicato del contesto del certificato. Usare [**CertFreeCertificateContext,**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfreecertificatecontext) [**CertFreeCRLContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfreecrlcontext)e [**CertFreeCTLContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfreectlcontext) per liberare tutti i certificati lasciati aperti.

> [!Note]
> Un [*contesto del*](../secgloss/c-gly.md) certificato è una struttura di tipo [**CERT \_ CONTEXT**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context) che include, tra gli altri membri, un puntatore al [*BLOB*](../secgloss/c-gly.md) del certificato codificato e un puntatore a una [**struttura CERT \_ INFO.**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_info) La **struttura CERT \_ INFO** contiene i dati del certificato più significativi. Per altre informazioni [*sulle*](../secgloss/c-gly.md)strutture di contesto del certificato, dell'elenco di [*revoche*](../secgloss/c-gly.md) di certificati (CRL) e dell'elenco di certificati attendibili (CTL), vedere Codifica e decodifica di un [contesto di certificato.](encoding-and-decoding-a-certificate-context.md) [](../secgloss/c-gly.md)
> 
> Ogni contesto certificato contiene anche [*un conteggio*](../secgloss/r-gly.md) dei riferimenti che indica il numero di copie dell'indirizzo del contesto assegnato. Ogni volta che un contesto del certificato viene duplicato in qualsiasi modo, il conteggio dei riferimenti viene incrementato di uno. Ogni volta che viene liberato un puntatore a un contesto di certificato, il conteggio dei riferimenti nel contesto del certificato viene decrementato di uno. Quando il conteggio dei riferimenti in un contesto del certificato raggiunge lo zero, la memoria che contiene il contesto viene deallocato. Anche la memoria allocata per un contesto certificato viene deallocato quando tale contesto si trova in un archivio e l'archivio viene chiuso tramite CERT \_ CLOSE \_ STORE FORCE \_ \_ FLAG. Se la memoria per un contesto viene deallocato e i puntatori a tale contesto sono ancora in uso, tali puntatori non sono più validi.

 

[**CertDuplicateStore aumenta**](/windows/desktop/api/Wincrypt/nf-wincrypt-certduplicatestore) il [*numero di riferimenti*](../secgloss/r-gly.md) nell'archivio.

[**CertSaveStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certsavestore) salva il contenuto di un archivio in un file su disco o in un percorso di memoria e

[**CertControlStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certcontrolstore) gestisce un archivio mentre è aperto. Un'applicazione con un archivio aperto può ricevere una notifica quando lo stato persistente di tale archivio è stato modificato da un altro processo. Questo problema può verificarsi se sono stati copiati nuovi certificati nell'archivio del computer locale da un computer di controllo di dominio.

Quando vengono individuate modifiche, l'archivio memorizzato nella cache può sincronizzare nuovamente l'archivio memorizzato nella cache in modo che corrisponda allo stato persistente dell'archivio. [**CertControlStore supporta**](/windows/desktop/api/Wincrypt/nf-wincrypt-certcontrolstore) anche un processo che copia le modifiche dell'archivio memorizzate nella cache nell'archiviazione permanente quando queste modifiche nell'archivio memorizzato nella cache non vengono salvate automaticamente.

I contesti di certificato simili all'archivio certificati possono avere proprietà estese. [**CertSetStoreProperty aggiunge**](/windows/desktop/api/Wincrypt/nf-wincrypt-certsetstoreproperty) proprietà estese a un archivio certificati. [**CertGetStoreProperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetstoreproperty) recupera tutte le proprietà impostate in un archivio certificati. Attualmente, l'unica proprietà predefinita dell'archivio certificati è il nome localizzato di un archivio.

 

 
