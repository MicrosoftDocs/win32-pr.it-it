---
description: ICE67 verifica che la destinazione di un collegamento non annunciato appartenga allo stesso componente del collegamento stesso o che gli attributi del componente di destinazione garantisca che non cambino i percorsi di installazione.
ms.assetid: 3fc462e7-4c11-4167-a157-6c1e0791901d
title: ICE67
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b25f3bba6bd6efaf20b55982524840348f39e8717dc53b7699a6f5f2886df01
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119787391"
---
# <a name="ice67"></a>ICE67

ICE67 verifica che la destinazione di un collegamento non annunciato appartenga allo stesso componente del collegamento stesso o che gli attributi del componente di destinazione garantisca che non cambino i percorsi di installazione.

Se non si corregge un avviso o un errore segnalato da ICE67, il collegamento può non essere valido se il componente di destinazione cambia stato e il componente di origine non lo fa. Ad esempio, quando il componente del file di destinazione è impostato per l'esecuzione dall'origine, una reinstallazione che modifica il componente in locale determina la non reinstallazione del componente contenente il collegamento. Il collegamento punta quindi a una posizione non valida.

Si noti che in alcuni casi è inevitabile usare un componente diverso per il collegamento. Ad esempio, se il collegamento viene creato nel profilo utente e il file viene installato in una directory non di profilo, potrebbe non essere possibile usare lo stesso componente per entrambi i dati. Ciò comporta errori in scenari multi-utente, ad esempio quelli descritti in [ICE57.](ice57.md) In questo caso, è possibile usare i collegamenti annunciati per ottenere il comportamento desiderato oppure assicurarsi semplicemente che il componente di destinazione non possa passare dall'esecuzione dall'origine a quella locale.

## <a name="result"></a>Risultato

ICE67 restituisce un errore o un avviso se la destinazione di un collegamento non annunciato non appartiene allo stesso componente del collegamento stesso o se gli attributi del componente di destinazione non garantiscono che i percorsi di installazione non cambino.

## <a name="example"></a>Esempio

ICE67 segnala l'avviso e gli errori seguenti per l'esempio illustrato.

``` syntax
The shortcut 'Shortcut1' is a non-advertised shortcut with a file target. The shortcut and target are installed by different components, and the target component can run locally or from source.
```

Shortcut1 viene installato da Component2, ma il relativo file di destinazione, File1, viene installato da component1. Il componente di destinazione è contrassegnato come facoltativo, ovvero può essere locale o run-from-source. Una possibile situazione che potrebbe causare un problema è se Component1 cambia da run-from-source a local. In questo modo Shortcut1 fa in modo che punti a una posizione non valida.

Per correggere l'avviso, installare il collegamento come parte di Component1 o contrassegnare Component1 come LocalOnly o SourceOnly.

[Tabella file](file-table.md) (parziale)



| File  | Componente\_ |
|-------|-------------|
| File1 | Componente1  |



 

[Tabella dei collegamenti](shortcut-table.md) (parziale)



| Tasto di scelta rapida  | Componente\_ | Destinazione      |
|-----------|-------------|-------------|
| Collegamento1 | Componente2  | \[\#File1\] |



 

[Tabella dei componenti](component-table.md) (parziale)



| Componente  | Attributi |
|------------|------------|
| Componente1 | 2          |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni di riferimento su ICE](ice-reference.md)
</dt> </dl>

 

 



