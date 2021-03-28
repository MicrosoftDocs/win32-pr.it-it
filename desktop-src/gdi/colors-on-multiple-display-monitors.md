---
description: Ogni monitoraggio può avere una profondità di colore specifica.
ms.assetid: 8d1ba8d2-b43d-498d-be5a-100fe9fc0f61
title: Colori su più monitor di visualizzazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50410631cf0ea3ac0a1b9967f1116809be0a4851
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103967064"
---
# <a name="colors-on-multiple-display-monitors"></a><span data-ttu-id="0937f-103">Colori su più monitor di visualizzazione</span><span class="sxs-lookup"><span data-stu-id="0937f-103">Colors on Multiple Display Monitors</span></span>

<span data-ttu-id="0937f-104">Ogni monitoraggio può avere una profondità di colore specifica.</span><span class="sxs-lookup"><span data-stu-id="0937f-104">Each monitor can have its own color depth.</span></span> <span data-ttu-id="0937f-105">Il sistema regola automaticamente i colori durante lo spostamento di Windows tra i monitoraggi con profondità dei colori differenti.</span><span class="sxs-lookup"><span data-stu-id="0937f-105">The system automatically adjusts colors as windows move across monitors with different color depths.</span></span> <span data-ttu-id="0937f-106">In generale, questo produce risultati soddisfacenti.</span><span class="sxs-lookup"><span data-stu-id="0937f-106">In general, this produces good results.</span></span> <span data-ttu-id="0937f-107">Tuttavia, questo non è sempre ottimale.</span><span class="sxs-lookup"><span data-stu-id="0937f-107">However, this is not always optimal.</span></span> <span data-ttu-id="0937f-108">Per sfruttare i vantaggi delle funzionalità relative ai colori dei diversi monitoraggi, vedere la sezione [disegno su più monitor di visualizzazione](painting-on-multiple-display-monitors.md) riportata di seguito.</span><span class="sxs-lookup"><span data-stu-id="0937f-108">To take advantage of the color capabilities of different monitors, see the [Painting on Multiple Display Monitors](painting-on-multiple-display-monitors.md) section that follows.</span></span>

<span data-ttu-id="0937f-109">Per determinare se tutti i monitoraggi hanno lo stesso formato di colore, chiamare [**GetSystemMetrics**](/windows/win32/api/winuser/nf-winuser-getsystemmetrics) con SM \_ SAMEDISPLAYFORMAT.</span><span class="sxs-lookup"><span data-stu-id="0937f-109">To determine if all monitors have the same color format, call [**GetSystemMetrics**](/windows/win32/api/winuser/nf-winuser-getsystemmetrics) with SM\_SAMEDISPLAYFORMAT.</span></span>

<span data-ttu-id="0937f-110">Se il monitoraggio primario è pallettizzati, [**SelectPalette**](/windows/desktop/api/Wingdi/nf-wingdi-selectpalette) e [**RealizePalette**](/windows/desktop/api/Wingdi/nf-wingdi-realizepalette) funzionano come prima, ma in tutti i monitoraggi.</span><span class="sxs-lookup"><span data-stu-id="0937f-110">If the primary monitor is palettized, [**SelectPalette**](/windows/desktop/api/Wingdi/nf-wingdi-selectpalette) and [**RealizePalette**](/windows/desktop/api/Wingdi/nf-wingdi-realizepalette) work the same as before, but across all monitors.</span></span> <span data-ttu-id="0937f-111">Inoltre, le tavolozze di tutti i dispositivi pallettizzati sono sincronizzate.</span><span class="sxs-lookup"><span data-stu-id="0937f-111">In addition, the palettes of all palettized devices are synchronized.</span></span> <span data-ttu-id="0937f-112">Se il monitoraggio primario non è pallettizzati, **SelectPalette** e **RealizePalette** selezioneranno la tavolozza in background e i dispositivi pallettizzati non verranno sincronizzati.</span><span class="sxs-lookup"><span data-stu-id="0937f-112">If the primary monitor is not palettized, **SelectPalette** and **RealizePalette** will select the palette into the background and palettized devices will not be synchronized.</span></span>

 

 
