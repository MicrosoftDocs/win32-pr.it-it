---
Description: Recupera i dati dal database dettagli apphelp.
ms.assetid: f3731561-bf3f-4139-9890-bd4ce73d83fa
title: SdbReadApphelpDetailsData (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbReadApphelpDetailsData
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: a0a352e3fe33115133b827b5ad03d99a14101b34
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964154"
---
# <a name="sdbreadapphelpdetailsdata-function"></a><span data-ttu-id="a75ae-103">SdbReadApphelpDetailsData (funzione)</span><span class="sxs-lookup"><span data-stu-id="a75ae-103">SdbReadApphelpDetailsData function</span></span>

<span data-ttu-id="a75ae-104">Recupera i dati dal database dettagli apphelp.</span><span class="sxs-lookup"><span data-stu-id="a75ae-104">Retrieves data from the Apphelp details database.</span></span>

## <a name="syntax"></a><span data-ttu-id="a75ae-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a75ae-105">Syntax</span></span>


```C++
BOOL WINAPI SdbReadApphelpDetailsData(
  _In_  PDB           pdb,
  _Out_ PAPPHELP_DATA pData
);
```



## <a name="parameters"></a><span data-ttu-id="a75ae-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="a75ae-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a75ae-107">*PDB* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a75ae-107">*pdb* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a75ae-108">Handle per il database di dettagli AppHelp, AppHelp. sdb.</span><span class="sxs-lookup"><span data-stu-id="a75ae-108">A handle to the Apphelp details database, Apphelp.sdb.</span></span>

</dd> <dt>

<span data-ttu-id="a75ae-109">*pData* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="a75ae-109">*pData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a75ae-110">Struttura [**di \_ dati APPHELP**](apphelp-data.md) .</span><span class="sxs-lookup"><span data-stu-id="a75ae-110">An [**APPHELP\_DATA**](apphelp-data.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a75ae-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a75ae-111">Return value</span></span>

<span data-ttu-id="a75ae-112">La funzione restituisce **true** in caso di esito positivo o **false** in caso di errore.</span><span class="sxs-lookup"><span data-stu-id="a75ae-112">The function returns **TRUE** on success or **FALSE** on failure.</span></span>

## <a name="requirements"></a><span data-ttu-id="a75ae-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a75ae-113">Requirements</span></span>



| <span data-ttu-id="a75ae-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="a75ae-114">Requirement</span></span> | <span data-ttu-id="a75ae-115">Valore</span><span class="sxs-lookup"><span data-stu-id="a75ae-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a75ae-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a75ae-116">Minimum supported client</span></span><br/> | <span data-ttu-id="a75ae-117">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a75ae-117">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="a75ae-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a75ae-118">Minimum supported server</span></span><br/> | <span data-ttu-id="a75ae-119">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="a75ae-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="a75ae-120">DLL</span><span class="sxs-lookup"><span data-stu-id="a75ae-120">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a75ae-121"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a75ae-121"><dt>Apphelp.dll</dt></span></span> </dl> |



 

 




