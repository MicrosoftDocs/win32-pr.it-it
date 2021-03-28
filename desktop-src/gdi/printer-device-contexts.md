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
# <a name="printer-device-contexts-windows-gdi"></a>Contesti di dispositivo stampante (Windows GDI)

Il controller di dominio della stampante può essere utilizzato per la stampa su una stampante a matrice di punti, una stampante Ink-Jet, una stampante laser o un plotter. Un'applicazione crea un controller di dominio della stampante chiamando la funzione [**CreateDC**](/windows/desktop/api/Wingdi/nf-wingdi-createdca) e specificando gli argomenti appropriati (il nome del driver della stampante, il nome della stampante, il nome del file o del dispositivo per il supporto di output fisico e altri dati di inizializzazione). Quando un'applicazione ha terminato la stampa, il controller di dominio della stampante viene eliminato chiamando la funzione [**DeleteDC**](/windows/desktop/api/Wingdi/nf-wingdi-deletedc) . Un'applicazione deve eliminare, anziché rilasciare, un controller di dominio della stampante; la funzione [**ReleaseDC**](/windows/desktop/api/Winuser/nf-winuser-releasedc) ha esito negativo quando un'applicazione tenta di usarla per rilasciare un controller di dominio della stampante.

Per ulteriori informazioni, vedere [Printer output](../printdocs/printer-output.md).

 

 
