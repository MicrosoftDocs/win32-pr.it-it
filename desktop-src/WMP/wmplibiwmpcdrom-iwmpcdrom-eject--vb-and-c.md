---
title: Metodo EJECT IWMPCdrom
description: Il metodo EJECT espelle il CD o il DVD dall'unità. | Metodo EJECT IWMPCdrom
ms.assetid: c0a69252-fd79-452c-bc61-3c3e8bcaaf48
keywords:
- Metodo EJECT Media Player Windows
- Metodo EJECT Media Player Windows, interfaccia IWMPCdrom
- Interfaccia IWMPCdrom Windows Media Player, metodo EJECT
topic_type:
- apiref
api_name:
- IWMPCdrom.eject
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b8ca2403b86b648e98861d91a21db80ddb64aac
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329674"
---
# <a name="iwmpcdromeject-method"></a><span data-ttu-id="18fbb-107">Metodo IWMPCdrom:: Eject</span><span class="sxs-lookup"><span data-stu-id="18fbb-107">IWMPCdrom::eject method</span></span>

<span data-ttu-id="18fbb-108">Il metodo **eject** espelle il CD o il DVD dall'unità.</span><span class="sxs-lookup"><span data-stu-id="18fbb-108">The **eject** method ejects the CD or DVD from the drive.</span></span>

## <a name="syntax"></a><span data-ttu-id="18fbb-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="18fbb-109">Syntax</span></span>


```CSharp
public void eject();
```


```VB

Public Sub eject()
Implements IWMPCdrom.eject
```





## <a name="parameters"></a><span data-ttu-id="18fbb-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="18fbb-110">Parameters</span></span>

<span data-ttu-id="18fbb-111">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="18fbb-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="18fbb-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="18fbb-112">Return value</span></span>

<span data-ttu-id="18fbb-113">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="18fbb-113">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="18fbb-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="18fbb-114">Remarks</span></span>

<span data-ttu-id="18fbb-115">Se lo sportello dell'unità è aperto, questo metodo chiude lo sportello.</span><span class="sxs-lookup"><span data-stu-id="18fbb-115">If the drive door is open, this method closes the door.</span></span>

<span data-ttu-id="18fbb-116">Per usare questo metodo, è necessario l'accesso in lettura alla libreria.</span><span class="sxs-lookup"><span data-stu-id="18fbb-116">To use this method, read access to the library is required.</span></span> <span data-ttu-id="18fbb-117">Per altre informazioni, vedere [accesso alla libreria](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="18fbb-117">For more information, see [Library Access](library-access.md).</span></span>

## <a name="examples"></a><span data-ttu-id="18fbb-118">Esempio</span><span class="sxs-lookup"><span data-stu-id="18fbb-118">Examples</span></span>

<span data-ttu-id="18fbb-119">Nell'esempio seguente viene usato **eject** per aprire lo sportello dell'unità CD o DVD con indice zero in risposta all'evento Click di un pulsante.</span><span class="sxs-lookup"><span data-stu-id="18fbb-119">The following example uses **eject** to open the door of the CD or DVD drive that has the index of zero in response to the Click event of a button.</span></span> <span data-ttu-id="18fbb-120">L'oggetto **AxWMPLib. AxWindowsMediaPlayer** è rappresentato dalla variabile denominata Player.</span><span class="sxs-lookup"><span data-stu-id="18fbb-120">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
private void ejectButton_Click(object o, System.EventArgs args)
{
    player.cdromCollection.Item(0).eject();
}
```


```VB

Public Sub ejectButton_Click(ByVal o As Object, ByVal args As System.EventArgs) Handles ejectButton.Click

    player.cdromCollection.Item(0).eject()

End Sub
```





## <a name="requirements"></a><span data-ttu-id="18fbb-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="18fbb-121">Requirements</span></span>



| <span data-ttu-id="18fbb-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="18fbb-122">Requirement</span></span> | <span data-ttu-id="18fbb-123">Valore</span><span class="sxs-lookup"><span data-stu-id="18fbb-123">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="18fbb-124">Versione</span><span class="sxs-lookup"><span data-stu-id="18fbb-124">Version</span></span><br/>   | <span data-ttu-id="18fbb-125">Windows Media Player 9 serie o versione successiva</span><span class="sxs-lookup"><span data-stu-id="18fbb-125">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="18fbb-126">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="18fbb-126">Namespace</span></span><br/> | <span data-ttu-id="18fbb-127">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="18fbb-127">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="18fbb-128">Assembly</span><span class="sxs-lookup"><span data-stu-id="18fbb-128">Assembly</span></span><br/>  | <dl> <span data-ttu-id="18fbb-129"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="18fbb-129"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="18fbb-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="18fbb-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="18fbb-131">**AxWindowsMediaPlayer. riproduzione (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="18fbb-131">**AxWindowsMediaPlayer.playState (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-playstate--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="18fbb-132">**Interfaccia IWMPCdrom (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="18fbb-132">**IWMPCdrom Interface (VB and C#)**</span></span>](iwmpcdrom--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="18fbb-133">**IWMPSettings2. mediaAccessRights (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="18fbb-133">**IWMPSettings2.mediaAccessRights (VB and C#)**</span></span>](wmplibiwmpsettings2-iwmpsettings2-mediaaccessrights--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="18fbb-134">**IWMPSettings2. requestMediaAccessRights (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="18fbb-134">**IWMPSettings2.requestMediaAccessRights (VB and C#)**</span></span>](wmplibiwmpsettings2-iwmpsettings2-requestmediaaccessrights--vb-and-c.md)
</dt> </dl>

 

 





