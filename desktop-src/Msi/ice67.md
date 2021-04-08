---
description: ICE67 verifica che la destinazione di un collegamento non annunciato appartenga allo stesso componente del collegamento stesso o che gli attributi del componente di destinazione garantiscano che non modifichi i percorsi di installazione.
ms.assetid: 3fc462e7-4c11-4167-a157-6c1e0791901d
title: ICE67
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ca140a2d7eace9b693e82763f6bf5824346b51e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968236"
---
# <a name="ice67"></a>ICE67

ICE67 verifica che la destinazione di un collegamento non annunciato appartenga allo stesso componente del collegamento stesso o che gli attributi del componente di destinazione garantiscano che non modifichi i percorsi di installazione.

Se si verifica un errore durante la correzione di un avviso o di un errore segnalato da ICE67, il collegamento non può essere valido se lo stato del componente di destinazione è diverso da quello di origine. Ad esempio, quando il componente del file di destinazione è impostato per l'esecuzione dall'origine, una reinstallazione che modifica il componente in locale genera il componente contenente il collegamento che non viene reinstallato. Quindi il collegamento punta a una posizione non valida.

Si noti che in alcuni casi l'uso di un componente diverso per il collegamento è inevitabile. Se, ad esempio, il collegamento viene creato nel profilo utente e il file viene installato in una directory non del profilo, potrebbe non essere possibile utilizzare lo stesso componente per entrambe le parti di dati. Ciò comporta errori negli scenari multiutente, ad esempio quelli descritti in [ICE57](ice57.md). In questo caso, è possibile usare i tasti di scelta rapida annunciati per ottenere il comportamento desiderato. in alternativa, è sufficiente assicurarsi che il componente di destinazione non sia in grado di passare da Run-from-source a local.

## <a name="result"></a>Risultato

ICE67 restituisce un errore o un avviso se la destinazione di un collegamento non annunciato non appartiene allo stesso componente del collegamento stesso o se gli attributi del componente di destinazione non assicurano che i percorsi di installazione non vengano modificati.

## <a name="example"></a>Esempio

ICE67 segnala i seguenti avvisi ed errori per l'esempio illustrato.

``` syntax
The shortcut 'Shortcut1' is a non-advertised shortcut with a file target. The shortcut and target are installed by different components, and the target component can run locally or from source.
```

Shortcut1 viene installato da Component2, ma il relativo file di destinazione, file1, viene installato da Component1. Il componente di destinazione è contrassegnato come facoltativo, ovvero può essere locale o di origine. Una possibile situazione che potrebbe causare un problema è il caso in cui Component1 modifiche da Run-from-source a local. In questo modo Shortcut1 potrebbe puntare a una posizione non valida.

Per correggere il problema, installare il collegamento come parte di Component1 oppure contrassegnare Component1 come LocalOnly o SourceOnly.

[Tabella file](file-table.md) (parziale)



| File  | Componente\_ |
|-------|-------------|
| File1 | Component1  |



 

[Tabella collegamenti](shortcut-table.md) (parziale)



| Tasto di scelta rapida  | Componente\_ | Destinazione      |
|-----------|-------------|-------------|
| Shortcut1 | Component2  | \[\#File1\] |



 

[Tabella componenti](component-table.md) (parziale)



| Componente  | Attributi |
|------------|------------|
| Component1 | 2          |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Riferimento ghiaccio](ice-reference.md)
</dt> </dl>

 

 



