---
description: La funzione DllGetVersion Recupera il numero di versione di Cabinet.dll usando la struttura CABINETDLLVERSIONINFO.
ms.assetid: 93f6c29e-6a62-46c2-a42b-8270fe522494
title: DllGetVersion (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DllGetVersion
api_type:
- DllExport
api_location:
- Cabinet.dll
ms.openlocfilehash: e04fd8bc520f037c89912af730c537159867219e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326676"
---
# <a name="dllgetversion-function"></a><span data-ttu-id="6d4b7-103">DllGetVersion (funzione)</span><span class="sxs-lookup"><span data-stu-id="6d4b7-103">DllGetVersion function</span></span>

<span data-ttu-id="6d4b7-104">\[Questa funzione non è più supportata, pertanto non è possibile garantirne il comportamento.\]</span><span class="sxs-lookup"><span data-stu-id="6d4b7-104">\[This function is no longer supported, so its behavior cannot be guaranteed.\]</span></span>

<span data-ttu-id="6d4b7-105">La funzione **DllGetVersion** Recupera il numero di versione di Cabinet.dll usando la struttura [**CABINETDLLVERSIONINFO**](cabinetdllversioninfo.md) .</span><span class="sxs-lookup"><span data-stu-id="6d4b7-105">The **DllGetVersion** function retrieves the version number of Cabinet.dll using the [**CABINETDLLVERSIONINFO**](cabinetdllversioninfo.md) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="6d4b7-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6d4b7-106">Syntax</span></span>


```C++
VOID WINAPI DllGetVersion(
   PCABINETDLLVERSIONINFO pcdvi
);
```



## <a name="parameters"></a><span data-ttu-id="6d4b7-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="6d4b7-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6d4b7-108">*pcdvi*</span><span class="sxs-lookup"><span data-stu-id="6d4b7-108">*pcdvi*</span></span> 
</dt> <dd>

<span data-ttu-id="6d4b7-109">Puntatore alla struttura [**CABINETDLLVERSIONINFO**](cabinetdllversioninfo.md) che contiene le informazioni sulla versione.</span><span class="sxs-lookup"><span data-stu-id="6d4b7-109">Pointer to the [**CABINETDLLVERSIONINFO**](cabinetdllversioninfo.md) structure that contains the version information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6d4b7-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="6d4b7-110">Return value</span></span>

<span data-ttu-id="6d4b7-111">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="6d4b7-111">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="6d4b7-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="6d4b7-112">Remarks</span></span>

<span data-ttu-id="6d4b7-113">A questa funzione non è associato alcun file di intestazione o libreria di importazione. è necessario chiamarla usando le funzioni [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="6d4b7-113">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="6d4b7-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6d4b7-114">Requirements</span></span>



| <span data-ttu-id="6d4b7-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="6d4b7-115">Requirement</span></span> | <span data-ttu-id="6d4b7-116">Valore</span><span class="sxs-lookup"><span data-stu-id="6d4b7-116">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6d4b7-117">DLL</span><span class="sxs-lookup"><span data-stu-id="6d4b7-117">DLL</span></span><br/> | <dl> <span data-ttu-id="6d4b7-118"><dt>Cabinet.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6d4b7-118"><dt>Cabinet.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6d4b7-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6d4b7-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6d4b7-120">**CABINETDLLVERSIONINFO**</span><span class="sxs-lookup"><span data-stu-id="6d4b7-120">**CABINETDLLVERSIONINFO**</span></span>](cabinetdllversioninfo.md)
</dt> <dt>

[<span data-ttu-id="6d4b7-121">**GetDllVersion**</span><span class="sxs-lookup"><span data-stu-id="6d4b7-121">**GetDllVersion**</span></span>](getdllversion.md)
</dt> </dl>

 

 
