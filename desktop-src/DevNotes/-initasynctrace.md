---
description: Inizializza la traccia.
ms.assetid: d2708e29-920d-4b13-8917-a6f2065ba58c
title: InitAsyncTrace (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InitAsyncTrace
api_type:
- DllExport
api_location:
- Exstrace.dll
ms.openlocfilehash: f79137fe4e832a193bafa59a573e5eb541884a2c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325691"
---
# <a name="initasynctrace-function"></a><span data-ttu-id="d3c9a-103">InitAsyncTrace (funzione)</span><span class="sxs-lookup"><span data-stu-id="d3c9a-103">InitAsyncTrace function</span></span>

<span data-ttu-id="d3c9a-104">Inizializza la traccia.</span><span class="sxs-lookup"><span data-stu-id="d3c9a-104">Initializes the trace.</span></span>

## <a name="syntax"></a><span data-ttu-id="d3c9a-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d3c9a-105">Syntax</span></span>


```C++
BOOL InitAsyncTrace(void);
```



## <a name="parameters"></a><span data-ttu-id="d3c9a-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="d3c9a-106">Parameters</span></span>

<span data-ttu-id="d3c9a-107">Questa funzione non ha parametri.</span><span class="sxs-lookup"><span data-stu-id="d3c9a-107">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="d3c9a-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d3c9a-108">Return value</span></span>

<span data-ttu-id="d3c9a-109">Questa funzione restituisce **true** se la funzione ha esito positivo; in caso contrario, restituisce **false**.</span><span class="sxs-lookup"><span data-stu-id="d3c9a-109">This function returns **TRUE** if the function succeeds; otherwise, it returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="d3c9a-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="d3c9a-110">Remarks</span></span>

<span data-ttu-id="d3c9a-111">Exstrace.dll è un componente facoltativo che viene installato con il Simple Mail Transfer Protocol (SMTP) e il protocollo NNTP (Network News Transfer Protocol).</span><span class="sxs-lookup"><span data-stu-id="d3c9a-111">Exstrace.dll is an optional component that installs with the Simple Mail Transfer Protocol (SMTP) and the Network News Transfer Protocol (NNTP).</span></span>

<span data-ttu-id="d3c9a-112">A questa funzione non è associato alcun file di intestazione o libreria di importazione. è necessario chiamarla usando le funzioni [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="d3c9a-112">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="d3c9a-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d3c9a-113">Requirements</span></span>



| <span data-ttu-id="d3c9a-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="d3c9a-114">Requirement</span></span> | <span data-ttu-id="d3c9a-115">Valore</span><span class="sxs-lookup"><span data-stu-id="d3c9a-115">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d3c9a-116">DLL</span><span class="sxs-lookup"><span data-stu-id="d3c9a-116">DLL</span></span><br/> | <dl> <span data-ttu-id="d3c9a-117"><dt>Exstrace.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d3c9a-117"><dt>Exstrace.dll</dt></span></span> </dl> |



 

 
