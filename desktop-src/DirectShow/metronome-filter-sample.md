---
description: Esempio di filtro metronomo
ms.assetid: bb279898-875a-4ce4-ac69-6c58f640fbbd
title: Esempio di filtro metronomo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 361b46aafa84590243cfcc05445d91a56ce56e83
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106303993"
---
# <a name="metronome-filter-sample"></a>Esempio di filtro metronomo

## <a name="description"></a>Descrizione

Questo filtro di esempio Mostra come implementare un orologio di riferimento. Il filtro usa l'input del microfono predefinito per ascoltare i picchi audio (ad esempio clic, applausi delle mani o tosse), che usa per determinare una frequenza di clock.

## <a name="usage"></a>Utilizzo

Compilare il progetto di esempio e copiare la DLL di filtro (Metronom.ax) nella directory di sistema di Windows. Eseguire il file Metronom. reg per registrare la DLL.

Per utilizzare il filtro:

1.  Creare un grafico di filtro in GraphEdit che esegue il rendering di un flusso video.
2.  Elimina tutti i flussi audio sottoposti a rendering.
3.  Aggiungere il filtro Metronome al grafico. Viene visualizzato nella categoria filtri DirectShow.
4.  Eseguire il grafo. Il video inizierà a giocare alla velocità normale.
5.  Battere le mani o usare un metronomo per impostare una nuova velocità.

## <a name="programming-notes"></a>Note sulla programmazione

Questo filtro funziona solo per i video. Il renderer audio non è in grado di eseguire la sincronizzazione con frequenze di clock radicalmente differenti.

Se si applaude 92 volte al minuto (una volta ogni ~ 652 MS), il video viene riprodotto alla tariffa normale. È possibile modificare questa impostazione predefinita modificando il valore della costante `BPM` in Metronom. cpp.

Se si smette di applaudire per un certo periodo di tempo e quindi si inizia di nuovo a applaudire, è necessario ricominciare approssimativamente la stessa velocità oppure il filtro lo ignorerà. Inoltre, la velocità di riproduzione del video è limitata dalla velocità della CPU. Se si supera il limite per un determinato periodo di tempo, il filtro smetterà di rispondere alle modifiche di frequenza. In questo caso, arrestare il grafo e riavviare.

Se si implementa un orologio personalizzato, le regole più importanti sono che gli orologi di riferimento non devono tornare indietro. Ovvero non devono mai segnalare un valore di ora minore del valore di ora precedente.

## <a name="downloading-the-sample"></a>Download dell'esempio

Per scaricare gli esempi di DirectShow SDK, installare la versione più recente del [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx).

Questo esempio viene installato nel seguente percorso: *\[ SDK radice \]* \\ Samples \\ Multimedia \\ DirectShow \\ Filters \\ Metronome.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Classe CBaseReferenceClock**](cbasereferenceclock.md)
</dt> <dt>

[Esempi di DirectShow](directshow-samples.md)
</dt> </dl>

 

 



