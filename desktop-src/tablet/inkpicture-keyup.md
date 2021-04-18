---
description: Si verifica quando viene rilasciato un tasto mentre il controllo InkPicture dispone dello stato attivo.
ms.assetid: e22633b5-40fe-4b94-a660-684c4f5c96f3
title: Evento InkPicture. KeyUp (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c2390b6cbb7b91ab8e447df912e591ea37248e9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314924"
---
# <a name="inkpicturekeyup-event"></a><span data-ttu-id="f5a29-103">Evento InkPicture. KeyUp</span><span class="sxs-lookup"><span data-stu-id="f5a29-103">InkPicture.KeyUp event</span></span>

<span data-ttu-id="f5a29-104">Si verifica quando viene rilasciato un tasto mentre il controllo [InkPicture](inkpicture-control-reference.md) dispone dello stato attivo.</span><span class="sxs-lookup"><span data-stu-id="f5a29-104">Occurs when a key is released while the [InkPicture](inkpicture-control-reference.md) control has focus.</span></span>

## <a name="syntax"></a><span data-ttu-id="f5a29-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f5a29-105">Syntax</span></span>


```C++
void KeyUp(
  [in, out] short *KeyCode,
  [in, out] short *Shift
);
```



## <a name="parameters"></a><span data-ttu-id="f5a29-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="f5a29-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f5a29-107">*Codice* \[ di stato in uscita\]</span><span class="sxs-lookup"><span data-stu-id="f5a29-107">*KeyCode* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="f5a29-108">Valore ASCII della chiave da premere.</span><span class="sxs-lookup"><span data-stu-id="f5a29-108">The ASCII value of the key that is being pressed.</span></span>

</dd> <dt>

<span data-ttu-id="f5a29-109">*Sposta* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="f5a29-109">*Shift* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="f5a29-110">Stato del tasto MAIUSC.</span><span class="sxs-lookup"><span data-stu-id="f5a29-110">The state of the SHIFT key.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f5a29-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f5a29-111">Return value</span></span>

<span data-ttu-id="f5a29-112">Questo evento non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="f5a29-112">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f5a29-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="f5a29-113">Remarks</span></span>

<span data-ttu-id="f5a29-114">Questo metodo di evento è definito nell'interfaccia **\_ IInkPictureEvents** .</span><span class="sxs-lookup"><span data-stu-id="f5a29-114">This event method is defined in the **\_IInkPictureEvents** interface.</span></span> <span data-ttu-id="f5a29-115">L'interfaccia **\_ IInkPictureEvents** implementa l'interfaccia [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) con un identificatore di DISPID \_ IPEKeyUp.</span><span class="sxs-lookup"><span data-stu-id="f5a29-115">The **\_IInkPictureEvents** interface implements the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface with an identifier of DISPID\_IPEKeyUp.</span></span>

## <a name="requirements"></a><span data-ttu-id="f5a29-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f5a29-116">Requirements</span></span>



| <span data-ttu-id="f5a29-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="f5a29-117">Requirement</span></span> | <span data-ttu-id="f5a29-118">Valore</span><span class="sxs-lookup"><span data-stu-id="f5a29-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f5a29-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f5a29-119">Minimum supported client</span></span><br/> | <span data-ttu-id="f5a29-120">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="f5a29-120">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="f5a29-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f5a29-121">Minimum supported server</span></span><br/> | <span data-ttu-id="f5a29-122">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="f5a29-122">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="f5a29-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f5a29-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="f5a29-124"><dt>Msinkaut. h (richiede anche Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="f5a29-124"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="f5a29-125">Libreria</span><span class="sxs-lookup"><span data-stu-id="f5a29-125">Library</span></span><br/>                  | <dl> <span data-ttu-id="f5a29-126"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f5a29-126"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="f5a29-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f5a29-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f5a29-128">InkPicture</span><span class="sxs-lookup"><span data-stu-id="f5a29-128">InkPicture</span></span>](inkpicture-control-reference.md)
</dt> </dl>

 

