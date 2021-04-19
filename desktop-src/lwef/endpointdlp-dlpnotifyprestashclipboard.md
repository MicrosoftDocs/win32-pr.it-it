---
description: Fornisce al sistema informazioni su un documento prima dell'avvio di un'operazione di stash clipboard.
title: Funzione DlpNotifyPreStashClipboard (endpointdlp.h)
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DlpNotifyPreStashClipboard
api_type:
- DllExport
api_location:
- EndpointDlp.dll
ms.openlocfilehash: 72ecabb2bbfb7517b52790c0d3b7c1ab8075dbd0
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/14/2021
ms.locfileid: "107495575"
---
# <a name="dlpnotifyprestashclipboard-function"></a><span data-ttu-id="fd4e3-103">Funzione DlpNotifyPreStashClipboard</span><span class="sxs-lookup"><span data-stu-id="fd4e3-103">DlpNotifyPreStashClipboard function</span></span>

<span data-ttu-id="fd4e3-104">Notifica al sistema prima che venga avviata un'operazione di stash clipboard.</span><span class="sxs-lookup"><span data-stu-id="fd4e3-104">Notifies the system before a stash clipboard operation is initiated.</span></span>

## <a name="syntax"></a><span data-ttu-id="fd4e3-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="fd4e3-105">Syntax</span></span>


```C++
void WINAPI DlpNotifyPreStashClipboard();
```



## <a name="parameters"></a><span data-ttu-id="fd4e3-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="fd4e3-106">Parameters</span></span>




## <a name="return-value"></a><span data-ttu-id="fd4e3-107">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="fd4e3-107">Return value</span></span>

<span data-ttu-id="fd4e3-108">Restituisce void.</span><span class="sxs-lookup"><span data-stu-id="fd4e3-108">Return void.</span></span>

## <a name="remarks"></a><span data-ttu-id="fd4e3-109">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="fd4e3-109">Remarks</span></span>


## <a name="requirements"></a><span data-ttu-id="fd4e3-110">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fd4e3-110">Requirements</span></span>



| <span data-ttu-id="fd4e3-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="fd4e3-111">Requirement</span></span>          |    <span data-ttu-id="fd4e3-112">Valore</span><span class="sxs-lookup"><span data-stu-id="fd4e3-112">Value</span></span>                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fd4e3-113">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fd4e3-113">Minimum supported client</span></span><br/> | <span data-ttu-id="fd4e3-114">Windows 10, versione 1809 (10.0; Build 17763)</span><span class="sxs-lookup"><span data-stu-id="fd4e3-114">Windows 10, version 1809 (10.0; Build 17763)</span></span>           |
| <span data-ttu-id="fd4e3-115">DLL</span><span class="sxs-lookup"><span data-stu-id="fd4e3-115">DLL</span></span><br/>                      | <span data-ttu-id="fd4e3-116">EndpointDlp.dll</span><span class="sxs-lookup"><span data-stu-id="fd4e3-116">EndpointDlp.dll</span></span> |