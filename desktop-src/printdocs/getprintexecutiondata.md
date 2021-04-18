---
description: GetPrintExecutionData Recupera il contesto di stampa corrente.
ms.assetid: bb9506aa-a0da-46bc-a86a-84a79587cd50
title: Funzione GetPrintExecutionData (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetPrintExecutionData
api_type:
- DllExport
api_location:
- winspool.drv
ms.openlocfilehash: a1b2f2674c9ef186338c91ed2e4500d8408964d3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318379"
---
# <a name="getprintexecutiondata-function"></a><span data-ttu-id="c570a-103">GetPrintExecutionData (funzione)</span><span class="sxs-lookup"><span data-stu-id="c570a-103">GetPrintExecutionData function</span></span>

<span data-ttu-id="c570a-104">**GetPrintExecutionData** Recupera il contesto di stampa corrente.</span><span class="sxs-lookup"><span data-stu-id="c570a-104">The **GetPrintExecutionData** retrieves the current print context.</span></span>

> [!Note]  
> <span data-ttu-id="c570a-105">Questa funzione è destinata all'utilizzo da parte di driver della stampante eseguiti nel contesto dello spooler di stampa.</span><span class="sxs-lookup"><span data-stu-id="c570a-105">This function is intended for use by printer drivers that are running in the context of the print spooler.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="c570a-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c570a-106">Syntax</span></span>


```C++
BOOL WINAPI GetPrintExecutionData(
  _Out_ PRINT_EXECUTION_DATA *pData
);
```



## <a name="parameters"></a><span data-ttu-id="c570a-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="c570a-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c570a-108">*pData* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="c570a-108">*pData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c570a-109">Puntatore a una variabile che riceve l'indirizzo della struttura dei [**\_ \_ dati di esecuzione di stampa**](print-execution-data.md) .</span><span class="sxs-lookup"><span data-stu-id="c570a-109">A pointer to a variable that receives the address of the [**PRINT\_EXECUTION\_DATA**](print-execution-data.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c570a-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c570a-110">Return value</span></span>

<span data-ttu-id="c570a-111">Restituisce **true** se la funzione ha esito positivo; in caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="c570a-111">Returns **TRUE** if the function succeeds; otherwise **FALSE**.</span></span> <span data-ttu-id="c570a-112">Se il valore restituito è **false**, chiamare [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) per ottenere lo stato di errore.</span><span class="sxs-lookup"><span data-stu-id="c570a-112">If the return value is **FALSE**, call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) to get the error status.</span></span>

## <a name="remarks"></a><span data-ttu-id="c570a-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="c570a-113">Remarks</span></span>

<span data-ttu-id="c570a-114">I driver della stampante devono chiamare [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) nel modulo winspool. DRV per ottenere l'indirizzo della funzione **GetPrintExecutionData** , perché **GetPrintExecutionData** non è supportato in Windows Vista o nelle versioni precedenti di Windows.</span><span class="sxs-lookup"><span data-stu-id="c570a-114">Printer drivers should call [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) on the winspool.drv module to get the address of the **GetPrintExecutionData** function because **GetPrintExecutionData** is not supported on Windows Vista or earlier versions of Windows.</span></span>

<span data-ttu-id="c570a-115">**GetPrintExecutionData** ha esito negativo solo se il valore di *pData* è **null**.</span><span class="sxs-lookup"><span data-stu-id="c570a-115">**GetPrintExecutionData** only fails if the value of *pData* is **NULL**.</span></span>

<span data-ttu-id="c570a-116">Il valore del membro **clientAppPID** dei [**dati di \_ esecuzione \_ di stampa**](print-execution-data.md) è significativo solo se il valore di **context** è il contesto di **esecuzione di stampa \_ \_ \_ WOW64**.</span><span class="sxs-lookup"><span data-stu-id="c570a-116">The value of the **clientAppPID** member of [**PRINT\_EXECUTION\_DATA**](print-execution-data.md) is only meaningful if the value of **context** is **PRINT\_EXECUTION\_CONTEXT\_WOW64**.</span></span> <span data-ttu-id="c570a-117">Se il valore di **context** non è **il \_ contesto di esecuzione di stampa \_ \_ WOW64**, il valore di **clientAppPID** è 0.</span><span class="sxs-lookup"><span data-stu-id="c570a-117">If the value of **context** is not **PRINT\_EXECUTION\_CONTEXT\_WOW64**, the value of **clientAppPID** is 0.</span></span>

## <a name="requirements"></a><span data-ttu-id="c570a-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c570a-118">Requirements</span></span>



| <span data-ttu-id="c570a-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="c570a-119">Requirement</span></span> | <span data-ttu-id="c570a-120">Valore</span><span class="sxs-lookup"><span data-stu-id="c570a-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c570a-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c570a-121">Minimum supported client</span></span><br/> | <span data-ttu-id="c570a-122">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="c570a-122">Windows 7 \[desktop apps only\]</span></span><br/>                                                                |
| <span data-ttu-id="c570a-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c570a-123">Minimum supported server</span></span><br/> | <span data-ttu-id="c570a-124">Solo app desktop Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="c570a-124">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="c570a-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c570a-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="c570a-126"><dt>Winspool. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c570a-126"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="c570a-127">DLL</span><span class="sxs-lookup"><span data-stu-id="c570a-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c570a-128"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="c570a-128"><dt>Winspool.drv</dt></span></span> </dl>                   |



## <a name="see-also"></a><span data-ttu-id="c570a-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c570a-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c570a-130">**GetLastError**</span><span class="sxs-lookup"><span data-stu-id="c570a-130">**GetLastError**</span></span>](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror)
</dt> <dt>

[<span data-ttu-id="c570a-131">**GetProcAddress**</span><span class="sxs-lookup"><span data-stu-id="c570a-131">**GetProcAddress**</span></span>](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress)
</dt> <dt>

[<span data-ttu-id="c570a-132">**\_contesto di esecuzione di stampa \_**</span><span class="sxs-lookup"><span data-stu-id="c570a-132">**PRINT\_EXECUTION\_CONTEXT**</span></span>](print-execution-context.md)
</dt> <dt>

[<span data-ttu-id="c570a-133">**STAMPA \_ dati di esecuzione \_**</span><span class="sxs-lookup"><span data-stu-id="c570a-133">**PRINT\_EXECUTION\_DATA**</span></span>](print-execution-data.md)
</dt> </dl>

 

