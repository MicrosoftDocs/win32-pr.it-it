---
description: Disattiva la sottoclasse per il controllo specificato.
ms.assetid: d4d34624-7d85-4c53-8318-b3e5d6f95f7a
title: Ctl3dUnsubclassCtl (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Ctl3dUnsubclassCtl
api_type:
- DllExport
api_location:
- Ctl3d32.dll
ms.openlocfilehash: ec62c2ecab6d8c90a9c9b7b2570bf5d76afd0589
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331827"
---
# <a name="ctl3dunsubclassctl-function"></a><span data-ttu-id="96642-103">Ctl3dUnsubclassCtl (funzione)</span><span class="sxs-lookup"><span data-stu-id="96642-103">Ctl3dUnsubclassCtl function</span></span>

<span data-ttu-id="96642-104">Disattiva la sottoclasse per il controllo specificato.</span><span class="sxs-lookup"><span data-stu-id="96642-104">Turns off subclassing for the specified control.</span></span>

## <a name="syntax"></a><span data-ttu-id="96642-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="96642-105">Syntax</span></span>


```C++
BOOL WINAPI Ctl3dUnsubclassCtl(
   HWND hwnd
);
```



## <a name="parameters"></a><span data-ttu-id="96642-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="96642-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="96642-107">*HWND*</span><span class="sxs-lookup"><span data-stu-id="96642-107">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="96642-108">Handle per la finestra del controllo.</span><span class="sxs-lookup"><span data-stu-id="96642-108">A handle to the control window.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="96642-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="96642-109">Return value</span></span>

<span data-ttu-id="96642-110">Restituisce **true** se il controllo è sottoclassato correttamente; in caso contrario, restituisce **false**.</span><span class="sxs-lookup"><span data-stu-id="96642-110">Returns **TRUE** if the control is successfully subclassed; otherwise, it returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="96642-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="96642-111">Remarks</span></span>

<span data-ttu-id="96642-112">A questa funzione non è associato alcun file di intestazione o libreria di importazione. è necessario chiamarla usando le funzioni [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="96642-112">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="96642-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="96642-113">Requirements</span></span>



| <span data-ttu-id="96642-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="96642-114">Requirement</span></span> | <span data-ttu-id="96642-115">Valore</span><span class="sxs-lookup"><span data-stu-id="96642-115">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="96642-116">DLL</span><span class="sxs-lookup"><span data-stu-id="96642-116">DLL</span></span><br/> | <dl> <span data-ttu-id="96642-117"><dt>Ctl3d32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="96642-117"><dt>Ctl3d32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="96642-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="96642-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="96642-119">**Ctl3dSubclassCtl**</span><span class="sxs-lookup"><span data-stu-id="96642-119">**Ctl3dSubclassCtl**</span></span>](ctl3dsubclassctl.md)
</dt> </dl>

 

 
