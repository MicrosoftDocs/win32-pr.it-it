---
title: Cdrom. EJECT (metodo)
description: Il metodo EJECT espelle il CD o il DVD dall'unità. | Cdrom. EJECT (metodo)
ms.assetid: f43c7f10-7de2-488c-833a-ecd3ac21744b
keywords:
- Metodo EJECT Media Player Windows
- Metodo EJECT Windows Media Player, classe cdrom
- Classe cdrom Media Player Windows, metodo EJECT
topic_type:
- apiref
api_name:
- Cdrom.eject
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 78326ca57dcf097344fc073681fae772222ea9ad
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "106321459"
---
# <a name="cdromeject-method"></a><span data-ttu-id="3a71b-107">Cdrom. EJECT (metodo)</span><span class="sxs-lookup"><span data-stu-id="3a71b-107">Cdrom.eject method</span></span>

<span data-ttu-id="3a71b-108">Il metodo **eject** espelle il CD o il DVD dall'unità.</span><span class="sxs-lookup"><span data-stu-id="3a71b-108">The **eject** method ejects the CD or DVD from the drive.</span></span>

## <a name="syntax"></a><span data-ttu-id="3a71b-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3a71b-109">Syntax</span></span>


```JScript
Cdrom.eject()
```



## <a name="parameters"></a><span data-ttu-id="3a71b-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="3a71b-110">Parameters</span></span>

<span data-ttu-id="3a71b-111">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="3a71b-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="3a71b-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3a71b-112">Return value</span></span>

<span data-ttu-id="3a71b-113">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="3a71b-113">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="3a71b-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="3a71b-114">Remarks</span></span>

<span data-ttu-id="3a71b-115">Se lo sportello dell'unità è aperto, questo metodo chiude lo sportello.</span><span class="sxs-lookup"><span data-stu-id="3a71b-115">If the drive door is open, this method closes the door.</span></span>

<span data-ttu-id="3a71b-116">Per usare questo metodo, è necessario l'accesso in lettura alla libreria.</span><span class="sxs-lookup"><span data-stu-id="3a71b-116">To use this method, read access to the library is required.</span></span> <span data-ttu-id="3a71b-117">Per altre informazioni, vedere [accesso alla libreria](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="3a71b-117">For more information, see [Library Access](library-access.md).</span></span>

<span data-ttu-id="3a71b-118">**Windows Media Player 10 Mobile:** Questo metodo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="3a71b-118">**Windows Media Player 10 Mobile:** This method is not supported.</span></span>

## <a name="examples"></a><span data-ttu-id="3a71b-119">Esempio</span><span class="sxs-lookup"><span data-stu-id="3a71b-119">Examples</span></span>

<span data-ttu-id="3a71b-120">Nell'esempio seguente viene creato un elemento Button HTML che usa *CDROM*. **eject** per aprire la porta dell'unità con indice identificatore unità zero.</span><span class="sxs-lookup"><span data-stu-id="3a71b-120">The following example creates an HTML button element that uses *Cdrom*.**eject** to open the door of the drive that has drive specifier index zero.</span></span> <span data-ttu-id="3a71b-121">L'oggetto **Player** è stato creato con ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="3a71b-121">The **Player** object was created with ID = "Player".</span></span>


```JScript
<INPUT TYPE = "BUTTON"
       NAME = "EJECTBUTTON"
       VALUE = "EJECT"
       OnClick =  "Player.cdromCollection.item(0).eject()"
>
```



## <a name="requirements"></a><span data-ttu-id="3a71b-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3a71b-122">Requirements</span></span>



| <span data-ttu-id="3a71b-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="3a71b-123">Requirement</span></span> | <span data-ttu-id="3a71b-124">Valore</span><span class="sxs-lookup"><span data-stu-id="3a71b-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="3a71b-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3a71b-125">Minimum supported client</span></span><br/> | <span data-ttu-id="3a71b-126">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="3a71b-126">Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="3a71b-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3a71b-127">Minimum supported server</span></span><br/> | <span data-ttu-id="3a71b-128">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="3a71b-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="3a71b-129">Versione</span><span class="sxs-lookup"><span data-stu-id="3a71b-129">Version</span></span><br/>                  | <span data-ttu-id="3a71b-130">Windows Media Player versione 7,0 o successiva.</span><span class="sxs-lookup"><span data-stu-id="3a71b-130">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="3a71b-131">DLL</span><span class="sxs-lookup"><span data-stu-id="3a71b-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3a71b-132"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3a71b-132"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3a71b-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3a71b-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3a71b-134">**Oggetto cdrom**</span><span class="sxs-lookup"><span data-stu-id="3a71b-134">**Cdrom Object**</span></span>](cdrom-object.md)
</dt> <dt>

[<span data-ttu-id="3a71b-135">**Player. riproduzione**</span><span class="sxs-lookup"><span data-stu-id="3a71b-135">**Player.playState**</span></span>](player-playstate.md)
</dt> <dt>

[<span data-ttu-id="3a71b-136">**Settings. mediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="3a71b-136">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="3a71b-137">**Settings. requestMediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="3a71b-137">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





