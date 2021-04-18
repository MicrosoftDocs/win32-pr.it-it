---
title: Proprietà AxWindowsMediaPlayer. URL
description: La proprietà URL Ottiene o imposta il nome dell'elemento multimediale da riprodurre.
ms.assetid: 521a3b39-efd6-45a7-895b-a9ae69e0bf39
keywords:
- Proprietà URL Media Player Windows
- Proprietà URL Media Player Windows, classe AxWindowsMediaPlayer
- Classe AxWindowsMediaPlayer Media Player Windows, proprietà URL
topic_type:
- apiref
api_name:
- AxWindowsMediaPlayer.URL
api_location:
- AxInterop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3ed9e601aa581e988bac1a233f06c4f5c552353
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330898"
---
# <a name="axwindowsmediaplayerurl-property"></a><span data-ttu-id="cbe69-106">Proprietà AxWindowsMediaPlayer. URL</span><span class="sxs-lookup"><span data-stu-id="cbe69-106">AxWindowsMediaPlayer.URL property</span></span>

<span data-ttu-id="cbe69-107">La proprietà URL Ottiene o imposta il nome dell'elemento multimediale da riprodurre.</span><span class="sxs-lookup"><span data-stu-id="cbe69-107">The URL property gets or sets the name of the media item to play.</span></span>

## <a name="syntax"></a><span data-ttu-id="cbe69-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="cbe69-108">Syntax</span></span>


```CSharp
public System.String URL {get; set;}
```


```VB

Public Property URL As System.String
```





## <a name="property-value"></a><span data-ttu-id="cbe69-109">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="cbe69-109">Property value</span></span>

<span data-ttu-id="cbe69-110">System. String che rappresenta l'URL dell'elemento multimediale.</span><span class="sxs-lookup"><span data-stu-id="cbe69-110">A System.String that is the URL of the media item.</span></span>

## <a name="remarks"></a><span data-ttu-id="cbe69-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="cbe69-111">Remarks</span></span>

<span data-ttu-id="cbe69-112">Questa proprietà può essere impostata solo su un URL in un'area di sicurezza uguale o meno restrittiva rispetto all'area di sicurezza del programma chiamante o della pagina Web.</span><span class="sxs-lookup"><span data-stu-id="cbe69-112">This property can only be set to a URL in a security zone that is the same or is less restrictive than the security zone of the calling program or webpage.</span></span>

<span data-ttu-id="cbe69-113">Le applicazioni che aprono elementi multimediali da dietro un firewall avranno prestazioni migliori se l'indirizzo viene specificato usando il nome del Domain Name Server (DNS) invece dell'indirizzo IP.</span><span class="sxs-lookup"><span data-stu-id="cbe69-113">Applications that open media items from behind a firewall will have better performance if the address is specified using the domain name server (DNS) name instead of the IP address.</span></span>

<span data-ttu-id="cbe69-114">Non chiamare questo metodo dal codice del gestore eventi.</span><span class="sxs-lookup"><span data-stu-id="cbe69-114">Do not call this method from event handler code.</span></span> <span data-ttu-id="cbe69-115">L' **URL** chiamante da un gestore eventi può produrre risultati imprevisti.</span><span class="sxs-lookup"><span data-stu-id="cbe69-115">Calling **URL** from an event handler may yield unexpected results.</span></span>

## <a name="examples"></a><span data-ttu-id="cbe69-116">Esempio</span><span class="sxs-lookup"><span data-stu-id="cbe69-116">Examples</span></span>

<span data-ttu-id="cbe69-117">Nell'esempio seguente viene consentito all'utente di specificare un file multimediale immettendo un percorso di file in una casella di testo.</span><span class="sxs-lookup"><span data-stu-id="cbe69-117">The following example allows the user to specify a media file by entering a file path in a text box.</span></span> <span data-ttu-id="cbe69-118">Quando si fa clic su un pulsante, la proprietà URL viene impostata sul file specificato e il file viene riprodotto.</span><span class="sxs-lookup"><span data-stu-id="cbe69-118">When a button is clicked, the URL property is set to the specified file and the file is played.</span></span> <span data-ttu-id="cbe69-119">L'oggetto AxWMPLib. AxWindowsMediaPlayer è rappresentato dalla variabile denominata Player.</span><span class="sxs-lookup"><span data-stu-id="cbe69-119">The AxWMPLib.AxWindowsMediaPlayer object is represented by the variable named player.</span></span>


```CSharp
private void openMedia_Click(object sender, System.EventArgs e)
{
    // Set the URL property to the file path obtained from the text box. 
    player.URL = inputURL.Text;

    // Play the media file. 
    player.Ctlcontrols.play();
}
```


```VB

Public Sub openMedia_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles openMedia.Click

    &#39; Set the URL property to the file path obtained from the text box. 
    player.URL = inputURL.Text

    &#39; Play the media file. 
    player.Ctlcontrols.play()

End Sub
```





## <a name="requirements"></a><span data-ttu-id="cbe69-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="cbe69-120">Requirements</span></span>



| <span data-ttu-id="cbe69-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="cbe69-121">Requirement</span></span> | <span data-ttu-id="cbe69-122">Valore</span><span class="sxs-lookup"><span data-stu-id="cbe69-122">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cbe69-123">Versione</span><span class="sxs-lookup"><span data-stu-id="cbe69-123">Version</span></span><br/>   | <span data-ttu-id="cbe69-124">Windows Media Player 9 serie o versione successiva</span><span class="sxs-lookup"><span data-stu-id="cbe69-124">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="cbe69-125">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="cbe69-125">Namespace</span></span><br/> | <span data-ttu-id="cbe69-126">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="cbe69-126">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="cbe69-127">Assembly</span><span class="sxs-lookup"><span data-stu-id="cbe69-127">Assembly</span></span><br/>  | <dl> <span data-ttu-id="cbe69-128"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="cbe69-128"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cbe69-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="cbe69-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cbe69-130">**Oggetto AxWindowsMediaPlayer (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="cbe69-130">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> </dl>

 

 





