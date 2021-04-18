---
title: Player. enableContextMenu
description: La proprietà enableContextMenu specifica o recupera un valore che indica se abilitare il menu di scelta rapida che viene visualizzato quando si fa clic con il pulsante destro del mouse.
ms.assetid: 736c8714-5650-4912-9e97-914a20137b91
keywords:
- Player. enableContextMenu Windows Media Player
topic_type:
- apiref
api_name:
- Player.enableContextMenu
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 324ab0f14b83621651869e715c1fd4a882ceb650
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324985"
---
# <a name="playerenablecontextmenu"></a><span data-ttu-id="1460a-104">Player. enableContextMenu</span><span class="sxs-lookup"><span data-stu-id="1460a-104">Player.enableContextMenu</span></span>

<span data-ttu-id="1460a-105">La proprietà **enableContextMenu** specifica o recupera un valore che indica se abilitare il menu di scelta rapida che viene visualizzato quando si fa clic con il pulsante destro del mouse.</span><span class="sxs-lookup"><span data-stu-id="1460a-105">The **enableContextMenu** property specifies or retrieves a value indicating whether to enable the context menu, which appears when the right mouse button is clicked.</span></span>

## <a name="syntax"></a><span data-ttu-id="1460a-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1460a-106">Syntax</span></span>

<span data-ttu-id="1460a-107">*Player*. **enableContextMenu**</span><span class="sxs-lookup"><span data-stu-id="1460a-107">*player*.**enableContextMenu**</span></span>

## <a name="possible-values"></a><span data-ttu-id="1460a-108">Valori possibili</span><span class="sxs-lookup"><span data-stu-id="1460a-108">Possible Values</span></span>

<span data-ttu-id="1460a-109">Questa proprietà è un valore booleano di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="1460a-109">This property is a read/write Boolean.</span></span>



| <span data-ttu-id="1460a-110">Valore</span><span class="sxs-lookup"><span data-stu-id="1460a-110">Value</span></span> | <span data-ttu-id="1460a-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1460a-111">Description</span></span>                       |
|-------|-----------------------------------|
| <span data-ttu-id="1460a-112">true</span><span class="sxs-lookup"><span data-stu-id="1460a-112">true</span></span>  | <span data-ttu-id="1460a-113">Valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="1460a-113">Default.</span></span> <span data-ttu-id="1460a-114">Attivare il menu di scelta rapida.</span><span class="sxs-lookup"><span data-stu-id="1460a-114">Enable the context menu.</span></span> |
| <span data-ttu-id="1460a-115">false</span><span class="sxs-lookup"><span data-stu-id="1460a-115">false</span></span> | <span data-ttu-id="1460a-116">Non abilitare il menu di scelta rapida.</span><span class="sxs-lookup"><span data-stu-id="1460a-116">Do not enable the context menu.</span></span>   |



 

## <a name="remarks"></a><span data-ttu-id="1460a-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="1460a-117">Remarks</span></span>

<span data-ttu-id="1460a-118">Durante la riproduzione a schermo intero, Windows Media Player nasconde il cursore del mouse quando **enableContextMenu** è uguale a false e **uiMode** è uguale a "None".</span><span class="sxs-lookup"><span data-stu-id="1460a-118">During full-screen playback, Windows Media Player hides the mouse cursor when **enableContextMenu** equals false and **uiMode** equals "none".</span></span>

<span data-ttu-id="1460a-119">**Windows Media Player 10 Mobile:** Questa proprietà non è supportata.</span><span class="sxs-lookup"><span data-stu-id="1460a-119">**Windows Media Player 10 Mobile:** This property is not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="1460a-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1460a-120">Requirements</span></span>



| <span data-ttu-id="1460a-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="1460a-121">Requirement</span></span> | <span data-ttu-id="1460a-122">Valore</span><span class="sxs-lookup"><span data-stu-id="1460a-122">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="1460a-123">Versione</span><span class="sxs-lookup"><span data-stu-id="1460a-123">Version</span></span><br/> | <span data-ttu-id="1460a-124">Windows Media Player versione 7,0 o successiva.</span><span class="sxs-lookup"><span data-stu-id="1460a-124">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="1460a-125">DLL</span><span class="sxs-lookup"><span data-stu-id="1460a-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="1460a-126"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1460a-126"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1460a-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1460a-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1460a-128">**Oggetto Player**</span><span class="sxs-lookup"><span data-stu-id="1460a-128">**Player Object**</span></span>](player-object.md)
</dt> </dl>

 

 





