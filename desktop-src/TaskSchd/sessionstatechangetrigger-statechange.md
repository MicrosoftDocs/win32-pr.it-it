---
title: Proprietà SessionStateChangeTrigger. StateChange
description: Per la creazione di script, ottiene o imposta il tipo di modifica della sessione di Terminal Server che attiverà l'avvio di un'attività.
ms.assetid: ae1460c7-2939-4fcb-b7fc-edc859596bc4
keywords:
- Utilità di pianificazione proprietà StateChange
- Utilità di pianificazione proprietà StateChange, oggetto SessionStateChangeTrigger
- Oggetto SessionStateChangeTrigger Utilità di pianificazione, proprietà StateChange
topic_type:
- apiref
api_name:
- SessionStateChangeTrigger.StateChange
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac4be561482917788f6afb9b8eb7394cdcce7985
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740615"
---
# <a name="sessionstatechangetriggerstatechange-property"></a><span data-ttu-id="5ede6-106">Proprietà SessionStateChangeTrigger. StateChange</span><span class="sxs-lookup"><span data-stu-id="5ede6-106">SessionStateChangeTrigger.StateChange property</span></span>

<span data-ttu-id="5ede6-107">Per la creazione di script, ottiene o imposta il tipo di modifica della sessione di Terminal Server che attiverà l'avvio di un'attività.</span><span class="sxs-lookup"><span data-stu-id="5ede6-107">For scripting, gets or sets the kind of Terminal Server session change that would trigger a task launch.</span></span>

## <a name="syntax"></a><span data-ttu-id="5ede6-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5ede6-108">Syntax</span></span>


```VB
SessionStateChangeTrigger.StateChange As Integer
```



## <a name="property-value"></a><span data-ttu-id="5ede6-109">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="5ede6-109">Property value</span></span>

<span data-ttu-id="5ede6-110">Tipo di modifica della sessione di Terminal Server che attiva un'attività da avviare.</span><span class="sxs-lookup"><span data-stu-id="5ede6-110">The kind of Terminal Server session change that triggers a task to launch.</span></span>

<span data-ttu-id="5ede6-111">I valori possibili sono dall'enumerazione [**del \_ \_ tipo di \_ modifica \_ dello stato della sessione di attività**](/windows/desktop/api/taskschd/ne-taskschd-task_session_state_change_type) .</span><span class="sxs-lookup"><span data-stu-id="5ede6-111">The possible values are from the [**TASK\_SESSION\_STATE\_CHANGE\_TYPE**](/windows/desktop/api/taskschd/ne-taskschd-task_session_state_change_type) enumeration.</span></span>



| <span data-ttu-id="5ede6-112">Valore</span><span class="sxs-lookup"><span data-stu-id="5ede6-112">Value</span></span>                                                                                                                                                                                                                                               | <span data-ttu-id="5ede6-113">Significato</span><span class="sxs-lookup"><span data-stu-id="5ede6-113">Meaning</span></span>                                                                                                                                                                                          |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TASK_CONSOLE_CONNECT"></span><span id="task_console_connect"></span><dl> <span data-ttu-id="5ede6-114"><dt>**Attività \_ \_Connessione console**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="5ede6-114"><dt>**TASK\_CONSOLE\_CONNECT**</dt> <dt>1</dt></span></span> </dl>          | <span data-ttu-id="5ede6-115">Modifica dello stato di connessione della console Terminal Server.</span><span class="sxs-lookup"><span data-stu-id="5ede6-115">Terminal Server console connection state change.</span></span> <span data-ttu-id="5ede6-116">Ad esempio, quando si esegue la connessione a una sessione utente nel computer locale cambiando gli utenti del computer.</span><span class="sxs-lookup"><span data-stu-id="5ede6-116">For example, when you connect to a user session on the local computer by switching users on the computer.</span></span> <br/>                           |
| <span id="TASK_CONSOLE_DISCONNECT"></span><span id="task_console_disconnect"></span><dl> <span data-ttu-id="5ede6-117"><dt>**Attività \_ \_Disconnessione console**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="5ede6-117"><dt>**TASK\_CONSOLE\_DISCONNECT**</dt> <dt>2</dt></span></span> </dl> | <span data-ttu-id="5ede6-118">Modifica dello stato di disconnessione della console Terminal Server.</span><span class="sxs-lookup"><span data-stu-id="5ede6-118">Terminal Server console disconnection state change.</span></span> <span data-ttu-id="5ede6-119">Ad esempio, quando si esegue la disconnessione a una sessione utente nel computer locale cambiando gli utenti del computer.</span><span class="sxs-lookup"><span data-stu-id="5ede6-119">For example, when you disconnect to a user session on the local computer by switching users on the computer.</span></span><br/>                      |
| <span id="TASK_REMOTE_CONNECT"></span><span id="task_remote_connect"></span><dl> <span data-ttu-id="5ede6-120"><dt>**Attività \_ \_Connessione remota**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="5ede6-120"><dt>**TASK\_REMOTE\_CONNECT**</dt> <dt>3</dt></span></span> </dl>             | <span data-ttu-id="5ede6-121">Terminal Server modifica dello stato della connessione remota.</span><span class="sxs-lookup"><span data-stu-id="5ede6-121">Terminal Server remote connection state change.</span></span> <span data-ttu-id="5ede6-122">Ad esempio, quando un utente si connette a una sessione utente utilizzando il programma Connessione Desktop remoto da un computer remoto.</span><span class="sxs-lookup"><span data-stu-id="5ede6-122">For example, when a user connects to a user session by using the Remote Desktop Connection program from a remote computer.</span></span><br/>            |
| <span id="TASK_REMOTE_DISCONNECT"></span><span id="task_remote_disconnect"></span><dl> <span data-ttu-id="5ede6-123"><dt>**Attività \_ \_Disconnessione remota**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="5ede6-123"><dt>**TASK\_REMOTE\_DISCONNECT**</dt> <dt>4</dt></span></span> </dl>    | <span data-ttu-id="5ede6-124">Terminal Server modifica dello stato di disconnessione remota.</span><span class="sxs-lookup"><span data-stu-id="5ede6-124">Terminal Server remote disconnection state change.</span></span> <span data-ttu-id="5ede6-125">Ad esempio, quando un utente si disconnette da una sessione utente durante l'utilizzo del programma Connessione Desktop remoto da un computer remoto.</span><span class="sxs-lookup"><span data-stu-id="5ede6-125">For example, when a user disconnects from a user session while using the Remote Desktop Connection program from a remote computer.</span></span><br/> |
| <span id="TASK_SESSION_LOCK"></span><span id="task_session_lock"></span><dl> <span data-ttu-id="5ede6-126"><dt>**Attività \_ \_Blocco sessione**</dt> <dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="5ede6-126"><dt>**TASK\_SESSION\_LOCK**</dt> <dt>7</dt></span></span> </dl>                   | <span data-ttu-id="5ede6-127">Modifica dello stato di blocco della sessione Terminal Server.</span><span class="sxs-lookup"><span data-stu-id="5ede6-127">Terminal Server session locked state change.</span></span> <span data-ttu-id="5ede6-128">Ad esempio, questa modifica di stato comporta l'esecuzione dell'attività quando il computer è bloccato.</span><span class="sxs-lookup"><span data-stu-id="5ede6-128">For example, this state change causes the task to run when the computer is locked.</span></span> <br/>                                                      |
| <span id="TASK_SESSION_UNLOCK"></span><span id="task_session_unlock"></span><dl> <span data-ttu-id="5ede6-129"><dt>**Attività \_ \_Sblocco sessione**</dt> <dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="5ede6-129"><dt>**TASK\_SESSION\_UNLOCK**</dt> <dt>8</dt></span></span> </dl>             | <span data-ttu-id="5ede6-130">Modifica dello stato di Terminal Server sessione sbloccata.</span><span class="sxs-lookup"><span data-stu-id="5ede6-130">Terminal Server session unlocked state change.</span></span> <span data-ttu-id="5ede6-131">Ad esempio, questa modifica di stato comporta l'esecuzione dell'attività quando il computer è sbloccato.</span><span class="sxs-lookup"><span data-stu-id="5ede6-131">For example, this state change causes the task to run when the computer is unlocked.</span></span><br/>                                                   |



 

## <a name="requirements"></a><span data-ttu-id="5ede6-132">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5ede6-132">Requirements</span></span>



| <span data-ttu-id="5ede6-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="5ede6-133">Requirement</span></span> | <span data-ttu-id="5ede6-134">Valore</span><span class="sxs-lookup"><span data-stu-id="5ede6-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5ede6-135">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5ede6-135">Minimum supported client</span></span><br/> | <span data-ttu-id="5ede6-136">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="5ede6-136">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="5ede6-137">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5ede6-137">Minimum supported server</span></span><br/> | <span data-ttu-id="5ede6-138">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="5ede6-138">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="5ede6-139">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="5ede6-139">Type library</span></span><br/>             | <dl> <span data-ttu-id="5ede6-140"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="5ede6-140"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="5ede6-141">DLL</span><span class="sxs-lookup"><span data-stu-id="5ede6-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5ede6-142"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5ede6-142"><dt>Taskschd.dll</dt></span></span> </dl> |



 

 





