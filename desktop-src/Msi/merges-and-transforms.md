---
description: Il Windows Installer conserva tutte le informazioni sull'installazione di in un database relazionale. È possibile modificare il database e, di conseguenza, l'installazione utilizzando le trasformazioni e le unioni.
ms.assetid: 32163e06-d03d-4b65-b744-62f306f2100d
title: Unioni e trasformazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aec6314e81afb5afa9d74346b64fe3129ba5ed30
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318659"
---
# <a name="merges-and-transforms"></a>Unioni e trasformazioni

Il Windows Installer conserva tutte le informazioni sull'installazione di in un database relazionale. È possibile modificare il database e, di conseguenza, l'installazione utilizzando le trasformazioni e le unioni.

## <a name="transforms"></a>Trasformazioni

Una [trasformazione del database](database-transforms.md) aggiunge o sostituisce gli elementi nel database originale. Una trasformazione, ad esempio, può modificare tutto il testo dell'interfaccia utente di un'applicazione da Francese a inglese.

Gli utilizzi primari per le trasformazioni includono:

-   Personalizzazione dei pacchetti di installazione di base per determinati gruppi di utenti.

    Le trasformazioni possono essere utilizzate per incapsulare le varie personalizzazioni di un singolo pacchetto di base richieste da gruppi di utenti diversi. Ad esempio, questa operazione è utile nelle organizzazioni in cui i reparti del supporto Finance e del personale richiedono installazioni diverse di un determinato prodotto. Il pacchetto di base di un prodotto può essere disponibile per tutti gli utenti in un punto di installazione amministrativa con personalizzazioni appropriate distribuite a ogni gruppo di utenti separatamente.

-   Sincronizzazione di applicazioni in più lingue.

    Le trasformazioni sono utili per mantenere i pacchetti creati in posizioni ampiamente separate sincronizzate durante la creazione. Se, ad esempio, un aggiornamento viene sviluppato per la prima volta in una versione in lingua inglese di un'applicazione presente in inglese e francese, è possibile applicare una trasformazione alla versione in lingua inglese aggiornata che la converte in una versione francese aggiornata.

    È possibile applicare più trasformazioni a un pacchetto di base e quindi applicarle in tempo reale durante l'installazione. Questo consente di estendere le funzionalità del programma di installazione per creare pacchetti personalizzati e fornisce un meccanismo per assegnare in modo efficiente le installazioni più appropriate a diversi gruppi di utenti.

-   Applicazione di patch.

    Le trasformazioni possono essere utilizzate per applicare una correzione secondaria a un'applicazione che non richiede un aggiornamento importante. Per ulteriori informazioni sulle patch, vedere la pagina relativa ai [pacchetti di patch](patch-packages.md).

## <a name="merges"></a>Unioni

Un'Unione combina due database in un unico database e aggiunge, anziché sostituire, le informazioni. Se le stesse informazioni sono presenti in entrambi i database, si verifica un conflitto di merge. Le unioni sono utili per i team di sviluppo perché consentono a un'applicazione di grandi dimensioni di essere divisa in parti che possono essere ricombinate in un secondo momento. Ad esempio, gli elementi del database per l'installazione di un nuovo componente possono essere sviluppati separatamente e successivamente Uniti nel database di installazione principale. Per altre informazioni, vedere [merge modules](merge-modules.md).

Un team di sviluppo può applicare un'operazione di Unione nel modo seguente:

1.  Separa i gruppi e lavora simultaneamente su componenti diversi di un'applicazione di grandi dimensioni.
2.  Ogni gruppo di sviluppo compila quindi un database con le informazioni di installazione per il proprio componente, senza preoccuparsi degli altri componenti dell'applicazione.
3.  Una volta completato lo sviluppo di un componente, il database del componente può essere Unito nel database di installazione principale per l'intera applicazione.

 

 



