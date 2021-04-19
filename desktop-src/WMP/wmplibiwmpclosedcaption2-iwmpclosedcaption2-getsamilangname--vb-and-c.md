---
title: Metodo IWMPClosedCaption2 getSAMILangName
description: Il metodo getSAMILangName restituisce il nome di una lingua supportata dal file SAMI corrente.
ms.assetid: 52aaf1cc-89ef-4c4c-af43-3f88dc4a9539
keywords:
- Metodo getSAMILangName Windows Media Player
- Metodo getSAMILangName Windows Media Player, interfaccia IWMPClosedCaption2
- Interfaccia IWMPClosedCaption2 Windows Media Player, metodo getSAMILangName
topic_type:
- apiref
api_name:
- IWMPClosedCaption2.getSAMILangName
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e50df643fdd6b665de1275873fb8de9d5d094a42
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332495"
---
# <a name="iwmpclosedcaption2getsamilangname-method"></a><span data-ttu-id="37a71-106">Metodo IWMPClosedCaption2:: getSAMILangName</span><span class="sxs-lookup"><span data-stu-id="37a71-106">IWMPClosedCaption2::getSAMILangName method</span></span>

<span data-ttu-id="37a71-107">Il metodo **getSAMILangName** restituisce il nome di una lingua supportata dal file Sami corrente.</span><span class="sxs-lookup"><span data-stu-id="37a71-107">The **getSAMILangName** method returns the name of a language supported by the current SAMI file.</span></span>

## <a name="syntax"></a><span data-ttu-id="37a71-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="37a71-108">Syntax</span></span>


```CSharp
public System.String getSAMILangName(
  System.Int32 nIndex
);
```


```VB

Public Function getSAMILangName( _
  ByVal nIndex As System.Int32 _
) As System.String
Implements IWMPClosedCaption2.getSAMILangName
```





## <a name="parameters"></a><span data-ttu-id="37a71-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="37a71-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="37a71-110">*nIndex* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="37a71-110">*nIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="37a71-111">**System. Int32** che rappresenta l'indice in base zero del nome del linguaggio da recuperare.</span><span class="sxs-lookup"><span data-stu-id="37a71-111">**A System.Int32** that is the zero-based index of the language name to retrieve.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="37a71-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="37a71-112">Return value</span></span>

<span data-ttu-id="37a71-113">**System. String** che rappresenta il nome del linguaggio come specificato nel file Sami.</span><span class="sxs-lookup"><span data-stu-id="37a71-113">A **System.String** that is the name of the language as specified in the SAMI file.</span></span>

## <a name="remarks"></a><span data-ttu-id="37a71-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="37a71-114">Remarks</span></span>

<span data-ttu-id="37a71-115">Le lingue in un file SAMI sono indicizzate nell'ordine indicato nel file, a partire da zero.</span><span class="sxs-lookup"><span data-stu-id="37a71-115">The languages in a SAMI file are indexed in the order shown in the file, starting with zero.</span></span>

<span data-ttu-id="37a71-116">Questo metodo restituisce una stringa di lunghezza zero (""), a meno che non sia aperto un file multimediale digitale (AxWindowsMediaPlayer. openState è uguale a 13).</span><span class="sxs-lookup"><span data-stu-id="37a71-116">This method returns a zero-length string ("") unless a digital media file is open (AxWindowsMediaPlayer.openState is equal to 13).</span></span>

## <a name="requirements"></a><span data-ttu-id="37a71-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="37a71-117">Requirements</span></span>



| <span data-ttu-id="37a71-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="37a71-118">Requirement</span></span> | <span data-ttu-id="37a71-119">Valore</span><span class="sxs-lookup"><span data-stu-id="37a71-119">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="37a71-120">Versione</span><span class="sxs-lookup"><span data-stu-id="37a71-120">Version</span></span><br/>   | <span data-ttu-id="37a71-121">Windows Media Player 9 serie o versione successiva</span><span class="sxs-lookup"><span data-stu-id="37a71-121">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="37a71-122">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="37a71-122">Namespace</span></span><br/> | <span data-ttu-id="37a71-123">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="37a71-123">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="37a71-124">Assembly</span><span class="sxs-lookup"><span data-stu-id="37a71-124">Assembly</span></span><br/>  | <dl> <span data-ttu-id="37a71-125"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="37a71-125"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="37a71-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="37a71-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="37a71-127">**Aggiunta di didascalie chiuse a file multimediali digitali**</span><span class="sxs-lookup"><span data-stu-id="37a71-127">**Adding Closed Captions to Digital Media**</span></span>](adding-closed-captions-to-digital-media.md)
</dt> <dt>

[<span data-ttu-id="37a71-128">**Interfaccia IWMPClosedCaption (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="37a71-128">**IWMPClosedCaption Interface (VB and C#)**</span></span>](iwmpclosedcaption--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="37a71-129">**IWMPClosedCaption. SAMILang (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="37a71-129">**IWMPClosedCaption.SAMILang (VB and C#)**</span></span>](wmplibiwmpclosedcaption-iwmpclosedcaption-samilang--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="37a71-130">**Interfaccia IWMPClosedCaption2 (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="37a71-130">**IWMPClosedCaption2 Interface (VB and C#)**</span></span>](iwmpclosedcaption2--vb-and-c.md)
</dt> </dl>

 

 





