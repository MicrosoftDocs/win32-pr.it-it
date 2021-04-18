---
title: Proprietà AxWindowsMediaPlayer. versionInfo
description: La proprietà versionInfo ottiene un valore che specifica la versione di Windows Media Player.
ms.assetid: e128bec5-1ae9-4710-800e-4f97df362909
keywords:
- Finestra delle proprietà di versionInfo Media Player
- Proprietà versionInfo Windows Media Player, classe AxWindowsMediaPlayer
- Classe AxWindowsMediaPlayer Media Player Windows, proprietà versionInfo
topic_type:
- apiref
api_name:
- AxWindowsMediaPlayer.versionInfo
api_location:
- AxInterop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e2f759c2aedb19e21c4b7d90f3634141e4c37ec8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330897"
---
# <a name="axwindowsmediaplayerversioninfo-property"></a><span data-ttu-id="eef52-106">Proprietà AxWindowsMediaPlayer. versionInfo</span><span class="sxs-lookup"><span data-stu-id="eef52-106">AxWindowsMediaPlayer.versionInfo property</span></span>

<span data-ttu-id="eef52-107">La proprietà versionInfo ottiene un valore che specifica la versione di Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="eef52-107">The versionInfo property gets a value that specifies the version of the Windows Media Player.</span></span>

<span data-ttu-id="eef52-108">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="eef52-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="eef52-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="eef52-109">Syntax</span></span>


```CSharp
public System.String versionInfo {get;}
```


```VB

Public ReadOnly Property versionInfo As System.String
```





## <a name="property-value"></a><span data-ttu-id="eef52-110">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="eef52-110">Property value</span></span>

<span data-ttu-id="eef52-111">System. String che rappresenta le informazioni sulla versione nel formato seguente: "*X*. 0,0. *Aaaa*"dove *X* rappresenta il numero di versione principale e *aaaa* rappresenta il numero di Build.</span><span class="sxs-lookup"><span data-stu-id="eef52-111">A System.String that is the version information in the following format: "*X*.0.0.*YYYY*" where *X* represents the major version number and *YYYY* represents the build number.</span></span>

## <a name="examples"></a><span data-ttu-id="eef52-112">Esempio</span><span class="sxs-lookup"><span data-stu-id="eef52-112">Examples</span></span>

<span data-ttu-id="eef52-113">Nell'esempio seguente viene creato un pulsante che, se selezionato, Visualizza una finestra di messaggio contenente le informazioni sulla versione di Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="eef52-113">The following example creates a button that, when clicked, displays a message box containing the version information for Windows Media Player.</span></span> <span data-ttu-id="eef52-114">L'oggetto AxWMPLib. AxWindowsMediaPlayer è rappresentato dalla variabile denominata Player.</span><span class="sxs-lookup"><span data-stu-id="eef52-114">The AxWMPLib.AxWindowsMediaPlayer object is represented by the variable named player.</span></span>


```CSharp
private void showVersion_Click(object sender, System.EventArgs e)
{
    // Build the message containing the version info. 
    string message = ("Windows Media Player Version: " + player.versionInfo);

    // Display the message. 
    System.Windows.Forms.MessageBox.Show(message);
}
```


```VB

Public Sub showVersion_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles showVersion.Click

    &#39; Build the message containing the version info. 
    Dim message As String = (&quot;Windows Media Player Version: &quot; + player.versionInfo)

    &#39; Display the message. 
    System.Windows.Forms.MessageBox.Show(message)

End Sub
```





## <a name="requirements"></a><span data-ttu-id="eef52-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="eef52-115">Requirements</span></span>



| <span data-ttu-id="eef52-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="eef52-116">Requirement</span></span> | <span data-ttu-id="eef52-117">Valore</span><span class="sxs-lookup"><span data-stu-id="eef52-117">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eef52-118">Versione</span><span class="sxs-lookup"><span data-stu-id="eef52-118">Version</span></span><br/>   | <span data-ttu-id="eef52-119">Windows Media Player 9 serie o versione successiva</span><span class="sxs-lookup"><span data-stu-id="eef52-119">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="eef52-120">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="eef52-120">Namespace</span></span><br/> | <span data-ttu-id="eef52-121">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="eef52-121">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="eef52-122">Assembly</span><span class="sxs-lookup"><span data-stu-id="eef52-122">Assembly</span></span><br/>  | <dl> <span data-ttu-id="eef52-123"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="eef52-123"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eef52-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="eef52-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eef52-125">**Oggetto AxWindowsMediaPlayer (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="eef52-125">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> </dl>

 

 





