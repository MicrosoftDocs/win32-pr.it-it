---
description: Si verifica dopo la modifica della proprietà SizeMode del controllo InkPicture.
ms.assetid: ae56b5a2-e3e2-468c-a572-a9b46eb1d39d
title: Evento InkPicture. SizeModeChanged (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f270ea141bc8803cbcf1ce4e54b0f73318ed69d7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104348656"
---
# <a name="inkpicturesizemodechanged-event"></a><span data-ttu-id="0ac8e-103">Evento InkPicture. SizeModeChanged</span><span class="sxs-lookup"><span data-stu-id="0ac8e-103">InkPicture.SizeModeChanged event</span></span>

<span data-ttu-id="0ac8e-104">Si verifica dopo la modifica della proprietà [**SizeMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_sizemode) del controllo [InkPicture](inkpicture-control-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="0ac8e-104">Occurs after the [**SizeMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_sizemode) property of the [InkPicture](inkpicture-control-reference.md) control has been changed.</span></span>

## <a name="syntax"></a><span data-ttu-id="0ac8e-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0ac8e-105">Syntax</span></span>


```C++
void SizeModeChanged(
  [in] InkPictureSizeMode NewMode,
  [in] InkPictureSizeMode OldMode
);
```



## <a name="parameters"></a><span data-ttu-id="0ac8e-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="0ac8e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0ac8e-107">*NewMode* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0ac8e-107">*NewMode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0ac8e-108">Nuovo stato del controllo [InkPicture](inkpicture-control-reference.md) , in base al nuovo valore della proprietà [**SizeMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_sizemode) .</span><span class="sxs-lookup"><span data-stu-id="0ac8e-108">The new state of the [InkPicture](inkpicture-control-reference.md) control, based on the new value of the [**SizeMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_sizemode) property.</span></span>

</dd> <dt>

<span data-ttu-id="0ac8e-109">*OldMode* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0ac8e-109">*OldMode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0ac8e-110">Stato precedente del controllo [InkPicture](inkpicture-control-reference.md) , in base al valore precedente della proprietà [**SizeMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_sizemode) .</span><span class="sxs-lookup"><span data-stu-id="0ac8e-110">The old state of the [InkPicture](inkpicture-control-reference.md) control, based on the old value of the [**SizeMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_sizemode) property.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0ac8e-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0ac8e-111">Return value</span></span>

<span data-ttu-id="0ac8e-112">Questo evento non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="0ac8e-112">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="0ac8e-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="0ac8e-113">Remarks</span></span>

<span data-ttu-id="0ac8e-114">Questo metodo di evento è definito nell'interfaccia **\_ IInkPictureEvents** .</span><span class="sxs-lookup"><span data-stu-id="0ac8e-114">This event method is defined in the **\_IInkPictureEvents** interface.</span></span> <span data-ttu-id="0ac8e-115">L'interfaccia **\_ IInkPictureEvents** implementa l'interfaccia [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) con un identificatore di DISPID \_ IPESizeModeChanged.</span><span class="sxs-lookup"><span data-stu-id="0ac8e-115">The **\_IInkPictureEvents** interface implements the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface with an identifier of DISPID\_IPESizeModeChanged.</span></span>

## <a name="requirements"></a><span data-ttu-id="0ac8e-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0ac8e-116">Requirements</span></span>



| <span data-ttu-id="0ac8e-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="0ac8e-117">Requirement</span></span> | <span data-ttu-id="0ac8e-118">Valore</span><span class="sxs-lookup"><span data-stu-id="0ac8e-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0ac8e-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0ac8e-119">Minimum supported client</span></span><br/> | <span data-ttu-id="0ac8e-120">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="0ac8e-120">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="0ac8e-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0ac8e-121">Minimum supported server</span></span><br/> | <span data-ttu-id="0ac8e-122">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="0ac8e-122">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="0ac8e-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0ac8e-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="0ac8e-124"><dt>Msinkaut. h (richiede anche Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="0ac8e-124"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="0ac8e-125">Libreria</span><span class="sxs-lookup"><span data-stu-id="0ac8e-125">Library</span></span><br/>                  | <dl> <span data-ttu-id="0ac8e-126"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0ac8e-126"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="0ac8e-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0ac8e-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0ac8e-128">InkPicture</span><span class="sxs-lookup"><span data-stu-id="0ac8e-128">InkPicture</span></span>](inkpicture-control-reference.md)
</dt> </dl>

 

