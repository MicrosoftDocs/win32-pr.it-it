---
description: Configurazione
ms.assetid: aba21473-07cc-4de9-a310-ad9b43c133eb
title: Configurazione (Windows e messaggi)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bac66d2ba25e81582734eb13148d2651b276ea01
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233326"
---
# <a name="configuration-windows-and-messages"></a><span data-ttu-id="284ce-103">Configurazione (Windows e messaggi)</span><span class="sxs-lookup"><span data-stu-id="284ce-103">Configuration (Windows and Messages)</span></span>

<span data-ttu-id="284ce-104">*Gli elementi di visualizzazione* sono le parti di una finestra e la visualizzazione visualizzata nella schermata di visualizzazione del sistema.</span><span class="sxs-lookup"><span data-stu-id="284ce-104">*Display elements* are the parts of a window and the display that appear on the system display screen.</span></span> <span data-ttu-id="284ce-105">Le *metriche di sistema* sono le dimensioni dei vari elementi di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="284ce-105">*System metrics* are the dimensions of various display elements.</span></span> <span data-ttu-id="284ce-106">Le metriche di sistema tipiche includono lo spessore del bordo della finestra, l'altezza dell'icona e così via.</span><span class="sxs-lookup"><span data-stu-id="284ce-106">Typical system metrics include the window border width, icon height, and so on.</span></span> <span data-ttu-id="284ce-107">Le metriche di sistema descrivono anche altri aspetti del sistema, ad esempio se è installato un mouse, sono supportati caratteri a byte doppio oppure è installata una versione di debug del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="284ce-107">System metrics also describe other aspects of the system, such as whether a mouse is installed, double-byte characters are supported, or a debugging version of the operating system is installed.</span></span> <span data-ttu-id="284ce-108">La funzione [**GetSystemMetrics**](/windows/win32/api/winuser/nf-winuser-getsystemmetrics) recupera la metrica di sistema specificata.</span><span class="sxs-lookup"><span data-stu-id="284ce-108">The [**GetSystemMetrics**](/windows/win32/api/winuser/nf-winuser-getsystemmetrics) function retrieves the specified system metric.</span></span>

<span data-ttu-id="284ce-109">Le applicazioni possono anche recuperare e impostare il colore degli elementi della finestra, ad esempio i menu, le barre di scorrimento e i pulsanti usando rispettivamente le funzioni [**GetSysColor**](/windows/desktop/api/winuser/nf-winuser-getsyscolor) e [**SetSysColors**](/windows/desktop/api/winuser/nf-winuser-setsyscolors) .</span><span class="sxs-lookup"><span data-stu-id="284ce-109">Applications can also retrieve and set the color of window elements such as menus, scroll bars, and buttons by using the [**GetSysColor**](/windows/desktop/api/winuser/nf-winuser-getsyscolor) and [**SetSysColors**](/windows/desktop/api/winuser/nf-winuser-setsyscolors) functions, respectively.</span></span>

<span data-ttu-id="284ce-110">La funzione [**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) Recupera o imposta diversi attributi di sistema, ad esempio l'ora di doppio clic, il timeout screen saver, lo spessore del bordo della finestra e il modello desktop.</span><span class="sxs-lookup"><span data-stu-id="284ce-110">The [**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) function retrieves or sets various system attributes, such as double-click time, screen saver time-out, window border width, and desktop pattern.</span></span> <span data-ttu-id="284ce-111">Quando un'applicazione usa **SystemParametersInfo** per impostare un parametro, la modifica viene immediatamente svolta.</span><span class="sxs-lookup"><span data-stu-id="284ce-111">When an application uses **SystemParametersInfo** to set a parameter, the change takes place immediately.</span></span> <span data-ttu-id="284ce-112">Questa funzione consente inoltre alle applicazioni di aggiornare il profilo utente, pertanto le modifiche apportate al sistema verranno mantenute al riavvio del sistema.</span><span class="sxs-lookup"><span data-stu-id="284ce-112">This function also enables applications to update the user profile, so changes to the system will be preserved when the system is restarted.</span></span>

 

 
