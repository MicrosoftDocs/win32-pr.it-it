---
description: Esempio di filtro metronome
ms.assetid: bb279898-875a-4ce4-ac69-6c58f640fbbd
title: Esempio di filtro metronome
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ea1b321dd2602829697862e2716c9017573a44b6162b355e78e586e14d85003
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119072985"
---
# <a name="metronome-filter-sample"></a>Esempio di filtro metronome

## <a name="description"></a>Descrizione

Questo filtro di esempio illustra come implementare un clock di riferimento. Il filtro usa l'input predefinito del microfono per ascoltare i picchi audio (ad esempio clic, mani o tosse), che usa per determinare una frequenza di clock.

## <a name="usage"></a>Utilizzo

Compilare il progetto di esempio e copiare la DLL di filtro (Metronom.ax) nella directory Windows di sistema. Eseguire il file Metronom.reg per registrare la DLL.

Per usare il filtro:

1.  Creare un grafo di filtro in GraphEdit che esegue il rendering di un flusso video.
2.  Elimina tutti i flussi audio di cui è stato eseguito il rendering.
3.  Aggiungere il filtro Metronome al grafico. Viene visualizzato nella categoria DirectShow Filtri.
4.  Eseguire il grafo. La riproduzione del video inizierà alla velocità normale.
5.  Clap your hands or use a metronome to set a new speed.

## <a name="programming-notes"></a>Note sulla programmazione

Questo filtro funziona solo per i video. Il renderer audio non è in grado di eseguire la sincronizzazione con frequenze di clock diverse.

Se si clap 92 volte al minuto (una volta ogni ~652 ms), il video verrà riprodotto alla frequenza normale. È possibile modificare questo valore predefinito modificando il valore della costante `BPM` in Metronom.cpp.

Se si interrompe l'affondo per un periodo di tempo e quindi si inizia a stringere di nuovo, è necessario ricominciare dalla stessa velocità. In caso contrario, il filtro lo ignorerà. Inoltre, la velocità di riproduzione video è limitata dalla velocità della CPU. Se si supera il limite per un periodo di tempo qualsiasi, il filtro smetterà di rispondere alle modifiche della frequenza. In questo caso, arrestare il grafico e riavviarlo.

Se si implementa un clock personalizzato, le regole più importanti sono che gli orologi di riferimento non devono tornare indietro. Ciò significa che non devono mai segnalare un valore di ora inferiore al valore dell'ora precedente.

## <a name="downloading-the-sample"></a>Download dell'esempio

Per scaricare gli esempi DirectShow SDK, installare la versione più recente di [Windows SDK.](https://msdn.microsoft.com/windowsvista/bb980924.aspx)

Questo esempio viene installato nel percorso seguente: *\[ SDK Root \]* Samples Multimedia DirectShow Filters \\ \\ \\ \\ \\ Metronome.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Classe CBaseReferenceClock**](cbasereferenceclock.md)
</dt> <dt>

[DirectShow Campioni](directshow-samples.md)
</dt> </dl>

 

 



