---
description: Registra un'applicazione come client di CTL3D.
ms.assetid: 38a4a04a-6322-4eb8-b272-ae9b90f84e0f
title: Ctl3dRegister (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Ctl3dRegister
api_type:
- DllExport
api_location:
- Ctl3d32.dll
ms.openlocfilehash: 4b855c162d9d5f1c43a15d1ebd7219da6f847f37
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331669"
---
# <a name="ctl3dregister-function"></a><span data-ttu-id="e9efe-103">Ctl3dRegister (funzione)</span><span class="sxs-lookup"><span data-stu-id="e9efe-103">Ctl3dRegister function</span></span>

<span data-ttu-id="e9efe-104">Registra un'applicazione come client di CTL3D.</span><span class="sxs-lookup"><span data-stu-id="e9efe-104">Registers an application as a client of CTL3D.</span></span>

## <a name="syntax"></a><span data-ttu-id="e9efe-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e9efe-105">Syntax</span></span>


```C++
BOOL Ctl3dRegister(
   HANDLE hinstApp
);
```



## <a name="parameters"></a><span data-ttu-id="e9efe-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="e9efe-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e9efe-107">*hinstApp*</span><span class="sxs-lookup"><span data-stu-id="e9efe-107">*hinstApp*</span></span> 
</dt> <dd>

<span data-ttu-id="e9efe-108">Handle per l'applicazione da registrare come client.</span><span class="sxs-lookup"><span data-stu-id="e9efe-108">A handle to the application to be registered as a client.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e9efe-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e9efe-109">Return value</span></span>

<span data-ttu-id="e9efe-110">Restituisce **true** se gli effetti 3D sono attivi; in caso contrario, restituisce **false**.</span><span class="sxs-lookup"><span data-stu-id="e9efe-110">Returns **TRUE** if 3D effects are active; otherwise, it returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="e9efe-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="e9efe-111">Remarks</span></span>

<span data-ttu-id="e9efe-112">Un'applicazione che usa CTL3D deve chiamare questa funzione in WinMain.</span><span class="sxs-lookup"><span data-stu-id="e9efe-112">An application that uses CTL3D should call this function in WinMain.</span></span>

<span data-ttu-id="e9efe-113">gli effetti 3D non sono disponibili nei sistemi con una risoluzione inferiore a VGA.</span><span class="sxs-lookup"><span data-stu-id="e9efe-113">3D effects are not available on systems that have less than VGA resolution.</span></span>

<span data-ttu-id="e9efe-114">A questa funzione non è associato alcun file di intestazione o libreria di importazione. è necessario chiamarla usando le funzioni [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="e9efe-114">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="e9efe-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e9efe-115">Requirements</span></span>



| <span data-ttu-id="e9efe-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="e9efe-116">Requirement</span></span> | <span data-ttu-id="e9efe-117">Valore</span><span class="sxs-lookup"><span data-stu-id="e9efe-117">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e9efe-118">DLL</span><span class="sxs-lookup"><span data-stu-id="e9efe-118">DLL</span></span><br/> | <dl> <span data-ttu-id="e9efe-119"><dt>Ctl3d32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e9efe-119"><dt>Ctl3d32.dll</dt></span></span> </dl> |



 

 
