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
# <a name="using-application-dictionaries-with-the-tablet-pc-platform-apis"></a><span data-ttu-id="1690f-103">Uso dei dizionari applicazioni con le API della piattaforma Tablet PC</span><span class="sxs-lookup"><span data-stu-id="1690f-103">Using Application Dictionaries with the Tablet PC Platform APIs</span></span>

<span data-ttu-id="1690f-104">Per usare un dizionario applicazioni con l'API Tablet PC, è innanzitutto necessario creare un file con l'elenco delle parole per il dizionario dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="1690f-104">To use an application dictionary with the Tablet PC API, you must first create a file with the list of words for your application dictionary.</span></span>

<span data-ttu-id="1690f-105">La soluzione più semplice consiste nell'utilizzare un file di testo contenente un elenco di parole.</span><span class="sxs-lookup"><span data-stu-id="1690f-105">The easiest solution for this is to use a text file that contains a list of the words.</span></span> <span data-ttu-id="1690f-106">Quando l'applicazione viene caricata, legge il file di testo e crea un oggetto [**WordList**](inkwordlist-class.md) dall'elenco di parole nel file.</span><span class="sxs-lookup"><span data-stu-id="1690f-106">When your application loads, it reads the text file and creates a [**WordList**](inkwordlist-class.md) object from the list of words in the file.</span></span> <span data-ttu-id="1690f-107">Per ogni [**RecognizerContext**](inkrecognizercontext-class.md) associato al dizionario applicazioni, impostare la proprietà [**WordList**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_wordlist) dell'oggetto **RecognizerContext** sull'elenco di parole nel file di testo.</span><span class="sxs-lookup"><span data-stu-id="1690f-107">For each [**RecognizerContext**](inkrecognizercontext-class.md) associated with the application dictionary, set the [**WordList**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_wordlist) property of the **RecognizerContext** object to the word list in the text file.</span></span>

<span data-ttu-id="1690f-108">Nell'esempio seguente viene illustrato come creare un oggetto [**WordList**](inkwordlist-class.md) da una raccolta [StringCollection](/dotnet/api/system.collections.specialized.stringcollection?view=netcore-3.1) .</span><span class="sxs-lookup"><span data-stu-id="1690f-108">The following example illustrates how to create a [**WordList**](inkwordlist-class.md) object from a [StringCollection](/dotnet/api/system.collections.specialized.stringcollection?view=netcore-3.1) collection.</span></span> <span data-ttu-id="1690f-109">In questo esempio si presuppone che sia già stato caricato l'elenco di parole dal disco e che sia stata creata una raccolta StringCollection da queste parole.</span><span class="sxs-lookup"><span data-stu-id="1690f-109">This example assumes that you have already loaded the list of words from disk and created a StringCollection collection from these words.</span></span>


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
> <span data-ttu-id="1690f-110">Prima di impostare la proprietà [**WordList**](inkwordlist-class.md) , la proprietà [**Strokes**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_strokes) dell'oggetto [**RecognizerContext**](inkrecognizercontext-class.md) deve essere vuota.</span><span class="sxs-lookup"><span data-stu-id="1690f-110">The [**Strokes**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_strokes) property of the [**RecognizerContext**](inkrecognizercontext-class.md) object must be empty before you set the [**WordList**](inkwordlist-class.md) property.</span></span> <span data-ttu-id="1690f-111">Se la proprietà [**Strokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) non è vuota, viene generata un'eccezione.</span><span class="sxs-lookup"><span data-stu-id="1690f-111">If the [**Strokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) property is not empty, an exception is thrown.</span></span> <span data-ttu-id="1690f-112">Inoltre, le parole non devono mai essere aggiunte a un elenco di parole dopo che è stato assegnato a un oggetto **RecognizerContext** .</span><span class="sxs-lookup"><span data-stu-id="1690f-112">In addition, words should never be added to a word list after it has been assigned to a **RecognizerContext** object.</span></span> <span data-ttu-id="1690f-113">Le parole che vengono aggiunte all'elenco di parole dopo che è stato assegnato all'oggetto **RecognizerContext** non vengono aggiornate nel riconoscimento.</span><span class="sxs-lookup"><span data-stu-id="1690f-113">Words that are added to the word list after it is assigned to the **RecognizerContext** object are not updated in the recognizer.</span></span> <span data-ttu-id="1690f-114">Per aggiornare l'elenco di parole, è necessario riassegnare l'oggetto **WordList** alla proprietà [**WordList**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_wordlist) dell'oggetto **RecognizerContext** .</span><span class="sxs-lookup"><span data-stu-id="1690f-114">To update the word list you must reassign the **WordList** object to the [**WordList**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_wordlist) property of the **RecognizerContext** object.</span></span>

 

<span data-ttu-id="1690f-115">Per la massima accuratezza del riconoscimento, combinare factoids con il dizionario dell'applicazione in una relazione vantaggiosa.</span><span class="sxs-lookup"><span data-stu-id="1690f-115">For maximum recognition accuracy, combine factoids with your application dictionary in an advantageous relationship.</span></span> <span data-ttu-id="1690f-116">Per ulteriori informazioni sulla relazione tra factoids e i dizionari applicazione, vedere [informazioni sugli elenchi di parole, contesto di riconoscimento e factoids](understanding-wordlists--the-recognizercontext--and-factoids.md).</span><span class="sxs-lookup"><span data-stu-id="1690f-116">For more information about the relationship between factoids and application dictionaries, see [Understanding Word Lists, Recognizer Context, and Factoids](understanding-wordlists--the-recognizercontext--and-factoids.md).</span></span>

<span data-ttu-id="1690f-117">Per un esempio di utilizzo dei dizionari applicazione con il controllo [InkEdit](inkedit-control-reference.md) , vedere [utilizzo di un dizionario applicazioni con InkEdit](using-an-application-dictionary-with-inkedit.md).</span><span class="sxs-lookup"><span data-stu-id="1690f-117">For an example of using application dictionaries with the [InkEdit](inkedit-control-reference.md) control, see [Using an Application Dictionary with InkEdit](using-an-application-dictionary-with-inkedit.md).</span></span>

 

 
