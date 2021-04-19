---
title: Metodo IWMPClosedCaption2 getSAMIStyleName
description: Il metodo getSAMIStyleName restituisce il nome di uno stile supportato dal file SAMI corrente.
ms.assetid: e7678ca6-f52f-45f4-bd1c-7fbcdf1cc47c
keywords:
- Metodo getSAMIStyleName Windows Media Player
- Metodo getSAMIStyleName Windows Media Player, interfaccia IWMPClosedCaption2
- Interfaccia IWMPClosedCaption2 Windows Media Player, metodo getSAMIStyleName
topic_type:
- apiref
api_name:
- IWMPClosedCaption2.getSAMIStyleName
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 34ceb3f598ae603d478af5cad9c78333952530a2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332494"
---
# <a name="iwmpclosedcaption2getsamistylename-method"></a><span data-ttu-id="726b8-106">Metodo IWMPClosedCaption2:: getSAMIStyleName</span><span class="sxs-lookup"><span data-stu-id="726b8-106">IWMPClosedCaption2::getSAMIStyleName method</span></span>

<span data-ttu-id="726b8-107">Il metodo **getSAMIStyleName** restituisce il nome di uno stile supportato dal file Sami corrente.</span><span class="sxs-lookup"><span data-stu-id="726b8-107">The **getSAMIStyleName** method returns the name of a style supported by the current SAMI file.</span></span>

## <a name="syntax"></a><span data-ttu-id="726b8-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="726b8-108">Syntax</span></span>


```CSharp
public System.String getSAMIStyleName(
  System.Int32 nIndex
);
```


```VB

Public Function getSAMIStyleName( _
  ByVal nIndex As System.Int32 _
) As System.String
Implements IWMPClosedCaption2.getSAMIStyleName
```





## <a name="parameters"></a><span data-ttu-id="726b8-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="726b8-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="726b8-110">*nIndex* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="726b8-110">*nIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="726b8-111">**System. Int32** che rappresenta l'indice in base zero del nome dello stile da recuperare.</span><span class="sxs-lookup"><span data-stu-id="726b8-111">A **System.Int32** that is the zero-based index of the style name to retrieve</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="726b8-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="726b8-112">Return value</span></span>

<span data-ttu-id="726b8-113">**System. String** che rappresenta il nome dello stile specificato nel file Sami.</span><span class="sxs-lookup"><span data-stu-id="726b8-113">A **System.String** that is the name of the style as specified in the SAMI file.</span></span>

## <a name="remarks"></a><span data-ttu-id="726b8-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="726b8-114">Remarks</span></span>

<span data-ttu-id="726b8-115">Gli stili in un file SAMI vengono indicizzati nell'ordine indicato nel file, a partire da zero.</span><span class="sxs-lookup"><span data-stu-id="726b8-115">The styles in a SAMI file are indexed in the order shown in the file, starting with zero.</span></span>

<span data-ttu-id="726b8-116">Questo metodo restituisce una stringa di lunghezza zero (""), a meno che non sia aperto un file multimediale digitale (AxWindowsMediaPlayer. openState è uguale a 13).</span><span class="sxs-lookup"><span data-stu-id="726b8-116">This method returns a zero-length string ("") unless a digital media file is open (AxWindowsMediaPlayer.openState is equal to 13).</span></span>

## <a name="requirements"></a><span data-ttu-id="726b8-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="726b8-117">Requirements</span></span>



| <span data-ttu-id="726b8-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="726b8-118">Requirement</span></span> | <span data-ttu-id="726b8-119">Valore</span><span class="sxs-lookup"><span data-stu-id="726b8-119">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="726b8-120">Versione</span><span class="sxs-lookup"><span data-stu-id="726b8-120">Version</span></span><br/>   | <span data-ttu-id="726b8-121">Windows Media Player 9 serie o versione successiva</span><span class="sxs-lookup"><span data-stu-id="726b8-121">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="726b8-122">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="726b8-122">Namespace</span></span><br/> | <span data-ttu-id="726b8-123">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="726b8-123">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="726b8-124">Assembly</span><span class="sxs-lookup"><span data-stu-id="726b8-124">Assembly</span></span><br/>  | <dl> <span data-ttu-id="726b8-125"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="726b8-125"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="726b8-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="726b8-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="726b8-127">**Aggiunta di didascalie chiuse a file multimediali digitali**</span><span class="sxs-lookup"><span data-stu-id="726b8-127">**Adding Closed Captions to Digital Media**</span></span>](adding-closed-captions-to-digital-media.md)
</dt> <dt>

[<span data-ttu-id="726b8-128">**Interfaccia IWMPClosedCaption (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="726b8-128">**IWMPClosedCaption Interface (VB and C#)**</span></span>](iwmpclosedcaption--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="726b8-129">**IWMPClosedCaption. SAMIStyle (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="726b8-129">**IWMPClosedCaption.SAMIStyle (VB and C#)**</span></span>](wmplibiwmpclosedcaption-iwmpclosedcaption-samistyle--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="726b8-130">**Interfaccia IWMPClosedCaption2 (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="726b8-130">**IWMPClosedCaption2 Interface (VB and C#)**</span></span>](iwmpclosedcaption2--vb-and-c.md)
</dt> </dl>

 

 





