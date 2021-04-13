---
description: Imposta una attendibilità del codice dinamico di .NET CRL su disco per .NET.
ms.assetid: 4C8C3EF5-5C3C-4710-8223-D7B5BA86EF47
title: Funzione WldpSetDynamicCodeTrust (Wldp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WldpSetDynamicCodeTrust
api_type:
- DllExport
api_location:
- wldp.dll
ms.openlocfilehash: a266563b40d255fe9e904f02e4e4593d4c4d3f33
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104401410"
---
# <a name="wldpsetdynamiccodetrust-function"></a><span data-ttu-id="82d39-103">WldpSetDynamicCodeTrust (funzione)</span><span class="sxs-lookup"><span data-stu-id="82d39-103">WldpSetDynamicCodeTrust function</span></span>

<span data-ttu-id="82d39-104">Imposta una attendibilità del codice dinamico di .NET CRL su disco per .NET.</span><span class="sxs-lookup"><span data-stu-id="82d39-104">Sets an on-disk .NET CRL Dynamic Code trustable for .NET.</span></span>

## <a name="syntax"></a><span data-ttu-id="82d39-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="82d39-105">Syntax</span></span>


```C++
HRESULT WINAPI WldpSetDynamicCodeTrust(
   HANDLE FileHandle
);
```



## <a name="parameters"></a><span data-ttu-id="82d39-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="82d39-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="82d39-107">*FileHandle*</span><span class="sxs-lookup"><span data-stu-id="82d39-107">*FileHandle*</span></span> 
</dt> <dd>

<span data-ttu-id="82d39-108">Handle per un file di codice dinamico su disco.</span><span class="sxs-lookup"><span data-stu-id="82d39-108">Handle to a on-disk dynamic code file.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="82d39-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="82d39-109">Return value</span></span>

<span data-ttu-id="82d39-110">Questo metodo restituisce **\_ OK** se l'esito è positivo o un codice di errore; in caso contrario,.</span><span class="sxs-lookup"><span data-stu-id="82d39-110">This method returns **S\_OK** if successful or a failure code otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="82d39-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="82d39-111">Requirements</span></span>



| <span data-ttu-id="82d39-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="82d39-112">Requirement</span></span> | <span data-ttu-id="82d39-113">Valore</span><span class="sxs-lookup"><span data-stu-id="82d39-113">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="82d39-114">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="82d39-114">Minimum supported client</span></span><br/> | <span data-ttu-id="82d39-115">Solo app desktop Windows 10 versione 1803 \[\]</span><span class="sxs-lookup"><span data-stu-id="82d39-115">Windows 10, version 1803 \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="82d39-116">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="82d39-116">Minimum supported server</span></span><br/> | <span data-ttu-id="82d39-117">\[Solo app desktop Windows Server 2016\]</span><span class="sxs-lookup"><span data-stu-id="82d39-117">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="82d39-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="82d39-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="82d39-119"><dt>Wldp. h</dt></span><span class="sxs-lookup"><span data-stu-id="82d39-119"><dt>Wldp.h</dt></span></span> </dl>   |
| <span data-ttu-id="82d39-120">DLL</span><span class="sxs-lookup"><span data-stu-id="82d39-120">DLL</span></span><br/>                      | <dl> <span data-ttu-id="82d39-121"><dt>Wldp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="82d39-121"><dt>Wldp.dll</dt></span></span> </dl> |



 

 




