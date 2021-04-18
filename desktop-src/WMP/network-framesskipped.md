---
title: Rete. framesSkipped
description: La proprietà framesSkipped Recupera il numero totale di frame ignorati durante la riproduzione.
ms.assetid: fc7561a4-1e52-4192-b8df-ed2fb407fb78
keywords:
- Media Player di Windows Network. framesSkipped
topic_type:
- apiref
api_name:
- Network.framesSkipped
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6f33b778fffce071c47cb455f09e468243abab6a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329440"
---
# <a name="networkframesskipped"></a><span data-ttu-id="5fda8-104">Rete. framesSkipped</span><span class="sxs-lookup"><span data-stu-id="5fda8-104">Network.framesSkipped</span></span>

<span data-ttu-id="5fda8-105">La proprietà **framesSkipped** Recupera il numero totale di frame ignorati durante la riproduzione.</span><span class="sxs-lookup"><span data-stu-id="5fda8-105">The **framesSkipped** property retrieves the total number of frames skipped during playback.</span></span>

## <a name="syntax"></a><span data-ttu-id="5fda8-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5fda8-106">Syntax</span></span>

<span data-ttu-id="5fda8-107">*Player*. *rete*. **framesSkipped**</span><span class="sxs-lookup"><span data-stu-id="5fda8-107">*player*.*network*.**framesSkipped**</span></span>

## <a name="possible-values"></a><span data-ttu-id="5fda8-108">Valori possibili</span><span class="sxs-lookup"><span data-stu-id="5fda8-108">Possible Values</span></span>

<span data-ttu-id="5fda8-109">Questa proprietà è un **numero** di sola lettura (**Long**).</span><span class="sxs-lookup"><span data-stu-id="5fda8-109">This property is a read-only **Number** (**long**).</span></span>

## <a name="examples"></a><span data-ttu-id="5fda8-110">Esempio</span><span class="sxs-lookup"><span data-stu-id="5fda8-110">Examples</span></span>

<span data-ttu-id="5fda8-111">Nell'esempio JScript seguente viene utilizzata la *rete*. **framesSkipped** per visualizzare il numero totale di frame ignorati durante la riproduzione quando l'utente fa clic su un pulsante.</span><span class="sxs-lookup"><span data-stu-id="5fda8-111">The following JScript example uses *Network*.**framesSkipped** to display the total number of frames skipped during playback when the user clicks a button.</span></span> <span data-ttu-id="5fda8-112">Le informazioni vengono visualizzate in un DIV HTML creato con ID = "FS".</span><span class="sxs-lookup"><span data-stu-id="5fda8-112">The information is displayed in an HTML DIV created with ID = "FS".</span></span> <span data-ttu-id="5fda8-113">L'oggetto **Player** è stato creato con ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="5fda8-113">The **Player** object was created with ID = "Player".</span></span>


```JScript
<!-- Create an HTML BUTTON element. -->
<INPUT TYPE = "BUTTON" ID = "skipped" NAME = "skipped"
       VALUE = "Count frames skipped" 
       onClick = "FS.innerHTML = 'Frames skipped: ' + Player.network.framesSkipped;">

```



## <a name="requirements"></a><span data-ttu-id="5fda8-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5fda8-114">Requirements</span></span>



| <span data-ttu-id="5fda8-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="5fda8-115">Requirement</span></span> | <span data-ttu-id="5fda8-116">Valore</span><span class="sxs-lookup"><span data-stu-id="5fda8-116">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="5fda8-117">Versione</span><span class="sxs-lookup"><span data-stu-id="5fda8-117">Version</span></span><br/> | <span data-ttu-id="5fda8-118">Windows Media Player versione 7,0 o successiva.</span><span class="sxs-lookup"><span data-stu-id="5fda8-118">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="5fda8-119">DLL</span><span class="sxs-lookup"><span data-stu-id="5fda8-119">DLL</span></span><br/>     | <dl> <span data-ttu-id="5fda8-120"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5fda8-120"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5fda8-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5fda8-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5fda8-122">**Oggetto di rete**</span><span class="sxs-lookup"><span data-stu-id="5fda8-122">**Network Object**</span></span>](network-object.md)
</dt> </dl>

 

 





