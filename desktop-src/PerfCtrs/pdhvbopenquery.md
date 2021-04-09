---
description: La funzione PdhVbOpenQuery crea e Inizializza una struttura di query univoca usata per gestire la raccolta di dati sulle prestazioni.
ms.assetid: 9cf535ef-76ad-4773-8414-8e289f3c52f6
title: PdhVbOpenQuery (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PdhVbOpenQuery
api_type:
- DllExport
api_location:
- Pdh.dll
ms.openlocfilehash: c657f033e2e972473218f2b283e03b11659d9f2c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131678"
---
# <a name="pdhvbopenquery-function"></a><span data-ttu-id="e35ad-103">PdhVbOpenQuery (funzione)</span><span class="sxs-lookup"><span data-stu-id="e35ad-103">PdhVbOpenQuery function</span></span>

<span data-ttu-id="e35ad-104">La funzione **PdhVbOpenQuery** crea e Inizializza una struttura di query univoca usata per gestire la raccolta di dati sulle prestazioni.</span><span class="sxs-lookup"><span data-stu-id="e35ad-104">The **PdhVbOpenQuery** function creates and initializes a unique query structure that is used to manage the collection of performance data.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e35ad-105">La funzione descritta in questo argomento può essere modificata o non disponibile in futuro.</span><span class="sxs-lookup"><span data-stu-id="e35ad-105">The function that this topic describes may be altered or unavailable in the future.</span></span> <span data-ttu-id="e35ad-106">Microsoft consiglia invece di utilizzare le funzioni descritte in [funzioni dei contatori delle prestazioni](performance-counters-functions.md).</span><span class="sxs-lookup"><span data-stu-id="e35ad-106">Instead, Microsoft recommends that you use the functions described in [Performance Counters Functions](performance-counters-functions.md).</span></span>

<span data-ttu-id="e35ad-107">Funzione PdhVbOpenQuery ( \_ ByVal QueryHandle Long \_ ) Long</span><span class="sxs-lookup"><span data-stu-id="e35ad-107">Function PdhVbOpenQuery( \_ ByVal QueryHandle As Long \_ ) As Long</span></span>

## <a name="parameters"></a><span data-ttu-id="e35ad-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="e35ad-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e35ad-109">*QueryHandle*</span><span class="sxs-lookup"><span data-stu-id="e35ad-109">*QueryHandle*</span></span> 
</dt> <dd>

<span data-ttu-id="e35ad-110">Variabile cancellata (uguale a 0) prima della chiamata della funzione e, se la funzione ha esito positivo, contiene l'ID univoco della query creata e aperta.</span><span class="sxs-lookup"><span data-stu-id="e35ad-110">Variable that is cleared (equals 0) before the function is called and, if the function is successful, contains the unique ID of the query that is created and opened.</span></span> <span data-ttu-id="e35ad-111">Questo handle viene usato nelle chiamate successive ad altre funzioni PDH per identificare la query.</span><span class="sxs-lookup"><span data-stu-id="e35ad-111">This handle is used in the subsequent calls to other PDH functions to identify the query.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e35ad-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e35ad-112">Return value</span></span>

<span data-ttu-id="e35ad-113">Se la funzione ha esito positivo, restituisce un **Long** Integer uguale a Error \_ Success e un nuovo handle nella variabile *QueryHandle* .</span><span class="sxs-lookup"><span data-stu-id="e35ad-113">If the function succeeds, it returns a **Long** integer equal to ERROR\_SUCCESS and a new handle in the *QueryHandle* variable.</span></span>

<span data-ttu-id="e35ad-114">Se la funzione ha esito negativo, il valore restituito è un [codice di errore di sistema](/windows/desktop/Debug/system-error-codes) o un codice di [errore PDH](pdh-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="e35ad-114">If the function fails, the return value is a [system error code](/windows/desktop/Debug/system-error-codes) or a [PDH error code](pdh-error-codes.md).</span></span> <span data-ttu-id="e35ad-115">Di seguito sono riportati i valori possibili.</span><span class="sxs-lookup"><span data-stu-id="e35ad-115">The following are possible values.</span></span>



| <span data-ttu-id="e35ad-116">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="e35ad-116">Return code</span></span>                                                                                                     | <span data-ttu-id="e35ad-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e35ad-117">Description</span></span>                                                  |
|-----------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------|
| <dl> <span data-ttu-id="e35ad-118"><dt>**\_argomento PDH non valido \_**</dt></span><span class="sxs-lookup"><span data-stu-id="e35ad-118"><dt>**PDH\_INVALID\_ARGUMENT**</dt></span></span> </dl>           | <span data-ttu-id="e35ad-119">L'argomento non è valido o non è corretto.</span><span class="sxs-lookup"><span data-stu-id="e35ad-119">The argument is invalid or incorrect.</span></span><br/>             |
| <dl> <span data-ttu-id="e35ad-120"><dt>**\_errore di \_ allocazione della memoria PDH \_**</dt></span><span class="sxs-lookup"><span data-stu-id="e35ad-120"><dt>**PDH\_MEMORY\_ALLOCATION\_FAILURE**</dt></span></span> </dl> | <span data-ttu-id="e35ad-121">Impossibile allocare un buffer di memoria temporaneo.</span><span class="sxs-lookup"><span data-stu-id="e35ad-121">A temporary memory buffer could not be allocated.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="e35ad-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e35ad-122">Requirements</span></span>



| <span data-ttu-id="e35ad-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="e35ad-123">Requirement</span></span> | <span data-ttu-id="e35ad-124">Valore</span><span class="sxs-lookup"><span data-stu-id="e35ad-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="e35ad-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e35ad-125">Minimum supported client</span></span><br/> | <span data-ttu-id="e35ad-126">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="e35ad-126">Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="e35ad-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e35ad-127">Minimum supported server</span></span><br/> | <span data-ttu-id="e35ad-128">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="e35ad-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="e35ad-129">Libreria</span><span class="sxs-lookup"><span data-stu-id="e35ad-129">Library</span></span><br/>                  | <dl> <span data-ttu-id="e35ad-130"><dt>PDH. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e35ad-130"><dt>Pdh.lib</dt></span></span> </dl> |
| <span data-ttu-id="e35ad-131">DLL</span><span class="sxs-lookup"><span data-stu-id="e35ad-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e35ad-132"><dt>Pdh.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e35ad-132"><dt>Pdh.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e35ad-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e35ad-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e35ad-134">**PdhCloseQuery**</span><span class="sxs-lookup"><span data-stu-id="e35ad-134">**PdhCloseQuery**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhclosequery)
</dt> </dl>

 

