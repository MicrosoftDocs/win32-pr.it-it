---
description: La funzione ExpertGetStartupInfo recupera le informazioni di configurazione di avvio per l'esperto.
ms.assetid: 15f080ed-50b7-40c6-b283-dbe416a2b0e9
title: Funzione ExpertGetStartupInfo (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ExpertGetStartupInfo
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: f34ecc3d0c3eeb085d2a7c0f8c4cb0426663093c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104401606"
---
# <a name="expertgetstartupinfo-function"></a><span data-ttu-id="35585-103">ExpertGetStartupInfo (funzione)</span><span class="sxs-lookup"><span data-stu-id="35585-103">ExpertGetStartupInfo function</span></span>

<span data-ttu-id="35585-104">La funzione **ExpertGetStartupInfo** recupera le informazioni di configurazione di avvio per l'esperto.</span><span class="sxs-lookup"><span data-stu-id="35585-104">The **ExpertGetStartupInfo** function retrieves the startup configuration information for the expert.</span></span>

## <a name="syntax"></a><span data-ttu-id="35585-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="35585-105">Syntax</span></span>


```C++
DWORD WINAPI ExpertGetStartupInfo(
  _In_  HEXPERTKEY         hExpertKey,
  _Out_ PEXPERTSTARTUPINFO pExpertStartupInfo
);
```



## <a name="parameters"></a><span data-ttu-id="35585-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="35585-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="35585-107">*hExpertKey* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="35585-107">*hExpertKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="35585-108">Identificatore univoco dell'esperto.</span><span class="sxs-lookup"><span data-stu-id="35585-108">Unique expert identifier.</span></span> <span data-ttu-id="35585-109">Network Monitor passa *hExpertKey* all'esperto quando chiama la funzione [Run](run.md) .</span><span class="sxs-lookup"><span data-stu-id="35585-109">Network Monitor passes *hExpertKey* to the expert when it calls the [Run](run.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="35585-110">*pExpertStartupInfo* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="35585-110">*pExpertStartupInfo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="35585-111">Puntatore a una struttura [EXPERTSTARTUPINFO](expertstartupinfo.md) che contiene informazioni di avvio.</span><span class="sxs-lookup"><span data-stu-id="35585-111">Pointer to an [EXPERTSTARTUPINFO](expertstartupinfo.md) structure that contains startup information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="35585-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="35585-112">Return value</span></span>

<span data-ttu-id="35585-113">Se la funzione ha esito positivo, il valore restituito è NMERR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="35585-113">If the function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="35585-114">Se la funzione ha esito negativo, il valore restituito è NMERR.</span><span class="sxs-lookup"><span data-stu-id="35585-114">If the function is unsuccessful, the return value is NMERR.</span></span>

## <a name="remarks"></a><span data-ttu-id="35585-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="35585-115">Remarks</span></span>

<span data-ttu-id="35585-116">La funzione **ExpertGetStartupInfo** viene utilizzata se l'esperto deve determinare le informazioni di avvio utilizzate.</span><span class="sxs-lookup"><span data-stu-id="35585-116">The **ExpertGetStartupInfo** function is used if the expert must determine the startup information that is used.</span></span>

## <a name="requirements"></a><span data-ttu-id="35585-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="35585-117">Requirements</span></span>



| <span data-ttu-id="35585-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="35585-118">Requirement</span></span> | <span data-ttu-id="35585-119">Valore</span><span class="sxs-lookup"><span data-stu-id="35585-119">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="35585-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="35585-120">Minimum supported client</span></span><br/> | <span data-ttu-id="35585-121">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="35585-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="35585-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="35585-122">Minimum supported server</span></span><br/> | <span data-ttu-id="35585-123">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="35585-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="35585-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="35585-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="35585-125"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="35585-125"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="35585-126">Libreria</span><span class="sxs-lookup"><span data-stu-id="35585-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="35585-127"><dt>Nmap. lib</dt></span><span class="sxs-lookup"><span data-stu-id="35585-127"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="35585-128">DLL</span><span class="sxs-lookup"><span data-stu-id="35585-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="35585-129"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="35585-129"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 




