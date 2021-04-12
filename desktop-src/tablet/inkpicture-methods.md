---
description: Questa sezione contiene i metodi per il controllo InkPicture.
ms.assetid: 5691e595-f264-4547-9db6-f984483005e8
title: Metodi InkPicture
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b28d15c61105e9cb5aa690860a0362aac826f019
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104349896"
---
# <a name="inkpicture-methods"></a><span data-ttu-id="84bb7-103">Metodi InkPicture</span><span class="sxs-lookup"><span data-stu-id="84bb7-103">InkPicture Methods</span></span>

<span data-ttu-id="84bb7-104">Questa sezione contiene i metodi per il controllo InkPicture.</span><span class="sxs-lookup"><span data-stu-id="84bb7-104">This section contains Methods for the InkPicture Control.</span></span>



| <span data-ttu-id="84bb7-105">Metodo</span><span class="sxs-lookup"><span data-stu-id="84bb7-105">Method</span></span>                                                                                   | <span data-ttu-id="84bb7-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="84bb7-106">Description</span></span>                                                                                                                                                                      |
|------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="84bb7-107">**Metodo GetEventInterest**</span><span class="sxs-lookup"><span data-stu-id="84bb7-107">**GetEventInterest Method**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-geteventinterest)                           | <span data-ttu-id="84bb7-108">Recupera un valore che indica se il controllo [InkPicture](inkpicture-control-reference.md) è interessato da un particolare evento.</span><span class="sxs-lookup"><span data-stu-id="84bb7-108">Retrieves a value that indicates whether the [InkPicture](inkpicture-control-reference.md) control has interest in a particular event.</span></span><br/>                               |
| [<span data-ttu-id="84bb7-109">**GetGestureStatus**</span><span class="sxs-lookup"><span data-stu-id="84bb7-109">**GetGestureStatus**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-getgesturestatus)                                  | <span data-ttu-id="84bb7-110">Recupera un valore che indica se il controllo [InkPicture](inkpicture-control-reference.md) è interessato da un particolare movimento dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="84bb7-110">Retrieves a value that indicates whether the [InkPicture](inkpicture-control-reference.md) control has interest in a particular application gesture.</span></span><br/>                 |
| [<span data-ttu-id="84bb7-111">**Metodo GetWindowInputRectangle**</span><span class="sxs-lookup"><span data-stu-id="84bb7-111">**GetWindowInputRectangle Method**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-getwindowinputrectangle)             | <span data-ttu-id="84bb7-112">Restituisce il rettangolo della finestra, in pixel, all'interno del quale viene disegnato l'input penna.</span><span class="sxs-lookup"><span data-stu-id="84bb7-112">Returns the window rectangle, in pixels, within which ink is drawn.</span></span><br/>                                                                                                   |
| [<span data-ttu-id="84bb7-113">**HitTestSelection**</span><span class="sxs-lookup"><span data-stu-id="84bb7-113">**HitTestSelection**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-hittestselection)                                  | <span data-ttu-id="84bb7-114">Recupera un membro dell'enumerazione [**SelectionHitResult**](/windows/desktop/api/msinkaut/ne-msinkaut-selectionhitresult) , che specifica quale parte di una selezione, se presente, è stata raggiunta durante un hit test.</span><span class="sxs-lookup"><span data-stu-id="84bb7-114">Retrieves a member of the [**SelectionHitResult**](/windows/desktop/api/msinkaut/ne-msinkaut-selectionhitresult) enumeration, which specifies which part of a selection, if any, was hit during a hit test.</span></span><br/> |
| [<span data-ttu-id="84bb7-115">**Metodo SetAllTabletsMode**</span><span class="sxs-lookup"><span data-stu-id="84bb7-115">**SetAllTabletsMode Method**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-setalltabletsmode)                         | <span data-ttu-id="84bb7-116">Consente al controllo [InkPicture](inkpicture-control-reference.md) di raccogliere input penna da qualsiasi tablet collegato al Tablet PC.</span><span class="sxs-lookup"><span data-stu-id="84bb7-116">Enables the [InkPicture](inkpicture-control-reference.md) control to collect ink from any tablet attached to the Tablet PC.</span></span><br/>                                          |
| [<span data-ttu-id="84bb7-117">**Metodo SetEventInterest**</span><span class="sxs-lookup"><span data-stu-id="84bb7-117">**SetEventInterest Method**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-seteventinterest)                           | <span data-ttu-id="84bb7-118">Modifica un valore che indica se un controllo [InkPicture](inkpicture-control-reference.md) è interessato a un evento specificato.</span><span class="sxs-lookup"><span data-stu-id="84bb7-118">Modifies a value that indicates whether an [InkPicture](inkpicture-control-reference.md) control has interest in a specified event.</span></span><br/>                                  |
| [<span data-ttu-id="84bb7-119">**Metodo SetGestureStatus**</span><span class="sxs-lookup"><span data-stu-id="84bb7-119">**SetGestureStatus Method**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-setgesturestatus)                           | <span data-ttu-id="84bb7-120">Modifica l'interesse dell'oggetto [InkPicture](inkpicture-control-reference.md) in un movimento dell'applicazione specificato.</span><span class="sxs-lookup"><span data-stu-id="84bb7-120">Modifies the interest of the [InkPicture](inkpicture-control-reference.md) object in a specified application gesture.</span></span><br/>                                                |
| [<span data-ttu-id="84bb7-121">**Metodo SetSingleTabletIntegratedMode**</span><span class="sxs-lookup"><span data-stu-id="84bb7-121">**SetSingleTabletIntegratedMode Method**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-setsingletabletintegratedmode) | <span data-ttu-id="84bb7-122">Modifica il controllo [InkPicture](inkpicture-control-reference.md) per raccogliere l'input penna da un solo tablet collegato al Tablet PC.</span><span class="sxs-lookup"><span data-stu-id="84bb7-122">Modifies the [InkPicture](inkpicture-control-reference.md) control to collect ink from only one tablet attached to the Tablet PC.</span></span> <span data-ttu-id="84bb7-123">L'input penna da altre tavolette viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="84bb7-123">Ink from other tablets is ignored.</span></span><br/> |
| [<span data-ttu-id="84bb7-124">**Metodo SetWindowInputRectangle**</span><span class="sxs-lookup"><span data-stu-id="84bb7-124">**SetWindowInputRectangle Method**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-setwindowinputrectangle)             | <span data-ttu-id="84bb7-125">Specifica il rettangolo della finestra da impostare, nelle coordinate della finestra, all'interno del quale viene disegnato l'input penna.</span><span class="sxs-lookup"><span data-stu-id="84bb7-125">Specifies the window rectangle to set, in window coordinates, within which ink is drawn.</span></span><br/>                                                                              |



 

 

 




