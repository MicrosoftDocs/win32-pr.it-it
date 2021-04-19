---
title: Proprietà defaultFrame di IWMPSettings
description: La proprietà defaultFrame Ottiene o imposta il nome del frame utilizzato per visualizzare un URL ricevuto in un \_ evento AxWindowsMediaPlayer WMPOCXEvents \_ ScriptCommandEvent.
ms.assetid: 92c775ac-5ff1-4d21-b21d-491bc48a033f
keywords:
- Finestra delle proprietà di defaultFrame Media Player
- Proprietà di defaultFrame Media Player Windows, interfaccia IWMPSettings
- Interfaccia IWMPSettings Windows Media Player, proprietà defaultFrame
topic_type:
- apiref
api_name:
- IWMPSettings.defaultFrame
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 28539640214165ab5b2808762ed854b19b434311
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325965"
---
# <a name="iwmpsettingsdefaultframe-property"></a><span data-ttu-id="baa9c-106">IWMPSettings::d proprietà efaultFrame</span><span class="sxs-lookup"><span data-stu-id="baa9c-106">IWMPSettings::defaultFrame property</span></span>

<span data-ttu-id="baa9c-107">La proprietà **DefaultFrame** Ottiene o imposta il nome del frame utilizzato per visualizzare un URL ricevuto in un evento **AxWindowsMediaPlayer \_ WMPOCXEvents \_ ScriptCommandEvent** .</span><span class="sxs-lookup"><span data-stu-id="baa9c-107">The **defaultFrame** property gets or sets the name of the frame used to display a URL that is received in an **AxWindowsMediaPlayer\_WMPOCXEvents\_ScriptCommandEvent** event.</span></span>

## <a name="syntax"></a><span data-ttu-id="baa9c-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="baa9c-108">Syntax</span></span>


```CSharp
public System.String defaultFrame {get; set;}
```


```VB

Public Property defaultFrame As System.String
```





## <a name="property-value"></a><span data-ttu-id="baa9c-109">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="baa9c-109">Property value</span></span>

<span data-ttu-id="baa9c-110">**System. String** che corrisponde al valore dell'attributo Name dell'elemento **frame** di destinazione.</span><span class="sxs-lookup"><span data-stu-id="baa9c-110">A **System.String** that is the value of the name attribute of the target **FRAME** element.</span></span>

## <a name="remarks"></a><span data-ttu-id="baa9c-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="baa9c-111">Remarks</span></span>

<span data-ttu-id="baa9c-112">Se viene specificato un frame di destinazione nell'evento **\_ WMPOCXEvents \_ ScriptCommandEvent** , questa proprietà viene ignorata.</span><span class="sxs-lookup"><span data-stu-id="baa9c-112">If a target frame is specified in the **\_WMPOCXEvents\_ScriptCommandEvent** event itself, this property is ignored.</span></span>

<span data-ttu-id="baa9c-113">Questa proprietà viene ignorata quando si usa l'applet Java del navigatore Netscape.</span><span class="sxs-lookup"><span data-stu-id="baa9c-113">This property is ignored when using the Netscape Navigator Java applet.</span></span> <span data-ttu-id="baa9c-114">In Netscape Navigator ogni comando script URL ricevuto visualizzerà l'URL in una nuova finestra del browser, indipendentemente dal valore di **DefaultFrame**.</span><span class="sxs-lookup"><span data-stu-id="baa9c-114">In Netscape Navigator, each URL script command received will display the URL in a new browser window, regardless of the value of **defaultFrame**.</span></span>

## <a name="requirements"></a><span data-ttu-id="baa9c-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="baa9c-115">Requirements</span></span>



| <span data-ttu-id="baa9c-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="baa9c-116">Requirement</span></span> | <span data-ttu-id="baa9c-117">Valore</span><span class="sxs-lookup"><span data-stu-id="baa9c-117">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="baa9c-118">Versione</span><span class="sxs-lookup"><span data-stu-id="baa9c-118">Version</span></span><br/>   | <span data-ttu-id="baa9c-119">Windows Media Player 9 serie o versione successiva</span><span class="sxs-lookup"><span data-stu-id="baa9c-119">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="baa9c-120">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="baa9c-120">Namespace</span></span><br/> | <span data-ttu-id="baa9c-121">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="baa9c-121">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="baa9c-122">Assembly</span><span class="sxs-lookup"><span data-stu-id="baa9c-122">Assembly</span></span><br/>  | <dl> <span data-ttu-id="baa9c-123"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="baa9c-123"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="baa9c-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="baa9c-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="baa9c-125">**Evento AxWindowsMediaPlayer. ScriptCommand (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="baa9c-125">**AxWindowsMediaPlayer.ScriptCommand Event (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-scriptcommand.md)
</dt> <dt>

[<span data-ttu-id="baa9c-126">**Interfaccia IWMPSettings (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="baa9c-126">**IWMPSettings Interface (VB and C#)**</span></span>](iwmpsettings--vb-and-c.md)
</dt> </dl>

 

 





