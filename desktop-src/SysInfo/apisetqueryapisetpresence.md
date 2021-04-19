---
description: Questa API è solo per uso interno e non deve essere usata nel codice.
ms.assetid: 836A7515-8C22-4032-9E99-F89B32C21685
title: Funzione ApiSetQueryApiSetPresence (Apiquery. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ApiSetQueryApiSetPresence
api_type:
- DllExport
api_location:
- api-ms-win-core-apiquery-l1-1-0.dll
- ntdll.dll
ms.openlocfilehash: 738a69b0d08f7e619dbd64229d0c13b2ae7dfaca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319905"
---
# <a name="apisetqueryapisetpresence-function"></a><span data-ttu-id="07547-103">ApiSetQueryApiSetPresence (funzione)</span><span class="sxs-lookup"><span data-stu-id="07547-103">ApiSetQueryApiSetPresence function</span></span>

<span data-ttu-id="07547-104">\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale.</span><span class="sxs-lookup"><span data-stu-id="07547-104">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="07547-105">Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]</span><span class="sxs-lookup"><span data-stu-id="07547-105">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="07547-106">Questa API è solo per uso interno e non deve essere usata nel codice.</span><span class="sxs-lookup"><span data-stu-id="07547-106">This API is intended for internal use only and should not be used in your code.</span></span>

## <a name="syntax"></a><span data-ttu-id="07547-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="07547-107">Syntax</span></span>


```C++
BOOL WINAPI ApiSetQueryApiSetPresence(
  _In_  PCUNICODE_STRING Namespace,
  _Out_ PBOOLEAN         Present
);
```



## <a name="parameters"></a><span data-ttu-id="07547-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="07547-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="07547-109">*Spazio dei nomi* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="07547-109">*Namespace* \[in\]</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="07547-110">*Presente* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="07547-110">*Present* \[out\]</span></span>
<span data-ttu-id="07547-111"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="07547-111"></dt> <dd></dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="07547-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="07547-112">Requirements</span></span>



| <span data-ttu-id="07547-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="07547-113">Requirement</span></span> | <span data-ttu-id="07547-114">Valore</span><span class="sxs-lookup"><span data-stu-id="07547-114">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="07547-115">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="07547-115">Minimum supported client</span></span><br/> | <span data-ttu-id="07547-116">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="07547-116">Windows 10 \[desktop apps only\]</span></span><br/>                                                                                                                                                           |
| <span data-ttu-id="07547-117">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="07547-117">Minimum supported server</span></span><br/> | <span data-ttu-id="07547-118">\[Solo app desktop Windows Server 2016\]</span><span class="sxs-lookup"><span data-stu-id="07547-118">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                                                                                                                                  |
| <span data-ttu-id="07547-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="07547-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="07547-120"><dt>Apiquery. h</dt></span><span class="sxs-lookup"><span data-stu-id="07547-120"><dt>Apiquery.h</dt></span></span> </dl>                                                                                                                 |
| <span data-ttu-id="07547-121">Libreria</span><span class="sxs-lookup"><span data-stu-id="07547-121">Library</span></span><br/>                  | <dl> <span data-ttu-id="07547-122"><dt>API-MS-Win-Core-apiquery-L1. lib; </dt> <dt>API-MS-Win-Core-apiquery-L1-1-0. lib</dt></span><span class="sxs-lookup"><span data-stu-id="07547-122"><dt>Api-ms-win-core-apiquery-l1.lib; </dt> <dt>Api-ms-win-core-apiquery-l1-1-0.lib</dt></span></span> </dl> |
| <span data-ttu-id="07547-123">DLL</span><span class="sxs-lookup"><span data-stu-id="07547-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="07547-124"><dt>Api-ms-win-core-apiquery-l1-1-0.dll</dt></span><span class="sxs-lookup"><span data-stu-id="07547-124"><dt>Api-ms-win-core-apiquery-l1-1-0.dll</dt></span></span> </dl>                                                                                        |



 

 




