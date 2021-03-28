---
description: Microsoft Image Color Management (ICM) assicura che un'immagine di colore, un elemento grafico o un oggetto testo venga sottoposto al rendering il più vicino possibile alla finalità originale su qualsiasi dispositivo, nonostante le differenze nelle tecnologie di imaging e nelle funzionalità cromatiche tra i dispositivi.
ms.assetid: 55452048-aacd-4772-9345-3efcf0350ce6
title: Funzioni di ICM-Enabled Pen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ec35b11a46646a6f7588443ac7a66aee23aae10
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528327"
---
# <a name="icm-enabled-pen-functions"></a><span data-ttu-id="468d0-103">Funzioni di ICM-Enabled Pen</span><span class="sxs-lookup"><span data-stu-id="468d0-103">ICM-Enabled Pen Functions</span></span>

<span data-ttu-id="468d0-104">Microsoft Image Color Management (ICM) assicura che un'immagine di colore, un elemento grafico o un oggetto testo venga sottoposto al rendering il più vicino possibile alla finalità originale su qualsiasi dispositivo, nonostante le differenze nelle tecnologie di imaging e nelle funzionalità cromatiche tra i dispositivi.</span><span class="sxs-lookup"><span data-stu-id="468d0-104">Microsoft Image Color Management (ICM) ensures that a color image, graphic, or text object is rendered as close as possible to its original intent on any device, despite differences in imaging technologies and color capabilities among devices.</span></span> <span data-ttu-id="468d0-105">Se si sta eseguendo la scansione di un'immagine o di un altro elemento grafico su uno scanner di colori, il download su Internet, la visualizzazione o la modifica sullo schermo o l'output su carta, film o altri supporti, ICM versione 2,0 consente di garantire la coerenza e l'accuratezza dei colori.</span><span class="sxs-lookup"><span data-stu-id="468d0-105">Whether you are scanning an image or other graphic on a color scanner, downloading it over the Internet, viewing or editing it on the screen, or outputting it to paper, film, or other media, ICM version 2.0 helps you keep its colors consistent and accurate.</span></span> <span data-ttu-id="468d0-106">Per ulteriori informazioni su ICM, vedere [sistema colori Windows](/previous-versions//dd372446(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="468d0-106">For more information about ICM, see [Windows Color System](/previous-versions//dd372446(v=vs.85))</span></span>

<span data-ttu-id="468d0-107">Sono disponibili varie funzioni nell'interfaccia GDI (Graphics Device Interface) che usano o operano sui dati di colore.</span><span class="sxs-lookup"><span data-stu-id="468d0-107">There are various functions in the graphics device interface (GDI) that use or operate on color data.</span></span> <span data-ttu-id="468d0-108">Le funzioni di penna seguenti sono abilitate per l'uso con ICM:</span><span class="sxs-lookup"><span data-stu-id="468d0-108">The following pen functions are enabled for use with ICM:</span></span>

-   [<span data-ttu-id="468d0-109">**CreatePen**</span><span class="sxs-lookup"><span data-stu-id="468d0-109">**CreatePen**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-createpen)
-   [<span data-ttu-id="468d0-110">**ExtCreatePen**</span><span class="sxs-lookup"><span data-stu-id="468d0-110">**ExtCreatePen**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-extcreatepen)

 

 
