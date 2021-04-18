---
title: Proprietà baseURL di IWMPSettings
description: La proprietà baseURL Ottiene o imposta l'URL di base usato per la risoluzione del percorso relativo con i comandi script URL incorporati nel contenuto multimediale digitale.
ms.assetid: e136303f-ba08-434f-ad7e-9fffa66785c4
keywords:
- Finestra delle proprietà di baseURL Media Player
- Proprietà di baseURL Media Player Windows, interfaccia IWMPSettings
- Interfaccia IWMPSettings Windows Media Player, proprietà baseURL
topic_type:
- apiref
api_name:
- IWMPSettings.baseURL
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 393575a93bf904f6fe312b13647ad5a7557b15bc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324362"
---
# <a name="iwmpsettingsbaseurl-property"></a><span data-ttu-id="01169-106">Proprietà IWMPSettings:: baseURL</span><span class="sxs-lookup"><span data-stu-id="01169-106">IWMPSettings::baseURL property</span></span>

<span data-ttu-id="01169-107">La proprietà **BaseUrl** Ottiene o imposta l'URL di base usato per la risoluzione del percorso relativo con i comandi script URL incorporati nel contenuto multimediale digitale.</span><span class="sxs-lookup"><span data-stu-id="01169-107">The **baseURL** property gets or sets the base URL used for relative path resolution with URL script commands that are embedded in digital media content.</span></span>

## <a name="syntax"></a><span data-ttu-id="01169-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="01169-108">Syntax</span></span>


```CSharp
public System.String baseURL {get; set;}
```


```VB

Public Property baseURL As System.String
```





## <a name="property-value"></a><span data-ttu-id="01169-109">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="01169-109">Property value</span></span>

<span data-ttu-id="01169-110">**System. String** che rappresenta l'URL di base.</span><span class="sxs-lookup"><span data-stu-id="01169-110">A **System.String** that is the base URL.</span></span>

## <a name="remarks"></a><span data-ttu-id="01169-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="01169-111">Remarks</span></span>

<span data-ttu-id="01169-112">Questa proprietà specifica l'URL HTTP di base che viene passato come parametro Command dall'evento **AxWindowsMediaPlayer \_ WMPOCXEvents \_ ScriptCommandEvent** .</span><span class="sxs-lookup"><span data-stu-id="01169-112">This property specifies the base HTTP URL that is passed as the command parameter by the **AxWindowsMediaPlayer\_WMPOCXEvents\_ScriptCommandEvent** event.</span></span> <span data-ttu-id="01169-113">L'URL di base viene concatenato all'URL relativo, come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="01169-113">The base URL is concatenated with the relative URL as follows:</span></span>

1.  <span data-ttu-id="01169-114">Viene aggiunta una barra (/) finale al valore recuperato dalla proprietà **BaseUrl** .</span><span class="sxs-lookup"><span data-stu-id="01169-114">A trailing forward slash (/) is added to the value retrieved by the **baseURL** property.</span></span>
2.  <span data-ttu-id="01169-115">Un punto principale, una barra rovesciata o un carattere barra rovesciata (., \\ e/) viene eliminato dall'URL relativo.</span><span class="sxs-lookup"><span data-stu-id="01169-115">A leading period, backward slash, or forward slash character (., \\, and /) is deleted from the relative URL.</span></span>
3.  <span data-ttu-id="01169-116">L'URL relativo viene aggiunto alla fine dell'URL di base.</span><span class="sxs-lookup"><span data-stu-id="01169-116">The relative URL is added to the end of the base URL.</span></span>
4.  <span data-ttu-id="01169-117">Tutti i caratteri della barra nell'URL completo risultante vengono puntati nella stessa direzione (convertiti in avanti o in barra rovesciata) in base alla direzione del primo carattere barra rilevato nel nuovo URL.</span><span class="sxs-lookup"><span data-stu-id="01169-117">All slash characters in the resulting fully qualified URL are pointed in the same direction (converted to forward or backward slashes) based on the direction of the first slash character encountered in the new URL.</span></span>

<span data-ttu-id="01169-118">**Nota**</span><span class="sxs-lookup"><span data-stu-id="01169-118">**Note**</span></span>

<span data-ttu-id="01169-119">Il controllo Media Player di Windows non supporta l'utilizzo di due punti (..) nell'URL relativo per indicare l'elemento padre della posizione corrente.</span><span class="sxs-lookup"><span data-stu-id="01169-119">The Windows Media Player control does not support the use of two periods (..) in the relative URL to indicate the parent of the current location.</span></span>

## <a name="requirements"></a><span data-ttu-id="01169-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="01169-120">Requirements</span></span>



| <span data-ttu-id="01169-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="01169-121">Requirement</span></span> | <span data-ttu-id="01169-122">Valore</span><span class="sxs-lookup"><span data-stu-id="01169-122">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="01169-123">Versione</span><span class="sxs-lookup"><span data-stu-id="01169-123">Version</span></span><br/>   | <span data-ttu-id="01169-124">Windows Media Player 9 serie o versione successiva</span><span class="sxs-lookup"><span data-stu-id="01169-124">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="01169-125">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="01169-125">Namespace</span></span><br/> | <span data-ttu-id="01169-126">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="01169-126">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="01169-127">Assembly</span><span class="sxs-lookup"><span data-stu-id="01169-127">Assembly</span></span><br/>  | <dl> <span data-ttu-id="01169-128"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="01169-128"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="01169-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="01169-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="01169-130">**Evento AxWindowsMediaPlayer. ScriptCommand (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="01169-130">**AxWindowsMediaPlayer.ScriptCommand Event (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-scriptcommand.md)
</dt> <dt>

[<span data-ttu-id="01169-131">**Interfaccia IWMPSettings (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="01169-131">**IWMPSettings Interface (VB and C#)**</span></span>](iwmpsettings--vb-and-c.md)
</dt> </dl>

 

 





