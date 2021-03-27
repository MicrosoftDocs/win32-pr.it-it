---
description: "Le funzioni seguenti consentono a un'applicazione di salvare, ripristinare e reimpostare un contesto di dispositivo: SaveDC, RestoreDC e ResetDC."
ms.assetid: 22837876-2665-49c6-908e-80e107fc09f4
title: Salvataggio, ripristino e reimpostazione di un contesto di dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2714360c07f4a4eca354ede5b460864cc897e58
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104979791"
---
# <a name="saving-restoring-and-resetting-a-device-context"></a><span data-ttu-id="2bd25-103">Salvataggio, ripristino e reimpostazione di un contesto di dispositivo</span><span class="sxs-lookup"><span data-stu-id="2bd25-103">Saving, Restoring, and Resetting a Device Context</span></span>

<span data-ttu-id="2bd25-104">Le funzioni seguenti consentono a un'applicazione di salvare, ripristinare e reimpostare un contesto di dispositivo: [**SaveDC**](/windows/desktop/api/Wingdi/nf-wingdi-savedc), [**RestoreDC**](/windows/desktop/api/Wingdi/nf-wingdi-restoredc)e [**ResetDC**](/windows/desktop/api/Wingdi/nf-wingdi-resetdca).</span><span class="sxs-lookup"><span data-stu-id="2bd25-104">The following functions enable an application to save, restore, and reset a device context: [**SaveDC**](/windows/desktop/api/Wingdi/nf-wingdi-savedc), [**RestoreDC**](/windows/desktop/api/Wingdi/nf-wingdi-restoredc), and [**ResetDC**](/windows/desktop/api/Wingdi/nf-wingdi-resetdca).</span></span> <span data-ttu-id="2bd25-105">La funzione SaveDC registra in uno stack GDI speciale gli oggetti grafici del controller di dominio corrente, i relativi attributi e le modalità grafiche.</span><span class="sxs-lookup"><span data-stu-id="2bd25-105">The SaveDC function records on a special GDI stack the current DC's graphic objects and their attributes, and graphic modes.</span></span> <span data-ttu-id="2bd25-106">Un'applicazione di disegno può chiamare questa funzione prima che un utente inizi a disegnare e salvare lo stato originale dell'applicazione fornendo uno Slate pulito per l'utente.</span><span class="sxs-lookup"><span data-stu-id="2bd25-106">A drawing application can call this function before a user begins drawing and save the application's original state providing a clean slate for the user.</span></span> <span data-ttu-id="2bd25-107">Per tornare a questo stato originale, l'applicazione chiama la funzione RestoreDC.</span><span class="sxs-lookup"><span data-stu-id="2bd25-107">To return to this original state, the application calls the RestoreDC function.</span></span>

<span data-ttu-id="2bd25-108">[**ResetDC**](/windows/desktop/api/Wingdi/nf-wingdi-resetdca) viene fornito per reimpostare i dati del controller di dominio della stampante.</span><span class="sxs-lookup"><span data-stu-id="2bd25-108">[**ResetDC**](/windows/desktop/api/Wingdi/nf-wingdi-resetdca) is provided to reset printer DC data.</span></span> <span data-ttu-id="2bd25-109">Un'applicazione chiama questa funzione per reimpostare l'orientamento della carta, il formato della carta, il fattore di scala di output, il numero di copie da stampare, l'origine (o il contenitore) della carta, la modalità duplex e così via.</span><span class="sxs-lookup"><span data-stu-id="2bd25-109">An application calls this function to reset the paper orientation, paper size, output scaling factor, number of copies to be printed, paper source (or bin), duplex mode, and so on.</span></span> <span data-ttu-id="2bd25-110">In genere, un'applicazione chiama questa funzione dopo che un utente ha modificato una delle opzioni della stampante e il sistema ha emesso un messaggio [**WM \_ DEVMODECHANGE**](wm-devmodechange.md) .</span><span class="sxs-lookup"><span data-stu-id="2bd25-110">Typically, an application calls this function after a user has changed one of the printer options and the system has issued a [**WM\_DEVMODECHANGE**](wm-devmodechange.md) message.</span></span>

 

 



