---
title: Voci del registro di sistema per il rilevamento dello stato dell'installazione
description: Voci del registro di sistema per il rilevamento dello stato dell'installazione
ms.assetid: 898f9117-94fd-4230-9378-b8c6a4401a96
keywords:
- Windows Media Player, verifica dello stato di avanzamento dell'installazione
- Windows Media Player, rilevamento stato installazione
- Windows Media Player, rilevamento dello stato di avanzamento delle installazioni
- Windows Media Player, registro di sistema
- Registro di sistema, verifica dello stato dell'installazione
- registro, rilevamento stato installazione
- Registro di sistema, rilevamento dello stato delle installazioni
- Registro di sistema, impostazioni per Windows Media Player
- Verifica dello stato di avanzamento dell'installazione
- installazione del rilevamento dello stato
- rilevamento dello stato delle installazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3add1d2feb668ee90418704b9a11b0072530f120
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104045346"
---
# <a name="registry-entries-for-tracking-installation-progress"></a><span data-ttu-id="16e35-114">Voci del registro di sistema per il rilevamento dello stato dell'installazione</span><span class="sxs-lookup"><span data-stu-id="16e35-114">Registry Entries for Tracking Installation Progress</span></span>

<span data-ttu-id="16e35-115">Il programma di installazione di Windows Media Player 11, installazione \_wm.exe, scrive le seguenti voci nel registro di sistema in modo che i programmi di installazione possano tenere traccia dello stato di avanzamento del programma di installazione di windows media Player durante l'esecuzione.</span><span class="sxs-lookup"><span data-stu-id="16e35-115">The Windows Media Player 11 setup program, setup\_wm.exe, writes the following entries in the registry so that installation programs can track the progress of the Windows Media Player setup program as it runs.</span></span>


```C++
[HKEY_LOCAL_MACHINE\Software\Microsoft\MediaPlayer\Setup]
"Progress_CurrentDialog" = dword:value
"Progress_MaxDialog" = dword:value
"Progress_CurrentInstall" = dword:value
"Progress_MaxInstall" = dword:value
```



<span data-ttu-id="16e35-116">Nella sintassi del registro di sistema precedente, *value* è un segnaposto per un valore integer.</span><span class="sxs-lookup"><span data-stu-id="16e35-116">In the preceding registry syntax, *value* is a placeholder for an integer value.</span></span>

<span data-ttu-id="16e35-117">Stato \_ CurrentDialog indica la finestra di dialogo in cui è attualmente visualizzato il programma di installazione di Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="16e35-117">Progress\_CurrentDialog indicates which dialog box Windows Media Player setup is currently displaying.</span></span> <span data-ttu-id="16e35-118">Stato \_ MaxDialog indica il numero totale di finestre di dialogo che Windows Media visualizzerà.</span><span class="sxs-lookup"><span data-stu-id="16e35-118">Progress\_MaxDialog indicates the total number of dialog boxes that Windows Media will display.</span></span> <span data-ttu-id="16e35-119">Ad esempio, se Progress \_ CurrentDialog = 2 e Progress \_ MaxDialog = 5, Windows Media Player attualmente Visualizza la seconda finestra di dialogo in una sequenza di cinque.</span><span class="sxs-lookup"><span data-stu-id="16e35-119">For example, if Progress\_CurrentDialog = 2 and Progress\_MaxDialog = 5, Windows Media Player is currently displaying the second dialog box in a sequence of five.</span></span>

<span data-ttu-id="16e35-120">Lo stato \_ CurrentInstall e \_ lo stato MaxInstall, insieme, indicano la percentuale di completamento della finestra di dialogo corrente.</span><span class="sxs-lookup"><span data-stu-id="16e35-120">Progress\_CurrentInstall and Progress\_MaxInstall, taken together, indicate the percent of completion of the current dialog.</span></span> <span data-ttu-id="16e35-121">Ad esempio, se Progress \_ CurrentInstall = 6 e Progress \_ MaxInstall = 25, la finestra di dialogo corrente è 6/25 (ovvero 24%) completare.</span><span class="sxs-lookup"><span data-stu-id="16e35-121">For example, if Progress\_CurrentInstall = 6 and Progress\_MaxInstall = 25, the current dialog is 6/25 (that is, 24%) complete.</span></span>

## <a name="related-topics"></a><span data-ttu-id="16e35-122">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="16e35-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="16e35-123">**Impostazioni del registro di sistema**</span><span class="sxs-lookup"><span data-stu-id="16e35-123">**Registry Settings**</span></span>](registry-settings.md)
</dt> </dl>

 

 




