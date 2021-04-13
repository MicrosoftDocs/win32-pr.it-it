---
description: La funzione ExpertSubmitEvent indica che esiste una condizione dell'evento e fornisce una struttura di dati che descrive la condizione.
ms.assetid: 2339b530-427b-4028-aef6-c2cdd1353f77
title: Funzione ExpertSubmitEvent (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ExpertSubmitEvent
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 448d77e9cb009b8aced0aba752526dc08b503066
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104342761"
---
# <a name="expertsubmitevent-function"></a><span data-ttu-id="83611-103">ExpertSubmitEvent (funzione)</span><span class="sxs-lookup"><span data-stu-id="83611-103">ExpertSubmitEvent function</span></span>

<span data-ttu-id="83611-104">La funzione **ExpertSubmitEvent** indica che esiste una condizione dell'evento e fornisce una struttura di dati che descrive la condizione.</span><span class="sxs-lookup"><span data-stu-id="83611-104">The **ExpertSubmitEvent** function indicates that an event condition exists and provides a data structure that describes the condition.</span></span>

## <a name="syntax"></a><span data-ttu-id="83611-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="83611-105">Syntax</span></span>


```C++
DWORD WINAPI ExpertSubmitEvent(
  _In_ HEXPERTKEY   hExpertKey,
  _In_ PNMEVENTDATA pExpertEvent
);
```



## <a name="parameters"></a><span data-ttu-id="83611-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="83611-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="83611-107">*hExpertKey* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="83611-107">*hExpertKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="83611-108">Identificatore univoco dell'esperto.</span><span class="sxs-lookup"><span data-stu-id="83611-108">Unique identifier of the expert.</span></span> <span data-ttu-id="83611-109">Network Monitor passa *hExpertKey* all'esperto quando chiama la funzione [Run](run.md) .</span><span class="sxs-lookup"><span data-stu-id="83611-109">Network Monitor passes *hExpertKey* to the expert when it calls the [Run](run.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="83611-110">*pExpertEvent* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="83611-110">*pExpertEvent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="83611-111">Puntatore a una struttura **NMEVENTDATA** che descrive la condizione dell'evento.</span><span class="sxs-lookup"><span data-stu-id="83611-111">A pointer to an **NMEVENTDATA** structure that describes the event condition.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="83611-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="83611-112">Return value</span></span>

<span data-ttu-id="83611-113">Se la funzione ha esito positivo, il valore restituito è NMERR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="83611-113">If the function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="83611-114">Se la funzione ha esito negativo, il valore restituito indica il motivo dell'errore.</span><span class="sxs-lookup"><span data-stu-id="83611-114">If the function is unsuccessful, the return value indicates the reason for the failure.</span></span> <span data-ttu-id="83611-115">Se il valore restituito è NMERR \_ Expert \_ Terminate, l'esperto viene immediatamente ripulito e restituito.</span><span class="sxs-lookup"><span data-stu-id="83611-115">If the return value is NMERR\_EXPERT\_TERMINATE, the expert immediately cleans up and returns.</span></span>

## <a name="requirements"></a><span data-ttu-id="83611-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="83611-116">Requirements</span></span>



| <span data-ttu-id="83611-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="83611-117">Requirement</span></span> | <span data-ttu-id="83611-118">Valore</span><span class="sxs-lookup"><span data-stu-id="83611-118">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="83611-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="83611-119">Minimum supported client</span></span><br/> | <span data-ttu-id="83611-120">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="83611-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="83611-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="83611-121">Minimum supported server</span></span><br/> | <span data-ttu-id="83611-122">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="83611-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="83611-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="83611-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="83611-124"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="83611-124"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="83611-125">Libreria</span><span class="sxs-lookup"><span data-stu-id="83611-125">Library</span></span><br/>                  | <dl> <span data-ttu-id="83611-126"><dt>Nmap. lib</dt></span><span class="sxs-lookup"><span data-stu-id="83611-126"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="83611-127">DLL</span><span class="sxs-lookup"><span data-stu-id="83611-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="83611-128"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="83611-128"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 




