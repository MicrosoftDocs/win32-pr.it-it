---
description: La memoria che appartiene a un processo è protetta in modo implicito dallo spazio degli indirizzi virtuali privato.
ms.assetid: 70ded07a-7be6-4189-a1ae-281917f42a1e
title: Protezione della memoria
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd30df8084c91a62c28414f4a8142397ee777e52
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104132035"
---
# <a name="memory-protection"></a>Protezione della memoria

La memoria che appartiene a un processo è protetta in modo implicito dallo spazio degli indirizzi virtuali privato. Windows garantisce inoltre la protezione della memoria utilizzando l'hardware della memoria virtuale. L'implementazione di questa protezione varia a seconda del processore. ad esempio, le tabelle codici nello spazio degli indirizzi di un processo possono essere contrassegnate come di sola lettura e protette da modifiche da parte dei thread in modalità utente.

Per l'elenco completo degli attributi, vedere [costanti di protezione della memoria](memory-protection-constants.md).

## <a name="copy-on-write-protection"></a>Protezione copia su scrittura

La protezione copy-on-Write è un'ottimizzazione che consente a più processi di mappare gli spazi degli indirizzi virtuali in modo che condividano una pagina fisica finché uno dei processi non modifica la pagina. Questo fa parte di una tecnica denominata *Lazy Evaluation*, che consente al sistema di conservare la memoria fisica e il tempo senza eseguire un'operazione fino a quando non è assolutamente necessario.

Si supponga ad esempio che due processi carichino pagine dalla stessa DLL negli spazi di memoria virtuale. Queste pagine di memoria virtuale sono mappate alle stesse pagine di memoria fisica per entrambi i processi. Finché nessuno dei due processi scrive in queste pagine, è possibile eseguirne il mapping a e condividere le stesse pagine fisiche, come illustrato nel diagramma seguente.

![caselle e frecce del processo 1 e 2 pagine mappate alla stessa memoria fisica](images/mem1.png)

Se il processo 1 scrive in una di queste pagine, il contenuto della pagina fisica viene copiato in un'altra pagina fisica e la mappa della memoria virtuale viene aggiornata per il processo 1. Entrambi i processi dispongono ora di una propria istanza della pagina nella memoria fisica. Non è pertanto possibile che un processo scriva in una pagina fisica condivisa e che l'altro processo visualizzi le modifiche.

![caselle e frecce dei processi e rimapping della memoria fisica](images/mem2.png)

## <a name="loading-applications-and-dlls"></a>Caricamento di applicazioni e dll

Quando vengono caricate più istanze della stessa applicazione basata su Windows, ogni istanza viene eseguita nello spazio degli indirizzi virtuale protetto. Tuttavia, i rispettivi handle di istanza (*HINSTANCE*) hanno in genere lo stesso valore. Questo valore rappresenta l'indirizzo di base dell'applicazione nello spazio degli indirizzi virtuali. Se ogni istanza può essere caricata nell'indirizzo di base predefinito, può eseguire il mapping a e condividere le stesse pagine fisiche con le altre istanze, usando la protezione copy-on-Write. Il sistema consente a queste istanze di condividere le stesse pagine fisiche fino a quando uno di essi non modifica una pagina. Se per qualche motivo una di queste istanze non può essere caricata nell'indirizzo di base desiderato, riceve le proprie pagine fisiche.

Le dll vengono create con un indirizzo di base predefinito. Ogni processo che utilizza una DLL tenterà di caricare la DLL all'interno del proprio spazio degli indirizzi all'indirizzo virtuale predefinito per la DLL. Se più applicazioni possono caricare una DLL all'indirizzo virtuale predefinito, possono condividere le stesse pagine fisiche per la DLL. Se per qualche motivo un processo non è in grado di caricare la DLL all'indirizzo predefinito, carica la DLL altrove. La protezione tramite copia su scrittura impone la copia di alcune pagine della DLL in pagine fisiche diverse per questo processo, perché le correzioni per le istruzioni di salto vengono scritte nelle pagine della DLL e saranno diverse per questo processo. Se la sezione di codice contiene molti riferimenti alla sezione dati, questa operazione può causare la copia dell'intera sezione di codice in nuove pagine fisiche.

 

 



