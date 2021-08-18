---
description: Il Windows installer mantiene tutte le informazioni sull'installazione in un database relazionale. È possibile modificare questo database e quindi l'installazione usando trasformazioni e unioni.
ms.assetid: 32163e06-d03d-4b65-b744-62f306f2100d
title: Unioni e trasformazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9779cd901df349b80dba84f056104c316810f8a3f67b19cdd4622dd68480ce1d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119012979"
---
# <a name="merges-and-transforms"></a>Unioni e trasformazioni

Il Windows installer mantiene tutte le informazioni sull'installazione in un database relazionale. È possibile modificare questo database e quindi l'installazione usando trasformazioni e unioni.

## <a name="transforms"></a>Trasformazioni

Una [trasformazione del database](database-transforms.md) aggiunge o sostituisce gli elementi nel database originale. Ad esempio, una trasformazione può modificare tutto il testo nell'interfaccia utente di un'applicazione dal francese all'inglese.

Gli usi primari per le trasformazioni includono:

-   Personalizzazione dei pacchetti di installazione di base per determinati gruppi di utenti.

    Le trasformazioni possono essere usate per incapsulare le varie personalizzazioni di un singolo pacchetto di base richieste da diversi gruppi di utenti. Ad esempio, ciò è utile nelle organizzazioni in cui i reparti di supporto finanziario e del personale richiedono installazioni diverse di un determinato prodotto. Il pacchetto di base di un prodotto può essere disponibile a tutti gli utenti in un unico punto di installazione amministrativa con personalizzazioni appropriate distribuite separatamente a ogni gruppo di utenti.

-   Sincronizzazione delle applicazioni tra più lingue.

    Le trasformazioni sono utili per mantenere sincronizzati i pacchetti creati in posizioni ampiamente separate durante la creazione. Ad esempio, se un aggiornamento viene sviluppato per la prima volta per una versione inglese di un'applicazione esistente in inglese e francese, è possibile applicare una trasformazione alla versione inglese aggiornata che la converte in una versione francese aggiornata.

    È possibile applicare più trasformazioni a un pacchetto di base e quindi applicarsi in tempo reale durante l'installazione. In questo modo si estendono le funzionalità del programma di installazione per creare pacchetti personalizzati e viene fornito un meccanismo per assegnare in modo efficiente le installazioni più appropriate a gruppi diversi di utenti.

-   Applicazione di patch alle applicazioni.

    Le trasformazioni possono essere usate per applicare una correzione secondaria a un'applicazione che non richiede un aggiornamento importante. Per altre informazioni sulle patch, vedere [Patch Packages](patch-packages.md).

## <a name="merges"></a>Unioni

Un'unione combina due database in un unico database e aggiunge, anziché sostituire, informazioni. Se in entrambi i database sono presenti le stesse informazioni, si verifica un conflitto di merge. Le unioni sono utili per i team di sviluppo perché consentono di suddividere un'applicazione di grandi dimensioni in parti che possono essere ricombinate in un secondo momento. Ad esempio, gli elementi del database per l'installazione di un nuovo componente possono essere sviluppati separatamente e successivamente uniti nel database di installazione principale. Per altre informazioni, vedere [Merge Modules](merge-modules.md).

Un team di sviluppo potrebbe applicare un'operazione di unione nel modo seguente:

1.  Separare in gruppi e lavorare contemporaneamente su componenti diversi di un'applicazione di grandi dimensioni.
2.  Ogni gruppo di sviluppo popola quindi un database con le informazioni di installazione per il proprio componente, senza preoccuparsi degli altri componenti dell'applicazione.
3.  Al termine dello sviluppo di un componente, il database di tale componente può essere unito al database di installazione principale per l'intera applicazione.

 

 



