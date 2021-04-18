---
description: Ricarica le impostazioni dei colori dal registro di sistema.
ms.assetid: 1F2EE08A-4193-4F0C-BE4F-0551FA71CFA8
title: FRefreshStyle (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FRefreshStyle
api_type:
- DllExport
api_location:
- Imeshare.dll
ms.openlocfilehash: 098e79ab49373dc115189a2c47dc3604fba10ef9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327679"
---
# <a name="frefreshstyle-function"></a><span data-ttu-id="ac731-103">FRefreshStyle (funzione)</span><span class="sxs-lookup"><span data-stu-id="ac731-103">FRefreshStyle function</span></span>

<span data-ttu-id="ac731-104">Ricarica le impostazioni dei colori dal registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="ac731-104">Reloads color settings from registry.</span></span>

## <a name="syntax"></a><span data-ttu-id="ac731-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ac731-105">Syntax</span></span>


```C++
BOOL __cdecl FRefreshStyle(void);
```



## <a name="parameters"></a><span data-ttu-id="ac731-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="ac731-106">Parameters</span></span>

<span data-ttu-id="ac731-107">Questa funzione non ha parametri.</span><span class="sxs-lookup"><span data-stu-id="ac731-107">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="ac731-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ac731-108">Return value</span></span>

<span data-ttu-id="ac731-109">Restituisce TRUE in caso di esito positivo; in caso contrario, FALSE.</span><span class="sxs-lookup"><span data-stu-id="ac731-109">Returns TRUE on success; otherwise, FALSE.</span></span>

## <a name="remarks"></a><span data-ttu-id="ac731-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="ac731-110">Remarks</span></span>

<span data-ttu-id="ac731-111">Questa funzione non è associata a una libreria di importazione o a un file di intestazione. deve essere chiamato usando le funzioni [**LoadLibrary**](-loadlibrary.md) e [**GetProcAddress**](-getprocaddress-.md) .</span><span class="sxs-lookup"><span data-stu-id="ac731-111">This function is not associated with an import library or header file; it must be called using the [**LoadLibrary**](-loadlibrary.md) and [**GetProcAddress**](-getprocaddress-.md) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="ac731-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ac731-112">Requirements</span></span>



| <span data-ttu-id="ac731-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="ac731-113">Requirement</span></span> | <span data-ttu-id="ac731-114">Valore</span><span class="sxs-lookup"><span data-stu-id="ac731-114">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ac731-115">DLL</span><span class="sxs-lookup"><span data-stu-id="ac731-115">DLL</span></span><br/> | <dl> <span data-ttu-id="ac731-116"><dt>Imeshare.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ac731-116"><dt>Imeshare.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ac731-117">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ac731-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ac731-118">**GetProcAddress**</span><span class="sxs-lookup"><span data-stu-id="ac731-118">**GetProcAddress**</span></span>](-getprocaddress-.md)
</dt> <dt>

[<span data-ttu-id="ac731-119">**LoadLibrary**</span><span class="sxs-lookup"><span data-stu-id="ac731-119">**LoadLibrary**</span></span>](-loadlibrary.md)
</dt> </dl>

 

 




