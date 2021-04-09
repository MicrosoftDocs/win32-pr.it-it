---
description: È necessario utilizzare la funzione SetupOpenInfFile per aprire il file INF prima di poter recuperare informazioni da esso o aggiungere altri file INF.
ms.assetid: ba4d511a-ad19-4619-a10a-cafef789821b
title: Apertura del file INF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d8493fda983f2942705b97ea243f6cb95e91c15
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103882362"
---
# <a name="opening-the-inf-file"></a><span data-ttu-id="18481-103">Apertura del file INF</span><span class="sxs-lookup"><span data-stu-id="18481-103">Opening the INF File</span></span>

<span data-ttu-id="18481-104">È necessario utilizzare la funzione [**SetupOpenInfFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupopeninffilea) per aprire il file inf prima di poter recuperare informazioni da esso o aggiungere altri file inf.</span><span class="sxs-lookup"><span data-stu-id="18481-104">You must use the [**SetupOpenInfFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupopeninffilea) function to open the INF file before you can retrieve information from it, or append other INF files to it.</span></span>

<span data-ttu-id="18481-105">Il codice seguente apre un file INF con [**SetupOpenInfFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupopeninffilea) e restituisce un handle, MyInf, al file inf aperto.</span><span class="sxs-lookup"><span data-stu-id="18481-105">The following opens an INF file using [**SetupOpenInfFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupopeninffilea) and returns a handle, MyInf, to the opened INF file.</span></span> <span data-ttu-id="18481-106">Il parametro *InfClass* di **SetupOpenInfFile** è specificato come **null** per indicare che la classe del file inf deve essere ignorata.</span><span class="sxs-lookup"><span data-stu-id="18481-106">The *InfClass* parameter of **SetupOpenInfFile** is specified as **NULL** to indicate that the Class of the INF file should be ignored.</span></span>


```C++
HINF MyInf;                //variable to hold the INF handle
UINT ErrorLine;            //variable to hold errors returned
BOOL test=0;                 //variable to receive function success
 
MyInf = SetupOpenInfFile (
      szInfFileName,       //the filename of the inf file to open
      NULL,                //optional class information
      INF_STYLE_WIN4,      //the inf style
      &ErrorLine           //line number of the syntax error
);
```



<span data-ttu-id="18481-107">Dopo l'apertura di un file INF, è possibile chiamare la funzione [**SetupOpenAppendInfFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupopenappendinffilea) per aggiungere un file al file inf aperto.</span><span class="sxs-lookup"><span data-stu-id="18481-107">After an INF file is opened, you can call the [**SetupOpenAppendInfFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupopenappendinffilea) function to append a file to the open INF file.</span></span> <span data-ttu-id="18481-108">Per aggiungere più file, ripetere questo processo.</span><span class="sxs-lookup"><span data-stu-id="18481-108">To append several files, repeat this process.</span></span> <span data-ttu-id="18481-109">Se si chiama la funzione **SetupOpenAppendInfFile** e il nome file passato è **null**, la funzione cercherà nella sezione Version del file inf aperto (e di eventuali file inf aggiunti) una chiave LayoutFile.</span><span class="sxs-lookup"><span data-stu-id="18481-109">If you call the **SetupOpenAppendInfFile** function and the filename passed to it is **NULL**, then the function will search the Version section of the open INF file (and any appended INF files) for a LayoutFile key.</span></span> <span data-ttu-id="18481-110">Se la funzione trova una chiave, verrà aggiunto il file specificato da tale chiave, in genere LAYOUT. INF).</span><span class="sxs-lookup"><span data-stu-id="18481-110">If the function finds a key, it will append the file specified by that key (usually LAYOUT.INF).</span></span> <span data-ttu-id="18481-111">Quando più file INF sono stati combinati, **SetupOpenAppendInfFile** inizia con l'ultimo file inf accodato durante la ricerca di una sezione di versione.</span><span class="sxs-lookup"><span data-stu-id="18481-111">When multiple INF files have been combined, **SetupOpenAppendInfFile** starts with the last appended INF file when it searches for a Version section.</span></span>

 

 



