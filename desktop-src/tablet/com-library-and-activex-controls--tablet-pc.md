---
description: In questa sezione viene descritto come configurare l'ambiente per l'utilizzo delle librerie COM della piattaforma Tablet PC in C++.
ms.assetid: c0d7f703-d4aa-4c26-ae81-a4c888383c1e
title: Libreria COM e controlli ActiveX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b9304880380ea95bc698c52d200931b77f64480
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305689"
---
# <a name="com-library-and-activex-controls"></a><span data-ttu-id="76a60-103">Libreria COM e controlli ActiveX</span><span class="sxs-lookup"><span data-stu-id="76a60-103">COM Library and ActiveX Controls</span></span>

<span data-ttu-id="76a60-104">In questa sezione viene descritto come configurare l'ambiente per l'utilizzo delle librerie COM della piattaforma Tablet PC in C++.</span><span class="sxs-lookup"><span data-stu-id="76a60-104">This section describes how to set up your environment to use the Tablet PC platform COM libraries in C++.</span></span>

## <a name="microsoft-visual-c"></a><span data-ttu-id="76a60-105">Microsoft Visual C++</span><span class="sxs-lookup"><span data-stu-id="76a60-105">Microsoft Visual C++</span></span>

<span data-ttu-id="76a60-106">Per compilare applicazioni per Tablet PC in Visual C++, è necessario aggiornare le variabili di ambiente di sistema, impostare le opzioni di directory per Visual Studio e accedere alle interfacce di Tablet PC nel progetto.</span><span class="sxs-lookup"><span data-stu-id="76a60-106">To build Tablet PC applications in Visual C++, you need to update the system environment variables, set up directory options for Visual Studio, and access the Tablet PC interfaces in your project.</span></span>

<span data-ttu-id="76a60-107">Per aggiornare le variabili di ambiente, seguire le istruzioni fornite dal Windows SDK per aggiungere le variabili di ambiente a Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="76a60-107">To update the environment variables, follow the instructions provided by the Windows SDK for adding the environment variables to Visual Studio.</span></span>

### <a name="accessing-the-tablet-pc-interfaces"></a><span data-ttu-id="76a60-108">Accesso alle interfacce di Tablet PC</span><span class="sxs-lookup"><span data-stu-id="76a60-108">Accessing the Tablet PC Interfaces</span></span>

<span data-ttu-id="76a60-109">Per accedere alle interfacce di Tablet PC, è necessario includere i file Msinkaut. h e Msinkaut \_ i. c nel progetto.</span><span class="sxs-lookup"><span data-stu-id="76a60-109">To access the Tablet PC interfaces, you must include the Msinkaut.h and Msinkaut\_i.c files in your project.</span></span>


```C++
#include <msinkaut.h>
#include <msinkaut_i.c>
```



<span data-ttu-id="76a60-110">È anche possibile usare la direttiva import seguente anziché le \# istruzioni include elencate in precedenza.</span><span class="sxs-lookup"><span data-stu-id="76a60-110">You can also use the following import directive instead of the \#include statements previously listed.</span></span>


```C++
#import "InkObj.dll" no_namespace exclude("tagXFORM")
```



<span data-ttu-id="76a60-111">Per accedere alle interfacce InkAnalysis, è necessario includere i file IACom. h e IACom \_ i. c nel progetto.</span><span class="sxs-lookup"><span data-stu-id="76a60-111">To access the InkAnalysis interfaces, you must include IACom.h and IACom\_i.c files in your project.</span></span>


```C++
#include <IACom.h>
#include <IACom_i.c>
```



<span data-ttu-id="76a60-112">È anche possibile usare la direttiva import seguente anziché le \# istruzioni include elencate in precedenza.</span><span class="sxs-lookup"><span data-stu-id="76a60-112">You can also use the following import directive instead of the \#include statements previously listed.</span></span>


```C++
#import "IACom.dll" no_namespace exclude("tagXFORM")
```



<span data-ttu-id="76a60-113">Per accedere alle interfacce [**InkDivider**](inkdivider-class.md) , è necessario includere \_ i file msinkaut15 i. c e msinkaut15. h nel progetto.</span><span class="sxs-lookup"><span data-stu-id="76a60-113">To access the [**InkDivider**](inkdivider-class.md) interfaces, you must include msinkaut15\_i.c and msinkaut15.h files in your project.</span></span>

> [!Note]  
> <span data-ttu-id="76a60-114">InkDivider è stato sostituito dalle API di analisi dell'input penna.</span><span class="sxs-lookup"><span data-stu-id="76a60-114">InkDivider has been superseded by the Ink Analysis APIs.</span></span>

 


```C++
#include <msinkaut15.h>
#include <msinkaut15_i.c>
```



<span data-ttu-id="76a60-115">È anche possibile usare la direttiva import seguente anziché le \# istruzioni include.</span><span class="sxs-lookup"><span data-stu-id="76a60-115">You can also use the following import directive instead of the \# include statements.</span></span>


```C++
#import "InkDiv.dll" no_namespace exclude("tagXFORM")
```



<span data-ttu-id="76a60-116">Per accedere alle interfacce [**PenInputPanel**](peninputpanel-class.md) , è necessario includere \_ i file PenInputPanel i. c e PenInputPanel. h nel progetto.</span><span class="sxs-lookup"><span data-stu-id="76a60-116">To access the [**PenInputPanel**](peninputpanel-class.md) interfaces, you must include PenInputPanel\_i.c and PenInputPanel.h files in your project.</span></span>


```C++
#include <PenInputPanel.h>
#include <PenInputPanel_i.c>
```



<span data-ttu-id="76a60-117">È anche possibile usare la direttiva import seguente anziché le \# istruzioni include.</span><span class="sxs-lookup"><span data-stu-id="76a60-117">You can also use the following import directive instead of the \# include statements.</span></span>


```C++
#import "PIPanel.dll" no_namespace 
```



> [!Note]  
> <span data-ttu-id="76a60-118">Le API PenInputPanel sono state sostituite in Windows Vista dalle nuove interfacce del pannello di input di testo.</span><span class="sxs-lookup"><span data-stu-id="76a60-118">The PenInputPanel APIs have been superseded in Windows Vista by the new Text Input Panel interfaces.</span></span>

 

<span data-ttu-id="76a60-119">Per accedere alle interfacce di controllo [InkEdit](inkedit-control-reference.md) , è necessario includere i file inchiostrate. h e inchiostrati \_ i. c nel progetto.</span><span class="sxs-lookup"><span data-stu-id="76a60-119">To access the [InkEdit](inkedit-control-reference.md) Control interfaces, you must include the Inked.h and Inked\_i.c files in your project.</span></span>


```C++
#include <inked.h>
#include <inked_i.c>
```



<span data-ttu-id="76a60-120">In alternativa, è possibile \# importare il file di InkEd.dll.</span><span class="sxs-lookup"><span data-stu-id="76a60-120">Alternatively, you can \#import the InkEd.dll file.</span></span>


```C++
#import "InkEd.dll" no_namespace exclude("tagXFORM")
```



 

 



