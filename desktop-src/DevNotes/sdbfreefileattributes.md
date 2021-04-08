---
description: Libera i dati dell'attributo di file specificati.
ms.assetid: c1a4dcf8-614f-49a5-a923-8d7d610e6406
title: SdbFreeFileAttributes (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbFreeFileAttributes
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 6f28812fbbec83dd1a41c8a21cb4c9544dbefea5
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103747687"
---
# <a name="sdbfreefileattributes-function"></a><span data-ttu-id="42ccb-103">SdbFreeFileAttributes (funzione)</span><span class="sxs-lookup"><span data-stu-id="42ccb-103">SdbFreeFileAttributes function</span></span>

<span data-ttu-id="42ccb-104">Libera i dati dell'attributo di file specificati.</span><span class="sxs-lookup"><span data-stu-id="42ccb-104">Frees the specified file attribute data.</span></span>

## <a name="syntax"></a><span data-ttu-id="42ccb-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="42ccb-105">Syntax</span></span>


```C++
BOOL WINAPI SdbFreeFileAttributes(
  _In_ PATTRINFO pFileAttributes
);
```



## <a name="parameters"></a><span data-ttu-id="42ccb-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="42ccb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="42ccb-107">*pFileAttributes* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="42ccb-107">*pFileAttributes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="42ccb-108">Struttura [**ATTRINFO**](attrinfo.md) restituita dalla funzione [**SdbGetFileAttributes**](sdbgetfileattributes.md) .</span><span class="sxs-lookup"><span data-stu-id="42ccb-108">An [**ATTRINFO**](attrinfo.md) structure returned by the [**SdbGetFileAttributes**](sdbgetfileattributes.md) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="42ccb-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="42ccb-109">Return value</span></span>

<span data-ttu-id="42ccb-110">La funzione restituisce **true** in caso di esito positivo o **false** in caso di errore.</span><span class="sxs-lookup"><span data-stu-id="42ccb-110">The function returns **TRUE** on success or **FALSE** on failure.</span></span>

## <a name="requirements"></a><span data-ttu-id="42ccb-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="42ccb-111">Requirements</span></span>



| <span data-ttu-id="42ccb-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="42ccb-112">Requirement</span></span> | <span data-ttu-id="42ccb-113">Valore</span><span class="sxs-lookup"><span data-stu-id="42ccb-113">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="42ccb-114">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="42ccb-114">Minimum supported client</span></span><br/> | <span data-ttu-id="42ccb-115">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="42ccb-115">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="42ccb-116">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="42ccb-116">Minimum supported server</span></span><br/> | <span data-ttu-id="42ccb-117">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="42ccb-117">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="42ccb-118">DLL</span><span class="sxs-lookup"><span data-stu-id="42ccb-118">DLL</span></span><br/>                      | <dl> <span data-ttu-id="42ccb-119"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="42ccb-119"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="42ccb-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="42ccb-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="42ccb-121">**SdbGetFileAttributes**</span><span class="sxs-lookup"><span data-stu-id="42ccb-121">**SdbGetFileAttributes**</span></span>](sdbgetfileattributes.md)
</dt> </dl>

 

 




