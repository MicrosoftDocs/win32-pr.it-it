---
title: Metodo IWMPClosedCaption2 getSAMILangID
description: Il metodo getSAMILangID restituisce l'identificatore delle impostazioni locali (LCID) di una lingua supportata dal file SAMI corrente.
ms.assetid: 41aca317-6182-47c3-8bd9-ba42b92b10f4
keywords:
- Metodo getSAMILangID Windows Media Player
- Metodo getSAMILangID Windows Media Player, interfaccia IWMPClosedCaption2
- Interfaccia IWMPClosedCaption2 Windows Media Player, metodo getSAMILangID
topic_type:
- apiref
api_name:
- IWMPClosedCaption2.getSAMILangID
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb9aaebecf8e86c056fa9c91141042facc6bcc18
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332502"
---
# <a name="iwmpclosedcaption2getsamilangid-method"></a><span data-ttu-id="9ed7d-106">Metodo IWMPClosedCaption2:: getSAMILangID</span><span class="sxs-lookup"><span data-stu-id="9ed7d-106">IWMPClosedCaption2::getSAMILangID method</span></span>

<span data-ttu-id="9ed7d-107">Il metodo **getSAMILangID** restituisce l'identificatore delle impostazioni locali (LCID) di una lingua supportata dal file Sami corrente.</span><span class="sxs-lookup"><span data-stu-id="9ed7d-107">The **getSAMILangID** method returns the locale identifier (LCID) of a language supported by the current SAMI file.</span></span>

## <a name="syntax"></a><span data-ttu-id="9ed7d-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9ed7d-108">Syntax</span></span>


```CSharp
public System.Int32 getSAMILangID(
  System.Int32 nIndex
);
```


```VB

Public Function getSAMILangID( _
  ByVal nIndex As System.Int32 _
) As System.Int32
Implements IWMPClosedCaption2.getSAMILangID
```





## <a name="parameters"></a><span data-ttu-id="9ed7d-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="9ed7d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9ed7d-110">*nIndex* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9ed7d-110">*nIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9ed7d-111">**System. Int32** che rappresenta l'indice in base zero dell'LCID da recuperare.</span><span class="sxs-lookup"><span data-stu-id="9ed7d-111">A **System.Int32** that is the zero-based index of the LCID to retrieve.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9ed7d-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="9ed7d-112">Return value</span></span>

<span data-ttu-id="9ed7d-113">**System. Int32** che rappresenta l'identificatore LCID della lingua con l'indice specificato.</span><span class="sxs-lookup"><span data-stu-id="9ed7d-113">A **System.Int32** that is the LCID of the language with the specified index.</span></span>

## <a name="remarks"></a><span data-ttu-id="9ed7d-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="9ed7d-114">Remarks</span></span>

<span data-ttu-id="9ed7d-115">Le lingue in un file SAMI sono indicizzate nell'ordine indicato nel file, a partire da zero.</span><span class="sxs-lookup"><span data-stu-id="9ed7d-115">The languages in a SAMI file are indexed in the order shown in the file, starting with zero.</span></span>

<span data-ttu-id="9ed7d-116">Questo metodo restituisce 0, a meno che non sia aperto un file multimediale digitale (AxWindowsMediaPlayer. openState è uguale a 13).</span><span class="sxs-lookup"><span data-stu-id="9ed7d-116">This method returns 0 unless a digital media file is open (AxWindowsMediaPlayer.openState is equal to 13).</span></span>

## <a name="requirements"></a><span data-ttu-id="9ed7d-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9ed7d-117">Requirements</span></span>



| <span data-ttu-id="9ed7d-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="9ed7d-118">Requirement</span></span> | <span data-ttu-id="9ed7d-119">Valore</span><span class="sxs-lookup"><span data-stu-id="9ed7d-119">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9ed7d-120">Versione</span><span class="sxs-lookup"><span data-stu-id="9ed7d-120">Version</span></span><br/>   | <span data-ttu-id="9ed7d-121">Windows Media Player 9 serie o versione successiva</span><span class="sxs-lookup"><span data-stu-id="9ed7d-121">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="9ed7d-122">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="9ed7d-122">Namespace</span></span><br/> | <span data-ttu-id="9ed7d-123">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="9ed7d-123">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="9ed7d-124">Assembly</span><span class="sxs-lookup"><span data-stu-id="9ed7d-124">Assembly</span></span><br/>  | <dl> <span data-ttu-id="9ed7d-125"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="9ed7d-125"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9ed7d-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9ed7d-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9ed7d-127">**Aggiunta di didascalie chiuse a file multimediali digitali**</span><span class="sxs-lookup"><span data-stu-id="9ed7d-127">**Adding Closed Captions to Digital Media**</span></span>](adding-closed-captions-to-digital-media.md)
</dt> <dt>

[<span data-ttu-id="9ed7d-128">**Interfaccia IWMPClosedCaption (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="9ed7d-128">**IWMPClosedCaption Interface (VB and C#)**</span></span>](iwmpclosedcaption--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="9ed7d-129">**Interfaccia IWMPClosedCaption2 (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="9ed7d-129">**IWMPClosedCaption2 Interface (VB and C#)**</span></span>](iwmpclosedcaption2--vb-and-c.md)
</dt> </dl>

 

 





