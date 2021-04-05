---
description: Una volta eseguito correttamente il commit della coda, sarà necessario aggiornare le informazioni del registro di sistema per il prodotto che si sta installando.
ms.assetid: 32161538-c1bd-41a0-bb4f-a32883fe8285
title: Aggiornamento delle informazioni del registro di sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4aa6a77f231f3a4fe754b589e3f20ed67e78e548
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968193"
---
# <a name="updating-registry-information"></a><span data-ttu-id="64132-103">Aggiornamento delle informazioni del registro di sistema</span><span class="sxs-lookup"><span data-stu-id="64132-103">Updating Registry Information</span></span>

<span data-ttu-id="64132-104">Una volta eseguito correttamente il commit della coda, sarà necessario aggiornare le informazioni del registro di sistema per il prodotto che si sta installando.</span><span class="sxs-lookup"><span data-stu-id="64132-104">After the queue has successfully committed, you will need to update registry information for the product you are installing.</span></span> <span data-ttu-id="64132-105">Prima di modificare le informazioni del registro di sistema, si consiglia di attendere il completamento di tutte le operazioni di copia del file necessarie.</span><span class="sxs-lookup"><span data-stu-id="64132-105">It is recommended that you wait until all necessary file copy operations have been successfully completed before altering registry information.</span></span>

<span data-ttu-id="64132-106">Un modo per aggiornare il registro di sistema consiste nel chiamare [**SetupInstallFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona) con il INIFILES spinoso, il registro di sistema di rotazione \_ o i \_ \_ flag INI2REG spinti specificati.</span><span class="sxs-lookup"><span data-stu-id="64132-106">One way to update the registry is to call [**SetupInstallFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona) with the SPINST\_INIFILES, SPINST\_REGISTRY, or SPINST\_INI2REG flags specified.</span></span> <span data-ttu-id="64132-107">Questi flag possono essere combinati in una sola chiamata a **SetupInstallFromInfSection**.</span><span class="sxs-lookup"><span data-stu-id="64132-107">These flags can be combined in one call to **SetupInstallFromInfSection**.</span></span>

<span data-ttu-id="64132-108">Nell'esempio seguente vengono utilizzati \_ tutti i ^ file rotanti \_ per indicare che la funzione deve elaborare tutte le operazioni elencate ad eccezione delle operazioni sui file.</span><span class="sxs-lookup"><span data-stu-id="64132-108">The following example uses SPINST\_ALL^SPINST\_FILES to indicate that the function should process all of the listed operations except file operations.</span></span> <span data-ttu-id="64132-109">Poiché nella sezione **Install** sono elencate solo le operazioni ini, registro di sistema e file, si tratta di un metodo a sintassi abbreviata per specificare che la funzione deve elaborare tutte le operazioni ini e del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="64132-109">Since only INI, registry, and file operations are listed in the **Install** section, this is a shorthand method of specifying the function should process all INI and registry operations.</span></span>

<span data-ttu-id="64132-110">Nell'esempio seguente viene illustrato come installare le informazioni del registro di sistema tramite la funzione **SetupInstallFromINFSection** .</span><span class="sxs-lookup"><span data-stu-id="64132-110">The following example shows how to install registry information using the **SetupInstallFromINFSection** function.</span></span>

``` syntax
Test = SetupInstallFromINFSection (
     NULL,                     //Window to own any dialog boxes
                               //created 
     MyInf,                    //INF file containing the section 
     MySection,                //the section to install
     SPINST_ALL ^ SPINST_FILES,//which installation operations 
                               //to process
     NULL,                     //the relative root key
     NULL,                     //the source root path
     0,                        //copy style
     NULL,                     //Message handler routine
     NULL,                     //Context
     NULL,                     //Device info set
     NULL                      //device info data
);
```

<span data-ttu-id="64132-111">Nell'esempio *OwnerWindow* è **null** perché solo le operazioni sui file generano finestre di dialogo e pertanto non è necessaria una finestra padre.</span><span class="sxs-lookup"><span data-stu-id="64132-111">In the example, *OwnerWindow* is **NULL** because only file operations generate dialog boxes, and thus a parent window is not needed.</span></span> <span data-ttu-id="64132-112">"MyInf" è il file INF contenente la sezione da elaborare.</span><span class="sxs-lookup"><span data-stu-id="64132-112">"MyInf" is the INF file containing the section to process.</span></span> <span data-ttu-id="64132-113">Il parametro "sezione" specifica la sezione da installare.</span><span class="sxs-lookup"><span data-stu-id="64132-113">The parameter, "MySection", specifies the section to be installed.</span></span> <span data-ttu-id="64132-114">I flag combinati, RUOTAndo \_ tutti i ^ \_ file spinti, specificano le operazioni di installazione da elaborare, in questo caso tutte le operazioni ad eccezione dei file.</span><span class="sxs-lookup"><span data-stu-id="64132-114">The combined flags, SPINST\_ALL ^ SPINST\_FILES, specify which installation operations to process, in this case, all operations except file operations.</span></span> <span data-ttu-id="64132-115">Il percorso radice di origine viene specificato come "A: \\ ".</span><span class="sxs-lookup"><span data-stu-id="64132-115">The source root path is specified as "A:\\".</span></span>

<span data-ttu-id="64132-116">Poiché non viene elaborata alcuna operazione di copia, non vengono specificati i parametri *CopyFlags*, *MsgHandler*, *context*, *DeviceInfoSet* e *DeviceInfoData* .</span><span class="sxs-lookup"><span data-stu-id="64132-116">Since no copy operations are being processed, the *CopyFlags*, *MsgHandler*, *Context*, *DeviceInfoSet*, and *DeviceInfoData* parameters are not specified.</span></span>

 

 



