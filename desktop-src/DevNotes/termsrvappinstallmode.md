---
description: Determina se l'Terminal Server è in modalità di installazione.
ms.assetid: edf362e6-c1a4-49fe-8e07-1188c66616be
title: TermsrvAppInstallMode (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TermsrvAppInstallMode
api_type:
- DllExport
api_location:
- Kernel32.dll
ms.openlocfilehash: f80e51dc417cd637b2abaf8d5dfdc5c0d00f6578
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324861"
---
# <a name="termsrvappinstallmode-function"></a><span data-ttu-id="97f12-103">TermsrvAppInstallMode (funzione)</span><span class="sxs-lookup"><span data-stu-id="97f12-103">TermsrvAppInstallMode function</span></span>

<span data-ttu-id="97f12-104">\[Questa funzione non è supportata e non deve essere utilizzata.</span><span class="sxs-lookup"><span data-stu-id="97f12-104">\[This function is not supported and should not be used.</span></span> <span data-ttu-id="97f12-105">Potrebbe cambiare o scomparire completamente senza preavviso.\]</span><span class="sxs-lookup"><span data-stu-id="97f12-105">It may change or disappear completely without advance notice.\]</span></span>

<span data-ttu-id="97f12-106">Determina se l'Terminal Server è in modalità di installazione.</span><span class="sxs-lookup"><span data-stu-id="97f12-106">Determines whether the Terminal Server is in the INSTALL mode.</span></span>

## <a name="syntax"></a><span data-ttu-id="97f12-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="97f12-107">Syntax</span></span>


```C++
BOOL TermsrvAppInstallMode(void);
```



## <a name="parameters"></a><span data-ttu-id="97f12-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="97f12-108">Parameters</span></span>

<span data-ttu-id="97f12-109">Questa funzione non ha parametri.</span><span class="sxs-lookup"><span data-stu-id="97f12-109">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="97f12-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="97f12-110">Return value</span></span>

<span data-ttu-id="97f12-111">Questa funzione restituisce **true** se il Terminal Server è in modalità di installazione e **false** se è in modalità di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="97f12-111">This function returns **TRUE** if the Terminal Server is in INSTALL mode and **FALSE** if it is in EXECUTE mode.</span></span>

## <a name="requirements"></a><span data-ttu-id="97f12-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="97f12-112">Requirements</span></span>



| <span data-ttu-id="97f12-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="97f12-113">Requirement</span></span> | <span data-ttu-id="97f12-114">Valore</span><span class="sxs-lookup"><span data-stu-id="97f12-114">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="97f12-115">DLL</span><span class="sxs-lookup"><span data-stu-id="97f12-115">DLL</span></span><br/> | <dl> <span data-ttu-id="97f12-116"><dt>Kernel32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="97f12-116"><dt>Kernel32.dll</dt></span></span> </dl> |



 

 




