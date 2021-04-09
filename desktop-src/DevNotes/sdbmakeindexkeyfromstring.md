---
description: Crea una chiave da una stringa.
ms.assetid: 107138b9-96f0-4144-a4bc-7115b6deab60
title: SdbMakeIndexKeyFromString (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbMakeIndexKeyFromString
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 691e691f14692775f0c681a7efa3ce91f756be1d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103965871"
---
# <a name="sdbmakeindexkeyfromstring-function"></a><span data-ttu-id="56cc5-103">SdbMakeIndexKeyFromString (funzione)</span><span class="sxs-lookup"><span data-stu-id="56cc5-103">SdbMakeIndexKeyFromString function</span></span>

<span data-ttu-id="56cc5-104">Crea una chiave da una stringa.</span><span class="sxs-lookup"><span data-stu-id="56cc5-104">Creates a key from a string.</span></span>

## <a name="syntax"></a><span data-ttu-id="56cc5-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="56cc5-105">Syntax</span></span>


```C++
ULONGLONG WINAPI SdbMakeIndexKeyFromString(
  _In_ LPCTSTR pwszKey
);
```



## <a name="parameters"></a><span data-ttu-id="56cc5-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="56cc5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="56cc5-107">*pwszKey* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="56cc5-107">*pwszKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="56cc5-108">Stringa.</span><span class="sxs-lookup"><span data-stu-id="56cc5-108">The string.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="56cc5-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="56cc5-109">Return value</span></span>

<span data-ttu-id="56cc5-110">La funzione restituisce la chiave o 0 se si verifica un errore.</span><span class="sxs-lookup"><span data-stu-id="56cc5-110">The function returns the key or 0 if there is an error.</span></span>

## <a name="remarks"></a><span data-ttu-id="56cc5-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="56cc5-111">Remarks</span></span>

<span data-ttu-id="56cc5-112">La chiave di indice standard è costituita dai primi otto caratteri della stringa, convertita in lettere maiuscole, quindi eseguito il cast a un valore **ULONGLONG** .</span><span class="sxs-lookup"><span data-stu-id="56cc5-112">The standard index key is the first eight characters of the string, converted to upper case, then cast to a **ULONGLONG** value.</span></span>

## <a name="requirements"></a><span data-ttu-id="56cc5-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="56cc5-113">Requirements</span></span>



| <span data-ttu-id="56cc5-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="56cc5-114">Requirement</span></span> | <span data-ttu-id="56cc5-115">Valore</span><span class="sxs-lookup"><span data-stu-id="56cc5-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="56cc5-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="56cc5-116">Minimum supported client</span></span><br/> | <span data-ttu-id="56cc5-117">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="56cc5-117">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="56cc5-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="56cc5-118">Minimum supported server</span></span><br/> | <span data-ttu-id="56cc5-119">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="56cc5-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="56cc5-120">DLL</span><span class="sxs-lookup"><span data-stu-id="56cc5-120">DLL</span></span><br/>                      | <dl> <span data-ttu-id="56cc5-121"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="56cc5-121"><dt>Apphelp.dll</dt></span></span> </dl> |



 

 




