---
title: Metodo ISoftKbd CreateSoftKeyboardWindow (Softkbdc. h)
description: Il metodo ISoftKbd CreateSoftKeyboardWindow crea una finestra di tastiera soft.
ms.assetid: e9aa9d88-d0bb-407f-9b53-98c8747be5d3
keywords:
- Framework servizi di testo Metodo CreateSoftKeyboardWindow
- Framework dei servizi di testo del metodo CreateSoftKeyboardWindow, interfaccia ISoftKbd
- ISoftKbd Interface Text Services Framework, metodo CreateSoftKeyboardWindow
topic_type:
- apiref
api_name:
- ISoftKbd.CreateSoftKeyboardWindow
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e0ed6f9f91f335945d40dd0b995226a400965ab
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518406"
---
# <a name="isoftkbdcreatesoftkeyboardwindow-method"></a><span data-ttu-id="a1da1-106">Metodo ISoftKbd:: CreateSoftKeyboardWindow</span><span class="sxs-lookup"><span data-stu-id="a1da1-106">ISoftKbd::CreateSoftKeyboardWindow method</span></span>

<span data-ttu-id="a1da1-107">Il metodo **ISoftKbd:: CreateSoftKeyboardWindow** crea una finestra di tastiera soft.</span><span class="sxs-lookup"><span data-stu-id="a1da1-107">The **ISoftKbd::CreateSoftKeyboardWindow** method creates a soft keyboard window.</span></span>

## <a name="syntax"></a><span data-ttu-id="a1da1-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a1da1-108">Syntax</span></span>


```C++
HRESULT CreateSoftKeyboardWindow(
  [in] HWND          hOwner,
  [in] TITLEBAR_TYPE Titlebar_type,
  [in] INT           xPos,
  [in] INT           yPos,
  [in] INT           width,
  [in] INT           height
);
```



## <a name="parameters"></a><span data-ttu-id="a1da1-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="a1da1-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a1da1-110">*hOwner* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a1da1-110">*hOwner* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a1da1-111">Handle della finestra per contenere la tastiera soft.</span><span class="sxs-lookup"><span data-stu-id="a1da1-111">Handle of the window to contain the soft keyboard.</span></span>

</dd> <dt>

<span data-ttu-id="a1da1-112">*\_ Tipo di barra* \[ di titolo in\]</span><span class="sxs-lookup"><span data-stu-id="a1da1-112">*Titlebar\_type* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a1da1-113">Tipo di barra del titolo per la finestra della tastiera soft.</span><span class="sxs-lookup"><span data-stu-id="a1da1-113">Type of title bar for the soft keyboard window.</span></span> <span data-ttu-id="a1da1-114">I tipi possibili sono definiti dall'enumerazione del [**\_ tipo di barra**](titlebar-type.md) del titolo.</span><span class="sxs-lookup"><span data-stu-id="a1da1-114">Possible types are defined by the [**TITLEBAR\_TYPE**](titlebar-type.md) enumeration.</span></span>

</dd> <dt>

<span data-ttu-id="a1da1-115">*XPos* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a1da1-115">*xPos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a1da1-116">Posizione x dell'angolo superiore sinistro della finestra della tastiera soft.</span><span class="sxs-lookup"><span data-stu-id="a1da1-116">The x position of the upper left corner of the soft keyboard window.</span></span>

</dd> <dt>

<span data-ttu-id="a1da1-117">*YPos* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a1da1-117">*yPos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a1da1-118">Posizione y dell'angolo superiore sinistro della finestra della tastiera soft.</span><span class="sxs-lookup"><span data-stu-id="a1da1-118">The y position of the upper left corner of the soft keyboard window.</span></span>

</dd> <dt>

<span data-ttu-id="a1da1-119">*larghezza* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a1da1-119">*width* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a1da1-120">Larghezza della finestra della tastiera soft.</span><span class="sxs-lookup"><span data-stu-id="a1da1-120">The width of the soft keyboard window.</span></span>

</dd> <dt>

<span data-ttu-id="a1da1-121">*altezza* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a1da1-121">*height* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a1da1-122">Altezza della finestra della tastiera soft.</span><span class="sxs-lookup"><span data-stu-id="a1da1-122">The height of the soft keyboard window.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a1da1-123">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a1da1-123">Return value</span></span>

<span data-ttu-id="a1da1-124">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="a1da1-124">This method can return one of these values.</span></span>



| <span data-ttu-id="a1da1-125">Valore</span><span class="sxs-lookup"><span data-stu-id="a1da1-125">Value</span></span>                                                                                        | <span data-ttu-id="a1da1-126">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a1da1-126">Description</span></span>                                    |
|----------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <span data-ttu-id="a1da1-127"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="a1da1-127"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="a1da1-128">Il metodo è stato eseguito correttamente.</span><span class="sxs-lookup"><span data-stu-id="a1da1-128">The method was successful.</span></span><br/>          |
| <dl> <span data-ttu-id="a1da1-129"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="a1da1-129"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="a1da1-130">Uno o più parametri non sono validi.</span><span class="sxs-lookup"><span data-stu-id="a1da1-130">One or more parameters are invalid.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="a1da1-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a1da1-131">Requirements</span></span>



| <span data-ttu-id="a1da1-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="a1da1-132">Requirement</span></span> | <span data-ttu-id="a1da1-133">Valore</span><span class="sxs-lookup"><span data-stu-id="a1da1-133">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a1da1-134">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a1da1-134">Minimum supported client</span></span><br/> | <span data-ttu-id="a1da1-135">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="a1da1-135">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="a1da1-136">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a1da1-136">Minimum supported server</span></span><br/> | <span data-ttu-id="a1da1-137">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="a1da1-137">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="a1da1-138">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="a1da1-138">Redistributable</span></span><br/>          | <span data-ttu-id="a1da1-139">TSF 1,0 su Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="a1da1-139">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                        |
| <span data-ttu-id="a1da1-140">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a1da1-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="a1da1-141"><dt>Softkbdc. h</dt></span><span class="sxs-lookup"><span data-stu-id="a1da1-141"><dt>Softkbdc.h</dt></span></span> </dl>  |
| <span data-ttu-id="a1da1-142">IDL</span><span class="sxs-lookup"><span data-stu-id="a1da1-142">IDL</span></span><br/>                      | <dl> <span data-ttu-id="a1da1-143"><dt>Softkbd. idl</dt></span><span class="sxs-lookup"><span data-stu-id="a1da1-143"><dt>Softkbd.idl</dt></span></span> </dl> |
| <span data-ttu-id="a1da1-144">DLL</span><span class="sxs-lookup"><span data-stu-id="a1da1-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a1da1-145"><dt>Softkbd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a1da1-145"><dt>Softkbd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a1da1-146">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a1da1-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a1da1-147">**ISoftKbd**</span><span class="sxs-lookup"><span data-stu-id="a1da1-147">**ISoftKbd**</span></span>](isoftkbd.md)
</dt> <dt>

[<span data-ttu-id="a1da1-148">**ISoftKbd::CreateSoftKeyboardLayoutFromResource**</span><span class="sxs-lookup"><span data-stu-id="a1da1-148">**ISoftKbd::CreateSoftKeyboardLayoutFromResource**</span></span>](isoftkbd-createsoftkeyboardlayoutfromresource.md)
</dt> <dt>

[<span data-ttu-id="a1da1-149">**ISoftKbd::D estroySoftKeyboardWindow**</span><span class="sxs-lookup"><span data-stu-id="a1da1-149">**ISoftKbd::DestroySoftKeyboardWindow**</span></span>](isoftkbd-destroysoftkeyboardwindow.md)
</dt> <dt>

[<span data-ttu-id="a1da1-150">**ISoftKbd::ShowSoftKeyboard**</span><span class="sxs-lookup"><span data-stu-id="a1da1-150">**ISoftKbd::ShowSoftKeyboard**</span></span>](isoftkbd-showsoftkeyboard.md)
</dt> <dt>

[<span data-ttu-id="a1da1-151">**tipo di barra di titolo \_**</span><span class="sxs-lookup"><span data-stu-id="a1da1-151">**TITLEBAR\_TYPE**</span></span>](titlebar-type.md)
</dt> </dl>

 

 





