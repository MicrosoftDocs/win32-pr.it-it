---
description: Sottoclassi tutti i controlli in una finestra di dialogo e nella finestra di dialogo stessa.
ms.assetid: 4d3c298b-07ba-4668-badd-dddecc389e70
title: Ctl3dSubclassDlgEx (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Ctl3dSubclassDlgEx
api_type:
- DllExport
api_location:
- Ctl3d32.dll
ms.openlocfilehash: 6e29f65d5ddc3d0d9a7de05eef88b7a662e0e43f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332101"
---
# <a name="ctl3dsubclassdlgex-function"></a><span data-ttu-id="e0024-103">Ctl3dSubclassDlgEx (funzione)</span><span class="sxs-lookup"><span data-stu-id="e0024-103">Ctl3dSubclassDlgEx function</span></span>

<span data-ttu-id="e0024-104">Sottoclassi tutti i controlli in una finestra di dialogo e nella finestra di dialogo stessa.</span><span class="sxs-lookup"><span data-stu-id="e0024-104">Subclasses all controls in a dialog box and in the dialog window itself.</span></span>

## <a name="syntax"></a><span data-ttu-id="e0024-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e0024-105">Syntax</span></span>


```C++
PUBLIC BOOL FAR PASCAL Ctl3dSubclassDlgEx(
   HWND  hwndDlg,
   DWORD grbit
);
```



## <a name="parameters"></a><span data-ttu-id="e0024-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="e0024-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e0024-107">*hwndDlg*</span><span class="sxs-lookup"><span data-stu-id="e0024-107">*hwndDlg*</span></span> 
</dt> <dd>

<span data-ttu-id="e0024-108">Handle per la finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="e0024-108">A handle to the dialog window.</span></span>

</dd> <dt>

<span data-ttu-id="e0024-109">*grbit*</span><span class="sxs-lookup"><span data-stu-id="e0024-109">*grbit*</span></span> 
</dt> <dd>

<span data-ttu-id="e0024-110">Tipi di controllo da sottoclassare.</span><span class="sxs-lookup"><span data-stu-id="e0024-110">The control types to be subclassed.</span></span> <span data-ttu-id="e0024-111">Il valore può essere uno dei seguenti.</span><span class="sxs-lookup"><span data-stu-id="e0024-111">This value can be any of the following.</span></span>



| <span data-ttu-id="e0024-112">Valore</span><span class="sxs-lookup"><span data-stu-id="e0024-112">Value</span></span>                                                                                                                                                                                                                                     | <span data-ttu-id="e0024-113">Significato</span><span class="sxs-lookup"><span data-stu-id="e0024-113">Meaning</span></span>                                       |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| <span id="CTL3D_BUTTONS"></span><span id="ctl3d_buttons"></span><dl> <span data-ttu-id="e0024-114"><dt>**CTL3D \_ PULSANTI**</dt> <dt>0x0001</dt></span><span class="sxs-lookup"><span data-stu-id="e0024-114"><dt>**CTL3D\_BUTTONS**</dt> <dt>0x0001</dt></span></span> </dl>                 | <span data-ttu-id="e0024-115">Pulsanti della sottoclasse.</span><span class="sxs-lookup"><span data-stu-id="e0024-115">Subclass buttons.</span></span><br/>                  |
| <span id="CTL3D_LISTBOXES"></span><span id="ctl3d_listboxes"></span><dl> <span data-ttu-id="e0024-116"><dt>**CTL3D \_ LISTBOX**</dt> <dt>0x0002</dt></span><span class="sxs-lookup"><span data-stu-id="e0024-116"><dt>**CTL3D\_LISTBOXES**</dt> <dt>0x0002</dt></span></span> </dl>           | <span data-ttu-id="e0024-117">Caselle di riepilogo della sottoclasse.</span><span class="sxs-lookup"><span data-stu-id="e0024-117">Subclass list boxes.</span></span><br/>               |
| <span id="CTL3D_EDITS"></span><span id="ctl3d_edits"></span><dl> <span data-ttu-id="e0024-118"><dt>**CTL3D \_ MODIFICA**</dt> <dt>0x0004</dt></span><span class="sxs-lookup"><span data-stu-id="e0024-118"><dt>**CTL3D\_EDITS**</dt> <dt>0x0004</dt></span></span> </dl>                       | <span data-ttu-id="e0024-119">Controlli di modifica della sottoclasse.</span><span class="sxs-lookup"><span data-stu-id="e0024-119">Subclass edit controls.</span></span><br/>            |
| <span id="CTL3D_COMBOS"></span><span id="ctl3d_combos"></span><dl> <span data-ttu-id="e0024-120"><dt>**CTL3D \_**</dt> <dt>0x0008</dt> combo</span><span class="sxs-lookup"><span data-stu-id="e0024-120"><dt>**CTL3D\_COMBOS**</dt> <dt>0x0008</dt></span></span> </dl>                    | <span data-ttu-id="e0024-121">Caselle combinate della sottoclasse.</span><span class="sxs-lookup"><span data-stu-id="e0024-121">Subclass combo boxes.</span></span><br/>              |
| <span id="CTL3D_STATICTEXTS"></span><span id="ctl3d_statictexts"></span><dl> <span data-ttu-id="e0024-122"><dt>**CTL3D \_**</dt> <dt>0x0010</dt> STATICTEXTS</span><span class="sxs-lookup"><span data-stu-id="e0024-122"><dt>**CTL3D\_STATICTEXTS**</dt> <dt>0x0010</dt></span></span> </dl>     | <span data-ttu-id="e0024-123">Sottoclasse controlli di testo statici.</span><span class="sxs-lookup"><span data-stu-id="e0024-123">Subclass static text controls.</span></span><br/>     |
| <span id="CTL3D_STATICFRAMES"></span><span id="ctl3d_staticframes"></span><dl> <span data-ttu-id="e0024-124"><dt>**CTL3D \_**</dt> <dt>0x0020</dt> STATICFRAMES</span><span class="sxs-lookup"><span data-stu-id="e0024-124"><dt>**CTL3D\_STATICFRAMES**</dt> <dt>0x0020</dt></span></span> </dl>  | <span data-ttu-id="e0024-125">Frame statici della sottoclasse.</span><span class="sxs-lookup"><span data-stu-id="e0024-125">Subclass static frames.</span></span><br/>            |
| <span id="CTL3D_ALL"></span><span id="ctl3d_all"></span><dl> <span data-ttu-id="e0024-126"><dt>**CTL3D \_ Tutte le**</dt> <dt>0xFFFF</dt></span><span class="sxs-lookup"><span data-stu-id="e0024-126"><dt>**CTL3D\_ALL**</dt> <dt>0xffff</dt></span></span> </dl>                             | <span data-ttu-id="e0024-127">Sottoclassare tutti i controlli.</span><span class="sxs-lookup"><span data-stu-id="e0024-127">Subclass all controls.</span></span><br/>             |
| <span id="CTL3D_NODLGWINDOW"></span><span id="ctl3d_nodlgwindow"></span><dl> <span data-ttu-id="e0024-128"><dt>**CTL3D \_**</dt> <dt>0x00010000</dt> NODLGWINDOW</span><span class="sxs-lookup"><span data-stu-id="e0024-128"><dt>**CTL3D\_NODLGWINDOW**</dt> <dt>0x00010000</dt></span></span> </dl> | <span data-ttu-id="e0024-129">Non sottoclassare la finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="e0024-129">Do not subclass the dialog window.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e0024-130">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e0024-130">Return value</span></span>

<span data-ttu-id="e0024-131">Restituisce **true** se la funzione ha esito positivo; in caso contrario, restituisce **false**.</span><span class="sxs-lookup"><span data-stu-id="e0024-131">Returns **TRUE** if the function succeeds; otherwise, it returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="e0024-132">Commenti</span><span class="sxs-lookup"><span data-stu-id="e0024-132">Remarks</span></span>

<span data-ttu-id="e0024-133">Questa funzione è particolarmente utile nelle applicazioni basate su C++.</span><span class="sxs-lookup"><span data-stu-id="e0024-133">This function is especially useful in applications based on C++.</span></span>

<span data-ttu-id="e0024-134">A questa funzione non è associato alcun file di intestazione o libreria di importazione. è necessario chiamarla usando le funzioni [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="e0024-134">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="e0024-135">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e0024-135">Requirements</span></span>



| <span data-ttu-id="e0024-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="e0024-136">Requirement</span></span> | <span data-ttu-id="e0024-137">Valore</span><span class="sxs-lookup"><span data-stu-id="e0024-137">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e0024-138">DLL</span><span class="sxs-lookup"><span data-stu-id="e0024-138">DLL</span></span><br/> | <dl> <span data-ttu-id="e0024-139"><dt>Ctl3d32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e0024-139"><dt>Ctl3d32.dll</dt></span></span> </dl> |



 

 
