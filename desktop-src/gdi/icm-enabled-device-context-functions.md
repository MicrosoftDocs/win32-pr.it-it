---
description: Microsoft Image Color Management (ICM) assicura che un'immagine di colore, un elemento grafico o un oggetto testo venga sottoposto a rendering il più vicino possibile alla finalità originale su qualsiasi dispositivo, nonostante le differenze nelle tecnologie di imaging e nelle funzionalità cromatiche tra i dispositivi.
ms.assetid: eced18cf-be5a-4c61-b0e5-36d607daa6ff
title: Funzioni di contesto del dispositivo ICM-Enabled
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95a0b49e62d0b4d05e0690d2aee0d3c5f0f530cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104978583"
---
# <a name="icm-enabled-device-context-functions"></a><span data-ttu-id="b7e26-103">Funzioni di contesto del dispositivo ICM-Enabled</span><span class="sxs-lookup"><span data-stu-id="b7e26-103">ICM-Enabled Device Context Functions</span></span>

<span data-ttu-id="b7e26-104">Microsoft Image Color Management (ICM) assicura che un'immagine di colore, un elemento grafico o un oggetto testo venga sottoposto a rendering il più vicino possibile alla finalità originale su qualsiasi dispositivo, nonostante le differenze nelle tecnologie di imaging e nelle funzionalità cromatiche tra i dispositivi.</span><span class="sxs-lookup"><span data-stu-id="b7e26-104">Microsoft Image Color Management (ICM) ensures that a color image, graphic, or text object is rendered as closely as possible to its original intent on any device, despite differences in imaging technologies and color capabilities between devices.</span></span> <span data-ttu-id="b7e26-105">Per ulteriori informazioni, vedere [Windows Color System](/previous-versions//dd372446(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="b7e26-105">(For more information, see [Windows Color System](/previous-versions//dd372446(v=vs.85)).)</span></span>

<span data-ttu-id="b7e26-106">Sono disponibili varie funzioni nell'interfaccia GDI (Graphics Device Interface) che usano o operano sui dati di colore.</span><span class="sxs-lookup"><span data-stu-id="b7e26-106">There are various functions in the graphics device interface (GDI) that use or operate on color data.</span></span> <span data-ttu-id="b7e26-107">Le funzioni di contesto del dispositivo seguenti sono abilitate per l'uso con ICM:</span><span class="sxs-lookup"><span data-stu-id="b7e26-107">The following device context functions are enabled for use with ICM:</span></span>

-   [<span data-ttu-id="b7e26-108">**CreateCompatibleDC**</span><span class="sxs-lookup"><span data-stu-id="b7e26-108">**CreateCompatibleDC**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-createcompatibledc)
-   [<span data-ttu-id="b7e26-109">**CreateDC**</span><span class="sxs-lookup"><span data-stu-id="b7e26-109">**CreateDC**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-createdca)
-   [<span data-ttu-id="b7e26-110">**GetDCBrushColor**</span><span class="sxs-lookup"><span data-stu-id="b7e26-110">**GetDCBrushColor**</span></span>](/windows/desktop/api/WinGdi/nf-wingdi-getdcbrushcolor)
-   [<span data-ttu-id="b7e26-111">**GetDCPenColor**</span><span class="sxs-lookup"><span data-stu-id="b7e26-111">**GetDCPenColor**</span></span>](/windows/desktop/api/WinGdi/nf-wingdi-getdcpencolor)
-   [<span data-ttu-id="b7e26-112">**ResetDC**</span><span class="sxs-lookup"><span data-stu-id="b7e26-112">**ResetDC**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-resetdca)
-   [<span data-ttu-id="b7e26-113">**SelezionaOggetto**</span><span class="sxs-lookup"><span data-stu-id="b7e26-113">**SelectObject**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-selectobject)
-   [<span data-ttu-id="b7e26-114">**SetDCBrushColor**</span><span class="sxs-lookup"><span data-stu-id="b7e26-114">**SetDCBrushColor**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-setdcbrushcolor)
-   [<span data-ttu-id="b7e26-115">**SetDCPenColor**</span><span class="sxs-lookup"><span data-stu-id="b7e26-115">**SetDCPenColor**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-setdcpencolor)

 

 
