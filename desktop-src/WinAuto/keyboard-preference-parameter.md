---
title: Parametro preferenza tastiera
description: Il parametro preferenza tastiera indica che l'utente si basa sulla tastiera anziché sul mouse, quindi le applicazioni devono visualizzare le interfacce della tastiera che altrimenti sarebbero nascoste.
ms.assetid: dc3c02d2-a350-4a86-a0b0-9dbb83880029
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 802d4ff76efae985cc07b6fe42f9d6b53cdf0b53
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399271"
---
# <a name="keyboard-preference-parameter"></a><span data-ttu-id="d0642-103">Parametro preferenza tastiera</span><span class="sxs-lookup"><span data-stu-id="d0642-103">Keyboard preference parameter</span></span>

<span data-ttu-id="d0642-104">Il parametro preferenza tastiera indica che l'utente si basa sulla tastiera anziché sul mouse, quindi le applicazioni devono visualizzare le interfacce della tastiera che altrimenti sarebbero nascoste.</span><span class="sxs-lookup"><span data-stu-id="d0642-104">The keyboard preference parameter indicates that the user relies on the keyboard instead of the mouse, so applications should display keyboard interfaces that would otherwise be hidden.</span></span>

<span data-ttu-id="d0642-105">L'utente controlla l'impostazione del parametro preferenza tastiera usando il centro di accesso facilitato nel pannello di controllo o un'altra applicazione per la personalizzazione dell'ambiente.</span><span class="sxs-lookup"><span data-stu-id="d0642-105">The user controls the setting of the keyboard preference parameter by using the Ease of Access Center in Control Panel, or another application for customizing the environment.</span></span> <span data-ttu-id="d0642-106">Le applicazioni usano i flag **SPI \_ GETKEYBOARDPREF** e **SPI \_ SETKEYBOARDPREF** con la funzione [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) per ottenere e impostare il parametro di preferenza della tastiera.</span><span class="sxs-lookup"><span data-stu-id="d0642-106">Applications use the **SPI\_GETKEYBOARDPREF** and **SPI\_SETKEYBOARDPREF** flags with the [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) function to get and set the keyboard preference parameter.</span></span>

<span data-ttu-id="d0642-107">Inoltre, in Windows 2000, gli utenti possono impostare un parametro che indica se i tasti di scelta dei menu sono sempre sottolineati.</span><span class="sxs-lookup"><span data-stu-id="d0642-107">Additionally, on Windows 2000, users can set a parameter that indicates whether menu access keys are always underlined.</span></span> <span data-ttu-id="d0642-108">Le applicazioni usano i flag **SPI \_ GETMENUUNDERLINES** e **SPI \_ SETMENUUNDERLINES** con la funzione [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) per ottenere e impostare il parametro di sottolineatura menu.</span><span class="sxs-lookup"><span data-stu-id="d0642-108">Applications use the **SPI\_GETMENUUNDERLINES** and **SPI\_SETMENUUNDERLINES** flags with the [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) function to get and set the menu underlines parameter.</span></span>

<span data-ttu-id="d0642-109">Quando un'applicazione riceve un messaggio [**WM \_ SETTINGCHANGE**](/windows/desktop/winmsg/wm-settingchange) per il parametro preferenza tastiera o sottolineatura menu, è consigliabile che l'applicazione chiami [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) per aggiornare le informazioni per entrambi i parametri.</span><span class="sxs-lookup"><span data-stu-id="d0642-109">When an application receives a [**WM\_SETTINGCHANGE**](/windows/desktop/winmsg/wm-settingchange) message for either the keyboard preference or menu underline parameter, it is recommended that the application call [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) to update the information for both parameters.</span></span>

<span data-ttu-id="d0642-110">Si noti **che \_ SPI GETMENUUNDERLINES** è uguale a **SPI \_ GETKEYBOARDCUES** e **SPI \_ SETMENUUNDERLINES** è uguale a **SPI \_ SETKEYBOARDCUES**.</span><span class="sxs-lookup"><span data-stu-id="d0642-110">Note that **SPI\_GETMENUUNDERLINES** is the same as **SPI\_GETKEYBOARDCUES**, and **SPI\_SETMENUUNDERLINES** is the same as **SPI\_SETKEYBOARDCUES**.</span></span>

 

 