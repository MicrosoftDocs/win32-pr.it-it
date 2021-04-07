---
description: Determina se il database specificato è uno dei database standard (SysMain, AppHelp, Drvmain o Msimain).
ms.assetid: 7d7e3ca7-535e-40b3-b635-299eff8abea5
title: SdbIsStandardDatabase (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbIsStandardDatabase
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 9e9e445162c2bfc171ccf975981876f81a8bb804
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049081"
---
# <a name="sdbisstandarddatabase-function"></a><span data-ttu-id="0452c-103">SdbIsStandardDatabase (funzione)</span><span class="sxs-lookup"><span data-stu-id="0452c-103">SdbIsStandardDatabase function</span></span>

<span data-ttu-id="0452c-104">Determina se il database specificato è uno dei database standard (SysMain, AppHelp, Drvmain o Msimain).</span><span class="sxs-lookup"><span data-stu-id="0452c-104">Determines whether the specified database is one of the standard databases (Sysmain, Apphelp, Drvmain, or Msimain).</span></span>

## <a name="syntax"></a><span data-ttu-id="0452c-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0452c-105">Syntax</span></span>


```C++
BOOL WINAPI SdbIsStandardDatabase(
  _In_ GUID GuidDB
);
```



## <a name="parameters"></a><span data-ttu-id="0452c-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="0452c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0452c-107">*GuidDB* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0452c-107">*GuidDB* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0452c-108">GUID del database.</span><span class="sxs-lookup"><span data-stu-id="0452c-108">The GUID for the database.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0452c-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0452c-109">Return value</span></span>

<span data-ttu-id="0452c-110">La funzione restituisce **true** se il GUID rappresenta un database standard o **false** in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="0452c-110">The function returns **TRUE** if the GUID represents a standard database or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="0452c-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0452c-111">Requirements</span></span>



| <span data-ttu-id="0452c-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="0452c-112">Requirement</span></span> | <span data-ttu-id="0452c-113">Valore</span><span class="sxs-lookup"><span data-stu-id="0452c-113">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0452c-114">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0452c-114">Minimum supported client</span></span><br/> | <span data-ttu-id="0452c-115">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="0452c-115">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="0452c-116">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0452c-116">Minimum supported server</span></span><br/> | <span data-ttu-id="0452c-117">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="0452c-117">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="0452c-118">DLL</span><span class="sxs-lookup"><span data-stu-id="0452c-118">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0452c-119"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0452c-119"><dt>Apphelp.dll</dt></span></span> </dl> |



 

 




