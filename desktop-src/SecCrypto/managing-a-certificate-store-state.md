---
description: Diverse funzioni forniscono servizi per la gestione dello stato di un archivio certificati.
ms.assetid: bae3d693-31b3-4c1d-9a8f-0dafa8bb6897
title: Gestione dello stato di un archivio certificati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53d66e40817f0f92f48e8841455998eff4dbffd6
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/05/2021
ms.locfileid: "103968992"
---
# <a name="managing-a-certificate-store-state"></a>Gestione dello stato di un archivio certificati

Diverse funzioni forniscono servizi per la gestione [*dello stato*](../secgloss/s-gly.md)di un [*archivio certificati*](../secgloss/c-gly.md) .

Per ottenere l'accesso ai certificati, è necessario aprire l'archivio certificati in cui sono archiviati tramite una chiamata a [**CertOpenStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certopenstore) o [**CertOpenSystemStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certopensystemstorea).

Un archivio certificati viene in genere aperto nella memoria memorizzata nella cache. Può essere un nuovo archivio o il relativo contenuto può essere caricato dal registro di sistema locale, dal registro di sistema in un computer remoto, da un file su disco, da un \# messaggio PKCS 7 o da un'altra origine.

Le funzioni dell'archivio certificati CryptoAPI consentono inoltre a un archivio di mantenere certificati al di fuori della memoria memorizzata nella cache, ad esempio, un database esterno di certificati come quello fornito dal database del server di certificazione Microsoft.

Uno dei parametri della funzione [**CertOpenStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certopenstore) , *lpszStoreProvider,* determina il tipo di archivio aperto e il provider utilizzato per aprire tale archivio. Per esempi di apertura di archivi certificati con diversi provider, vedere [codice C di esempio per l'apertura di archivi certificati](example-c-code-for-opening-certificate-stores.md).

[**CertCloseStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certclosestore) chiude un archivio certificati. Quando un archivio certificati viene chiuso, ogni contesti di certificato in tale archivio ha un [*conteggio dei riferimenti*](../secgloss/r-gly.md) ridotto di uno. La memoria viene liberata per i certificati il cui conteggio dei riferimenti va a zero.

L'impostazione \_ \_ del flag di chiusura \_ dell'archivio del certificato \_ con [**CertCloseStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certclosestore) chiude l'archivio certificati e libera la memoria per tutti i contesti di certificato indipendentemente dal conteggio dei riferimenti. In alcuni casi, ad esempio nei programmi multithread, questa operazione non può essere utile. Se \_ \_ \_ è impostato il flag di controllo CERT Close Store \_ , l'archivio viene chiuso, ma un valore di avviso viene restituito dalla funzione se la memoria è ancora allocata per i certificati i cui conteggi dei riferimenti non sono stati ridotti a zero. Se il conteggio dei riferimenti di un certificato è maggiore di zero, non è stato liberato un duplicato del contesto del certificato. Usare [**CertFreeCertificateContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfreecertificatecontext), [**CertFreeCRLContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfreecrlcontext)e [**CertFreeCTLContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfreectlcontext) per liberare tutti i certificati rimasti aperti.

> [!Note]
> Un [*contesto del certificato*](../secgloss/c-gly.md) è una struttura di [**tipo \_ contesto**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context) del certificato che include, tra gli altri membri, un puntatore al [*BLOB di certificati*](../secgloss/c-gly.md) codificati e un puntatore a una struttura di [**\_ informazioni**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_info) sul certificato. La struttura delle **\_ informazioni** del certificato contiene i dati del certificato più significativi. Per ulteriori informazioni sulle strutture di [*contesto di certificato*](../secgloss/c-gly.md), elenco di [*revoche di certificati*](../secgloss/c-gly.md) (CRL) e [*elenco certificati attendibili*](../secgloss/c-gly.md) (CTL), vedere [codifica e decodifica di un contesto del certificato](encoding-and-decoding-a-certificate-context.md).
> 
> Ogni contesto del certificato contiene anche un [*conteggio dei riferimenti*](../secgloss/r-gly.md) che indica il numero di copie dell'indirizzo del contesto che sono state assegnate. Ogni volta che un contesto del certificato viene duplicato in qualsiasi modo, il conteggio dei riferimenti viene incrementato di uno. Ogni volta che viene liberato un puntatore a un contesto di certificato, il conteggio dei riferimenti nel contesto del certificato viene decrementato di uno. Quando il conteggio dei riferimenti in un contesto di certificato raggiunge lo zero, la memoria che contiene il contesto viene deallocata. La memoria allocata per un contesto di certificato viene anche deallocata quando tale contesto si trova in un archivio e l'archivio viene chiuso utilizzando il \_ flag di chiusura dell' \_ Archivio CERT \_ \_ . Se la memoria per un contesto è deallocata e i puntatori a tale contesto sono ancora in uso, tali puntatori non saranno più validi.

 

[**CertDuplicateStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certduplicatestore) aumenta il [*conteggio dei riferimenti*](../secgloss/r-gly.md) nell'archivio.

[**CertSaveStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certsavestore) Salva il contenuto di un archivio in un file su disco o in una posizione di memoria e

[**CertControlStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certcontrolstore) gestisce un archivio mentre è aperto. Un'applicazione con un archivio aperto può ricevere una notifica quando lo stato permanente di tale archivio è stato modificato da un altro processo. Questo problema può verificarsi se i nuovi certificati sono stati copiati nell'archivio del computer locale da un computer di controllo del dominio.

Quando vengono individuate le modifiche, l'archivio memorizzato nella cache può sincronizzare nuovamente l'archivio memorizzato nella cache in modo che corrisponda allo stato permanente dell'archivio. [**CertControlStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certcontrolstore) supporta anche un processo che copia le modifiche dell'archivio memorizzato nella cache in un archivio permanente quando queste modifiche nell'archivio memorizzato nella cache non vengono salvate automaticamente.

I contesti di certificato di tipo archivio certificati possono avere proprietà estese. [**CertSetStoreProperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certsetstoreproperty) aggiunge le proprietà estese a un archivio certificati. [**CertGetStoreProperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetstoreproperty) recupera tutte le proprietà impostate in un archivio certificati. Attualmente, l'unica proprietà dell'archivio certificati predefinita è il nome localizzato di un archivio.

 

 
