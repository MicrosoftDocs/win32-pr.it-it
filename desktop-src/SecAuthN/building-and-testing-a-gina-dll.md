---
description: Tutte le funzioni, i prototipi, le strutture e le costanti vengono definiti nel file di intestazione Winwlx. h.
ms.assetid: 13b5bc92-583d-4031-94f9-f84dbfbf7ee7
title: Compilazione e test di una DLL GINA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02e6e4a00f15e6ced4827bbc3efeb3c459f5d6a8
ms.sourcegitcommit: 70f39ec77d19d3c32c376ee2831753d2cafae41a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104352046"
---
# <a name="building-and-testing-a-gina-dll"></a><span data-ttu-id="1d8be-103">Compilazione e test di una DLL GINA</span><span class="sxs-lookup"><span data-stu-id="1d8be-103">Building and Testing a GINA DLL</span></span>

<span data-ttu-id="1d8be-104">Tutte le funzioni, i prototipi, le strutture e le costanti vengono definiti nel file di intestazione Winwlx. h.</span><span class="sxs-lookup"><span data-stu-id="1d8be-104">All functions, prototypes, structures, and constants are defined in the Winwlx.h header file.</span></span>

> [!Note]  
> <span data-ttu-id="1d8be-105">Le DLL GINA vengono ignorate in Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="1d8be-105">GINA DLLs are ignored in Windows Vista.</span></span>

 

<span data-ttu-id="1d8be-106">Per testare una dll [*Gina*](/windows/desktop/SecGloss/g-gly) , utilizzare il Winlogon.exe da una versione controllata del sistema operativo, disponibile con Microsoft Windows Driver Development Kit (DDK).</span><span class="sxs-lookup"><span data-stu-id="1d8be-106">To test a [*GINA*](/windows/desktop/SecGloss/g-gly) DLL, use the Winlogon.exe from a checked version of the operating system, which is available with the Microsoft Windows Driver Development Kit (DDK).</span></span> <span data-ttu-id="1d8be-107">La versione controllata di [*Winlogon*](/windows/desktop/SecGloss/w-gly) supporta il debug di Ginas come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="1d8be-107">The checked version of [*Winlogon*](/windows/desktop/SecGloss/w-gly) supports debugging GINAs as follows:</span></span>

-   <span data-ttu-id="1d8be-108">È possibile usare la sintassi seguente per creare una sezione in Win.ini per specificare le opzioni di debug di Winlogon.</span><span class="sxs-lookup"><span data-stu-id="1d8be-108">You can use the following syntax to create a section in Win.ini to specify Winlogon debugging options.</span></span>

    ``` syntax
    [WinlogonDebug]
    LogFile=C:\Winlogon.log
    DebugFlags=Flag1 [, Flag2 ...]
    ```

    <span data-ttu-id="1d8be-109">Se specificato, **logfile** deve contenere il nome completo del file che verrà usato per registrare le informazioni di debug.</span><span class="sxs-lookup"><span data-stu-id="1d8be-109">If specified, **LogFile** should contain the fully qualified name of the file that will be used to log debugging information.</span></span> <span data-ttu-id="1d8be-110">Se il file non esiste, verrà creato automaticamente.</span><span class="sxs-lookup"><span data-stu-id="1d8be-110">If the file does not exist, it will be created.</span></span>

    <span data-ttu-id="1d8be-111">Le opzioni **DebugFlags** specificano i tipi di informazioni di debug da scrivere nel file di log o nel debugger.</span><span class="sxs-lookup"><span data-stu-id="1d8be-111">The **DebugFlags** options specify which kinds of debugging information to write to the log file, or debugger.</span></span> <span data-ttu-id="1d8be-112">**DebugFlags** può contenere uno o più dei flag seguenti.</span><span class="sxs-lookup"><span data-stu-id="1d8be-112">**DebugFlags** can contain one or more of the following flags.</span></span>

    

    | <span data-ttu-id="1d8be-113">Flag di debug</span><span class="sxs-lookup"><span data-stu-id="1d8be-113">Debugging flag</span></span> | <span data-ttu-id="1d8be-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1d8be-114">Description</span></span>                                                                                                                                                                |
    |----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | <span data-ttu-id="1d8be-115">CoolSwitch</span><span class="sxs-lookup"><span data-stu-id="1d8be-115">CoolSwitch</span></span>     | <span data-ttu-id="1d8be-116">La combinazione di tasti CTRL + ALT + MAIUSC + TAB provocherà un'operazione di debug in Winlogon.</span><span class="sxs-lookup"><span data-stu-id="1d8be-116">The CTRL+ALT+SHIFT+TAB key combination will cause a debug break in Winlogon.</span></span>                                                                                               |
    | <span data-ttu-id="1d8be-117">Errore</span><span class="sxs-lookup"><span data-stu-id="1d8be-117">Error</span></span>          | <span data-ttu-id="1d8be-118">Errori di stampa.</span><span class="sxs-lookup"><span data-stu-id="1d8be-118">Print errors.</span></span>                                                                                                                                                              |
    | <span data-ttu-id="1d8be-119">Init</span><span class="sxs-lookup"><span data-stu-id="1d8be-119">Init</span></span>           | <span data-ttu-id="1d8be-120">Messaggi di inizializzazione e di stato di stampa.</span><span class="sxs-lookup"><span data-stu-id="1d8be-120">Print initialization and progress messages.</span></span>                                                                                                                                |
    | <span data-ttu-id="1d8be-121">Notifica</span><span class="sxs-lookup"><span data-stu-id="1d8be-121">Notify</span></span>         | <span data-ttu-id="1d8be-122">Stampa messaggi del pacchetto di notifica.</span><span class="sxs-lookup"><span data-stu-id="1d8be-122">Print notification package messages.</span></span>                                                                                                                                       |
    | <span data-ttu-id="1d8be-123">SAS</span><span class="sxs-lookup"><span data-stu-id="1d8be-123">SAS</span></span>            | <span data-ttu-id="1d8be-124">Stampa le informazioni sulle notifiche di [*Secure Attention Sequence*](/windows/desktop/SecGloss/s-gly) (SAS).</span><span class="sxs-lookup"><span data-stu-id="1d8be-124">Print information about [*secure attention sequence*](/windows/desktop/SecGloss/s-gly) (SAS) notifications.</span></span> |
    | <span data-ttu-id="1d8be-125">State</span><span class="sxs-lookup"><span data-stu-id="1d8be-125">State</span></span>          | <span data-ttu-id="1d8be-126">Stampare messaggi quando lo stato di Winlogon cambia.</span><span class="sxs-lookup"><span data-stu-id="1d8be-126">Print messages when Winlogon changes state.</span></span>                                                                                                                                |
    | <span data-ttu-id="1d8be-127">Timeout</span><span class="sxs-lookup"><span data-stu-id="1d8be-127">Timeout</span></span>        | <span data-ttu-id="1d8be-128">Stampare i messaggi quando viene impostato un limite di tempo o viene raggiunto un limite di tempo.</span><span class="sxs-lookup"><span data-stu-id="1d8be-128">Print messages when a time limit is set or a time limit is reached.</span></span>                                                                                                        |
    | <span data-ttu-id="1d8be-129">Trace</span><span class="sxs-lookup"><span data-stu-id="1d8be-129">Trace</span></span>          | <span data-ttu-id="1d8be-130">Stampa le informazioni di traccia dettagliate.</span><span class="sxs-lookup"><span data-stu-id="1d8be-130">Print verbose trace information.</span></span>                                                                                                                                           |
    | <span data-ttu-id="1d8be-131">Avvisa</span><span class="sxs-lookup"><span data-stu-id="1d8be-131">Warn</span></span>           | <span data-ttu-id="1d8be-132">Avvisi di stampa.</span><span class="sxs-lookup"><span data-stu-id="1d8be-132">Print warnings.</span></span>                                                                                                                                                            |

    

     

-   <span data-ttu-id="1d8be-133">Per avviare la versione controllata di Winlogon in un debugger, aggiungere la voce seguente al registro di sistema:</span><span class="sxs-lookup"><span data-stu-id="1d8be-133">To start the checked version of Winlogon in a debugger, add the following entry to the registry:</span></span>

    ```
    HKEY_LOCAL_MACHINE
       Software
          Microsoft
             Windows NT
                CurrentVersion
                   Image File Execution Options
                      winlogon.exe
                         Debugger = ntsd -d<dl>
    <dt>

                     Data type
</dt>
    <dd>                     REG_SZ</dd>
    </dl>
    ```

> [!NOTE]
> <span data-ttu-id="1d8be-134">Per eseguire il debug di Winlogon, è necessario usare il debugger simbolico di Windows (NTSD).</span><span class="sxs-lookup"><span data-stu-id="1d8be-134">You must use the Windows symbolic debugger (NTSD) to debug Winlogon.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1d8be-135">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="1d8be-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1d8be-136">Caricamento ed esecuzione di una DLL GINA</span><span class="sxs-lookup"><span data-stu-id="1d8be-136">Loading and Running a GINA DLL</span></span>](loading-and-running-a-gina-dll.md)
</dt> <dt>

[<span data-ttu-id="1d8be-137">Funzioni di esportazione GINA</span><span class="sxs-lookup"><span data-stu-id="1d8be-137">GINA Export Functions</span></span>](authentication-functions.md)
</dt> <dt>

[<span data-ttu-id="1d8be-138">Strutture GINA</span><span class="sxs-lookup"><span data-stu-id="1d8be-138">GINA Structures</span></span>](authentication-structures.md)
</dt> <dt>

[<span data-ttu-id="1d8be-139">Funzioni di Servizi terminal GINA</span><span class="sxs-lookup"><span data-stu-id="1d8be-139">Terminal Services GINA Functions</span></span>](terminal-services-gina-functions.md)
</dt> </dl>

 

 
