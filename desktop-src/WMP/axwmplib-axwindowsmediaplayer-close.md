---
title: Metodo AxWindowsMediaPlayer. Close
description: Il metodo Close chiude il file multimediale digitale corrente, interrompe la riproduzione in Windows Media Player e rilascia le risorse di Windows Media Player.
ms.assetid: 3e555086-c31c-42d7-b671-0fd824f66641
keywords:
- Chiudi metodo Windows Media Player
- Metodo Close Media Player Windows, classe AxWindowsMediaPlayer
- Classe AxWindowsMediaPlayer Windows Media Player, metodo Close
topic_type:
- apiref
api_name:
- AxWindowsMediaPlayer.close
api_location:
- AxInterop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f1dc0c93e449e9ef1b00af7fb073068078f0fcc5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327080"
---
# <a name="axwindowsmediaplayerclose-method"></a><span data-ttu-id="8a14f-106">Metodo AxWindowsMediaPlayer. Close</span><span class="sxs-lookup"><span data-stu-id="8a14f-106">AxWindowsMediaPlayer.close method</span></span>

<span data-ttu-id="8a14f-107">Il metodo Close chiude il file multimediale digitale corrente, interrompe la riproduzione in Windows Media Player e rilascia le risorse di Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="8a14f-107">The close method closes the current digital media file, stops playback in Windows Media Player and releases Windows Media Player resources.</span></span>

## <a name="syntax"></a><span data-ttu-id="8a14f-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8a14f-108">Syntax</span></span>


```CSharp
public void close();
```


```VB

Public Sub close()
```





## <a name="parameters"></a><span data-ttu-id="8a14f-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="8a14f-109">Parameters</span></span>

<span data-ttu-id="8a14f-110">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="8a14f-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="8a14f-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8a14f-111">Return value</span></span>

<span data-ttu-id="8a14f-112">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="8a14f-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="8a14f-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="8a14f-113">Remarks</span></span>

<span data-ttu-id="8a14f-114">Questo metodo chiude il file multimediale digitale corrente, non Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="8a14f-114">This method closes the current digital media file, not Windows Media Player itself.</span></span>

## <a name="examples"></a><span data-ttu-id="8a14f-115">Esempio</span><span class="sxs-lookup"><span data-stu-id="8a14f-115">Examples</span></span>

<span data-ttu-id="8a14f-116">Nell'esempio seguente viene creato un pulsante che, se selezionato, interrompe la riproduzione in Windows Media Player e rilascia le risorse in uso.</span><span class="sxs-lookup"><span data-stu-id="8a14f-116">The following example creates a button that, when clicked, stops playback in Windows Media Player and releases the resources in use.</span></span> <span data-ttu-id="8a14f-117">L'oggetto AxWMPLib. AxWindowsMediaPlayer è rappresentato dalla variabile denominata Player.</span><span class="sxs-lookup"><span data-stu-id="8a14f-117">The AxWMPLib.AxWindowsMediaPlayer object is represented by the variable named player.</span></span>


```CSharp
private void closeIt_Click(object sender, System.EventArgs e)
{
    // Close the Player. 
    player.close();
}
```


```VB

Public Sub closeIt_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles closeIt.Click

    &#39; Close the Player. 
    player.close()

End Sub
```





## <a name="requirements"></a><span data-ttu-id="8a14f-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8a14f-118">Requirements</span></span>



| <span data-ttu-id="8a14f-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="8a14f-119">Requirement</span></span> | <span data-ttu-id="8a14f-120">Valore</span><span class="sxs-lookup"><span data-stu-id="8a14f-120">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8a14f-121">Versione</span><span class="sxs-lookup"><span data-stu-id="8a14f-121">Version</span></span><br/>   | <span data-ttu-id="8a14f-122">Windows Media Player 9 serie o versione successiva</span><span class="sxs-lookup"><span data-stu-id="8a14f-122">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="8a14f-123">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="8a14f-123">Namespace</span></span><br/> | <span data-ttu-id="8a14f-124">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="8a14f-124">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="8a14f-125">Assembly</span><span class="sxs-lookup"><span data-stu-id="8a14f-125">Assembly</span></span><br/>  | <dl> <span data-ttu-id="8a14f-126"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="8a14f-126"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8a14f-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8a14f-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8a14f-128">**Oggetto AxWindowsMediaPlayer (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="8a14f-128">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> </dl>

 

 





