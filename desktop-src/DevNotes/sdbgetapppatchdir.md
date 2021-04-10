---
description: Recupera la directory AppPatch di sistema.
ms.assetid: 1c79411f-1f90-4b90-84c7-24a34cf0d91d
title: SdbGetAppPatchDir (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbGetAppPatchDir
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 60a3b14bcca1be3ecb8d33b0d3f344f08bc11b28
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104125634"
---
# <a name="sdbgetapppatchdir-function"></a><span data-ttu-id="53d9e-103">SdbGetAppPatchDir (funzione)</span><span class="sxs-lookup"><span data-stu-id="53d9e-103">SdbGetAppPatchDir function</span></span>

<span data-ttu-id="53d9e-104">Recupera la directory AppPatch di sistema.</span><span class="sxs-lookup"><span data-stu-id="53d9e-104">Retrieves the system AppPatch directory.</span></span>

## <a name="syntax"></a><span data-ttu-id="53d9e-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="53d9e-105">Syntax</span></span>


```C++
void WINAPI SdbGetAppPatchDir(
  _In_opt_ HSDB   hSDB,
  _Out_    LPTSTR szAppPatchPath,
  _In_     DWORD  cchSize
);
```



## <a name="parameters"></a><span data-ttu-id="53d9e-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="53d9e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="53d9e-107">*hSDB* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="53d9e-107">*hSDB* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="53d9e-108">Handle per il database shim restituito dalla funzione [**SdbInitDatabase**](sdbinitdatabase.md) .</span><span class="sxs-lookup"><span data-stu-id="53d9e-108">A handle to the shim database returned by the [**SdbInitDatabase**](sdbinitdatabase.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="53d9e-109">*szAppPatchPath* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="53d9e-109">*szAppPatchPath* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="53d9e-110">Percorso risultante.</span><span class="sxs-lookup"><span data-stu-id="53d9e-110">The resulting path.</span></span>

</dd> <dt>

<span data-ttu-id="53d9e-111">*cchSize* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="53d9e-111">*cchSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="53d9e-112">Dimensioni del buffer *szAppPatchPath* , in caratteri.</span><span class="sxs-lookup"><span data-stu-id="53d9e-112">The size of the *szAppPatchPath* buffer, in characters.</span></span> <span data-ttu-id="53d9e-113">Se la funzione ha esito negativo, questo parametro viene impostato sulla stringa vuota ("").</span><span class="sxs-lookup"><span data-stu-id="53d9e-113">If the function fails, this parameter is set to the empty string ("").</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="53d9e-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="53d9e-114">Return value</span></span>

<span data-ttu-id="53d9e-115">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="53d9e-115">This function does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="53d9e-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="53d9e-116">Requirements</span></span>



| <span data-ttu-id="53d9e-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="53d9e-117">Requirement</span></span> | <span data-ttu-id="53d9e-118">Valore</span><span class="sxs-lookup"><span data-stu-id="53d9e-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="53d9e-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="53d9e-119">Minimum supported client</span></span><br/> | <span data-ttu-id="53d9e-120">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="53d9e-120">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="53d9e-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="53d9e-121">Minimum supported server</span></span><br/> | <span data-ttu-id="53d9e-122">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="53d9e-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="53d9e-123">DLL</span><span class="sxs-lookup"><span data-stu-id="53d9e-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="53d9e-124"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="53d9e-124"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="53d9e-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="53d9e-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="53d9e-126">**SdbInitDatabase**</span><span class="sxs-lookup"><span data-stu-id="53d9e-126">**SdbInitDatabase**</span></span>](sdbinitdatabase.md)
</dt> </dl>

 

 




