---
description: I contesti di flusso gestiscono i protocolli sicuri orientati al flusso, ad esempio SSL o PCT.
ms.assetid: 05a6b036-1f7f-473f-9813-a1e1534e0f0d
title: Contesti di flusso
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c843889df6aec3f82e8cb8516a7c23ccbf7a6de9957f9a0c572f6e6ca63ac75d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118916680"
---
# <a name="stream-contexts"></a>Contesti di flusso

I contesti di flusso gestiscono i protocolli sicuri orientati al flusso, ad esempio SSL o PCT. Al fine di condividere la stessa interfaccia e una gestione delle credenziali simile, SSPI fornisce il supporto per i contesti di flusso. Il [*protocollo di sicurezza*](../secgloss/s-gly.md) incorpora sia lo schema di autenticazione del flusso che i formati di record.

Per fornire protocolli orientati al flusso, [*i pacchetti di sicurezza che*](../secgloss/s-gly.md) supportano i contesti di flusso hanno le caratteristiche di processo seguenti:

-   Il pacchetto imposta il flag SECPKG \_ FLAG STREAM per indicare che supporta la \_ semantica del flusso.
-   Le applicazioni di trasporto richiede la semantica del flusso impostando i flag ISC REQ STREAM e ASC REQ STREAM nelle chiamate alle funzioni \_ \_ \_ \_ [**InitializeSecurityContext (Generale)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) e [**AcceptSecurityContext (Generale).**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext)
-   L'applicazione chiama la funzione [**QueryContextAttributes (General)**](/windows/win32/api/sspi/nf-sspi-querycontextattributesa) con una struttura [](../secgloss/s-gly.md) [**SecPkgContext \_ StreamSizes**](/windows/desktop/api/Sspi/ns-sspi-secpkgcontext_streamsizes) per eseguire una query sul contesto di sicurezza per il numero di buffer da fornire e le dimensioni da riservare per intestazioni o trailer.
-   L'applicazione fornisce descrittori di buffer da riservare durante l'elaborazione effettiva dei dati. Specificando la semantica del flusso, il chiamante indica la [](../secgloss/s-gly.md) disponibilità a eseguire un'elaborazione aggiuntiva in modo che il pacchetto di sicurezza possa gestire il blocco dei messaggi. In sostanza, per [**le funzioni MakeSignature**](/windows/desktop/api/Sspi/nf-sspi-makesignature) [**e VerifySignature,**](/windows/desktop/api/Sspi/nf-sspi-verifysignature) il chiamante passa un elenco di buffer. Quando un messaggio viene ricevuto da un canale orientato al flusso ,ad esempio una porta TCP, il chiamante passa un elenco di buffer come indicato di seguito.

    | Buffer | Length         | Tipo di buffer      |
    |--------|----------------|------------------|
    | 1      | Lunghezza messaggio | SECBUFFER \_ DATA  |
    | 2      | 0              | SECBUFFER \_ EMPTY |
    | 3      | 0              | SECBUFFER \_ EMPTY |
    | 4      | 0              | SECBUFFER \_ EMPTY |
    | 5      | 0              | SECBUFFER \_ EMPTY |

    

     

    Il pacchetto di sicurezza funziona quindi sul [*BLOB*](../secgloss/b-gly.md). Se la funzione viene restituita correttamente, l'elenco di buffer sarà simile al seguente.

    

    | Buffer | Length         | Tipo di buffer                |
    |--------|----------------|----------------------------|
    | 1      | Lunghezza intestazione  | INTESTAZIONE DEL FLUSSO SECBUFFER \_ \_  |
    | 2      | Lunghezza dei dati    | SECBUFFER \_ DATA            |
    | 3      | Lunghezza trailer | TRAILER DEL FLUSSO SECBUFFER \_ \_ |
    | 4      | 0              | SECBUFFER \_ EMPTY           |
    | 5      | 0              | SECBUFFER \_ EMPTY           |

    

     

    Il pacchetto potrebbe anche aver restituito il buffer 4 con lunghezza x e il tipo di buffer SECBUFFER EXTRA che indica che i dati in questo buffer fanno parte del record successivo e non sono ancora stati \# \_ elaborati. Viceversa, se la funzione message restituisce il codice di errore SEC E INCOMPLETE MESSAGE, l'elenco di buffer restituito \_ \_ sarà simile al \_ seguente.

    

    | Buffer | Length | Tipo di buffer        |
    |--------|--------|--------------------|
    | 1      | x      | SECBUFFER \_ MANCANTE |

    

     

    Ciò indica che erano necessari più dati per elaborare il record. A differenza della maggior parte degli errori restituiti da una funzione di messaggio, questo tipo di buffer non indica che il contesto è stato compromesso. Indica invece che sono necessari più dati. [*I pacchetti di*](../secgloss/s-gly.md) sicurezza non devono aggiornare [*il proprio stato*](../secgloss/s-gly.md) in questa condizione.

    Analogamente, sul lato mittente della comunicazione, il chiamante può chiamare la [**funzione MakeSignature.**](/windows/desktop/api/Sspi/nf-sspi-makesignature) Il pacchetto di sicurezza potrebbe dover riallocare il buffer o copiare elementi. Il chiamante può essere più efficiente fornendo un elenco di buffer come indicato di seguito.

    

    | Buffer | Length         | Tipo                       |
    |--------|----------------|----------------------------|
    | 1      | Lunghezza intestazione  | INTESTAZIONE DEL FLUSSO SECBUFFER \_ \_  |
    | 2      | Lunghezza dei dati    | SECBUFFER \_ DATA            |
    | 3      | Lunghezza trailer | TRAILER DEL FLUSSO SECBUFFER \_ \_ |

    

     

    In questo modo il chiamante può usare i buffer in modo più efficiente. Chiamando la [**funzione QueryContextAttributes**](/windows/win32/api/sspi/nf-sspi-querycontextattributesa) per determinare la quantità di spazio da riservare prima di chiamare [**MakeSignature,**](/windows/desktop/api/Sspi/nf-sspi-makesignature)l'operazione è più efficiente per l'applicazione e il pacchetto di sicurezza.

 

 
