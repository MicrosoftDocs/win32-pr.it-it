---
description: Questa sezione di riferimento descrive la configurazione per Windows e Messaggi. Informazioni sugli elementi di visualizzazione e sulle metriche di sistema.
ms.assetid: aba21473-07cc-4de9-a310-ad9b43c133eb
title: Configurazione (Windows e messaggi)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ffa516e87aa7d338d4e2fd46a160fcbd6dadb305
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112406344"
---
# <a name="configuration-windows-and-messages"></a><span data-ttu-id="563be-104">Configurazione (Windows e messaggi)</span><span class="sxs-lookup"><span data-stu-id="563be-104">Configuration (Windows and Messages)</span></span>

<span data-ttu-id="563be-105">*Gli elementi* di visualizzazione sono le parti di una finestra e la visualizzazione visualizzata sullo schermo del sistema.</span><span class="sxs-lookup"><span data-stu-id="563be-105">*Display elements* are the parts of a window and the display that appear on the system display screen.</span></span> <span data-ttu-id="563be-106">*Le metriche di* sistema sono le dimensioni dei vari elementi di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="563be-106">*System metrics* are the dimensions of various display elements.</span></span> <span data-ttu-id="563be-107">Le metriche di sistema tipiche includono la larghezza del bordo della finestra, l'altezza dell'icona e così via.</span><span class="sxs-lookup"><span data-stu-id="563be-107">Typical system metrics include the window border width, icon height, and so on.</span></span> <span data-ttu-id="563be-108">Le metriche di sistema descrivono anche altri aspetti del sistema, ad esempio se è installato un mouse, sono supportati caratteri a doppio byte o è installata una versione di debug del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="563be-108">System metrics also describe other aspects of the system, such as whether a mouse is installed, double-byte characters are supported, or a debugging version of the operating system is installed.</span></span> <span data-ttu-id="563be-109">La [**funzione GetSystemMetrics**](/windows/win32/api/winuser/nf-winuser-getsystemmetrics) recupera la metrica di sistema specificata.</span><span class="sxs-lookup"><span data-stu-id="563be-109">The [**GetSystemMetrics**](/windows/win32/api/winuser/nf-winuser-getsystemmetrics) function retrieves the specified system metric.</span></span>

<span data-ttu-id="563be-110">Le applicazioni possono anche recuperare e impostare il colore degli elementi della finestra, ad esempio menu, barre di scorrimento e pulsanti, usando rispettivamente le funzioni [**GetSysColor**](/windows/desktop/api/winuser/nf-winuser-getsyscolor) e [**SetSysColors.**](/windows/desktop/api/winuser/nf-winuser-setsyscolors)</span><span class="sxs-lookup"><span data-stu-id="563be-110">Applications can also retrieve and set the color of window elements such as menus, scroll bars, and buttons by using the [**GetSysColor**](/windows/desktop/api/winuser/nf-winuser-getsyscolor) and [**SetSysColors**](/windows/desktop/api/winuser/nf-winuser-setsyscolors) functions, respectively.</span></span>

<span data-ttu-id="563be-111">La [**funzione SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) recupera o imposta vari attributi di sistema, ad esempio l'ora del doppio clic, screen saver timeout, lo spessore del bordo della finestra e il modello del desktop.</span><span class="sxs-lookup"><span data-stu-id="563be-111">The [**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) function retrieves or sets various system attributes, such as double-click time, screen saver time-out, window border width, and desktop pattern.</span></span> <span data-ttu-id="563be-112">Quando un'applicazione **usa SystemParametersInfo per** impostare un parametro, la modifica viene apportata immediatamente.</span><span class="sxs-lookup"><span data-stu-id="563be-112">When an application uses **SystemParametersInfo** to set a parameter, the change takes place immediately.</span></span> <span data-ttu-id="563be-113">Questa funzione consente anche alle applicazioni di aggiornare il profilo utente, in modo che le modifiche apportate al sistema verranno mantenute al riavvio del sistema.</span><span class="sxs-lookup"><span data-stu-id="563be-113">This function also enables applications to update the user profile, so changes to the system will be preserved when the system is restarted.</span></span>

 

 
