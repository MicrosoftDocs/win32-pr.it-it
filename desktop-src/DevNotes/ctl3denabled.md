---
description: Verifica se i controlli possono utilizzare effetti 3D.
ms.assetid: fb7b892f-2580-41ac-b2ef-938da3cc1dc2
title: Ctl3dEnabled (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Ctl3dEnabled
api_type:
- DllExport
api_location:
- Ctl3d32.dll
ms.openlocfilehash: d0eecec5650ecc00b69c0745e58a3e1d0f931a00
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331674"
---
# <a name="ctl3denabled-function"></a><span data-ttu-id="b73c7-103">Ctl3dEnabled (funzione)</span><span class="sxs-lookup"><span data-stu-id="b73c7-103">Ctl3dEnabled function</span></span>

<span data-ttu-id="b73c7-104">Verifica se i controlli possono utilizzare effetti 3D.</span><span class="sxs-lookup"><span data-stu-id="b73c7-104">Verifies whether controls can use 3D effects.</span></span>

## <a name="syntax"></a><span data-ttu-id="b73c7-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b73c7-105">Syntax</span></span>


```C++
BOOL Ctl3dEnabled(void);
```



## <a name="parameters"></a><span data-ttu-id="b73c7-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="b73c7-106">Parameters</span></span>

<span data-ttu-id="b73c7-107">Questa funzione non ha parametri.</span><span class="sxs-lookup"><span data-stu-id="b73c7-107">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="b73c7-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b73c7-108">Return value</span></span>

<span data-ttu-id="b73c7-109">Restituisce **true** se i controlli possono utilizzare effetti 3D; in caso contrario, restituisce **false**.</span><span class="sxs-lookup"><span data-stu-id="b73c7-109">Returns **TRUE** if controls can use 3D effects; otherwise, it returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="b73c7-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="b73c7-110">Remarks</span></span>

<span data-ttu-id="b73c7-111">In Windows 4,0 o versioni successive, **Ctl3dEnabled** e [**Ctl3dRegister**](ctl3dregister.md) restituiscono **false**.</span><span class="sxs-lookup"><span data-stu-id="b73c7-111">In Windows 4.0 or later, **Ctl3dEnabled** and [**Ctl3dRegister**](ctl3dregister.md) return **FALSE**.</span></span>

<span data-ttu-id="b73c7-112">A questa funzione non è associato alcun file di intestazione o libreria di importazione. è necessario chiamarla usando le funzioni [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="b73c7-112">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="b73c7-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b73c7-113">Requirements</span></span>



| <span data-ttu-id="b73c7-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="b73c7-114">Requirement</span></span> | <span data-ttu-id="b73c7-115">Valore</span><span class="sxs-lookup"><span data-stu-id="b73c7-115">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b73c7-116">DLL</span><span class="sxs-lookup"><span data-stu-id="b73c7-116">DLL</span></span><br/> | <dl> <span data-ttu-id="b73c7-117"><dt>Ctl3d32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b73c7-117"><dt>Ctl3d32.dll</dt></span></span> </dl> |



 

 
