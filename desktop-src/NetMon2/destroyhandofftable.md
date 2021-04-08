---
description: La funzione DestroyHandoffTable Elimina una tabella di continuità creata con CreateHandoffTable.
ms.assetid: 01ae9899-4f7c-4706-a2ce-9f55b112351d
title: Funzione DestroyHandoffTable (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DestroyHandoffTable
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 7afccfd1932c57b2a0d77dbb5467afc31726c6fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103967400"
---
# <a name="destroyhandofftable-function"></a><span data-ttu-id="dd7f8-103">DestroyHandoffTable (funzione)</span><span class="sxs-lookup"><span data-stu-id="dd7f8-103">DestroyHandoffTable function</span></span>

<span data-ttu-id="dd7f8-104">La funzione **DestroyHandoffTable** Elimina una tabella di continuità creata con **CreateHandoffTable**.</span><span class="sxs-lookup"><span data-stu-id="dd7f8-104">The **DestroyHandoffTable** function destroys a handoff table created with **CreateHandoffTable**.</span></span>

## <a name="syntax"></a><span data-ttu-id="dd7f8-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="dd7f8-105">Syntax</span></span>


```C++
VOID WINAPI DestroyHandoffTable(
  _In_ LPHANDOFFTABLE hTable
);
```



## <a name="parameters"></a><span data-ttu-id="dd7f8-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="dd7f8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dd7f8-107">*hTable* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="dd7f8-107">*hTable* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dd7f8-108">Handle per la tabella di continuità eliminata.</span><span class="sxs-lookup"><span data-stu-id="dd7f8-108">Handle to the destroyed handoff table.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dd7f8-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="dd7f8-109">Return value</span></span>

<span data-ttu-id="dd7f8-110">Nessuna.</span><span class="sxs-lookup"><span data-stu-id="dd7f8-110">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="dd7f8-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="dd7f8-111">Requirements</span></span>



| <span data-ttu-id="dd7f8-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="dd7f8-112">Requirement</span></span> | <span data-ttu-id="dd7f8-113">Valore</span><span class="sxs-lookup"><span data-stu-id="dd7f8-113">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="dd7f8-114">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="dd7f8-114">Minimum supported client</span></span><br/> | <span data-ttu-id="dd7f8-115">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="dd7f8-115">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="dd7f8-116">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="dd7f8-116">Minimum supported server</span></span><br/> | <span data-ttu-id="dd7f8-117">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="dd7f8-117">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="dd7f8-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="dd7f8-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="dd7f8-119"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="dd7f8-119"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="dd7f8-120">Libreria</span><span class="sxs-lookup"><span data-stu-id="dd7f8-120">Library</span></span><br/>                  | <dl> <span data-ttu-id="dd7f8-121"><dt>Nmap. lib</dt></span><span class="sxs-lookup"><span data-stu-id="dd7f8-121"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="dd7f8-122">DLL</span><span class="sxs-lookup"><span data-stu-id="dd7f8-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dd7f8-123"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dd7f8-123"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 




