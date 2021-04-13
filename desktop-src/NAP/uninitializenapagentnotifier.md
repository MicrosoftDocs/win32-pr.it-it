---
title: Funzione UninitializeNapAgentNotifier (NapUtil. h)
description: Annulla la sottoscrizione del processo chiamante dalle notifiche di modifica dello stato NapAgent e quarantena.
ms.assetid: b676ee33-caf6-48f0-acf8-5be1b23c62fe
keywords:
- NAP funzione UninitializeNapAgentNotifier
topic_type:
- apiref
api_name:
- UninitializeNapAgentNotifier
api_location:
- qutil.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b5d68b43fba64be82908d73803113f871b08c93c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400486"
---
# <a name="uninitializenapagentnotifier-function"></a><span data-ttu-id="af3de-104">UninitializeNapAgentNotifier (funzione)</span><span class="sxs-lookup"><span data-stu-id="af3de-104">UninitializeNapAgentNotifier function</span></span>

> [!Note]  
> <span data-ttu-id="af3de-105">La piattaforma protezione accesso alla rete non è disponibile a partire da Windows 10</span><span class="sxs-lookup"><span data-stu-id="af3de-105">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="af3de-106">La funzione **UninitializeNapAgentNotifier** Annulla la sottoscrizione del processo chiamante dalle notifiche di modifica dello stato di napagent e dalla quarantena.</span><span class="sxs-lookup"><span data-stu-id="af3de-106">The **UninitializeNapAgentNotifier** function unsubscribes the calling process from NapAgent state change notifications and quarantine state change notifications.</span></span> <span data-ttu-id="af3de-107">Queste notifiche vengono fornite dal servizio NapAgent.</span><span class="sxs-lookup"><span data-stu-id="af3de-107">These notifications are provided by the NapAgent service.</span></span>

## <a name="syntax"></a><span data-ttu-id="af3de-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="af3de-108">Syntax</span></span>


```C++
NAPAPI VOID WINAPI UninitializeNapAgentNotifier(
  _In_ NapNotifyType type
);
```



## <a name="parameters"></a><span data-ttu-id="af3de-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="af3de-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="af3de-110">*tipo* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="af3de-110">*type* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="af3de-111">Valore [**NapNotifyType**](/windows/win32/api/naptypes/ne-naptypes-napnotifytype) che specifica il tipo di notifiche del servizio da cui annullare la sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="af3de-111">A [**NapNotifyType**](/windows/win32/api/naptypes/ne-naptypes-napnotifytype) value that specifies the type of service notifications to unsubscribe from.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="af3de-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="af3de-112">Return value</span></span>

<span data-ttu-id="af3de-113">Questa funzione non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="af3de-113">This function has no return values.</span></span>

## <a name="remarks"></a><span data-ttu-id="af3de-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="af3de-114">Remarks</span></span>

<span data-ttu-id="af3de-115">Questa funzione non è thread-safe.</span><span class="sxs-lookup"><span data-stu-id="af3de-115">This function is not thread safe.</span></span>

<span data-ttu-id="af3de-116">Ogni processo sottoscritto per le notifiche del servizio NapAgent del *tipo* specificato deve chiamare **UninitializeNapAgentNotifier** per annullare la sottoscrizione alle notifiche.</span><span class="sxs-lookup"><span data-stu-id="af3de-116">Each process subscribed to NapAgent service notifications of the specified *type* must call **UninitializeNapAgentNotifier** to unsubscribe from notifications.</span></span> <span data-ttu-id="af3de-117">Se un processo viene sottoscritto a più di un tipo di notifica, deve chiamare **UninitializeNapAgentNotifier** una volta per ogni tipo di notifica.</span><span class="sxs-lookup"><span data-stu-id="af3de-117">If a process is subscribed to more than one type of notification, it must call **UninitializeNapAgentNotifier** once for each type of notification.</span></span>

<span data-ttu-id="af3de-118">Questa funzione avrà esito negativo automaticamente se il processo non era stato precedentemente chiamato [**InitializeNapAgentNotifier**](initializenapagentnotifier.md) per il tipo di notifica.</span><span class="sxs-lookup"><span data-stu-id="af3de-118">This function will fail silently if the process had not previously called [**InitializeNapAgentNotifier**](initializenapagentnotifier.md) for the notification type.</span></span>

## <a name="requirements"></a><span data-ttu-id="af3de-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="af3de-119">Requirements</span></span>



| <span data-ttu-id="af3de-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="af3de-120">Requirement</span></span> | <span data-ttu-id="af3de-121">Valore</span><span class="sxs-lookup"><span data-stu-id="af3de-121">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="af3de-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="af3de-122">Minimum supported client</span></span><br/> | <span data-ttu-id="af3de-123">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="af3de-123">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="af3de-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="af3de-124">Minimum supported server</span></span><br/> | <span data-ttu-id="af3de-125">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="af3de-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="af3de-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="af3de-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="af3de-127"><dt>NapUtil. h</dt></span><span class="sxs-lookup"><span data-stu-id="af3de-127"><dt>NapUtil.h</dt></span></span> </dl> |
| <span data-ttu-id="af3de-128">DLL</span><span class="sxs-lookup"><span data-stu-id="af3de-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="af3de-129"><dt>Qutil.dll</dt></span><span class="sxs-lookup"><span data-stu-id="af3de-129"><dt>Qutil.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="af3de-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="af3de-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="af3de-131">**InitializeNapAgentNotifier**</span><span class="sxs-lookup"><span data-stu-id="af3de-131">**InitializeNapAgentNotifier**</span></span>](initializenapagentnotifier.md)
</dt> </dl>

 

 





