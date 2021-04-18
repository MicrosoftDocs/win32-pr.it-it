---
title: Proprietà SAMIFileName di IWMPClosedCaption
description: La proprietà SAMIFileName Ottiene o imposta il nome di un file contenente le informazioni necessarie per la didascalia chiusa.
ms.assetid: c3162c5f-9d66-41d4-920c-ed9840742d9d
keywords:
- Finestra delle proprietà di SAMIFileName Media Player
- Proprietà di SAMIFileName Media Player Windows, interfaccia IWMPClosedCaption
- Interfaccia IWMPClosedCaption Windows Media Player, proprietà SAMIFileName
topic_type:
- apiref
api_name:
- IWMPClosedCaption.SAMIFileName
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d251f2bbf0c8839ab9a0005c69e1869c47af16ef
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329283"
---
# <a name="iwmpclosedcaptionsamifilename-property"></a><span data-ttu-id="06283-106">Proprietà IWMPClosedCaption:: SAMIFileName</span><span class="sxs-lookup"><span data-stu-id="06283-106">IWMPClosedCaption::SAMIFileName property</span></span>

<span data-ttu-id="06283-107">La proprietà **SAMIFileName** Ottiene o imposta il nome di un file contenente le informazioni necessarie per la didascalia chiusa.</span><span class="sxs-lookup"><span data-stu-id="06283-107">The **SAMIFileName** property gets or sets the name of a file containing the information needed for closed captioning.</span></span>

## <a name="syntax"></a><span data-ttu-id="06283-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="06283-108">Syntax</span></span>


```CSharp
public System.String SAMIFileName {get; set;}
```


```VB

Public Property SAMIFileName As System.String
```





## <a name="property-value"></a><span data-ttu-id="06283-109">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="06283-109">Property value</span></span>

<span data-ttu-id="06283-110">**System. String** che rappresenta il nome del file di Media Interchange accessibile sincronizzato (Sami).</span><span class="sxs-lookup"><span data-stu-id="06283-110">The **System.String** that is the name of the Synchronized Accessible Media Interchange (SAMI) file.</span></span>

## <a name="remarks"></a><span data-ttu-id="06283-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="06283-111">Remarks</span></span>

<span data-ttu-id="06283-112">Il file SAMI deve usare un'estensione del nome file. SMI o. Sami.</span><span class="sxs-lookup"><span data-stu-id="06283-112">The SAMI file must use an .smi or .sami file name extension.</span></span>

<span data-ttu-id="06283-113">Se non si imposta un valore utilizzando **SAMIFileName**, questa proprietà ottiene una **stringa** contenente il nome file o l'URL predefinito associato all'elemento multimediale corrente.</span><span class="sxs-lookup"><span data-stu-id="06283-113">If you do not set a value using **SAMIFileName**, this property gets a **string** containing the default file name or URL associated with the current media item.</span></span> <span data-ttu-id="06283-114">Questa associazione può verificarsi quando un file SAMI viene specificato tramite il parametro dell'URL *Sami* oppure automaticamente quando il file Sami ha lo stesso nome del file multimediale digitale, ad eccezione dell'estensione del nome file.</span><span class="sxs-lookup"><span data-stu-id="06283-114">This association can occur when a SAMI file is specified by using the *sami* URL parameter, or automatically when the SAMI file has the same name as the digital media file (except for the file name extension).</span></span> <span data-ttu-id="06283-115">Se al supporto corrente non è associato alcun file SAMI predefinito, questa proprietà ottiene una stringa di lunghezza zero ("").</span><span class="sxs-lookup"><span data-stu-id="06283-115">If there is no default SAMI file associated with the current media, this property gets a zero-length string ("").</span></span>

<span data-ttu-id="06283-116">Quando si imposta un valore usando **SAMIFileName**, tale valore viene mantenuto fino a quando non si imposta un nuovo valore (o fino a quando non viene aperto un nuovo elemento multimediale usando il parametro dell'URL Sami).</span><span class="sxs-lookup"><span data-stu-id="06283-116">Once you set a value using **SAMIFileName**, that value persists until you set a new value (or until a new media item is opened using the sami URL parameter).</span></span> <span data-ttu-id="06283-117">Pertanto, è necessario impostare un nuovo valore per questa proprietà prima di riprodurre ogni nuovo elemento multimediale.</span><span class="sxs-lookup"><span data-stu-id="06283-117">Therefore, you must set a new value for this property before you play each new media item.</span></span> <span data-ttu-id="06283-118">In questo modo, il nuovo valore di **SAMIFileName** verrà applicato quando viene aperto il successivo elemento multimediale (o quando viene chiamato **AxWindowsMediaPlayer. Close** ).</span><span class="sxs-lookup"><span data-stu-id="06283-118">That way, the new value for **SAMIFileName** will take effect when the next media item is opened (or when **AxWindowsMediaPlayer.close** is called).</span></span> <span data-ttu-id="06283-119">La specifica di un nuovo valore per **SAMIFileName** non ha alcun effetto sui supporti correnti.</span><span class="sxs-lookup"><span data-stu-id="06283-119">Specifying a new value for **SAMIFileName** has no effect for the current media.</span></span>

<span data-ttu-id="06283-120">Per fare in modo che Windows Media Player usi il file SAMI predefinito associato a un particolare elemento multimediale, impostare **SAMIFileName** su una stringa di lunghezza zero ("") prima di riprodurre il successivo elemento multimediale.</span><span class="sxs-lookup"><span data-stu-id="06283-120">To cause Windows Media Player to use the default SAMI file associated with a particular media item, set **SAMIFileName** to a zero-length string ("") before you play the next media item.</span></span>

## <a name="requirements"></a><span data-ttu-id="06283-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="06283-121">Requirements</span></span>



| <span data-ttu-id="06283-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="06283-122">Requirement</span></span> | <span data-ttu-id="06283-123">Valore</span><span class="sxs-lookup"><span data-stu-id="06283-123">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="06283-124">Versione</span><span class="sxs-lookup"><span data-stu-id="06283-124">Version</span></span><br/>   | <span data-ttu-id="06283-125">Windows Media Player 9 serie o versione successiva</span><span class="sxs-lookup"><span data-stu-id="06283-125">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="06283-126">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="06283-126">Namespace</span></span><br/> | <span data-ttu-id="06283-127">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="06283-127">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="06283-128">Assembly</span><span class="sxs-lookup"><span data-stu-id="06283-128">Assembly</span></span><br/>  | <dl> <span data-ttu-id="06283-129"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="06283-129"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="06283-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="06283-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="06283-131">**Aggiunta di didascalie chiuse a file multimediali digitali**</span><span class="sxs-lookup"><span data-stu-id="06283-131">**Adding Closed Captions to Digital Media**</span></span>](adding-closed-captions-to-digital-media.md)
</dt> <dt>

[<span data-ttu-id="06283-132">**AxWindowsMediaPlayer. Close**</span><span class="sxs-lookup"><span data-stu-id="06283-132">**AxWindowsMediaPlayer.close**</span></span>](axwmplib-axwindowsmediaplayer-close.md)
</dt> <dt>

[<span data-ttu-id="06283-133">**Interfaccia IWMPClosedCaption (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="06283-133">**IWMPClosedCaption Interface (VB and C#)**</span></span>](iwmpclosedcaption--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="06283-134">**Interfaccia IWMPClosedCaption2 (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="06283-134">**IWMPClosedCaption2 Interface (VB and C#)**</span></span>](iwmpclosedcaption2--vb-and-c.md)
</dt> </dl>

 

 





