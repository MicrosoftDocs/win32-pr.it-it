---
description: Microsoft Image Color Management (ICM) assicura che un'immagine di colore, un oggetto grafico o un oggetto testo venga sottoposto al rendering il più vicino possibile alla finalità originale su qualsiasi dispositivo, nonostante le differenze nelle tecnologie di imaging e nelle funzionalità cromatiche tra i dispositivi.
ms.assetid: 7b3cb9a4-ffd2-4867-85bd-0e663fdde6e3
title: Funzioni bitmap ICM-Enabled
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4b89dac569aafad1ef94b066bc97f588bac62c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103880282"
---
# <a name="icm-enabled-bitmap-functions"></a><span data-ttu-id="b45ad-103">Funzioni bitmap ICM-Enabled</span><span class="sxs-lookup"><span data-stu-id="b45ad-103">ICM-Enabled Bitmap Functions</span></span>

<span data-ttu-id="b45ad-104">Microsoft Image Color Management (ICM) assicura che un'immagine di colore, un oggetto grafico o un oggetto testo venga sottoposto al rendering il più vicino possibile alla finalità originale su qualsiasi dispositivo, nonostante le differenze nelle tecnologie di imaging e nelle funzionalità cromatiche tra i dispositivi.</span><span class="sxs-lookup"><span data-stu-id="b45ad-104">Microsoft Image Color Management (ICM) ensures that a color image, graphic object, or text object is rendered as closely as possible to its original intent on any device, despite differences in imaging technologies and color capabilities between devices.</span></span> <span data-ttu-id="b45ad-105">Se si sta eseguendo la scansione di un'immagine o di un altro elemento grafico su uno scanner di colori, lo si scarica su Internet, lo si visualizza o lo si modifica sullo schermo oppure lo si stampa su carta, film o altri supporti, ICM 2,0 consente di garantire la coerenza e l'accuratezza dei colori.</span><span class="sxs-lookup"><span data-stu-id="b45ad-105">Whether you are scanning an image or other graphic on a color scanner, downloading it over the Internet, viewing or editing it onscreen, or printing it on paper, film, or other media, ICM 2.0 helps you keep colors consistent and accurate.</span></span> <span data-ttu-id="b45ad-106">Per ulteriori informazioni su ICM, vedere [Windows Color System](/previous-versions//dd372446(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="b45ad-106">For more information about ICM, see [Windows Color System](/previous-versions//dd372446(v=vs.85)).</span></span>

<span data-ttu-id="b45ad-107">Sono disponibili varie funzioni nell'interfaccia GDI (Graphics Device Interface) che usano o operano sui dati di colore.</span><span class="sxs-lookup"><span data-stu-id="b45ad-107">There are various functions in the graphics device interface (GDI) that use or operate on color data.</span></span> <span data-ttu-id="b45ad-108">Le funzioni bitmap seguenti sono abilitate per l'uso con ICM:</span><span class="sxs-lookup"><span data-stu-id="b45ad-108">The following bitmap functions are enabled for use with ICM:</span></span>

-   [<span data-ttu-id="b45ad-109">**BitBlt**</span><span class="sxs-lookup"><span data-stu-id="b45ad-109">**BitBlt**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-bitblt)
-   [<span data-ttu-id="b45ad-110">**CreateDIBitmap**</span><span class="sxs-lookup"><span data-stu-id="b45ad-110">**CreateDIBitmap**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-createdibitmap)
-   [<span data-ttu-id="b45ad-111">**CreateDIBSection**</span><span class="sxs-lookup"><span data-stu-id="b45ad-111">**CreateDIBSection**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-createdibsection)
-   [<span data-ttu-id="b45ad-112">**MaskBlt**</span><span class="sxs-lookup"><span data-stu-id="b45ad-112">**MaskBlt**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-maskblt)
-   [<span data-ttu-id="b45ad-113">**SetDIBColorTable**</span><span class="sxs-lookup"><span data-stu-id="b45ad-113">**SetDIBColorTable**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-setdibcolortable)
-   [<span data-ttu-id="b45ad-114">**StretchBlt**</span><span class="sxs-lookup"><span data-stu-id="b45ad-114">**StretchBlt**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-stretchblt)
-   [<span data-ttu-id="b45ad-115">**SetDIBits**</span><span class="sxs-lookup"><span data-stu-id="b45ad-115">**SetDIBits**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-setdibits)
-   [<span data-ttu-id="b45ad-116">**SetDIBitsToDevice**</span><span class="sxs-lookup"><span data-stu-id="b45ad-116">**SetDIBitsToDevice**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-setdibitstodevice)
-   [<span data-ttu-id="b45ad-117">**StretchDIBits**</span><span class="sxs-lookup"><span data-stu-id="b45ad-117">**StretchDIBits**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-stretchdibits)

 

 
