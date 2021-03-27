---
description: Disegno di testo
ms.assetid: 8a06f659-4e08-4738-b7a9-956b599c1344
title: Disegno di testo (Windows GDI)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7db44a756ff211bcae7605cb87bdac77005b34f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103754423"
---
# <a name="drawing-text-windows-gdi"></a><span data-ttu-id="c8b7a-103">Disegno di testo (Windows GDI)</span><span class="sxs-lookup"><span data-stu-id="c8b7a-103">Drawing Text (Windows GDI)</span></span>

<span data-ttu-id="c8b7a-104">Dopo che un'applicazione ha selezionato il tipo di carattere appropriato, imposta le opzioni di formattazione del testo necessarie e calcola i valori di larghezza e altezza dei caratteri necessari per una stringa di testo, può iniziare a disegnare caratteri e simboli chiamando una delle funzioni di output di testo:</span><span class="sxs-lookup"><span data-stu-id="c8b7a-104">After an application selects the appropriate font, sets the required text-formatting options, and computes the necessary character width and height values for a string of text, it can begin drawing characters and symbols by calling any of the text-output functions:</span></span>

-   [<span data-ttu-id="c8b7a-105">DrawText</span><span class="sxs-lookup"><span data-stu-id="c8b7a-105">DrawText</span></span>](/windows/desktop/api/Winuser/nf-winuser-drawtext)
-   [<span data-ttu-id="c8b7a-106">DrawTextEx</span><span class="sxs-lookup"><span data-stu-id="c8b7a-106">DrawTextEx</span></span>](/windows/desktop/api/Winuser/nf-winuser-drawtextexa)
-   [<span data-ttu-id="c8b7a-107">ExtTextOut</span><span class="sxs-lookup"><span data-stu-id="c8b7a-107">ExtTextOut</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-exttextouta)
-   [<span data-ttu-id="c8b7a-108">Sottotesto</span><span class="sxs-lookup"><span data-stu-id="c8b7a-108">PolyTextOut</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-polytextouta)
-   [<span data-ttu-id="c8b7a-109">TabbedTextOut</span><span class="sxs-lookup"><span data-stu-id="c8b7a-109">TabbedTextOut</span></span>](/windows/desktop/api/Winuser/nf-winuser-tabbedtextouta)
-   [<span data-ttu-id="c8b7a-110">TextOut</span><span class="sxs-lookup"><span data-stu-id="c8b7a-110">TextOut</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-textouta)

<span data-ttu-id="c8b7a-111">Quando un'applicazione chiama una di queste funzioni, il sistema operativo passa la chiamata al motore di grafica, che a sua volta passa la chiamata al driver di dispositivo appropriato.</span><span class="sxs-lookup"><span data-stu-id="c8b7a-111">When an application calls one of these functions, the operating system passes the call to the graphics engine, which in turn passes the call to the appropriate device driver.</span></span> <span data-ttu-id="c8b7a-112">A livello di driver di dispositivo, tutte queste chiamate sono supportate da una o più chiamate alla funzione [ExtTextOut](/windows/desktop/api/Wingdi/nf-wingdi-exttextouta) o [Text](/windows/desktop/api/Wingdi/nf-wingdi-textouta) out del driver.</span><span class="sxs-lookup"><span data-stu-id="c8b7a-112">At the device driver level, all of these calls are supported by one or more calls to the driver's own [ExtTextOut](/windows/desktop/api/Wingdi/nf-wingdi-exttextouta) or [TextOut](/windows/desktop/api/Wingdi/nf-wingdi-textouta) function.</span></span> <span data-ttu-id="c8b7a-113">Un'applicazione raggiungerà l'esecuzione più veloce chiamando [**ExtTextOut**](/windows/win32/api/wingdi/nf-wingdi-exttextouta), che viene rapidamente convertito in una chiamata **ExtTextOut** per il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c8b7a-113">An application will achieve the fastest execution by calling [**ExtTextOut**](/windows/win32/api/wingdi/nf-wingdi-exttextouta), which is quickly converted into an **ExtTextOut** call for the device.</span></span> <span data-ttu-id="c8b7a-114">Tuttavia, esistono istanze quando un'applicazione deve chiamare una delle altre tre funzioni; per creare, ad esempio, più righe di testo all'interno dei bordi di un'area rettangolare specificata, è più efficiente chiamare [**DrawText**](/windows/win32/api/winuser/nf-winuser-drawtext).</span><span class="sxs-lookup"><span data-stu-id="c8b7a-114">However, there are instances when an application should call one of the other three functions; for example, to draw multiple lines of text within the borders of a specified rectangular region, it is more efficient to call [**DrawText**](/windows/win32/api/winuser/nf-winuser-drawtext).</span></span> <span data-ttu-id="c8b7a-115">Per creare una tabella a più colonne con colonne giustificate di testo, è più efficiente chiamare [**TabbedTextOut**](/windows/win32/api/winuser/nf-winuser-tabbedtextouta).</span><span class="sxs-lookup"><span data-stu-id="c8b7a-115">To create a multicolumn table with justified columns of text, it is more efficient to call [**TabbedTextOut**](/windows/win32/api/winuser/nf-winuser-tabbedtextouta).</span></span>

 

 
