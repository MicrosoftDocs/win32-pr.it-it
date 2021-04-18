---
title: Proprietà invokeURLs di IWMPSettings
description: La proprietà invokeURLs Ottiene o imposta un valore che indica se gli eventi URL devono avviare un Web browser.
ms.assetid: e16c968d-a1b7-4c3a-9c1a-5748ed44cdac
keywords:
- Finestra delle proprietà di invokeURLs Media Player
- Proprietà di invokeURLs Media Player Windows, interfaccia IWMPSettings
- Interfaccia IWMPSettings Windows Media Player, proprietà invokeURLs
topic_type:
- apiref
api_name:
- IWMPSettings.invokeURLs
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bbdd68d797b54f4e9365f381b2b5c705dffc419b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333910"
---
# <a name="iwmpsettingsinvokeurls-property"></a><span data-ttu-id="50041-106">Proprietà IWMPSettings:: invokeURLs</span><span class="sxs-lookup"><span data-stu-id="50041-106">IWMPSettings::invokeURLs property</span></span>

<span data-ttu-id="50041-107">La proprietà **invokeURLs** Ottiene o imposta un valore che indica se gli eventi URL devono avviare un Web browser.</span><span class="sxs-lookup"><span data-stu-id="50041-107">The **invokeURLs** property gets or sets a value indicating whether URL events should launch a Web browser.</span></span>

## <a name="syntax"></a><span data-ttu-id="50041-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="50041-108">Syntax</span></span>


```CSharp
public System.Boolean invokeURLs {get; set;}
```


```VB

Public Property invokeURLs As System.Boolean
```





## <a name="property-value"></a><span data-ttu-id="50041-109">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="50041-109">Property value</span></span>

<span data-ttu-id="50041-110">Valore **System. Boolean** che indica se gli eventi URL devono avviare un Web browser.</span><span class="sxs-lookup"><span data-stu-id="50041-110">A **System.Boolean** value indicating whether URL events should launch a Web browser.</span></span> <span data-ttu-id="50041-111">Il valore predefinito è **True**.</span><span class="sxs-lookup"><span data-stu-id="50041-111">The default is **true**.</span></span>

## <a name="remarks"></a><span data-ttu-id="50041-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="50041-112">Remarks</span></span>

<span data-ttu-id="50041-113">I file multimediali digitali e i flussi possono contenere comandi di script URL.</span><span class="sxs-lookup"><span data-stu-id="50041-113">Digital media files and streams can contain URL script commands.</span></span> <span data-ttu-id="50041-114">Quando un comando script URL viene inviato al controllo Media Player di Windows, viene passato prima al gestore eventi **AxWindowsMediaPlayer \_ WMPOCXEvents \_ ScriptCommandEvent** , indipendentemente dal valore recuperato da **invokeURLs**.</span><span class="sxs-lookup"><span data-stu-id="50041-114">When a URL script command is sent to the Windows Media Player control, it is passed first to the **AxWindowsMediaPlayer\_WMPOCXEvents\_ScriptCommandEvent** event handler regardless of the value retrieved by **invokeURLs**.</span></span> <span data-ttu-id="50041-115">Dopo la chiusura di **\_ WMPOCXEvents \_ ScriptCommandEvent** , Windows Media Player controlla **invokeURLs** per determinare se avviare il Web browser predefinito con l'URL.</span><span class="sxs-lookup"><span data-stu-id="50041-115">After **\_WMPOCXEvents\_ScriptCommandEvent** exits, Windows Media Player checks **invokeURLs** to determine whether to launch the default Web browser with the URL.</span></span> <span data-ttu-id="50041-116">È possibile visualizzare gli URL in modo selettivo selezionando **\_ WMPOCXEvents \_ ScriptCommandEvent** e impostando **invokeURLs** come desiderato.</span><span class="sxs-lookup"><span data-stu-id="50041-116">You can selectively display URLs by checking them in **\_WMPOCXEvents\_ScriptCommandEvent** and setting **invokeURLs** as desired.</span></span>

## <a name="requirements"></a><span data-ttu-id="50041-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="50041-117">Requirements</span></span>



| <span data-ttu-id="50041-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="50041-118">Requirement</span></span> | <span data-ttu-id="50041-119">Valore</span><span class="sxs-lookup"><span data-stu-id="50041-119">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="50041-120">Versione</span><span class="sxs-lookup"><span data-stu-id="50041-120">Version</span></span><br/>   | <span data-ttu-id="50041-121">Windows Media Player 9 serie o versione successiva</span><span class="sxs-lookup"><span data-stu-id="50041-121">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="50041-122">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="50041-122">Namespace</span></span><br/> | <span data-ttu-id="50041-123">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="50041-123">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="50041-124">Assembly</span><span class="sxs-lookup"><span data-stu-id="50041-124">Assembly</span></span><br/>  | <dl> <span data-ttu-id="50041-125"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="50041-125"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="50041-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="50041-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="50041-127">**Evento AxWindowsMediaPlayer. ScriptCommand (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="50041-127">**AxWindowsMediaPlayer.ScriptCommand Event (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-scriptcommand.md)
</dt> <dt>

[<span data-ttu-id="50041-128">**Interfaccia IWMPSettings (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="50041-128">**IWMPSettings Interface (VB and C#)**</span></span>](iwmpsettings--vb-and-c.md)
</dt> </dl>

 

 





