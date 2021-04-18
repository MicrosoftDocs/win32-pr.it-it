---
description: Chiude un handle di ricerca.
ms.assetid: 2e6a547f-26a7-401a-b1e4-3f085ce82729
title: CSCFindClose (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSCFindClose
api_type:
- DllExport
api_location:
- Cscmig.dll
ms.openlocfilehash: 69e3ea972ccd67a1db999c186709ef3aeff84be9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331201"
---
# <a name="cscfindclose-function"></a><span data-ttu-id="c61e0-103">CSCFindClose (funzione)</span><span class="sxs-lookup"><span data-stu-id="c61e0-103">CSCFindClose function</span></span>

<span data-ttu-id="c61e0-104">\[Questa funzione non è supportata e non deve essere utilizzata.\]</span><span class="sxs-lookup"><span data-stu-id="c61e0-104">\[This function is not supported and should not be used.\]</span></span>

<span data-ttu-id="c61e0-105">Chiude un handle di ricerca.</span><span class="sxs-lookup"><span data-stu-id="c61e0-105">Closes a search handle.</span></span>

## <a name="syntax"></a><span data-ttu-id="c61e0-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c61e0-106">Syntax</span></span>


```C++
BOOL WINAPI CSCFindClose(
  _In_ HANDLE hFind
);
```



## <a name="parameters"></a><span data-ttu-id="c61e0-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="c61e0-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c61e0-108">*hFind* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c61e0-108">*hFind* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c61e0-109">Handle di ricerca restituito dalla funzione [**CSCFindFirstFileW**](cscfindfirstfilew.md) .</span><span class="sxs-lookup"><span data-stu-id="c61e0-109">A search handle returned by the [**CSCFindFirstFileW**](cscfindfirstfilew.md) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c61e0-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c61e0-110">Return value</span></span>

<span data-ttu-id="c61e0-111">Questa funzione restituisce **true** se ha esito positivo; in caso contrario, restituisce **false**.</span><span class="sxs-lookup"><span data-stu-id="c61e0-111">This function returns **TRUE** if it succeeds; otherwise, it returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="c61e0-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="c61e0-112">Remarks</span></span>

<span data-ttu-id="c61e0-113">A questa funzione non è associato alcun file di intestazione o libreria di importazione. è necessario chiamarla usando le funzioni [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="c61e0-113">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="c61e0-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c61e0-114">Requirements</span></span>



| <span data-ttu-id="c61e0-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="c61e0-115">Requirement</span></span> | <span data-ttu-id="c61e0-116">Valore</span><span class="sxs-lookup"><span data-stu-id="c61e0-116">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c61e0-117">DLL</span><span class="sxs-lookup"><span data-stu-id="c61e0-117">DLL</span></span><br/> | <dl> <span data-ttu-id="c61e0-118"><dt>Cscmig.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c61e0-118"><dt>Cscmig.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c61e0-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c61e0-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c61e0-120">**CSCFindFirstFileW**</span><span class="sxs-lookup"><span data-stu-id="c61e0-120">**CSCFindFirstFileW**</span></span>](cscfindfirstfilew.md)
</dt> </dl>

 

 
