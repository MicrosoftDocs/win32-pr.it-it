---
description: Il controller di dominio della stampante può essere utilizzato per la stampa su una stampante a matrice di punti, una stampante Ink-Jet, una stampante laser o un plotter.
ms.assetid: c53f15d8-5a02-4095-8f05-ae309d4553ff
title: Contesti di dispositivo stampante (Windows GDI)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7475776a3d13394b210f8289b458b8e99c474c93
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104978386"
---
# <a name="printer-device-contexts-windows-gdi"></a><span data-ttu-id="6c992-103">Contesti di dispositivo stampante (Windows GDI)</span><span class="sxs-lookup"><span data-stu-id="6c992-103">Printer Device Contexts (Windows GDI)</span></span>

<span data-ttu-id="6c992-104">Il controller di dominio della stampante può essere utilizzato per la stampa su una stampante a matrice di punti, una stampante Ink-Jet, una stampante laser o un plotter.</span><span class="sxs-lookup"><span data-stu-id="6c992-104">The printer DC can be used when printing on a dot-matrix printer, ink-jet printer, laser printer, or plotter.</span></span> <span data-ttu-id="6c992-105">Un'applicazione crea un controller di dominio della stampante chiamando la funzione [**CreateDC**](/windows/desktop/api/Wingdi/nf-wingdi-createdca) e specificando gli argomenti appropriati (il nome del driver della stampante, il nome della stampante, il nome del file o del dispositivo per il supporto di output fisico e altri dati di inizializzazione).</span><span class="sxs-lookup"><span data-stu-id="6c992-105">An application creates a printer DC by calling the [**CreateDC**](/windows/desktop/api/Wingdi/nf-wingdi-createdca) function and supplying the appropriate arguments (the name of the printer driver, the name of the printer, the file or device name for the physical output medium, and other initialization data).</span></span> <span data-ttu-id="6c992-106">Quando un'applicazione ha terminato la stampa, il controller di dominio della stampante viene eliminato chiamando la funzione [**DeleteDC**](/windows/desktop/api/Wingdi/nf-wingdi-deletedc) .</span><span class="sxs-lookup"><span data-stu-id="6c992-106">When an application has finished printing, it deletes the printer DC by calling the [**DeleteDC**](/windows/desktop/api/Wingdi/nf-wingdi-deletedc) function.</span></span> <span data-ttu-id="6c992-107">Un'applicazione deve eliminare, anziché rilasciare, un controller di dominio della stampante; la funzione [**ReleaseDC**](/windows/desktop/api/Winuser/nf-winuser-releasedc) ha esito negativo quando un'applicazione tenta di usarla per rilasciare un controller di dominio della stampante.</span><span class="sxs-lookup"><span data-stu-id="6c992-107">An application must delete (rather than release) a printer DC; the [**ReleaseDC**](/windows/desktop/api/Winuser/nf-winuser-releasedc) function fails when an application attempts to use it to release a printer DC.</span></span>

<span data-ttu-id="6c992-108">Per ulteriori informazioni, vedere [Printer output](../printdocs/printer-output.md).</span><span class="sxs-lookup"><span data-stu-id="6c992-108">For more information, see [Printer Output](../printdocs/printer-output.md).</span></span>

 

 
