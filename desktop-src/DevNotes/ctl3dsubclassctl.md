---
description: Sottoclassi di un singolo controllo a meno che il controllo non venga visualizzato in una finestra di dialogo.
ms.assetid: 07a2bce1-4c69-4f8d-bb24-b17351f5e771
title: Ctl3dSubclassCtl (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Ctl3dSubclassCtl
api_type:
- DllExport
api_location:
- Ctl3d32.dll
ms.openlocfilehash: 0ff6c6744c4ddda203149981218b8143fb78bce7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331668"
---
# <a name="ctl3dsubclassctl-function"></a><span data-ttu-id="50e3b-103">Ctl3dSubclassCtl (funzione)</span><span class="sxs-lookup"><span data-stu-id="50e3b-103">Ctl3dSubclassCtl function</span></span>

<span data-ttu-id="50e3b-104">Sottoclassi di un singolo controllo a meno che il controllo non venga visualizzato in una finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="50e3b-104">Subclasses an individual control unless the control appears in a dialog box.</span></span>

## <a name="syntax"></a><span data-ttu-id="50e3b-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="50e3b-105">Syntax</span></span>


```C++
BOOL Ctl3dSubclassCtl(
   HWND hwnd
);
```



## <a name="parameters"></a><span data-ttu-id="50e3b-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="50e3b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="50e3b-107">*HWND*</span><span class="sxs-lookup"><span data-stu-id="50e3b-107">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="50e3b-108">Handle per la finestra del controllo.</span><span class="sxs-lookup"><span data-stu-id="50e3b-108">A handle to the control window.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="50e3b-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="50e3b-109">Return value</span></span>

<span data-ttu-id="50e3b-110">Restituisce **true** se il controllo è sottoclassato correttamente; in caso contrario, restituisce **false**.</span><span class="sxs-lookup"><span data-stu-id="50e3b-110">Returns **TRUE** if the control is successfully subclassed; otherwise, it returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="50e3b-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="50e3b-111">Remarks</span></span>

<span data-ttu-id="50e3b-112">A questa funzione non è associato alcun file di intestazione o libreria di importazione. è necessario chiamarla usando le funzioni [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="50e3b-112">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="50e3b-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="50e3b-113">Requirements</span></span>



| <span data-ttu-id="50e3b-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="50e3b-114">Requirement</span></span> | <span data-ttu-id="50e3b-115">Valore</span><span class="sxs-lookup"><span data-stu-id="50e3b-115">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="50e3b-116">DLL</span><span class="sxs-lookup"><span data-stu-id="50e3b-116">DLL</span></span><br/> | <dl> <span data-ttu-id="50e3b-117"><dt>Ctl3d32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="50e3b-117"><dt>Ctl3d32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="50e3b-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="50e3b-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="50e3b-119">**Ctl3dUnsubclassCtl**</span><span class="sxs-lookup"><span data-stu-id="50e3b-119">**Ctl3dUnsubclassCtl**</span></span>](ctl3dunsubclassctl.md)
</dt> </dl>

 

 
