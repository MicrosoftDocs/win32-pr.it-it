---
description: La memoria che appartiene a un processo è protetta in modo implicito dal relativo spazio di indirizzi virtuali privato.
ms.assetid: 70ded07a-7be6-4189-a1ae-281917f42a1e
title: Protezione della memoria
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4421b07ee4ed88dffe0e46d1121d5d4117b471a84ffcf4f85738bd8be912f09c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117809072"
---
# <a name="memory-protection"></a>Protezione della memoria

La memoria che appartiene a un processo è protetta in modo implicito dal relativo spazio di indirizzi virtuali privato. Inoltre, Windows protezione della memoria tramite l'hardware della memoria virtuale. L'implementazione di questa protezione varia a seconda del processore, ad esempio le code-pages nello spazio degli indirizzi di un processo possono essere contrassegnate come di sola lettura e protette dalla modifica da thread in modalità utente.

Per l'elenco completo degli attributi, vedere [Costanti di protezione della memoria](memory-protection-constants.md).

## <a name="copy-on-write-protection"></a>Protezione da copia in scrittura

La protezione da copia in scrittura è un'ottimizzazione che consente a più processi di eseguire il mapping dei propri spazi indirizzi virtuali in modo da condividere una pagina fisica fino a quando uno dei processi non modifica la pagina. Questo fa parte di una tecnica denominata *valutazione differita,* che consente al sistema di risparmiare memoria fisica e tempo, non eseguendo un'operazione fino a quando non è assolutamente necessario.

Si supponga, ad esempio, che due processi carichino le pagine dalla stessa DLL nei rispettivi spazi di memoria virtuale. Queste pagine di memoria virtuale vengono mappate alle stesse pagine di memoria fisica per entrambi i processi. Finché nessuno dei due processi scrive in queste pagine, è possibile eseguire il mapping a e condividere le stesse pagine fisiche, come illustrato nel diagramma seguente.

![caselle e frecce del processo 1 e 2 pagine mappate alla stessa memoria fisica](images/mem1.png)

Se il processo 1 scrive in una di queste pagine, il contenuto della pagina fisica viene copiato in un'altra pagina fisica e la mappa della memoria virtuale viene aggiornata per il processo 1. Entrambi i processi hanno ora la propria istanza della pagina nella memoria fisica. Pertanto, non è possibile che un processo scrivo in una pagina fisica condivisa e che l'altro processo veda le modifiche.

![caselle e frecce di processi e modifica del mapping della memoria fisica](images/mem2.png)

## <a name="loading-applications-and-dlls"></a>Caricamento di applicazioni e DLL

Quando vengono caricate più istanze della stessa applicazione Windows basata su , ogni istanza viene eseguita nel proprio spazio di indirizzi virtuali protetto. Tuttavia, gli handle di istanza (*hInstance*) hanno in genere lo stesso valore. Questo valore rappresenta l'indirizzo di base dell'applicazione nello spazio di indirizzi virtuali. Se ogni istanza può essere caricata nell'indirizzo di base predefinito, può eseguire il mapping a e condividere le stesse pagine fisiche con le altre istanze, usando la protezione da copia in scrittura. Il sistema consente a queste istanze di condividere le stesse pagine fisiche fino a quando una di esse non modifica una pagina. Se per qualche motivo una di queste istanze non può essere caricata nell'indirizzo di base desiderato, riceve le proprie pagine fisiche.

Le DLL vengono create con un indirizzo di base predefinito. Ogni processo che usa una DLL tenterà di caricare la DLL all'interno del proprio spazio indirizzi in corrispondenza dell'indirizzo virtuale predefinito per la DLL. Se più applicazioni possono caricare una DLL all'indirizzo virtuale predefinito, possono condividere le stesse pagine fisiche per la DLL. Se per qualche motivo un processo non riesce a caricare la DLL all'indirizzo predefinito, carica la DLL altrove. La protezione da copia in scrittura forza la copia di alcune pagine della DLL in pagine fisiche diverse per questo processo, perché le correzioni per le istruzioni di salto vengono scritte all'interno delle pagine della DLL e saranno diverse per questo processo. Se la sezione di codice contiene molti riferimenti alla sezione dei dati, l'intera sezione di codice può essere copiata in nuove pagine fisiche.

 

 



