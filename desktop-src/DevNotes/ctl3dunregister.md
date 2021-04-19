---
description: Annulla la registrazione di un'applicazione come client di CTL3D.
ms.assetid: 21990A79-F90D-4AE1-AB02-2B33583B47F5
title: Ctl3dUnregister (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Ctl3dUnregister
api_type:
- DllExport
api_location:
- Ctl3d32.dll
ms.openlocfilehash: 85cd45062da9c01ef8af5a312a855bfaab6a6bf7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331830"
---
# <a name="ctl3dunregister-function"></a><span data-ttu-id="765b9-103">Ctl3dUnregister (funzione)</span><span class="sxs-lookup"><span data-stu-id="765b9-103">Ctl3dUnregister function</span></span>

<span data-ttu-id="765b9-104">Annulla la registrazione di un'applicazione come client di CTL3D.</span><span class="sxs-lookup"><span data-stu-id="765b9-104">Unregisters an application as a client of CTL3D.</span></span>

## <a name="syntax"></a><span data-ttu-id="765b9-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="765b9-105">Syntax</span></span>


```C++
BOOL Ctl3dUnregister(
   HANDLE hinstApp
);
```



## <a name="parameters"></a><span data-ttu-id="765b9-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="765b9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="765b9-107">*hinstApp*</span><span class="sxs-lookup"><span data-stu-id="765b9-107">*hinstApp*</span></span> 
</dt> <dd>

<span data-ttu-id="765b9-108">Handle per l'applicazione di cui annullare la registrazione come client.</span><span class="sxs-lookup"><span data-stu-id="765b9-108">A handle to the application to be unregistered as a client.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="765b9-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="765b9-109">Return value</span></span>

<span data-ttu-id="765b9-110">Restituisce **true** se viene annullata la registrazione dell'applicazione come client di CTL3D; in caso contrario, restituisce **false**.</span><span class="sxs-lookup"><span data-stu-id="765b9-110">Returns **TRUE** if the application is unregistered as a client of CTL3D; otherwise, it returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="765b9-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="765b9-111">Remarks</span></span>

<span data-ttu-id="765b9-112">Un'applicazione che usa CTL3D deve chiamare questa funzione in WinMain.</span><span class="sxs-lookup"><span data-stu-id="765b9-112">An application that uses CTL3D should call this function in WinMain.</span></span>

<span data-ttu-id="765b9-113">gli effetti 3D non sono disponibili nei sistemi con una risoluzione inferiore a VGA.</span><span class="sxs-lookup"><span data-stu-id="765b9-113">3D effects are not available on systems that have less than VGA resolution.</span></span>

<span data-ttu-id="765b9-114">A questa funzione non è associato alcun file di intestazione o libreria di importazione. è necessario chiamarla usando le funzioni [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="765b9-114">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="765b9-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="765b9-115">Requirements</span></span>



| <span data-ttu-id="765b9-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="765b9-116">Requirement</span></span> | <span data-ttu-id="765b9-117">Valore</span><span class="sxs-lookup"><span data-stu-id="765b9-117">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="765b9-118">DLL</span><span class="sxs-lookup"><span data-stu-id="765b9-118">DLL</span></span><br/> | <dl> <span data-ttu-id="765b9-119"><dt>Ctl3d32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="765b9-119"><dt>Ctl3d32.dll</dt></span></span> </dl> |



 

 
