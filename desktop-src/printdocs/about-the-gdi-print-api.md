---
description: Una delle funzionalità principali delle funzioni nell'API di stampa GDI è il supporto dell'indipendenza del dispositivo.
ms.assetid: 3efcc6d0-14f0-4605-9603-ccc7ad0cc895
title: Informazioni sull'API di stampa GDI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e6e8a34552a1198ebe618f463003fe28ded6aed
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316429"
---
# <a name="about-the-gdi-print-api"></a><span data-ttu-id="d6cc5-103">Informazioni sull'API di stampa GDI</span><span class="sxs-lookup"><span data-stu-id="d6cc5-103">About the GDI Print API</span></span>

<span data-ttu-id="d6cc5-104">Una delle funzionalità principali delle funzioni nell'API di stampa GDI è il supporto dell'indipendenza del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d6cc5-104">One of the chief features of the functions in the GDI print API is their support of device independence.</span></span> <span data-ttu-id="d6cc5-105">Anziché emettere comandi specifici del dispositivo per tracciare l'output su una stampante o un plotter particolare, un'applicazione chiama funzioni di alto livello dall'interfaccia GDI (Graphics Device Interface).</span><span class="sxs-lookup"><span data-stu-id="d6cc5-105">Instead of issuing device-specific commands to draw output on a particular printer or plotter, an application calls high-level functions from the graphics device interface (GDI).</span></span> <span data-ttu-id="d6cc5-106">Per stampare un'immagine bitmap, ad esempio, un'applicazione può chiamare la funzione [**BitBlt**](/windows/desktop/api/wingdi/nf-wingdi-bitblt) , fornendo le coordinate per la bitmap, nonché gli handle che identificano i contesti di dispositivo di origine e di destinazione.</span><span class="sxs-lookup"><span data-stu-id="d6cc5-106">For example, to print a bitmapped image, an application can call the [**BitBlt**](/windows/desktop/api/wingdi/nf-wingdi-bitblt) function, supplying the coordinates for the bitmap as well as handles identifying the source and destination device contexts (DCs).</span></span> <span data-ttu-id="d6cc5-107">La chiamata a **BitBlt** viene quindi convertita in comandi di dispositivo RAW da parte di un driver della stampante.</span><span class="sxs-lookup"><span data-stu-id="d6cc5-107">The call to **BitBlt** is then converted to raw device commands by a printer driver.</span></span> <span data-ttu-id="d6cc5-108">Un driver di dispositivo è una libreria di collegamento dinamico (DLL) che supporta l'interfaccia DDI (Device Driver Interface).</span><span class="sxs-lookup"><span data-stu-id="d6cc5-108">A device driver is a dynamic-link library (DLL) that supports the device driver interface (DDI).</span></span> <span data-ttu-id="d6cc5-109">Un driver di dispositivo genera comandi per i dispositivi non elaborati quando elabora le chiamate alle funzioni DDI eseguite dal motore di grafica.</span><span class="sxs-lookup"><span data-stu-id="d6cc5-109">A device driver generates raw device commands when it processes calls to DDI functions made by the graphics engine.</span></span> <span data-ttu-id="d6cc5-110">I comandi vengono elaborati dalla stampante quando viene stampata l'immagine.</span><span class="sxs-lookup"><span data-stu-id="d6cc5-110">The commands are processed by the printer when it prints the image.</span></span> <span data-ttu-id="d6cc5-111">La sintassi, il numero e il tipo di questi comandi variano da dispositivo a dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d6cc5-111">The syntax, number, and type of these commands vary from device to device.</span></span>

<span data-ttu-id="d6cc5-112">In questa panoramica vengono fornite informazioni sui seguenti argomenti.</span><span class="sxs-lookup"><span data-stu-id="d6cc5-112">This overview provides information on the following topics.</span></span>

<dl>

[<span data-ttu-id="d6cc5-113">Interfaccia di stampa predefinita</span><span class="sxs-lookup"><span data-stu-id="d6cc5-113">Default Printing Interface</span></span>](default-printing-interface.md)  
[<span data-ttu-id="d6cc5-114">Contesti di dispositivo stampante</span><span class="sxs-lookup"><span data-stu-id="d6cc5-114">Printer Device Contexts</span></span>](printer-output.md)  
[<span data-ttu-id="d6cc5-115">Caratteri di escape della stampante</span><span class="sxs-lookup"><span data-stu-id="d6cc5-115">Printer Escapes</span></span>](printer-escapes.md)  
[<span data-ttu-id="d6cc5-116">Visualizzazione e output WYSIWYG</span><span class="sxs-lookup"><span data-stu-id="d6cc5-116">WYSIWYG Display and Output</span></span>](wysiwyg-display-and-output.md)  
[<span data-ttu-id="d6cc5-117">DEVMODE per utente</span><span class="sxs-lookup"><span data-stu-id="d6cc5-117">Per-User DEVMODE</span></span>](per-user-devmode.md)  
</dl>

 

 
