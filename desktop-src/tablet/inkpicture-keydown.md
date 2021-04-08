---
description: Si verifica quando viene premuto un tasto e nella posizione in giù mentre il controllo InkPicture dispone dello stato attivo.
ms.assetid: d83823ea-d863-4eb7-8f6b-fa7a3396e64b
title: Evento InkPicture. KeyDown (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b5d6bd3555aeec98ac28555c1674dfef32ecc53
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104058334"
---
# <a name="inkpicturekeydown-event"></a><span data-ttu-id="cb9b1-103">Evento InkPicture. KeyDown</span><span class="sxs-lookup"><span data-stu-id="cb9b1-103">InkPicture.KeyDown event</span></span>

<span data-ttu-id="cb9b1-104">Si verifica quando viene premuto un tasto e nella posizione in giù mentre il controllo [InkPicture](inkpicture-control-reference.md) dispone dello stato attivo.</span><span class="sxs-lookup"><span data-stu-id="cb9b1-104">Occurs when a key is pressed and in the down position while the [InkPicture](inkpicture-control-reference.md) control has focus.</span></span>

## <a name="syntax"></a><span data-ttu-id="cb9b1-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="cb9b1-105">Syntax</span></span>


```C++
void KeyDown(
  [in, out] short *KeyCode,
  [in, out] short *Shift
);
```



## <a name="parameters"></a><span data-ttu-id="cb9b1-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="cb9b1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cb9b1-107">*Codice* \[ di stato in uscita\]</span><span class="sxs-lookup"><span data-stu-id="cb9b1-107">*KeyCode* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="cb9b1-108">Valore ASCII della chiave da premere.</span><span class="sxs-lookup"><span data-stu-id="cb9b1-108">The ASCII value of the key that is being pressed.</span></span>

</dd> <dt>

<span data-ttu-id="cb9b1-109">*Sposta* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="cb9b1-109">*Shift* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="cb9b1-110">Stato del tasto MAIUSC.</span><span class="sxs-lookup"><span data-stu-id="cb9b1-110">The state of the SHIFT key.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cb9b1-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="cb9b1-111">Return value</span></span>

<span data-ttu-id="cb9b1-112">Questo evento non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="cb9b1-112">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="cb9b1-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="cb9b1-113">Remarks</span></span>

<span data-ttu-id="cb9b1-114">Questo metodo di evento è definito nell'interfaccia **\_ IInkPictureEvents** .</span><span class="sxs-lookup"><span data-stu-id="cb9b1-114">This event method is defined in the **\_IInkPictureEvents** interface.</span></span> <span data-ttu-id="cb9b1-115">L'interfaccia **\_ IInkPictureEvents** implementa l'interfaccia [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) con un identificatore di DISPID \_ IPEKeyDown.</span><span class="sxs-lookup"><span data-stu-id="cb9b1-115">The **\_IInkPictureEvents** interface implements the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface with an identifier of DISPID\_IPEKeyDown.</span></span>

## <a name="requirements"></a><span data-ttu-id="cb9b1-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="cb9b1-116">Requirements</span></span>



| <span data-ttu-id="cb9b1-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="cb9b1-117">Requirement</span></span> | <span data-ttu-id="cb9b1-118">Valore</span><span class="sxs-lookup"><span data-stu-id="cb9b1-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cb9b1-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cb9b1-119">Minimum supported client</span></span><br/> | <span data-ttu-id="cb9b1-120">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="cb9b1-120">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="cb9b1-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cb9b1-121">Minimum supported server</span></span><br/> | <span data-ttu-id="cb9b1-122">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="cb9b1-122">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="cb9b1-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="cb9b1-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="cb9b1-124"><dt>Msinkaut. h (richiede anche Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="cb9b1-124"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="cb9b1-125">Libreria</span><span class="sxs-lookup"><span data-stu-id="cb9b1-125">Library</span></span><br/>                  | <dl> <span data-ttu-id="cb9b1-126"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cb9b1-126"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="cb9b1-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="cb9b1-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cb9b1-128">InkPicture</span><span class="sxs-lookup"><span data-stu-id="cb9b1-128">InkPicture</span></span>](inkpicture-control-reference.md)
</dt> </dl>

 

