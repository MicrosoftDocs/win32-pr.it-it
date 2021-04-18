---
title: AxWindowsMediaPlayer. launchURL, metodo
description: Il metodo launchURL Invia un URL al browser predefinito dell'utente di cui eseguire il rendering. | AxWindowsMediaPlayer. launchURL, metodo
ms.assetid: 3e8dfdbb-b5ad-44ea-97a6-e860386b7fb4
keywords:
- Metodo launchURL Windows Media Player
- Metodo launchURL Windows Media Player, classe AxWindowsMediaPlayer
- Classe AxWindowsMediaPlayer Windows Media Player, metodo launchURL
topic_type:
- apiref
api_name:
- AxWindowsMediaPlayer.launchURL
api_location:
- AxInterop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27fe8e544bb14b119785b26b9cb5be5cdad48015
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331887"
---
# <a name="axwindowsmediaplayerlaunchurl-method"></a><span data-ttu-id="4bc6b-107">AxWindowsMediaPlayer. launchURL, metodo</span><span class="sxs-lookup"><span data-stu-id="4bc6b-107">AxWindowsMediaPlayer.launchURL method</span></span>

<span data-ttu-id="4bc6b-108">Il metodo launchURL Invia un URL al browser predefinito dell'utente di cui eseguire il rendering.</span><span class="sxs-lookup"><span data-stu-id="4bc6b-108">The launchURL method sends a URL to the user's default browser to be rendered.</span></span>

## <a name="syntax"></a><span data-ttu-id="4bc6b-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4bc6b-109">Syntax</span></span>


```CSharp
public void launchURL(
  System.String bstrURL
);
```


```VB

Public Sub launchURL( _
  ByVal bstrURL As System.String _
)
```





## <a name="parameters"></a><span data-ttu-id="4bc6b-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="4bc6b-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4bc6b-111">*bstrURL*</span><span class="sxs-lookup"><span data-stu-id="4bc6b-111">*bstrURL*</span></span> 
</dt> <dd>

<span data-ttu-id="4bc6b-112">**System. String** che rappresenta l'URL da avviare.</span><span class="sxs-lookup"><span data-stu-id="4bc6b-112">The **System.String** that is the URL to launch.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4bc6b-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4bc6b-113">Return value</span></span>

<span data-ttu-id="4bc6b-114">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="4bc6b-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="4bc6b-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="4bc6b-115">Remarks</span></span>

<span data-ttu-id="4bc6b-116">Questo metodo apre solo le pagine Web usando i protocolli HTTP o HTTPS.</span><span class="sxs-lookup"><span data-stu-id="4bc6b-116">This method only opens webpages using the HTTP or HTTPS protocols.</span></span>

## <a name="examples"></a><span data-ttu-id="4bc6b-117">Esempio</span><span class="sxs-lookup"><span data-stu-id="4bc6b-117">Examples</span></span>

<span data-ttu-id="4bc6b-118">Nell'esempio seguente viene creato un pulsante che, se selezionato, Visualizza il sito Web Microsoft in una nuova finestra del browser.</span><span class="sxs-lookup"><span data-stu-id="4bc6b-118">The following example creates a button that, when clicked, displays the Microsoft website in a new browser window.</span></span> <span data-ttu-id="4bc6b-119">L'oggetto AxWMPLib. AxWindowsMediaPlayer è rappresentato dalla variabile denominata Player.</span><span class="sxs-lookup"><span data-stu-id="4bc6b-119">The AxWMPLib.AxWindowsMediaPlayer object is represented by the variable named player.</span></span>


```CSharp
private void goToMS_Click(object sender, System.EventArgs e)
{
    // Open the Microsoft website. 
    player.launchURL("https://www.microsoft.com");
}
```


```VB

Public Sub goToMS_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles goToMS.Click

    &#39; Open the Microsoft website. 
    player.launchURL(&quot;https://www.microsoft.com&quot;)

End Sub
```





## <a name="requirements"></a><span data-ttu-id="4bc6b-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4bc6b-120">Requirements</span></span>



| <span data-ttu-id="4bc6b-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="4bc6b-121">Requirement</span></span> | <span data-ttu-id="4bc6b-122">Valore</span><span class="sxs-lookup"><span data-stu-id="4bc6b-122">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4bc6b-123">Versione</span><span class="sxs-lookup"><span data-stu-id="4bc6b-123">Version</span></span><br/>   | <span data-ttu-id="4bc6b-124">Windows Media Player 9 serie o versione successiva</span><span class="sxs-lookup"><span data-stu-id="4bc6b-124">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="4bc6b-125">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="4bc6b-125">Namespace</span></span><br/> | <span data-ttu-id="4bc6b-126">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="4bc6b-126">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="4bc6b-127">Assembly</span><span class="sxs-lookup"><span data-stu-id="4bc6b-127">Assembly</span></span><br/>  | <dl> <span data-ttu-id="4bc6b-128"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="4bc6b-128"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4bc6b-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4bc6b-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4bc6b-130">**Oggetto AxWindowsMediaPlayer (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="4bc6b-130">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> </dl>

 

 





