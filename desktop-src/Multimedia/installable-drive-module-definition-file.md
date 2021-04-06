---
title: File di Module-Definition unità installabile
description: File di Module-Definition unità installabile
ms.assetid: d8d8d32e-18ac-47a5-a923-48b94b75e11d
keywords:
- driver installabili, file di definizione moduli
- driver installabili, file DEF
- driver nstallable, funzione DriverProc
- DriverProc (funzione)
- file di definizione moduli
- DEF (file)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 700931c91bfb3c17a36a1e3a1bbc4833097b4b38
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104046633"
---
# <a name="installable-drive-module-definition-file"></a><span data-ttu-id="665a3-109">File di Module-Definition unità installabile</span><span class="sxs-lookup"><span data-stu-id="665a3-109">Installable Drive Module-Definition File</span></span>

<span data-ttu-id="665a3-110">La definizione di modulo (. DEF) il file di un driver installabile assegna un nome al driver, Esporta la funzione [DriverProc](/windows/win32/api/mmiscapi/nc-mmiscapi-driverproc) e definisce una descrizione del driver.</span><span class="sxs-lookup"><span data-stu-id="665a3-110">The module-definition (.DEF) file of an installable driver names the driver, exports the [DriverProc](/windows/win32/api/mmiscapi/nc-mmiscapi-driverproc) function, and defines a driver description.</span></span> <span data-ttu-id="665a3-111">Nell'esempio seguente viene illustrato un file di definizione dei moduli tipico per un driver installabile:</span><span class="sxs-lookup"><span data-stu-id="665a3-111">The following example shows a typical module-definition file for an installable driver:</span></span>


```C++
LIBRARY OSCI 
DESCRIPTION 'FREQ,AMPL:Oscilloscope frequency and amplitude drivers.'
EXPORTS
    DriverProc
 
```



<span data-ttu-id="665a3-112">Alcune applicazioni di installazione possono aprire il driver e recuperare la riga di descrizione da usare durante l'installazione del driver.</span><span class="sxs-lookup"><span data-stu-id="665a3-112">Some installation applications may open the driver and retrieve the description line to use when installing the driver.</span></span> <span data-ttu-id="665a3-113">Per mantenere la compatibilità con queste applicazioni di installazione, la riga della descrizione deve avere il formato seguente:</span><span class="sxs-lookup"><span data-stu-id="665a3-113">To remain compatible with these installation applications, the description line should have this form:</span></span>

<span data-ttu-id="665a3-114">**Descrizione**  *alias* \[ ,*alias* \] ... **:* \* \* testo*</span><span class="sxs-lookup"><span data-stu-id="665a3-114">**DESCRIPTION**  *alias*\[,*alias*\]...\**:\*\*\*text*</span></span>

<span data-ttu-id="665a3-115">L' *alias* specifica un nome univoco per il driver che può essere utilizzato dalle applicazioni per aprire il driver.</span><span class="sxs-lookup"><span data-stu-id="665a3-115">The *alias* specifies a unique name for the driver that applications can use to open the driver.</span></span> <span data-ttu-id="665a3-116">L'alias funge anche da nome del valore associato al driver nel registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="665a3-116">The alias also serves as the value name associated with the driver in the registry.</span></span> <span data-ttu-id="665a3-117">Più alias sono separati da virgole.</span><span class="sxs-lookup"><span data-stu-id="665a3-117">Multiple aliases are separated by commas.</span></span> <span data-ttu-id="665a3-118">Il *testo* descrive lo scopo del driver.</span><span class="sxs-lookup"><span data-stu-id="665a3-118">The *text* describes the purpose of the driver.</span></span>

 

 