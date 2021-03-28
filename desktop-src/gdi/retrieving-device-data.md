---
description: 'Le applicazioni possono usare le funzioni seguenti per recuperare i dati del dispositivo usando un contesto di dispositivo: GetDeviceCaps e DeviceCapabilities.'
ms.assetid: eed6a323-b7eb-41a2-adb9-592f3f912884
title: Recupero dei dati del dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28fa4054170f9b66d73e3494928db312eb8aa9d3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104978306"
---
# <a name="retrieving-device-data"></a><span data-ttu-id="706ec-103">Recupero dei dati del dispositivo</span><span class="sxs-lookup"><span data-stu-id="706ec-103">Retrieving Device Data</span></span>

<span data-ttu-id="706ec-104">Le applicazioni possono usare le funzioni seguenti per recuperare i dati del dispositivo usando un contesto di dispositivo: [**GetDeviceCaps**](/windows/desktop/api/Wingdi/nf-wingdi-getdevicecaps) e [**DeviceCapabilities**](/windows/win32/api/wingdi/nf-wingdi-devicecapabilitiesa).</span><span class="sxs-lookup"><span data-stu-id="706ec-104">Applications can use the following functions to retrieve device data using a device context: [**GetDeviceCaps**](/windows/desktop/api/Wingdi/nf-wingdi-getdevicecaps) and [**DeviceCapabilities**](/windows/win32/api/wingdi/nf-wingdi-devicecapabilitiesa).</span></span>

<span data-ttu-id="706ec-105">[**GetDeviceCaps**](/windows/desktop/api/Wingdi/nf-wingdi-getdevicecaps) recupera i dati generali del dispositivo per i dispositivi seguenti:</span><span class="sxs-lookup"><span data-stu-id="706ec-105">[**GetDeviceCaps**](/windows/desktop/api/Wingdi/nf-wingdi-getdevicecaps) retrieves general device data for the following devices:</span></span>

-   <span data-ttu-id="706ec-106">Visualizzazioni raster</span><span class="sxs-lookup"><span data-stu-id="706ec-106">Raster displays</span></span>
-   <span data-ttu-id="706ec-107">Stampanti a matrice di punti</span><span class="sxs-lookup"><span data-stu-id="706ec-107">Dot-matrix printers</span></span>
-   <span data-ttu-id="706ec-108">Stampanti Ink-Jet</span><span class="sxs-lookup"><span data-stu-id="706ec-108">Ink-jet printers</span></span>
-   <span data-ttu-id="706ec-109">Stampanti laser</span><span class="sxs-lookup"><span data-stu-id="706ec-109">Laser printers</span></span>
-   <span data-ttu-id="706ec-110">Plotter vettoriali</span><span class="sxs-lookup"><span data-stu-id="706ec-110">Vector plotters</span></span>
-   <span data-ttu-id="706ec-111">Fotocamere raster</span><span class="sxs-lookup"><span data-stu-id="706ec-111">Raster cameras</span></span>

<span data-ttu-id="706ec-112">I dati includono le funzionalità supportate del dispositivo, inclusa la risoluzione del dispositivo (per le visualizzazioni video), il formato colori (per le visualizzazioni video e le stampanti colori), il numero di oggetti grafici, le funzionalità raster, il disegno a curva, il disegno a linee, il disegno del poligono e il disegno del testo.</span><span class="sxs-lookup"><span data-stu-id="706ec-112">The data includes the supported capabilities of the device, including device resolution (for video displays), color format (for video displays and color printers), number of graphic objects, raster capabilities, curve drawing, line drawing, polygon drawing, and text drawing.</span></span> <span data-ttu-id="706ec-113">Un'applicazione recupera questi dati fornendo un handle che identifica il contesto di dispositivo appropriato, oltre a un indice che specifica il tipo di dati che la funzione deve recuperare.</span><span class="sxs-lookup"><span data-stu-id="706ec-113">An application retrieves this data by supplying a handle identifying the appropriate device context, as well as an index specifying the type of data the function is to retrieve.</span></span>

<span data-ttu-id="706ec-114">La funzione [**DeviceCapabilities**](/windows/win32/api/wingdi/nf-wingdi-devicecapabilitiesa) recupera i dati specifici delle stampanti, incluso il numero di contenitori di carta disponibili, le funzionalità duplex della stampante, le risoluzioni supportate dalla stampante, le dimensioni massime e minime supportate della carta e così via.</span><span class="sxs-lookup"><span data-stu-id="706ec-114">The [**DeviceCapabilities**](/windows/win32/api/wingdi/nf-wingdi-devicecapabilitiesa) function retrieves data specific to printers, including the number of available paper bins, the duplex capabilities of the printer, the resolutions supported by the printer, the maximum and minimum supported paper size, and so on.</span></span> <span data-ttu-id="706ec-115">Un'applicazione recupera questi dati fornendo stringhe che specificano un dispositivo e una porta della stampante, oltre a un indice che specifica il tipo di dati che la funzione deve recuperare.</span><span class="sxs-lookup"><span data-stu-id="706ec-115">An application retrieves this data by supplying strings specifying a printer device and port, as well as an index specifying the type of data that the function is to retrieve.</span></span>

 

 
