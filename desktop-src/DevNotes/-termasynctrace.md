---
description: Termina la traccia.
ms.assetid: e823ed82-1966-4e44-b062-0c8ab0fb5f6e
title: TermAsyncTrace (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TermAsyncTrace
api_type:
- DllExport
api_location:
- Exstrace.dll
ms.openlocfilehash: c8f2ed58115130e141b5fc097965396847ebd147
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331720"
---
# <a name="termasynctrace-function"></a><span data-ttu-id="45a2c-103">TermAsyncTrace (funzione)</span><span class="sxs-lookup"><span data-stu-id="45a2c-103">TermAsyncTrace function</span></span>

<span data-ttu-id="45a2c-104">Termina la traccia.</span><span class="sxs-lookup"><span data-stu-id="45a2c-104">Terminates the trace.</span></span>

## <a name="syntax"></a><span data-ttu-id="45a2c-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="45a2c-105">Syntax</span></span>


```C++
BOOL TermAsyncTrace(void);
```



## <a name="parameters"></a><span data-ttu-id="45a2c-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="45a2c-106">Parameters</span></span>

<span data-ttu-id="45a2c-107">Questa funzione non ha parametri.</span><span class="sxs-lookup"><span data-stu-id="45a2c-107">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="45a2c-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="45a2c-108">Return value</span></span>

<span data-ttu-id="45a2c-109">Questa funzione restituisce **true** se ha esito positivo; in caso contrario, restituisce **false**.</span><span class="sxs-lookup"><span data-stu-id="45a2c-109">This function returns **TRUE** if it succeeds; otherwise, it returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="45a2c-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="45a2c-110">Remarks</span></span>

<span data-ttu-id="45a2c-111">Exstrace.dll è un componente facoltativo che viene installato con il Simple Mail Transfer Protocol (SMTP) e il protocollo NNTP (Network News Transfer Protocol).</span><span class="sxs-lookup"><span data-stu-id="45a2c-111">Exstrace.dll is an optional component that installs with the Simple Mail Transfer Protocol (SMTP) and the Network News Transfer Protocol (NNTP).</span></span>

<span data-ttu-id="45a2c-112">A questa funzione non è associato alcun file di intestazione o libreria di importazione. è necessario chiamarla usando le funzioni [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="45a2c-112">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="45a2c-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="45a2c-113">Requirements</span></span>



| <span data-ttu-id="45a2c-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="45a2c-114">Requirement</span></span> | <span data-ttu-id="45a2c-115">Valore</span><span class="sxs-lookup"><span data-stu-id="45a2c-115">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="45a2c-116">DLL</span><span class="sxs-lookup"><span data-stu-id="45a2c-116">DLL</span></span><br/> | <dl> <span data-ttu-id="45a2c-117"><dt>Exstrace.dll</dt></span><span class="sxs-lookup"><span data-stu-id="45a2c-117"><dt>Exstrace.dll</dt></span></span> </dl> |



 

 
