---
description: L'interfaccia di controllo della retroilluminazione è un'interfaccia IOCTL standardizzata per il controllo della luminosità della retroilluminazione LCD.
ms.assetid: edf2b7ed-2676-483a-80ba-f148951e0e58
title: Interfaccia di controllo retroilluminazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ecbcc3d635d120c1049f8ec586d7296a953dfac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106312068"
---
# <a name="backlight-control-interface"></a><span data-ttu-id="0392a-103">Interfaccia di controllo retroilluminazione</span><span class="sxs-lookup"><span data-stu-id="0392a-103">Backlight Control Interface</span></span>

<span data-ttu-id="0392a-104">L'interfaccia di controllo della retroilluminazione è un'interfaccia IOCTL standardizzata per il controllo della luminosità della retroilluminazione LCD.</span><span class="sxs-lookup"><span data-stu-id="0392a-104">The backlight control interface is a standardized IOCTL interface for controlling the brightness of the LCD backlight.</span></span>

<span data-ttu-id="0392a-105">Le applicazioni che richiedono il controllo a livello di codice della luminosità della retroilluminazione o forniscono controlli per l'utente devono usare questa interfaccia anziché un'interfaccia proprietaria; in caso contrario, il sistema non è in grado di eseguire query sulla luminosità hardware corrente e potrebbe non essere sincronizzato.</span><span class="sxs-lookup"><span data-stu-id="0392a-105">Applications that require programmatic control of the backlight brightness or provide controls for the user to do so should use this interface rather than a proprietary interface; otherwise, the system cannot query the current hardware brightness and may become unsynchronized.</span></span>

<span data-ttu-id="0392a-106">Il primo passaggio consiste nell'eseguire una query sul dispositivo per la luminosità supportata usando il codice di controllo della [**\_ \_ \_ \_ luminosità supportato dalla query video IOCTL**](ioctl-video-query-supported-brightness.md) .</span><span class="sxs-lookup"><span data-stu-id="0392a-106">The first step is to query the device for the supported brightness using the [**IOCTL\_VIDEO\_QUERY\_SUPPORTED\_BRIGHTNESS**](ioctl-video-query-supported-brightness.md) control code.</span></span> <span data-ttu-id="0392a-107">Questa operazione restituisce un buffer che specifica i livelli di luminosità disponibili.</span><span class="sxs-lookup"><span data-stu-id="0392a-107">This operation returns a buffer that specifies the available brightness levels.</span></span> <span data-ttu-id="0392a-108">Successivamente, è possibile eseguire una query sul dispositivo per la luminosità di visualizzazione corrente usando il codice di controllo della [**\_ \_ \_ \_ luminosità della query video IOCTL**](ioctl-video-query-display-brightness.md) .</span><span class="sxs-lookup"><span data-stu-id="0392a-108">Next, you can query the device for the current display brightness using the [**IOCTL\_VIDEO\_QUERY\_DISPLAY\_BRIGHTNESS**](ioctl-video-query-display-brightness.md) control code.</span></span> <span data-ttu-id="0392a-109">Questa operazione restituisce le impostazioni correnti per la luminosità corrente alternata (CA), la luminosità diretta corrente (DC) e lo stato di alimentazione.</span><span class="sxs-lookup"><span data-stu-id="0392a-109">This operation returns the current settings for alternating current (AC) brightness, direct current (DC) brightness, and the power state.</span></span>

<span data-ttu-id="0392a-110">Per modificare la luminosità dello schermo, usare il codice di controllo della [**\_ \_ \_ \_ luminosità del set di video IOCTL**](ioctl-video-set-display-brightness.md) .</span><span class="sxs-lookup"><span data-stu-id="0392a-110">To change the display brightness, use the [**IOCTL\_VIDEO\_SET\_DISPLAY\_BRIGHTNESS**](ioctl-video-set-display-brightness.md) control code.</span></span> <span data-ttu-id="0392a-111">È possibile impostare la luminosità AC, la luminosità del controller di dominio o entrambi.</span><span class="sxs-lookup"><span data-stu-id="0392a-111">You can set the AC brightness, the DC brightness, or both.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0392a-112">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="0392a-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0392a-113">Informazioni sul risparmio energia</span><span class="sxs-lookup"><span data-stu-id="0392a-113">About Power Management</span></span>](about-power-management.md)
</dt> </dl>

 

 



