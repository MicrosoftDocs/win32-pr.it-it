---
description: La comunicazione comporta spesso grandi quantità di dati o dati di lunghezza sconosciuta.
ms.assetid: e7b12b9e-8caa-4dad-b81f-b609ccb92c9f
title: Uso di SecBufferDesc e SecBuffer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06ad12120414a1e0acb7a6b1cfe211b0ed1787d9e676e8329df1e16ecfef17cd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117785911"
---
# <a name="using-secbufferdesc-and-secbuffer"></a>Uso di SecBufferDesc e SecBuffer

La comunicazione comporta spesso grandi quantità di dati o dati di lunghezza sconosciuta. In entrambi questi casi l'invio e la ricezione di dati vengono evasi in modo analogo o identico. Per gestire la lunghezza sconosciuta e potenzialmente grandi quantità di dati, la comunicazione SSPI viene eseguita usando due strutture, [**SecBufferDesc**](/windows/desktop/api/Sspi/ns-sspi-secbufferdesc) [**e SecBuffer**](/windows/desktop/api/Sspi/ns-sspi-secbuffer).

Una [**struttura SecBufferDesc**](/windows/desktop/api/Sspi/ns-sspi-secbufferdesc) è un contenitore per una matrice di [**strutture SecBuffer.**](/windows/desktop/api/Sspi/ns-sspi-secbuffer) Una **struttura SecBufferDesc** ha i membri seguenti:

-   Numero di versione
-   Numero di [**elementi SecBuffer**](/windows/desktop/api/Sspi/ns-sspi-secbuffer)
-   Indirizzo della matrice di [**strutture SecBuffer**](/windows/desktop/api/Sspi/ns-sspi-secbuffer)

Una [**struttura SecBuffer**](/windows/desktop/api/Sspi/ns-sspi-secbuffer) contiene i tre membri seguenti:

-   Numero di byte nel buffer
-   Tipo di informazioni contenute nell'elemento dati
-   I byte stessi

Un intero messaggio SSPI è spesso costituito da una matrice di [**strutture SecBuffer.**](/windows/desktop/api/Sspi/ns-sspi-secbuffer)

I tipi di dati del buffer seguenti sono definiti come indicato di seguito.



| Tipo di buffer                | Significato                                                                                                                                |
|----------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| SECBUFFER \_ VUOTO           | Non definito, sostituito dalla funzione [*del pacchetto di*](../secgloss/s-gly.md) sicurezza |
| DATI \_ SECBUFFER            | Dati dei pacchetti                                                                                                                            |
| SECBUFFER \_ TOKEN           | Token di sicurezza                                                                                                                         |
| SECBUFFER \_ PKG \_ PARAMS     | Parametri specifici del pacchetto                                                                                                            |
| SECBUFFER \_ MANCANTE         | Indicatore di dati mancante                                                                                                                 |
| SECBUFFER \_ EXTRA           | Dati aggiuntivi                                                                                                                             |
| FLUSSO \_ SECBUFFER          | Dati del flusso di sicurezza                                                                                                                   |
| TRAILER DEL FLUSSO SECBUFFER \_ \_ | Trailer del flusso di sicurezza                                                                                                                |
| INTESTAZIONE DEL \_ FLUSSO \_ SECBUFFER  | Intestazione del flusso di sicurezza                                                                                                                 |



 

I tipi di buffer precedenti possono essere combinati usando un'operazione **OR** bit per bit con uno dei tipi di buffer seguenti.



| Tipo di buffer         | Significato                                                                          |
|---------------------|----------------------------------------------------------------------------------|
| SECBUFFER \_ ATTRMASK | Mascherare gli attributi di sicurezza separando i flag di attributo dal tipo di buffer. |
| SECBUFFER \_ READONLY | Il buffer è di sola lettura                                                              |



 

Prima di ogni chiamata a un'API SSPI che richiede un parametro [**SecBufferDesc,**](/windows/desktop/api/Sspi/ns-sspi-secbufferdesc) vengono dichiarati e inizializzati uno o più elementi della matrice [**SecBuffer.**](/windows/desktop/api/Sspi/ns-sspi-secbuffer) Ad esempio, possono essere presenti due buffer di sicurezza: uno che contiene i dati del messaggio di input e l'altro per il token di sicurezza opaco di output restituito dal pacchetto di sicurezza. L'ordine dei buffer di sicurezza nel descrittore del buffer di sicurezza non è importante, ma ogni buffer deve essere contrassegnato con il tipo appropriato. Un tag di sola lettura può essere usato con qualsiasi buffer di input che non deve essere modificato dal pacchetto [*di sicurezza*](../secgloss/s-gly.md).

La dimensione del buffer di output che dovrebbe contenere il token di sicurezza è importante. Un'applicazione può trovare le dimensioni massime del token per un pacchetto di sicurezza durante la configurazione iniziale. La chiamata a [**EnumerateSecurityPackages**](/windows/desktop/api/Sspi/nf-sspi-enumeratesecuritypackagesa) restituisce una matrice di puntatori alle informazioni del pacchetto di sicurezza. La struttura delle informazioni del pacchetto di sicurezza contiene le dimensioni massime del token per ogni pacchetto. Nell'esempio le informazioni si trova nel **membro cbMaxToken** della [**struttura SecPkgInfo.**](/windows/desktop/api/Sspi/ns-sspi-secpkginfoa) Le stesse informazioni possono essere ottenute in un secondo momento [**usando QuerySecurityPackageInfo**](/windows/desktop/api/Sspi/nf-sspi-querysecuritypackageinfoa).

L'applicazione inizializza i puntatori al buffer e le dimensioni nella descrizione del buffer per indicare dove è possibile trovare i dati del messaggio e altre informazioni.

Per informazioni dettagliate, vedere Codice di esempio [secBuffer e SecBufferDesc](secbuffer-and-secbufferdesc-example-code.md).

 

 
