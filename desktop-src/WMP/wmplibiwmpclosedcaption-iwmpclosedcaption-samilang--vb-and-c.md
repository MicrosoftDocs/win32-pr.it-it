---
title: Proprietà SAMILang di IWMPClosedCaption
description: La proprietà SAMILang Ottiene o imposta la lingua visualizzata per la didascalia chiusa.
ms.assetid: dcdd6bcd-b869-439f-b500-df26d3873b04
keywords:
- Finestra delle proprietà di SAMILang Media Player
- Proprietà di SAMILang Media Player Windows, interfaccia IWMPClosedCaption
- Interfaccia IWMPClosedCaption Windows Media Player, proprietà SAMILang
topic_type:
- apiref
api_name:
- IWMPClosedCaption.SAMILang
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe29defa3736795c88613ee7ab2ef11a914a3f80
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332507"
---
# <a name="iwmpclosedcaptionsamilang-property"></a><span data-ttu-id="8a6bb-106">Proprietà IWMPClosedCaption:: SAMILang</span><span class="sxs-lookup"><span data-stu-id="8a6bb-106">IWMPClosedCaption::SAMILang property</span></span>

<span data-ttu-id="8a6bb-107">La proprietà **SAMILang** Ottiene o imposta la lingua visualizzata per la didascalia chiusa.</span><span class="sxs-lookup"><span data-stu-id="8a6bb-107">The **SAMILang** property gets or sets the language displayed for closed captioning.</span></span>

## <a name="syntax"></a><span data-ttu-id="8a6bb-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8a6bb-108">Syntax</span></span>


```CSharp
public System.String SAMILang {get; set;}
```


```VB

Public Property SAMILang As System.String
```





## <a name="property-value"></a><span data-ttu-id="8a6bb-109">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="8a6bb-109">Property value</span></span>

<span data-ttu-id="8a6bb-110">**System. String** che rappresenta il nome specificato nell'identificatore di lingua di un file Sami.</span><span class="sxs-lookup"><span data-stu-id="8a6bb-110">The **System.String** that is the name specified in the language identifier of a SAMI file.</span></span>

## <a name="remarks"></a><span data-ttu-id="8a6bb-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="8a6bb-111">Remarks</span></span>

<span data-ttu-id="8a6bb-112">Un file SAMI può contenere testo per una o più lingue.</span><span class="sxs-lookup"><span data-stu-id="8a6bb-112">A SAMI file can contain text for one or many languages.</span></span> <span data-ttu-id="8a6bb-113">Le lingue disponibili per la didascalia chiusa sono definite tra i tag <STYLE> e </STYLE> nel file Sami.</span><span class="sxs-lookup"><span data-stu-id="8a6bb-113">The languages available for closed captioning are defined between the <STYLE> and </STYLE> tags in the SAMI file.</span></span> <span data-ttu-id="8a6bb-114">Un identificatore di lingua viene specificato con una stringa alfanumerica univoca preceduta da un punto (.).</span><span class="sxs-lookup"><span data-stu-id="8a6bb-114">A language identifier is specified with a unique alphanumeric string that is preceded by a period (.).</span></span> <span data-ttu-id="8a6bb-115">Il nome specificato per una lingua può essere qualsiasi stringa.</span><span class="sxs-lookup"><span data-stu-id="8a6bb-115">The name specified for a language can be any string.</span></span> <span data-ttu-id="8a6bb-116">È ad esempio possibile utilizzare il codice seguente per definire l'inglese (Stati Uniti):</span><span class="sxs-lookup"><span data-stu-id="8a6bb-116">For example, the following could be used to define US English:</span></span>


```
.ENUSCC {Name:'English Captions' lang: en-US; SAMIType:CC;}
```



<span data-ttu-id="8a6bb-117">Se non si specifica alcun linguaggio SAMI, per impostazione predefinita viene usata la prima lingua definita nel file SAMI.</span><span class="sxs-lookup"><span data-stu-id="8a6bb-117">If no SAMI language is specified, the first language defined in the SAMI file is used by default.</span></span>

<span data-ttu-id="8a6bb-118">La stringa impostata utilizzando **SAMILang** deve corrispondere all'attributo **Name** nell'identificatore di linguaggio.</span><span class="sxs-lookup"><span data-stu-id="8a6bb-118">The string you set using **SAMILang** must match the **Name** attribute in the language specifier.</span></span>

## <a name="requirements"></a><span data-ttu-id="8a6bb-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8a6bb-119">Requirements</span></span>



| <span data-ttu-id="8a6bb-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="8a6bb-120">Requirement</span></span> | <span data-ttu-id="8a6bb-121">Valore</span><span class="sxs-lookup"><span data-stu-id="8a6bb-121">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8a6bb-122">Versione</span><span class="sxs-lookup"><span data-stu-id="8a6bb-122">Version</span></span><br/>   | <span data-ttu-id="8a6bb-123">Windows Media Player 9 serie o versione successiva</span><span class="sxs-lookup"><span data-stu-id="8a6bb-123">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="8a6bb-124">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="8a6bb-124">Namespace</span></span><br/> | <span data-ttu-id="8a6bb-125">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="8a6bb-125">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="8a6bb-126">Assembly</span><span class="sxs-lookup"><span data-stu-id="8a6bb-126">Assembly</span></span><br/>  | <dl> <span data-ttu-id="8a6bb-127"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="8a6bb-127"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8a6bb-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8a6bb-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8a6bb-129">**Aggiunta di didascalie chiuse a file multimediali digitali**</span><span class="sxs-lookup"><span data-stu-id="8a6bb-129">**Adding Closed Captions to Digital Media**</span></span>](adding-closed-captions-to-digital-media.md)
</dt> <dt>

[<span data-ttu-id="8a6bb-130">**Interfaccia IWMPClosedCaption (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="8a6bb-130">**IWMPClosedCaption Interface (VB and C#)**</span></span>](iwmpclosedcaption--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="8a6bb-131">**Interfaccia IWMPClosedCaption2 (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="8a6bb-131">**IWMPClosedCaption2 Interface (VB and C#)**</span></span>](iwmpclosedcaption2--vb-and-c.md)
</dt> </dl>

 

 





