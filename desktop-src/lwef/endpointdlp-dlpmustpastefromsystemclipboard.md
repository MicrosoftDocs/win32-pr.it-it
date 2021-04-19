---
description: Determina se l'app deve eseguire il pull dei dati dagli Appunti di sistema anziché dalla cache interna.
title: Funzione DlpMustPasteFromSystemClipboard (endpointdlp.h)
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DlpMustPasteFromSystemClipboard
api_type:
- DllExport
api_location:
- EndpointDlp.dll
ms.openlocfilehash: 5863173b02cb5c63a2de46653c2d268464e82e65
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/14/2021
ms.locfileid: "107495728"
---
# <a name="dlpmustpastefromsystemclipboard-function"></a><span data-ttu-id="264bb-103">Funzione DlpMustPasteFromSystemClipboard</span><span class="sxs-lookup"><span data-stu-id="264bb-103">DlpMustPasteFromSystemClipboard function</span></span>

<span data-ttu-id="264bb-104">Determina se l'app deve eseguire il pull dei dati dagli Appunti di sistema anziché dalla cache interna.</span><span class="sxs-lookup"><span data-stu-id="264bb-104">Determines whether the app must pull the data from the system clipboard rather than taking it from its internal cache.</span></span>

## <a name="syntax"></a><span data-ttu-id="264bb-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="264bb-105">Syntax</span></span>


```C++
BOOL WINAPI DlpMustPasteFromSystemClipboard();
```


## <a name="return-value"></a><span data-ttu-id="264bb-106">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="264bb-106">Return value</span></span>

<span data-ttu-id="264bb-107">TRUE se la chiamata negli Appunti del sistema operativo è obbligatoria; in caso contrario, FALSE.</span><span class="sxs-lookup"><span data-stu-id="264bb-107">TRUE if calling into the OS clipboard is mandatory; otherwise, FALSE.</span></span>

## <a name="remarks"></a><span data-ttu-id="264bb-108">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="264bb-108">Remarks</span></span>


## <a name="requirements"></a><span data-ttu-id="264bb-109">Requisiti</span><span class="sxs-lookup"><span data-stu-id="264bb-109">Requirements</span></span>



| <span data-ttu-id="264bb-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="264bb-110">Requirement</span></span>          |    <span data-ttu-id="264bb-111">Valore</span><span class="sxs-lookup"><span data-stu-id="264bb-111">Value</span></span>                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="264bb-112">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="264bb-112">Minimum supported client</span></span><br/> | <span data-ttu-id="264bb-113">Windows 10, versione 1809 (10.0; Build 17763)</span><span class="sxs-lookup"><span data-stu-id="264bb-113">Windows 10, version 1809 (10.0; Build 17763)</span></span>           |
| <span data-ttu-id="264bb-114">DLL</span><span class="sxs-lookup"><span data-stu-id="264bb-114">DLL</span></span><br/>                      | <span data-ttu-id="264bb-115">EndpointDlp.dll</span><span class="sxs-lookup"><span data-stu-id="264bb-115">EndpointDlp.dll</span></span> |