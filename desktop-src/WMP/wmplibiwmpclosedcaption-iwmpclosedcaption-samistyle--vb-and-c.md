---
title: Proprietà SAMIStyle di IWMPClosedCaption
description: La proprietà SAMIStyle Ottiene o imposta lo stile dei sottotitoli codificati.
ms.assetid: 0b1f92c6-b659-4ade-90c8-62a06e475f5c
keywords:
- Finestra delle proprietà di SAMIStyle Media Player
- Proprietà di SAMIStyle Media Player Windows, interfaccia IWMPClosedCaption
- Interfaccia IWMPClosedCaption Windows Media Player, proprietà SAMIStyle
topic_type:
- apiref
api_name:
- IWMPClosedCaption.SAMIStyle
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9bd0b48fc1807d6ca1854651c7f222183a845be3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332506"
---
# <a name="iwmpclosedcaptionsamistyle-property"></a><span data-ttu-id="8f56d-106">Proprietà IWMPClosedCaption:: SAMIStyle</span><span class="sxs-lookup"><span data-stu-id="8f56d-106">IWMPClosedCaption::SAMIStyle property</span></span>

<span data-ttu-id="8f56d-107">La proprietà **SAMIStyle** Ottiene o imposta lo stile dei sottotitoli codificati.</span><span class="sxs-lookup"><span data-stu-id="8f56d-107">The **SAMIStyle** property gets or sets the closed captioning style.</span></span>

## <a name="syntax"></a><span data-ttu-id="8f56d-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8f56d-108">Syntax</span></span>


```CSharp
public System.String SAMIStyle {get; set;}
```


```VB

Public Property SAMIStyle As System.String
```





## <a name="property-value"></a><span data-ttu-id="8f56d-109">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="8f56d-109">Property value</span></span>

<span data-ttu-id="8f56d-110">**System. String** che rappresenta il nome specificato nell'identificatore di stile di un file Sami.</span><span class="sxs-lookup"><span data-stu-id="8f56d-110">The **System.String** that is the name specified in the style identifier of a SAMI file.</span></span>

## <a name="remarks"></a><span data-ttu-id="8f56d-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="8f56d-111">Remarks</span></span>

<span data-ttu-id="8f56d-112">Un file SAMI può contenere diverse definizioni di stile del formato.</span><span class="sxs-lookup"><span data-stu-id="8f56d-112">A SAMI file can contain several format style definitions.</span></span> <span data-ttu-id="8f56d-113">Gli stili SAMI sono definiti tra i tag <STYLE> e </STYLE> nel file Sami.</span><span class="sxs-lookup"><span data-stu-id="8f56d-113">SAMI styles are defined between the <STYLE> and </STYLE> tags in the SAMI file.</span></span> <span data-ttu-id="8f56d-114">Uno stile viene definito con una stringa di testo preceduta da un \# carattere.</span><span class="sxs-lookup"><span data-stu-id="8f56d-114">A style is defined with a text string preceded by a \# character.</span></span> <span data-ttu-id="8f56d-115">Ad esempio:</span><span class="sxs-lookup"><span data-stu-id="8f56d-115">For example:</span></span>


```
#Emphasis1 {Name: Big Bold Italic; font-size: 14pt; text-align: center;
            color: blue; font-family: sans-serif; font-weight: bold;
            font-style: italic;}
```



<span data-ttu-id="8f56d-116">Specifica uno stile che produce un tipo di carattere specifico.</span><span class="sxs-lookup"><span data-stu-id="8f56d-116">This specifies a style that produces a particular font.</span></span>

<span data-ttu-id="8f56d-117">Se non viene specificato alcuno stile SAMI, per impostazione predefinita viene usato il primo stile definito nel file SAMI.</span><span class="sxs-lookup"><span data-stu-id="8f56d-117">If no SAMI style is specified, the first style defined in the SAMI file is used by default.</span></span>

## <a name="requirements"></a><span data-ttu-id="8f56d-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8f56d-118">Requirements</span></span>



| <span data-ttu-id="8f56d-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="8f56d-119">Requirement</span></span> | <span data-ttu-id="8f56d-120">Valore</span><span class="sxs-lookup"><span data-stu-id="8f56d-120">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8f56d-121">Versione</span><span class="sxs-lookup"><span data-stu-id="8f56d-121">Version</span></span><br/>   | <span data-ttu-id="8f56d-122">Windows Media Player 9 serie o versione successiva</span><span class="sxs-lookup"><span data-stu-id="8f56d-122">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="8f56d-123">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="8f56d-123">Namespace</span></span><br/> | <span data-ttu-id="8f56d-124">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="8f56d-124">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="8f56d-125">Assembly</span><span class="sxs-lookup"><span data-stu-id="8f56d-125">Assembly</span></span><br/>  | <dl> <span data-ttu-id="8f56d-126"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="8f56d-126"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8f56d-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8f56d-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8f56d-128">**Aggiunta di didascalie chiuse a file multimediali digitali**</span><span class="sxs-lookup"><span data-stu-id="8f56d-128">**Adding Closed Captions to Digital Media**</span></span>](adding-closed-captions-to-digital-media.md)
</dt> <dt>

[<span data-ttu-id="8f56d-129">**Interfaccia IWMPClosedCaption (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="8f56d-129">**IWMPClosedCaption Interface (VB and C#)**</span></span>](iwmpclosedcaption--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="8f56d-130">**Interfaccia IWMPClosedCaption2 (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="8f56d-130">**IWMPClosedCaption2 Interface (VB and C#)**</span></span>](iwmpclosedcaption2--vb-and-c.md)
</dt> </dl>

 

 





