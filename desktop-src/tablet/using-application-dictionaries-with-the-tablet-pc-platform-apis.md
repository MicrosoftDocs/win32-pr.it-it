---
description: Per usare un dizionario applicazioni con l'API Tablet PC, è innanzitutto necessario creare un file con l'elenco di parole per il dizionario dell'applicazione.
ms.assetid: 6abadad1-262b-4536-8846-1c06226dc18a
title: Uso dei dizionari applicazioni con le API della piattaforma Tablet PC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c30fec5539a9b1f4efb0ca89a53568becff2368942d069149106a4032676d50
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119091309"
---
# <a name="using-application-dictionaries-with-the-tablet-pc-platform-apis"></a>Uso dei dizionari applicazioni con le API della piattaforma Tablet PC

Per usare un dizionario applicazioni con l'API Tablet PC, è innanzitutto necessario creare un file con l'elenco di parole per il dizionario dell'applicazione.

La soluzione più semplice consiste nell'usare un file di testo contenente un elenco di parole. Quando l'applicazione viene caricata, legge il file di testo e crea un [**oggetto WordList**](inkwordlist-class.md) dall'elenco di parole nel file. Per ogni [**RecognizerContext**](inkrecognizercontext-class.md) associato al dizionario applicazioni, imposta la proprietà [**WordList**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_wordlist) dell'oggetto **RecognizerContext** sull'elenco di parole nel file di testo.

L'esempio seguente illustra come creare un [**oggetto WordList**](inkwordlist-class.md) da una [raccolta StringCollection.](/dotnet/api/system.collections.specialized.stringcollection?view=netcore-3.1) Questo esempio presuppone che sia già stato caricato l'elenco di parole dal disco e che sia stata creata una raccolta StringCollection da queste parole.


```C++
using System.Collections.Specialized;
using Microsoft.Ink;
//...
RecognizerContext theRecognizerContext;
StringCollection theUserDictionary;
//... 
// Initialize theRecognizerContext and theUserDictionary objects here.
//...
WordList theUserWordList = new WordList();
foreach (string s in theUserDictionary)
{
    theUserWordList.Add(s);
}
theRecognizerContext.WordList = theUserWordList;
```



> [!Note]  
> La [**proprietà Strokes**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_strokes) dell'oggetto [**RecognizerContext**](inkrecognizercontext-class.md) deve essere vuota prima di impostare la [**proprietà WordList.**](inkwordlist-class.md) Se la [**proprietà Strokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) non è vuota, viene generata un'eccezione. Inoltre, le parole non devono mai essere aggiunte a un elenco di parole dopo essere state assegnate a un **oggetto RecognizerContext.** Le parole aggiunte all'elenco di parole dopo l'assegnazione **all'oggetto RecognizerContext** non vengono aggiornate nel riconoscimento. Per aggiornare l'elenco di parole, è necessario riassegnare l'oggetto **WordList** alla [**proprietà WordList**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_wordlist) dell'oggetto **RecognizerContext.**

 

Per la massima accuratezza del riconoscimento, combinare i factoid con il dizionario dell'applicazione in una relazione vantaggiosa. Per altre informazioni sulla relazione tra factoid e dizionari dell'applicazione, vedere Understanding [Word Lists, Recognizer Context, and Factoids](understanding-wordlists--the-recognizercontext--and-factoids.md).

Per un esempio d'uso dei dizionari dell'applicazione con il [controllo InkEdit,](inkedit-control-reference.md) vedere Uso di un [dizionario applicazioni con InkEdit.](using-an-application-dictionary-with-inkedit.md)

 

 
