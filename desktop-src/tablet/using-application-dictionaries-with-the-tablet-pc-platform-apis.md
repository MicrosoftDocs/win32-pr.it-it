---
description: Per usare un dizionario applicazioni con l'API Tablet PC, è innanzitutto necessario creare un file con l'elenco delle parole per il dizionario dell'applicazione.
ms.assetid: 6abadad1-262b-4536-8846-1c06226dc18a
title: Uso dei dizionari applicazioni con le API della piattaforma Tablet PC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9fc0e444ad2213d945c0210d07c72f9540ae16be
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306721"
---
# <a name="using-application-dictionaries-with-the-tablet-pc-platform-apis"></a>Uso dei dizionari applicazioni con le API della piattaforma Tablet PC

Per usare un dizionario applicazioni con l'API Tablet PC, è innanzitutto necessario creare un file con l'elenco delle parole per il dizionario dell'applicazione.

La soluzione più semplice consiste nell'utilizzare un file di testo contenente un elenco di parole. Quando l'applicazione viene caricata, legge il file di testo e crea un oggetto [**WordList**](inkwordlist-class.md) dall'elenco di parole nel file. Per ogni [**RecognizerContext**](inkrecognizercontext-class.md) associato al dizionario applicazioni, impostare la proprietà [**WordList**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_wordlist) dell'oggetto **RecognizerContext** sull'elenco di parole nel file di testo.

Nell'esempio seguente viene illustrato come creare un oggetto [**WordList**](inkwordlist-class.md) da una raccolta [StringCollection](/dotnet/api/system.collections.specialized.stringcollection?view=netcore-3.1) . In questo esempio si presuppone che sia già stato caricato l'elenco di parole dal disco e che sia stata creata una raccolta StringCollection da queste parole.


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
> Prima di impostare la proprietà [**WordList**](inkwordlist-class.md) , la proprietà [**Strokes**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_strokes) dell'oggetto [**RecognizerContext**](inkrecognizercontext-class.md) deve essere vuota. Se la proprietà [**Strokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) non è vuota, viene generata un'eccezione. Inoltre, le parole non devono mai essere aggiunte a un elenco di parole dopo che è stato assegnato a un oggetto **RecognizerContext** . Le parole che vengono aggiunte all'elenco di parole dopo che è stato assegnato all'oggetto **RecognizerContext** non vengono aggiornate nel riconoscimento. Per aggiornare l'elenco di parole, è necessario riassegnare l'oggetto **WordList** alla proprietà [**WordList**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_wordlist) dell'oggetto **RecognizerContext** .

 

Per la massima accuratezza del riconoscimento, combinare factoids con il dizionario dell'applicazione in una relazione vantaggiosa. Per ulteriori informazioni sulla relazione tra factoids e i dizionari applicazione, vedere [informazioni sugli elenchi di parole, contesto di riconoscimento e factoids](understanding-wordlists--the-recognizercontext--and-factoids.md).

Per un esempio di utilizzo dei dizionari applicazione con il controllo [InkEdit](inkedit-control-reference.md) , vedere [utilizzo di un dizionario applicazioni con InkEdit](using-an-application-dictionary-with-inkedit.md).

 

 
