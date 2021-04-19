---
description: Disattiva la sottoclasse automatica.
ms.assetid: 85e5689f-6805-4aad-b97c-aa496e315900
title: Ctl3dUnAutoSubclass (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Ctl3dUnAutoSubclass
api_type:
- DllExport
api_location:
- Ctl3d32.dll
ms.openlocfilehash: 1250deb16307400898c92d36b9dda214115ec01d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332100"
---
# <a name="ctl3dunautosubclass-function"></a><span data-ttu-id="f4ef9-103">Ctl3dUnAutoSubclass (funzione)</span><span class="sxs-lookup"><span data-stu-id="f4ef9-103">Ctl3dUnAutoSubclass function</span></span>

<span data-ttu-id="f4ef9-104">Disattiva la sottoclasse automatica.</span><span class="sxs-lookup"><span data-stu-id="f4ef9-104">Turns off automatic subclassing.</span></span>

## <a name="syntax"></a><span data-ttu-id="f4ef9-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f4ef9-105">Syntax</span></span>


```C++
BOOL Ctl3dUnAutoSubclass(void);
```



## <a name="parameters"></a><span data-ttu-id="f4ef9-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="f4ef9-106">Parameters</span></span>

<span data-ttu-id="f4ef9-107">Questa funzione non ha parametri.</span><span class="sxs-lookup"><span data-stu-id="f4ef9-107">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="f4ef9-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f4ef9-108">Return value</span></span>

<span data-ttu-id="f4ef9-109">Restituisce **true** se la funzione ha esito positivo; in caso contrario, restituisce **false**.</span><span class="sxs-lookup"><span data-stu-id="f4ef9-109">Returns **TRUE** if the function succeeds; otherwise, it returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="f4ef9-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="f4ef9-110">Remarks</span></span>

<span data-ttu-id="f4ef9-111">A questa funzione non è associato alcun file di intestazione o libreria di importazione. è necessario chiamarla usando le funzioni [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="f4ef9-111">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="f4ef9-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f4ef9-112">Requirements</span></span>



| <span data-ttu-id="f4ef9-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="f4ef9-113">Requirement</span></span> | <span data-ttu-id="f4ef9-114">Valore</span><span class="sxs-lookup"><span data-stu-id="f4ef9-114">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f4ef9-115">DLL</span><span class="sxs-lookup"><span data-stu-id="f4ef9-115">DLL</span></span><br/> | <dl> <span data-ttu-id="f4ef9-116"><dt>Ctl3d32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f4ef9-116"><dt>Ctl3d32.dll</dt></span></span> </dl> |



 

 
