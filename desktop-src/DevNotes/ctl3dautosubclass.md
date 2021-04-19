---
description: Sottoclassi automaticamente e aggiunge effetti 3D a tutte le finestre di dialogo nell'applicazione.
ms.assetid: 96555052-c564-4cc7-9b24-e527f8e2f879
title: Ctl3dAutoSubclass (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Ctl3dAutoSubclass
api_type:
- DllExport
api_location:
- Ctl3d32.dll
ms.openlocfilehash: 85f4c85d1d608ff97147a935806b090162f5a78a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331971"
---
# <a name="ctl3dautosubclass-function"></a><span data-ttu-id="86a56-103">Ctl3dAutoSubclass (funzione)</span><span class="sxs-lookup"><span data-stu-id="86a56-103">Ctl3dAutoSubclass function</span></span>

<span data-ttu-id="86a56-104">Sottoclassi automaticamente e aggiunge effetti 3D a tutte le finestre di dialogo nell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="86a56-104">Automatically subclasses and adds 3D effects to all dialog boxes in the application.</span></span>

## <a name="syntax"></a><span data-ttu-id="86a56-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="86a56-105">Syntax</span></span>


```C++
PUBLIC BOOL FAR PASCAL Ctl3dAutoSubclass(
   HANDLE hinstApp
);
```



## <a name="parameters"></a><span data-ttu-id="86a56-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="86a56-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="86a56-107">*hinstApp*</span><span class="sxs-lookup"><span data-stu-id="86a56-107">*hinstApp*</span></span> 
</dt> <dd>

<span data-ttu-id="86a56-108">Handle per l'applicazione da registrare come client.</span><span class="sxs-lookup"><span data-stu-id="86a56-108">A handle to the application to be registered as a client.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="86a56-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="86a56-109">Return value</span></span>

<span data-ttu-id="86a56-110">Restituisce **true** a meno che non esista una delle condizioni seguenti, nel qual caso restituisce **false**:</span><span class="sxs-lookup"><span data-stu-id="86a56-110">Returns **TRUE** unless one of the following conditions exists, in which case it returns **FALSE**:</span></span>

-   <span data-ttu-id="86a56-111">CTL3D è in esecuzione in Windows versione 3,0 o versioni precedenti.</span><span class="sxs-lookup"><span data-stu-id="86a56-111">CTL3D is running under Windows version 3.0 or earlier.</span></span>
-   <span data-ttu-id="86a56-112">In CTL3D non è disponibile spazio nelle tabelle per l'applicazione corrente.</span><span class="sxs-lookup"><span data-stu-id="86a56-112">CTL3D does not have space available in its tables for the current application.</span></span> <span data-ttu-id="86a56-113">CTL3D è in grado di servire fino a 32 applicazioni nello stesso momento.</span><span class="sxs-lookup"><span data-stu-id="86a56-113">CTL3D can service up to 32 applications at the same time.</span></span>
-   <span data-ttu-id="86a56-114">CTL3D non è in grado di installare il relativo hook CBT.</span><span class="sxs-lookup"><span data-stu-id="86a56-114">CTL3D cannot install its CBT hook.</span></span>

## <a name="remarks"></a><span data-ttu-id="86a56-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="86a56-115">Remarks</span></span>

<span data-ttu-id="86a56-116">A questa funzione non è associato alcun file di intestazione o libreria di importazione. è necessario chiamarla usando le funzioni [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="86a56-116">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="86a56-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="86a56-117">Requirements</span></span>



| <span data-ttu-id="86a56-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="86a56-118">Requirement</span></span> | <span data-ttu-id="86a56-119">Valore</span><span class="sxs-lookup"><span data-stu-id="86a56-119">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="86a56-120">DLL</span><span class="sxs-lookup"><span data-stu-id="86a56-120">DLL</span></span><br/> | <dl> <span data-ttu-id="86a56-121"><dt>Ctl3d32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="86a56-121"><dt>Ctl3d32.dll</dt></span></span> </dl> |



 

 
