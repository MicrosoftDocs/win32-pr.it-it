---
description: Elimina una tabella di stringhe.
ms.assetid: a3ac1672-f898-44a0-bb7b-64ac24bdb9bf
title: pSetupStringTableDestroy (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- pSetupStringTableDestroy
api_type:
- DllExport
api_location:
- Setupapi.dll
ms.openlocfilehash: 472ee152d98c064edb8bac5d4de849b505b634da
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325206"
---
# <a name="psetupstringtabledestroy-function"></a><span data-ttu-id="7a091-103">pSetupStringTableDestroy (funzione)</span><span class="sxs-lookup"><span data-stu-id="7a091-103">pSetupStringTableDestroy function</span></span>

<span data-ttu-id="7a091-104">\[Questa funzione non è disponibile in Windows Vista o Windows Server 2008.\]</span><span class="sxs-lookup"><span data-stu-id="7a091-104">\[This function is not available in Windows Vista or Windows Server 2008.\]</span></span>

<span data-ttu-id="7a091-105">Elimina una tabella di stringhe.</span><span class="sxs-lookup"><span data-stu-id="7a091-105">Deletes a string table.</span></span>

## <a name="syntax"></a><span data-ttu-id="7a091-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7a091-106">Syntax</span></span>


```C++
void WINAPI pSetupStringTableDestroy(
  _In_ PVOID StringTable
);
```



## <a name="parameters"></a><span data-ttu-id="7a091-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="7a091-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7a091-108">*Un'STRINGTABLE* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7a091-108">*StringTable* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7a091-109">Puntatore alla tabella delle stringhe.</span><span class="sxs-lookup"><span data-stu-id="7a091-109">A pointer to the string table.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7a091-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="7a091-110">Return value</span></span>

<span data-ttu-id="7a091-111">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="7a091-111">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="7a091-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="7a091-112">Remarks</span></span>

<span data-ttu-id="7a091-113">A questa funzione non è associato alcun file di intestazione o libreria di importazione. è necessario chiamarla usando le funzioni [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="7a091-113">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="7a091-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7a091-114">Requirements</span></span>



| <span data-ttu-id="7a091-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="7a091-115">Requirement</span></span> | <span data-ttu-id="7a091-116">Valore</span><span class="sxs-lookup"><span data-stu-id="7a091-116">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7a091-117">DLL</span><span class="sxs-lookup"><span data-stu-id="7a091-117">DLL</span></span><br/> | <dl> <span data-ttu-id="7a091-118"><dt>Setupapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7a091-118"><dt>Setupapi.dll</dt></span></span> </dl> |



 

 
