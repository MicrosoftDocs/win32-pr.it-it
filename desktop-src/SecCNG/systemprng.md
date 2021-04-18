---
description: Recupera un numero specificato di byte casuali dal generatore di numeri casuali di sistema.
ms.assetid: 04746229-9dc1-4748-80c1-f1960bd1b768
title: SystemPrng (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SystemPrng
api_type:
- DllExport
api_location:
- Ksecdd.sys
- Cng.sys
ms.openlocfilehash: d847d34ffd11e158170f55599de0ceb3acf3c697
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306473"
---
# <a name="systemprng-function"></a><span data-ttu-id="d1e32-103">SystemPrng (funzione)</span><span class="sxs-lookup"><span data-stu-id="d1e32-103">SystemPrng function</span></span>

<span data-ttu-id="d1e32-104">\[**SystemPrng** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="d1e32-104">\[**SystemPrng** is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="d1e32-105">È possibile che in versioni successive sia stata modificata o non sia più disponibile.</span><span class="sxs-lookup"><span data-stu-id="d1e32-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="d1e32-106">Usare invece [**BCryptGenRandom**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptgenrandom).\]</span><span class="sxs-lookup"><span data-stu-id="d1e32-106">Instead, use [**BCryptGenRandom**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptgenrandom).\]</span></span>

<span data-ttu-id="d1e32-107">La funzione **SystemPrng** recupera un numero specificato di byte casuali dal generatore di numeri casuali di sistema.</span><span class="sxs-lookup"><span data-stu-id="d1e32-107">The **SystemPrng** function retrieves a specified number of random bytes from the system random number generator.</span></span>

> [!Note]  
> <span data-ttu-id="d1e32-108">A questa funzione non è associato alcun file di intestazione o libreria di importazione.</span><span class="sxs-lookup"><span data-stu-id="d1e32-108">This function has no associated header file or import library.</span></span> <span data-ttu-id="d1e32-109">Per chiamare questa funzione, è necessario creare un file di intestazione definito dall'utente.</span><span class="sxs-lookup"><span data-stu-id="d1e32-109">To call this function, you must create a user-defined header file.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="d1e32-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d1e32-110">Syntax</span></span>


```C++
BOOL SystemPrng(
  _Out_ unsigned char pbRandomData,
  _In_  size_t        cbRandomData
);
```



## <a name="parameters"></a><span data-ttu-id="d1e32-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="d1e32-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d1e32-112">*pbRandomData* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="d1e32-112">*pbRandomData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d1e32-113">Puntatore a un buffer che riceve i byte recuperati.</span><span class="sxs-lookup"><span data-stu-id="d1e32-113">A pointer to a buffer that receives the retrieved bytes.</span></span>

</dd> <dt>

<span data-ttu-id="d1e32-114">*cbRandomData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d1e32-114">*cbRandomData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d1e32-115">Numero di byte da recuperare.</span><span class="sxs-lookup"><span data-stu-id="d1e32-115">The number of bytes to retrieve.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d1e32-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d1e32-116">Return value</span></span>

<span data-ttu-id="d1e32-117">Restituisce sempre **true**.</span><span class="sxs-lookup"><span data-stu-id="d1e32-117">Always returns **TRUE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="d1e32-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d1e32-118">Requirements</span></span>



| <span data-ttu-id="d1e32-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="d1e32-119">Requirement</span></span> | <span data-ttu-id="d1e32-120">Valore</span><span class="sxs-lookup"><span data-stu-id="d1e32-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d1e32-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d1e32-121">Minimum supported client</span></span><br/> | <span data-ttu-id="d1e32-122">Solo app desktop Windows Vista con SP1 \[\]</span><span class="sxs-lookup"><span data-stu-id="d1e32-122">Windows Vista with SP1 \[desktop apps only\]</span></span><br/>                                                                                                                                                                                        |
| <span data-ttu-id="d1e32-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d1e32-123">Minimum supported server</span></span><br/> | <span data-ttu-id="d1e32-124">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="d1e32-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                                                                                                           |
| <span data-ttu-id="d1e32-125">DLL</span><span class="sxs-lookup"><span data-stu-id="d1e32-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d1e32-126"><dt>Ksecdd.sys in Windows Server 2008 e Windows Vista con SP1; </dt> <dt>Cng.sys in Windows 7 e Windows Server 2008 R2</dt></span><span class="sxs-lookup"><span data-stu-id="d1e32-126"><dt>Ksecdd.sys on Windows Server 2008 and Windows Vista with SP1; </dt> <dt>Cng.sys on Windows 7 and Windows Server 2008 R2</dt></span></span> </dl> |



 

 




