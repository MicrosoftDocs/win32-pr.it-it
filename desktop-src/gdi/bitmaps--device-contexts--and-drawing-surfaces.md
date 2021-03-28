---
description: Un contesto di dispositivo (DC) è una struttura di dati che definisce gli oggetti grafici, gli attributi associati e le modalità grafiche che interessano l'output in un dispositivo. Per creare un controller di dominio, chiamare la funzione CreateDC. per recuperare un controller di dominio, chiamare la funzione GetDC.
ms.assetid: 4feafb23-bf5a-493a-9d1d-96170711b907
title: Bitmap, contesti di dispositivo e superfici di disegno
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6297eb3446d05d0fa21ac23c9de9f3416a300746
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226710"
---
# <a name="bitmaps-device-contexts-and-drawing-surfaces"></a><span data-ttu-id="8ebf9-104">Bitmap, contesti di dispositivo e superfici di disegno</span><span class="sxs-lookup"><span data-stu-id="8ebf9-104">Bitmaps, Device Contexts, and Drawing Surfaces</span></span>

<span data-ttu-id="8ebf9-105">Un *contesto di dispositivo* (DC) è una struttura di dati che definisce gli oggetti grafici, gli attributi associati e le modalità grafiche che interessano l'output in un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8ebf9-105">A *device context* (DC) is a data structure defining the graphics objects, their associated attributes, and the graphics modes affecting output on a device.</span></span> <span data-ttu-id="8ebf9-106">Per creare un controller di dominio, chiamare la funzione [**CreateDC**](/windows/desktop/api/Wingdi/nf-wingdi-createdca) . per recuperare un controller di dominio, chiamare la funzione [**GetDC**](/windows/desktop/api/Winuser/nf-winuser-getdc) .</span><span class="sxs-lookup"><span data-stu-id="8ebf9-106">To create a DC, call the [**CreateDC**](/windows/desktop/api/Wingdi/nf-wingdi-createdca) function; to retrieve a DC, call the [**GetDC**](/windows/desktop/api/Winuser/nf-winuser-getdc) function.</span></span>

<span data-ttu-id="8ebf9-107">Prima di restituire un handle che identifichi il controller di dominio, il sistema seleziona una superficie di disegno nel controller di dominio.</span><span class="sxs-lookup"><span data-stu-id="8ebf9-107">Before returning a handle that identifies that DC, the system selects a drawing surface into the DC.</span></span> <span data-ttu-id="8ebf9-108">Se l'applicazione ha chiamato la funzione [**CreateDC**](/windows/desktop/api/Wingdi/nf-wingdi-createdca) per creare un contesto di dispositivo per una visualizzazione VGA, le dimensioni della superficie di disegno sono 640 per 480 pixel.</span><span class="sxs-lookup"><span data-stu-id="8ebf9-108">If the application called the [**CreateDC**](/windows/desktop/api/Wingdi/nf-wingdi-createdca) function to create a device context for a VGA display, the dimensions of this drawing surface are 640-by-480 pixels.</span></span> <span data-ttu-id="8ebf9-109">Se l'applicazione ha chiamato la funzione [**GetDC**](/windows/desktop/api/Winuser/nf-winuser-getdc) , le dimensioni riflettono le dimensioni dell'area client.</span><span class="sxs-lookup"><span data-stu-id="8ebf9-109">If the application called the [**GetDC**](/windows/desktop/api/Winuser/nf-winuser-getdc) function, the dimensions reflect the size of the client area.</span></span>

<span data-ttu-id="8ebf9-110">Prima che un'applicazione possa iniziare a disegnare, deve selezionare una bitmap con la larghezza e l'altezza appropriate per il controller di dominio chiamando la funzione [**SelezionaOggetto**](/windows/desktop/api/Wingdi/nf-wingdi-selectobject) .</span><span class="sxs-lookup"><span data-stu-id="8ebf9-110">Before an application can begin drawing, it must select a bitmap with the appropriate width and height into the DC by calling the [**SelectObject**](/windows/desktop/api/Wingdi/nf-wingdi-selectobject) function.</span></span> <span data-ttu-id="8ebf9-111">Quando un'applicazione passa l'handle al controller di dominio a una delle funzioni di disegno GDI (Graphics Device Interface), l'output richiesto viene visualizzato nella superficie di disegno selezionata nel controller di dominio.</span><span class="sxs-lookup"><span data-stu-id="8ebf9-111">When an application passes the handle to the DC to one of the graphics device interface (GDI) drawing functions, the requested output appears on the drawing surface selected into the DC.</span></span>

<span data-ttu-id="8ebf9-112">Per altre informazioni, vedere [contesti di dispositivo di memoria](memory-device-contexts.md).</span><span class="sxs-lookup"><span data-stu-id="8ebf9-112">For more information, see [Memory Device Contexts](memory-device-contexts.md).</span></span>

 

 



