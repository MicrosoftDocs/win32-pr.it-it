---
title: PlayerApplication.hasDisplay
description: La proprietà hasDisplay recupera un valore che indica se il video può essere visualizzato tramite il controllo lettore remoto.
ms.assetid: f90c5470-f985-4b98-823f-7395f89b238b
keywords:
- Media Player Windows PlayerApplication. hasDisplay
topic_type:
- apiref
api_name:
- PlayerApplication.hasDisplay
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3ef77cb42109decef6ab435aa031240f89b6cb98
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327050"
---
# <a name="playerapplicationhasdisplay"></a><span data-ttu-id="f858e-104">PlayerApplication.hasDisplay</span><span class="sxs-lookup"><span data-stu-id="f858e-104">PlayerApplication.hasDisplay</span></span>

<span data-ttu-id="f858e-105">La proprietà **hasDisplay** recupera un valore che indica se il video può essere visualizzato tramite il controllo lettore remoto.</span><span class="sxs-lookup"><span data-stu-id="f858e-105">The **hasDisplay** property retrieves a value indicating whether video can display through the remoted Player control.</span></span>

## <a name="syntax"></a><span data-ttu-id="f858e-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f858e-106">Syntax</span></span>

<span data-ttu-id="f858e-107">*playerApplication*. **hasDisplay**</span><span class="sxs-lookup"><span data-stu-id="f858e-107">*playerApplication*.**hasDisplay**</span></span>

## <a name="possible-values"></a><span data-ttu-id="f858e-108">Valori possibili</span><span class="sxs-lookup"><span data-stu-id="f858e-108">Possible Values</span></span>

<span data-ttu-id="f858e-109">Questa proprietà è un **valore booleano** di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="f858e-109">This property is a read-only **Boolean**.</span></span>

## <a name="remarks"></a><span data-ttu-id="f858e-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="f858e-110">Remarks</span></span>

<span data-ttu-id="f858e-111">Questa proprietà viene utilizzata solo per la comunicazione remota del controllo Media Player di Windows.</span><span class="sxs-lookup"><span data-stu-id="f858e-111">This property is used only when remoting the Windows Media Player control.</span></span>

<span data-ttu-id="f858e-112">È possibile eseguire contemporaneamente più controlli Media Player di Windows, ma i video possono essere visualizzati solo in una posizione alla volta, nella modalità completa del lettore o in uno dei controlli di Windows Media Player remoto.</span><span class="sxs-lookup"><span data-stu-id="f858e-112">Several Windows Media Player controls can be running remotely at the same time, but video can only display in one location at a time, either in the full mode of the Player or in one of the remoted Windows Media Player controls.</span></span> <span data-ttu-id="f858e-113">Usare questa proprietà per determinare se il controllo corrente è quello tramite il quale è possibile visualizzare il video.</span><span class="sxs-lookup"><span data-stu-id="f858e-113">Use this property to determine whether the current control is the one through which video can be displayed.</span></span>

<span data-ttu-id="f858e-114">**Windows Media Player 10 Mobile:** Questa proprietà restituisce sempre **true**.</span><span class="sxs-lookup"><span data-stu-id="f858e-114">**Windows Media Player 10 Mobile:** This property always returns **true**.</span></span>

## <a name="requirements"></a><span data-ttu-id="f858e-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f858e-115">Requirements</span></span>



| <span data-ttu-id="f858e-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="f858e-116">Requirement</span></span> | <span data-ttu-id="f858e-117">Valore</span><span class="sxs-lookup"><span data-stu-id="f858e-117">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="f858e-118">Versione</span><span class="sxs-lookup"><span data-stu-id="f858e-118">Version</span></span><br/> | <span data-ttu-id="f858e-119">Windows Media Player 9 serie o versione successiva.</span><span class="sxs-lookup"><span data-stu-id="f858e-119">Windows Media Player 9 Series or later.</span></span><br/>                                 |
| <span data-ttu-id="f858e-120">DLL</span><span class="sxs-lookup"><span data-stu-id="f858e-120">DLL</span></span><br/>     | <dl> <span data-ttu-id="f858e-121"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f858e-121"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f858e-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f858e-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f858e-123">**Oggetto PlayerApplication**</span><span class="sxs-lookup"><span data-stu-id="f858e-123">**PlayerApplication Object**</span></span>](playerapplication-object.md)
</dt> <dt>

[<span data-ttu-id="f858e-124">**Gestione remota del controllo di Windows Media Player**</span><span class="sxs-lookup"><span data-stu-id="f858e-124">**Remoting the Windows Media Player Control**</span></span>](remoting-the-windows-media-player-control.md)
</dt> </dl>

 

 





