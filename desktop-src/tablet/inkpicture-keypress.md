---
description: Si verifica quando viene premuto un tasto mentre il controllo InkPicture dispone dello stato attivo.
ms.assetid: adb61eff-a92c-40b0-940c-02e14cd34e5f
title: Evento InkPicture. KeyPress (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 35f9ef48a0e117d6a3d4c29a9ca69aba3bf6e054
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966796"
---
# <a name="inkpicturekeypress-event"></a><span data-ttu-id="85de9-103">Evento InkPicture. KeyPress</span><span class="sxs-lookup"><span data-stu-id="85de9-103">InkPicture.KeyPress event</span></span>

<span data-ttu-id="85de9-104">Si verifica quando viene premuto un tasto mentre il controllo [InkPicture](inkpicture-control-reference.md) dispone dello stato attivo.</span><span class="sxs-lookup"><span data-stu-id="85de9-104">Occurs when a key is pressed while the [InkPicture](inkpicture-control-reference.md) control has focus.</span></span>

## <a name="syntax"></a><span data-ttu-id="85de9-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="85de9-105">Syntax</span></span>


```C++
void KeyPress(
  [in, out] short *KeyAscii
);
```



## <a name="parameters"></a><span data-ttu-id="85de9-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="85de9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="85de9-107">*ASCII* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="85de9-107">*KeyAscii* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="85de9-108">Valore ASCII della chiave da premere.</span><span class="sxs-lookup"><span data-stu-id="85de9-108">The ASCII value of the key that is being pressed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="85de9-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="85de9-109">Return value</span></span>

<span data-ttu-id="85de9-110">Questo evento non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="85de9-110">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="85de9-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="85de9-111">Remarks</span></span>

<span data-ttu-id="85de9-112">Questo metodo di evento è definito nell'interfaccia **\_ IInkPictureEvents** .</span><span class="sxs-lookup"><span data-stu-id="85de9-112">This event method is defined in the **\_IInkPictureEvents** interface.</span></span> <span data-ttu-id="85de9-113">L'interfaccia **\_ IInkPictureEvents** implementa l'interfaccia [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) con un identificatore di DISPID \_ IPEKeyPress.</span><span class="sxs-lookup"><span data-stu-id="85de9-113">The **\_IInkPictureEvents** interface implements the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface with an identifier of DISPID\_IPEKeyPress.</span></span>

## <a name="requirements"></a><span data-ttu-id="85de9-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="85de9-114">Requirements</span></span>



| <span data-ttu-id="85de9-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="85de9-115">Requirement</span></span> | <span data-ttu-id="85de9-116">Valore</span><span class="sxs-lookup"><span data-stu-id="85de9-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="85de9-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="85de9-117">Minimum supported client</span></span><br/> | <span data-ttu-id="85de9-118">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="85de9-118">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="85de9-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="85de9-119">Minimum supported server</span></span><br/> | <span data-ttu-id="85de9-120">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="85de9-120">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="85de9-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="85de9-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="85de9-122"><dt>Msinkaut. h (richiede anche Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="85de9-122"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="85de9-123">Libreria</span><span class="sxs-lookup"><span data-stu-id="85de9-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="85de9-124"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="85de9-124"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="85de9-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="85de9-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="85de9-126">InkPicture</span><span class="sxs-lookup"><span data-stu-id="85de9-126">InkPicture</span></span>](inkpicture-control-reference.md)
</dt> </dl>

 

