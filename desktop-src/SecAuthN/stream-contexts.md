---
description: I contesti di flusso gestiscono i protocolli orientati al flusso sicuro, ad esempio SSL o PCT.
ms.assetid: 05a6b036-1f7f-473f-9813-a1e1534e0f0d
title: Contesti di flusso
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53103dc1269c05e5a2c162133d21e167d8035c2c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103967100"
---
# <a name="stream-contexts"></a>Contesti di flusso

I contesti di flusso gestiscono i protocolli orientati al flusso sicuro, ad esempio SSL o PCT. Per condividere la stessa interfaccia e la gestione delle credenziali analoghe, SSPI fornisce supporto per i contesti di flusso. Il [*protocollo di sicurezza*](../secgloss/s-gly.md) incorpora sia lo schema di autenticazione del flusso che i formati di record.

Per fornire i protocolli orientati al flusso, i [*pacchetti di sicurezza*](../secgloss/s-gly.md) che supportano i contesti di flusso hanno le caratteristiche di processo seguenti:

-   Il pacchetto imposta il \_ flag del flusso del flag SECPKG \_ per indicare che supporta la semantica del flusso.
-   Per le applicazioni di trasporto viene richiesta la semantica di flusso impostando il flusso di richiesta \_ di ISC e i flag di flusso per \_ ASC \_ req \_ nelle chiamate alle funzioni [**InitializeSecurityContext (generale)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) e [**AcceptSecurityContext (generale)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext) .
-   L'applicazione chiama la funzione [**QueryContextAttributes (generale)**](/windows/win32/api/sspi/nf-sspi-querycontextattributesa) con una [**struttura \_ StreamSizes di SecPkgContext**](/windows/desktop/api/Sspi/ns-sspi-secpkgcontext_streamsizes) per eseguire una query sul [*contesto di sicurezza*](../secgloss/s-gly.md) per il numero di buffer da fornire e le dimensioni da riservare per le intestazioni o i trailer.
-   L'applicazione fornisce descrittori di buffer da riservare durante l'effettiva elaborazione dei dati. Specificando la semantica del flusso, il chiamante indica la volontà di eseguire un'elaborazione aggiuntiva, in modo che il [*pacchetto di sicurezza*](../secgloss/s-gly.md) possa gestire il blocco dei messaggi. In sostanza, per le funzioni [**MakeSignature**](/windows/desktop/api/Sspi/nf-sspi-makesignature) e [**VerifySignature**](/windows/desktop/api/Sspi/nf-sspi-verifysignature) , il chiamante passa un elenco di buffer. Quando viene ricevuto un messaggio da un canale che è orientato al flusso, ad esempio una porta TCP, il chiamante passa un elenco di buffer come indicato di seguito.

    | Buffer | Length         | Tipo di buffer      |
    |--------|----------------|------------------|
    | 1      | Lunghezza messaggio | \_dati SECBUFFER  |
    | 2      | 0              | SECBUFFER \_ vuoto |
    | 3      | 0              | SECBUFFER \_ vuoto |
    | 4      | 0              | SECBUFFER \_ vuoto |
    | 5      | 0              | SECBUFFER \_ vuoto |

    

     

    Il pacchetto di sicurezza funziona quindi nel [*BLOB*](../secgloss/b-gly.md). Se la funzione viene restituita correttamente, l'elenco dei buffer è simile al seguente.

    

    | Buffer | Length         | Tipo di buffer                |
    |--------|----------------|----------------------------|
    | 1      | Lunghezza intestazione  | \_intestazione del flusso SECBUFFER \_  |
    | 2      | Lunghezza dei dati    | \_dati SECBUFFER            |
    | 3      | Lunghezza trailer | \_trailer del flusso SECBUFFER \_ |
    | 4      | 0              | SECBUFFER \_ vuoto           |
    | 5      | 0              | SECBUFFER \_ vuoto           |

    

     

    Il pacchetto potrebbe avere restituito anche il buffer \# 4 con lunghezza x e tipo di buffer SECBUFFER \_ che indica che i dati in questo buffer fanno parte del record successivo e non sono stati ancora elaborati. Viceversa, se la funzione Message restituisce il \_ codice di errore del \_ messaggio incompleto e del secondo \_ , l'elenco di buffer restituito sarà simile al seguente.

    

    | Buffer | Length | Tipo di buffer        |
    |--------|--------|--------------------|
    | 1      | x      | SECBUFFER \_ mancante |

    

     

    Ciò indica che sono necessari più dati per elaborare il record. A differenza della maggior parte degli errori restituiti da una funzione di messaggio, questo tipo di buffer non indica che il contesto è stato compromesso. Indica invece che sono necessari più dati. i [*pacchetti di sicurezza*](../secgloss/s-gly.md) non devono aggiornare [*lo stato*](../secgloss/s-gly.md) in questa condizione.

    Analogamente, sul lato mittente della comunicazione, il chiamante può chiamare la funzione [**MakeSignature**](/windows/desktop/api/Sspi/nf-sspi-makesignature) . Il pacchetto di sicurezza potrebbe dover riallocare il buffer o copiare le informazioni. Il chiamante può essere più efficiente fornendo un elenco di buffer come indicato di seguito.

    

    | Buffer | Length         | Tipo                       |
    |--------|----------------|----------------------------|
    | 1      | Lunghezza intestazione  | \_intestazione del flusso SECBUFFER \_  |
    | 2      | Lunghezza dei dati    | \_dati SECBUFFER            |
    | 3      | Lunghezza trailer | \_trailer del flusso SECBUFFER \_ |

    

     

    Ciò consente al chiamante di usare i buffer in modo più efficiente. Chiamando la funzione [**QueryContextAttributes**](/windows/win32/api/sspi/nf-sspi-querycontextattributesa) per determinare la quantità di spazio da riservare prima di chiamare [**MakeSignature**](/windows/desktop/api/Sspi/nf-sspi-makesignature), l'operazione risulta più efficiente per l'applicazione e il pacchetto di sicurezza.

 

 
