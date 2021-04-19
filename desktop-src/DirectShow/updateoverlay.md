---
description: L'evento UpdateOverlay viene inviato quando la superficie di sovrapposizione è stata spostata o ridimensionata o la chiave di colore è cambiata.
ms.assetid: 692cbd26-b7b3-4fa3-9157-ca96a33e3a1e
title: UpdateOverlay (ddraw. h)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2152e1f58ba161dc8dc3e04c908aaf037f1eed2a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333303"
---
# <a name="updateoverlay"></a><span data-ttu-id="d2714-103">UpdateOverlay</span><span class="sxs-lookup"><span data-stu-id="d2714-103">UpdateOverlay</span></span>

> [!Note]  
> <span data-ttu-id="d2714-104">Questo componente è disponibile per l'uso nei sistemi operativi Microsoft Windows 2000, Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="d2714-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="d2714-105">È possibile che in versioni successive sia stata modificata o non sia più disponibile.</span><span class="sxs-lookup"><span data-stu-id="d2714-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="d2714-106">L'evento **UpdateOverlay** viene inviato quando la superficie di sovrapposizione è stata spostata o ridimensionata o la chiave di colore è cambiata.</span><span class="sxs-lookup"><span data-stu-id="d2714-106">The **UpdateOverlay** event is sent when the overlay surface has been moved or resized or its color key has changed.</span></span>

``` syntax
UpdateOverlay()
```

## <a name="remarks"></a><span data-ttu-id="d2714-107">Commenti</span><span class="sxs-lookup"><span data-stu-id="d2714-107">Remarks</span></span>

<span data-ttu-id="d2714-108">Le applicazioni non dovrebbero mai preoccuparsi della superficie sovrapposta ridimensionata o spostata.</span><span class="sxs-lookup"><span data-stu-id="d2714-108">Applications should never be concerned about the overlay surface being resized or moved.</span></span> <span data-ttu-id="d2714-109">Questa operazione viene gestita internamente.</span><span class="sxs-lookup"><span data-stu-id="d2714-109">This is all handled internally.</span></span> <span data-ttu-id="d2714-110">Questo evento viene tuttavia inviato anche quando cambia la chiave di colore.</span><span class="sxs-lookup"><span data-stu-id="d2714-110">But this event is also sent when the color key changes.</span></span> <span data-ttu-id="d2714-111">Ciò significa che se un'applicazione ospita MSWebDVD come controllo senza finestra e Visualizza i pulsanti mobili nella parte superiore della superficie video in modalità schermo intero, deve rispondere a questo evento ottenendo il nuovo valore della proprietà **ColorKey** in modo da poter creare correttamente i pulsanti.</span><span class="sxs-lookup"><span data-stu-id="d2714-111">That means that if an application is hosting MSWebDVD as a windowless control and displaying floating buttons on top of the video surface in full-screen mode, it should respond to this event by getting the new value of the **ColorKey** property so that it can draw the buttons properly.</span></span>

## <a name="requirements"></a><span data-ttu-id="d2714-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d2714-112">Requirements</span></span>



| <span data-ttu-id="d2714-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="d2714-113">Requirement</span></span> | <span data-ttu-id="d2714-114">Valore</span><span class="sxs-lookup"><span data-stu-id="d2714-114">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="d2714-115">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d2714-115">Header</span></span><br/> | <dl> <span data-ttu-id="d2714-116"><dt>Ddraw. h</dt></span><span class="sxs-lookup"><span data-stu-id="d2714-116"><dt>Ddraw.h</dt></span></span> </dl> |



 

 




