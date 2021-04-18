---
description: Delle sei modalità di mapping predefinite, una è dipendente dal dispositivo ( \_ testo mm) e i restanti cinque (mm \_ HIENGLISH, mm \_ LOENGLISH, MM \_ HIMETRIC, mm \_ LOMETRIC e mm \_ twip) sono indipendenti dal dispositivo.
ms.assetid: 722df020-edf2-4763-b58c-3e29fa7007db
title: Modalità di mapping predefinite
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f252f587e98a739306a84450a1d9669ed21873cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104978383"
---
# <a name="predefined-mapping-modes"></a><span data-ttu-id="797c5-103">Modalità di mapping predefinite</span><span class="sxs-lookup"><span data-stu-id="797c5-103">Predefined Mapping Modes</span></span>

<span data-ttu-id="797c5-104">Delle sei modalità di mapping predefinite, una è dipendente dal dispositivo ( \_ testo mm) e i restanti cinque (mm \_ HIENGLISH, mm \_ LOENGLISH, MM \_ HIMETRIC, mm \_ LOMETRIC e mm \_ twip) sono indipendenti dal dispositivo.</span><span class="sxs-lookup"><span data-stu-id="797c5-104">Of the six predefined mapping modes, one is device dependent (MM\_TEXT) and the remaining five (MM\_HIENGLISH, MM\_LOENGLISH, MM\_HIMETRIC, MM\_LOMETRIC, and MM\_TWIPS) are device independent.</span></span>

<span data-ttu-id="797c5-105">La modalità di mapping predefinita è il \_ testo mm.</span><span class="sxs-lookup"><span data-stu-id="797c5-105">The default mapping mode is MM\_TEXT.</span></span> <span data-ttu-id="797c5-106">Un'unità logica equivale a un pixel.</span><span class="sxs-lookup"><span data-stu-id="797c5-106">One logical unit equals one pixel.</span></span> <span data-ttu-id="797c5-107">X positivo è a destra e y positivo è inattivo.</span><span class="sxs-lookup"><span data-stu-id="797c5-107">Positive x is to the right, and positive y is down.</span></span> <span data-ttu-id="797c5-108">Questa modalità è mappata direttamente al sistema di coordinate del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="797c5-108">This mode maps directly to the device's coordinate system.</span></span> <span data-ttu-id="797c5-109">Il mapping logico a fisico prevede solo un offset in x e y definito dalle origini della finestra controllata dall'applicazione e dal viewport.</span><span class="sxs-lookup"><span data-stu-id="797c5-109">The logical-to-physical mapping involves only an offset in x and y that is defined by the application-controlled window and viewport origins.</span></span> <span data-ttu-id="797c5-110">Gli extent del viewport e della finestra sono tutti impostati su 1, creando un mapping uno-a-uno.</span><span class="sxs-lookup"><span data-stu-id="797c5-110">The viewport and window extents are all set to 1, creating a one-to-one mapping.</span></span>

<span data-ttu-id="797c5-111">Le applicazioni che visualizzano forme geometriche (cerchi, quadrati, poligoni e così via) usano una delle modalità di mapping indipendenti dal dispositivo.</span><span class="sxs-lookup"><span data-stu-id="797c5-111">Applications that display geometric shapes (circles, squares, polygons, and so on) make use of one of the device-independent mapping modes.</span></span> <span data-ttu-id="797c5-112">Se, ad esempio, si scrive un'applicazione per fornire funzionalità di creazione di grafici per un programma di foglio di calcolo e si desidera garantire che il diametro di ogni grafico a torta sia di 2 centimetri, utilizzare la \_ modalità di mapping mm LOENGLISH e chiamare le funzioni appropriate per creare e riempire il grafico.</span><span class="sxs-lookup"><span data-stu-id="797c5-112">For example, if you are writing an application to provide charting capabilities for a spreadsheet program and want to guarantee that the diameter of each pie chart is 2 inches, use the MM\_LOENGLISH mapping mode and call the appropriate functions to draw and fill the chart.</span></span> <span data-ttu-id="797c5-113">\_Se si specifica mm LOENGLISH, il diametro del grafico sarà coerente in qualsiasi visualizzazione o stampante.</span><span class="sxs-lookup"><span data-stu-id="797c5-113">Specifying MM\_LOENGLISH, guarantees that the diameter of the chart is consistent on any display or printer.</span></span> <span data-ttu-id="797c5-114">Se \_ si usa il testo mm anziché mm \_ LOENGLISH, un grafico visualizzato circolare su una visualizzazione VGA sembrerebbe ellittico in una visualizzazione EGA e apparirebbe molto piccolo in una stampante laser con 300 dpi (punti per pollice).</span><span class="sxs-lookup"><span data-stu-id="797c5-114">If MM\_TEXT is used instead of MM\_LOENGLISH, a chart that appears circular on a VGA display would appear elliptical on an EGA display and would appear very small on a 300 dpi (dots per inch) laser printer.</span></span>

 

 



