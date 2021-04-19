---
title: Player. playerApplication
description: La proprietà playerApplication recupera l'oggetto PlayerApplication quando viene eseguito un controllo Media Player Windows remoto.
ms.assetid: 09a8a63f-455f-4f81-8fdb-7de337139dea
keywords:
- Player. playerApplication Windows Media Player
topic_type:
- apiref
api_name:
- Player.playerApplication
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 401ebaae52efb746e7119419774d87d72c642fc4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327709"
---
# <a name="playerplayerapplication"></a><span data-ttu-id="2a49a-104">Player. playerApplication</span><span class="sxs-lookup"><span data-stu-id="2a49a-104">Player.playerApplication</span></span>

<span data-ttu-id="2a49a-105">La proprietà **playerApplication** recupera l'oggetto **playerApplication** quando viene eseguito un controllo Media Player Windows remoto.</span><span class="sxs-lookup"><span data-stu-id="2a49a-105">The **playerApplication** property retrieves the **PlayerApplication** object when a remoted Windows Media Player control is running.</span></span>

## <a name="syntax"></a><span data-ttu-id="2a49a-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2a49a-106">Syntax</span></span>

<span data-ttu-id="2a49a-107">**playerApplication**</span><span class="sxs-lookup"><span data-stu-id="2a49a-107">**playerApplication**</span></span>

## <a name="possible-values"></a><span data-ttu-id="2a49a-108">Valori possibili</span><span class="sxs-lookup"><span data-stu-id="2a49a-108">Possible Values</span></span>

<span data-ttu-id="2a49a-109">Questa proprietà è un oggetto **PlayerApplication** di sola lettura o il valore null.</span><span class="sxs-lookup"><span data-stu-id="2a49a-109">This property is a read-only **PlayerApplication** object or the null value.</span></span>

## <a name="remarks"></a><span data-ttu-id="2a49a-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="2a49a-110">Remarks</span></span>

<span data-ttu-id="2a49a-111">Questa proprietà viene utilizzata solo quando si esegue la comunicazione remota di Windows Media playercontrol.</span><span class="sxs-lookup"><span data-stu-id="2a49a-111">This property is used only when remoting the Windows Media Playercontrol.</span></span> <span data-ttu-id="2a49a-112">Se il valore è null, Windows Media playercontrol non è incorporato in modalità remota.</span><span class="sxs-lookup"><span data-stu-id="2a49a-112">If the value is null, the Windows Media Playercontrol is not embedded in remote mode.</span></span>

<span data-ttu-id="2a49a-113">Questa proprietà è accessibile solo nel codice C++ o nel codice di script nelle interfacce tramite la variabile globale playerApplication.</span><span class="sxs-lookup"><span data-stu-id="2a49a-113">This property is only accessible in C++ code or in script code in skins through the playerApplication global variable.</span></span>

## <a name="requirements"></a><span data-ttu-id="2a49a-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2a49a-114">Requirements</span></span>



| <span data-ttu-id="2a49a-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="2a49a-115">Requirement</span></span> | <span data-ttu-id="2a49a-116">Valore</span><span class="sxs-lookup"><span data-stu-id="2a49a-116">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="2a49a-117">Versione</span><span class="sxs-lookup"><span data-stu-id="2a49a-117">Version</span></span><br/> | <span data-ttu-id="2a49a-118">Windows Media Player 9 serie o versione successiva.</span><span class="sxs-lookup"><span data-stu-id="2a49a-118">Windows Media Player 9 Series or later.</span></span><br/>                                 |
| <span data-ttu-id="2a49a-119">DLL</span><span class="sxs-lookup"><span data-stu-id="2a49a-119">DLL</span></span><br/>     | <dl> <span data-ttu-id="2a49a-120"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2a49a-120"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2a49a-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2a49a-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2a49a-122">**Attributi globali**</span><span class="sxs-lookup"><span data-stu-id="2a49a-122">**Global Attributes**</span></span>](global-attributes.md)
</dt> <dt>

[<span data-ttu-id="2a49a-123">**Oggetto Player**</span><span class="sxs-lookup"><span data-stu-id="2a49a-123">**Player Object**</span></span>](player-object.md)
</dt> <dt>

[<span data-ttu-id="2a49a-124">**Oggetto PlayerApplication**</span><span class="sxs-lookup"><span data-stu-id="2a49a-124">**PlayerApplication Object**</span></span>](playerapplication-object.md)
</dt> <dt>

[<span data-ttu-id="2a49a-125">**Gestione remota del controllo di Windows Media Player**</span><span class="sxs-lookup"><span data-stu-id="2a49a-125">**Remoting the Windows Media Player Control**</span></span>](remoting-the-windows-media-player-control.md)
</dt> </dl>

 

 





