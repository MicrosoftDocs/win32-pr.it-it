---
description: Carica il file di risorse apphelp.
ms.assetid: fca50e00-9324-410a-a572-69441f332593
title: SdbOpenApphelpResourceFile (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbOpenApphelpResourceFile
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 2f1dfb1695e25bfb82e01ffa4f9eac4e245a6ffa
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104401437"
---
# <a name="sdbopenapphelpresourcefile-function"></a><span data-ttu-id="887ef-103">SdbOpenApphelpResourceFile (funzione)</span><span class="sxs-lookup"><span data-stu-id="887ef-103">SdbOpenApphelpResourceFile function</span></span>

<span data-ttu-id="887ef-104">Carica il file di risorse apphelp.</span><span class="sxs-lookup"><span data-stu-id="887ef-104">Loads the Apphelp resource file.</span></span>

## <a name="syntax"></a><span data-ttu-id="887ef-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="887ef-105">Syntax</span></span>


```C++
HMODULE WINAPI SdbOpenApphelpResourceFile(
  _In_opt_ LPCWSTR pwszACResourceFile
);
```



## <a name="parameters"></a><span data-ttu-id="887ef-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="887ef-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="887ef-107">*pwszACResourceFile* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="887ef-107">*pwszACResourceFile* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="887ef-108">Percorso del file di risorse.</span><span class="sxs-lookup"><span data-stu-id="887ef-108">The path to the resource file.</span></span> <span data-ttu-id="887ef-109">Se questo parametro è **null**, viene aperta la dll della risorsa locale.</span><span class="sxs-lookup"><span data-stu-id="887ef-109">If this parameter is **NULL**, the local resource DLL is opened.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="887ef-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="887ef-110">Return value</span></span>

<span data-ttu-id="887ef-111">La funzione restituisce un handle per il file di risorse aperto.</span><span class="sxs-lookup"><span data-stu-id="887ef-111">The function returns a handle to the opened resource file.</span></span>

## <a name="requirements"></a><span data-ttu-id="887ef-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="887ef-112">Requirements</span></span>



| <span data-ttu-id="887ef-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="887ef-113">Requirement</span></span> | <span data-ttu-id="887ef-114">Valore</span><span class="sxs-lookup"><span data-stu-id="887ef-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="887ef-115">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="887ef-115">Minimum supported client</span></span><br/> | <span data-ttu-id="887ef-116">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="887ef-116">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="887ef-117">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="887ef-117">Minimum supported server</span></span><br/> | <span data-ttu-id="887ef-118">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="887ef-118">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="887ef-119">DLL</span><span class="sxs-lookup"><span data-stu-id="887ef-119">DLL</span></span><br/>                      | <dl> <span data-ttu-id="887ef-120"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="887ef-120"><dt>Apphelp.dll</dt></span></span> </dl> |



 

 




