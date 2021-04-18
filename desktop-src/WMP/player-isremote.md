---
title: Player. Remote
description: La proprietà Remote recupera un valore che indica se il controllo Media Player di Windows è in esecuzione in modalità remota.
ms.assetid: bfeab968-affb-4d5d-b88b-5caf50d34cee
keywords:
- Media Player Windows Player. Remote
topic_type:
- apiref
api_name:
- Player.isRemote
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b7c8d97ba212e032db16b43299d2a3a8a836f9b9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326006"
---
# <a name="playerisremote"></a><span data-ttu-id="fd217-104">Player. Remote</span><span class="sxs-lookup"><span data-stu-id="fd217-104">Player.isRemote</span></span>

<span data-ttu-id="fd217-105">La proprietà **Remote** recupera un valore che indica se il controllo Media Player di Windows è in esecuzione in modalità remota.</span><span class="sxs-lookup"><span data-stu-id="fd217-105">The **isRemote** property retrieves a value indicating whether the Windows Media Player control is running in remote mode.</span></span>

## <a name="syntax"></a><span data-ttu-id="fd217-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="fd217-106">Syntax</span></span>

<span data-ttu-id="fd217-107">*Player* . **Remote**</span><span class="sxs-lookup"><span data-stu-id="fd217-107">*player* .**isRemote**</span></span>

## <a name="possible-values"></a><span data-ttu-id="fd217-108">Valori possibili</span><span class="sxs-lookup"><span data-stu-id="fd217-108">Possible Values</span></span>

<span data-ttu-id="fd217-109">Questa proprietà è un **valore booleano** di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="fd217-109">This property is a read-only **Boolean**.</span></span>



| <span data-ttu-id="fd217-110">Valore</span><span class="sxs-lookup"><span data-stu-id="fd217-110">Value</span></span> | <span data-ttu-id="fd217-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fd217-111">Description</span></span>                                   |
|-------|-----------------------------------------------|
| <span data-ttu-id="fd217-112">true</span><span class="sxs-lookup"><span data-stu-id="fd217-112">true</span></span>  | <span data-ttu-id="fd217-113">Il controllo Player viene eseguito in modalità remota.</span><span class="sxs-lookup"><span data-stu-id="fd217-113">The Player control is running in remote mode.</span></span> |
| <span data-ttu-id="fd217-114">false</span><span class="sxs-lookup"><span data-stu-id="fd217-114">false</span></span> | <span data-ttu-id="fd217-115">Il controllo Player viene eseguito in modalità locale.</span><span class="sxs-lookup"><span data-stu-id="fd217-115">The Player control is running in local mode.</span></span>  |



 

## <a name="remarks"></a><span data-ttu-id="fd217-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="fd217-116">Remarks</span></span>

<span data-ttu-id="fd217-117">**Windows Media Player 10 Mobile:** Questa proprietà restituisce sempre false.</span><span class="sxs-lookup"><span data-stu-id="fd217-117">**Windows Media Player 10 Mobile:** This property always returns false.</span></span>

## <a name="requirements"></a><span data-ttu-id="fd217-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fd217-118">Requirements</span></span>



| <span data-ttu-id="fd217-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="fd217-119">Requirement</span></span> | <span data-ttu-id="fd217-120">Valore</span><span class="sxs-lookup"><span data-stu-id="fd217-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="fd217-121">Versione</span><span class="sxs-lookup"><span data-stu-id="fd217-121">Version</span></span><br/> | <span data-ttu-id="fd217-122">Windows Media Player 9 serie o versione successiva.</span><span class="sxs-lookup"><span data-stu-id="fd217-122">Windows Media Player 9 Series or later.</span></span><br/>                                 |
| <span data-ttu-id="fd217-123">DLL</span><span class="sxs-lookup"><span data-stu-id="fd217-123">DLL</span></span><br/>     | <dl> <span data-ttu-id="fd217-124"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fd217-124"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fd217-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="fd217-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fd217-126">**Oggetto Player**</span><span class="sxs-lookup"><span data-stu-id="fd217-126">**Player Object**</span></span>](player-object.md)
</dt> <dt>

[<span data-ttu-id="fd217-127">**Gestione remota del controllo di Windows Media Player**</span><span class="sxs-lookup"><span data-stu-id="fd217-127">**Remoting the Windows Media Player Control**</span></span>](remoting-the-windows-media-player-control.md)
</dt> </dl>

 

 





