---
description: La comunicazione comporta spesso grandi quantità di dati o dati di lunghezza sconosciuta.
ms.assetid: e7b12b9e-8caa-4dad-b81f-b609ccb92c9f
title: Uso di SecBufferDesc e SecBuffer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ca7d8155a610263838d2baf2a7d1c8fc96ec874
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103883881"
---
# <a name="using-secbufferdesc-and-secbuffer"></a>Uso di SecBufferDesc e SecBuffer

La comunicazione comporta spesso grandi quantità di dati o dati di lunghezza sconosciuta. L'invio e la ricezione di dati vengono eseguiti in modo analogo o identico in entrambi i casi. Per gestire la lunghezza sconosciuta e potenzialmente grandi quantità di dati, la comunicazione SSPI viene eseguita utilizzando due strutture, [**SecBufferDesc**](/windows/desktop/api/Sspi/ns-sspi-secbufferdesc) e [**SecBuffer**](/windows/desktop/api/Sspi/ns-sspi-secbuffer).

Una struttura [**SecBufferDesc**](/windows/desktop/api/Sspi/ns-sspi-secbufferdesc) è un contenitore per una matrice di strutture [**SecBuffer**](/windows/desktop/api/Sspi/ns-sspi-secbuffer) . Una struttura **SecBufferDesc** dispone dei seguenti membri:

-   Numero di versione
-   Numero di elementi [**SecBuffer**](/windows/desktop/api/Sspi/ns-sspi-secbuffer)
-   Indirizzo della matrice di strutture [**SecBuffer**](/windows/desktop/api/Sspi/ns-sspi-secbuffer)

Una struttura [**SecBuffer**](/windows/desktop/api/Sspi/ns-sspi-secbuffer) contiene i tre membri seguenti:

-   Numero di byte nel buffer
-   Tipo di informazioni contenute nell'elemento dati
-   Byte stessi

Un intero messaggio SSPI è spesso costituito da una matrice di strutture [**SecBuffer**](/windows/desktop/api/Sspi/ns-sspi-secbuffer) .

I tipi di dati del buffer seguenti sono definiti nel modo seguente.



| Tipo di buffer                | Significato                                                                                                                                |
|----------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| SECBUFFER \_ vuoto           | Non definito, sostituito dalla funzione del [*pacchetto di sicurezza*](../secgloss/s-gly.md) |
| \_dati SECBUFFER            | Dati dei pacchetti                                                                                                                            |
| \_token SECBUFFER           | Token di sicurezza                                                                                                                         |
| \_parametri pkg \_ SECBUFFER     | Parametri specifici del pacchetto                                                                                                            |
| SECBUFFER \_ mancante         | Indicatore dati mancante                                                                                                                 |
| SECBUFFER \_ extra           | Dati aggiuntivi                                                                                                                             |
| \_flusso SECBUFFER          | Dati del flusso di sicurezza                                                                                                                   |
| \_trailer del flusso SECBUFFER \_ | Trailer del flusso di sicurezza                                                                                                                |
| \_intestazione del flusso SECBUFFER \_  | Intestazione del flusso di sicurezza                                                                                                                 |



 

I tipi di buffer precedenti possono essere combinati utilizzando un'**operazione OR bit per** bit con uno dei seguenti tipi di buffer.



| Tipo di buffer         | Significato                                                                          |
|---------------------|----------------------------------------------------------------------------------|
| \_ATTRMASK SECBUFFER | Mascherare gli attributi di sicurezza separando i flag di attributo dal tipo di buffer. |
| SECBUFFER \_ ReadOnly | Il buffer è di sola lettura                                                              |



 

Prima di ogni chiamata a un'API SSPI che richiede un parametro [**SecBufferDesc**](/windows/desktop/api/Sspi/ns-sspi-secbufferdesc) , vengono dichiarati e inizializzati uno o più elementi della matrice [**SecBuffer**](/windows/desktop/api/Sspi/ns-sspi-secbuffer) . Ad esempio, possono essere presenti due buffer di sicurezza: uno contenente i dati del messaggio di input e l'altro per il token di sicurezza opaco di output restituito dal pacchetto di sicurezza. L'ordine dei buffer di sicurezza nel descrittore del buffer di sicurezza non è importante, ma ogni buffer deve essere contrassegnato con il tipo appropriato. Un tag di sola lettura può essere utilizzato con qualsiasi buffer di input che non deve essere modificato dal [*pacchetto di sicurezza*](../secgloss/s-gly.md).

La dimensione del buffer di output che dovrebbe contenere il token di sicurezza è importante. Un'applicazione è in grado di trovare le dimensioni massime del token per un pacchetto di sicurezza durante l'installazione iniziale. La chiamata a [**EnumerateSecurityPackages**](/windows/desktop/api/Sspi/nf-sspi-enumeratesecuritypackagesa) restituisce una matrice di puntatori alle informazioni sui pacchetti di sicurezza. La struttura delle informazioni del pacchetto di sicurezza contiene le dimensioni massime del token per ogni pacchetto. Nell'esempio le informazioni sono contenute nel membro **cbMaxToken** della struttura [**SecPkgInfo**](/windows/desktop/api/Sspi/ns-sspi-secpkginfoa) . Le stesse informazioni possono essere ottenute in un secondo momento usando [**QuerySecurityPackageInfo**](/windows/desktop/api/Sspi/nf-sspi-querysecuritypackageinfoa).

L'applicazione Inizializza i puntatori e le dimensioni del buffer nella descrizione del buffer per indicare dove è possibile trovare i dati del messaggio e altre informazioni.

Per informazioni dettagliate, vedere il [codice di esempio SecBuffer e SecBufferDesc](secbuffer-and-secbufferdesc-example-code.md).

 

 
