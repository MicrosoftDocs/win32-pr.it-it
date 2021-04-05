---
title: Metodo ShowDefaultCharacterProperties
description: Metodo ShowDefaultCharacterProperties
ms.assetid: a3b109c0-5701-4a72-baae-bcbb97b025a3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f055b2ca0f00e0a13c24ec95dc82509ae9c45b7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103709913"
---
# <a name="showdefaultcharacterproperties-method"></a><span data-ttu-id="aed41-103">Metodo ShowDefaultCharacterProperties</span><span class="sxs-lookup"><span data-stu-id="aed41-103">ShowDefaultCharacterProperties Method</span></span>

<span data-ttu-id="aed41-104">\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="aed41-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="aed41-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="aed41-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="aed41-106">Consente di visualizzare le proprietà del carattere predefinito.</span><span class="sxs-lookup"><span data-stu-id="aed41-106">Displays the default character's properties.</span></span>

</dd> <dt>

<span data-ttu-id="aed41-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**</span><span class="sxs-lookup"><span data-stu-id="aed41-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="aed41-108">\*agente \* \* *. ShowDefaultCharacterProperties* \*  \[ *X* , *Y*\]</span><span class="sxs-lookup"><span data-stu-id="aed41-108">*agent\*\*\*.ShowDefaultCharacterProperties*\* \[ *X* , *Y* \]</span></span>



| <span data-ttu-id="aed41-109">Parte</span><span class="sxs-lookup"><span data-stu-id="aed41-109">Part</span></span> | <span data-ttu-id="aed41-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="aed41-110">Description</span></span>                                                                                                                                                |
|------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aed41-111">*X*</span><span class="sxs-lookup"><span data-stu-id="aed41-111">*X*</span></span>  | <span data-ttu-id="aed41-112">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="aed41-112">Optional.</span></span> <span data-ttu-id="aed41-113">Valore short integer che indica la coordinata orizzontale (*X* ) dello schermo per visualizzare la finestra.</span><span class="sxs-lookup"><span data-stu-id="aed41-113">A short integer value that indicates the horizontal (*X* ) screen coordinate to display the window.</span></span> <span data-ttu-id="aed41-114">Questa coordinata deve essere specificata in pixel.</span><span class="sxs-lookup"><span data-stu-id="aed41-114">This coordinate must be specified in pixels.</span></span> |
| <span data-ttu-id="aed41-115">*S*</span><span class="sxs-lookup"><span data-stu-id="aed41-115">*Y*</span></span>  | <span data-ttu-id="aed41-116">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="aed41-116">Optional.</span></span> <span data-ttu-id="aed41-117">Valore short integer che indica la coordinata verticale (*Y*) dello schermo per visualizzare la finestra.</span><span class="sxs-lookup"><span data-stu-id="aed41-117">A short integer value that indicates the vertical (*Y*) screen coordinate to display the window.</span></span> <span data-ttu-id="aed41-118">Questa coordinata deve essere specificata in pixel.</span><span class="sxs-lookup"><span data-stu-id="aed41-118">This coordinate must be specified in pixels.</span></span>    |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="aed41-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="aed41-119">Remarks</span></span>

<span data-ttu-id="aed41-120">La chiamata a questo metodo consente di visualizzare la finestra Proprietà carattere predefinita (non la finestra delle proprietà dell'agente Microsoft).</span><span class="sxs-lookup"><span data-stu-id="aed41-120">Calling this method displays the default character properties window (not the Microsoft Agent property sheet).</span></span> <span data-ttu-id="aed41-121">Se non si specificano le coordinate X e Y, la finestra viene visualizzata nell'ultima posizione in cui è stata visualizzata.</span><span class="sxs-lookup"><span data-stu-id="aed41-121">If you do not specify the X and Y coordinates, the window appears at the last location it was displayed.</span></span>

## <a name="see-also"></a><span data-ttu-id="aed41-122">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="aed41-122">See Also</span></span>

[<span data-ttu-id="aed41-123">**Evento DefaultCharacterChange**</span><span class="sxs-lookup"><span data-stu-id="aed41-123">**DefaultCharacterChange event**</span></span>](defaultcharacterchange-event.md)


 

 




