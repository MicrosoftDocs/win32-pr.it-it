---
description: Le funzioni del prototipo del gestore eventi vengono usate per tutte le funzioni che gestiscono gli eventi di notifica Winlogon.
ms.assetid: 99b91e80-5e4e-4119-89aa-c0a80fce69e3
title: Funzione di callback del prototipo di funzione del gestore eventi
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Event_Handler_Function_Name
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: 935ddac5660c814b898be17218d879678f2135ac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317083"
---
# <a name="event-handler-function-prototype-callback-function"></a><span data-ttu-id="3575b-103">Funzione di callback del prototipo di funzione del gestore eventi</span><span class="sxs-lookup"><span data-stu-id="3575b-103">Event Handler Function Prototype callback function</span></span>

<span data-ttu-id="3575b-104">\[Le funzioni del prototipo del gestore eventi non sono più disponibili per l'uso a partire da Windows Server 2008 e Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="3575b-104">\[Event Handler Prototype functions are no longer available for use as of Windows Server 2008 and Windows Vista.</span></span> <span data-ttu-id="3575b-105">\]</span><span class="sxs-lookup"><span data-stu-id="3575b-105">\]</span></span>

<span data-ttu-id="3575b-106">Le funzioni del prototipo del gestore eventi vengono usate per tutte le funzioni che gestiscono gli eventi di notifica [*Winlogon*](/windows/desktop/SecGloss/w-gly) .</span><span class="sxs-lookup"><span data-stu-id="3575b-106">Event Handler Prototype functions are used for all functions that handle [*Winlogon*](/windows/desktop/SecGloss/w-gly) notification events.</span></span> <span data-ttu-id="3575b-107">Nome della funzione, rappresentato di seguito dal nome della funzione del *\_ gestore eventi \_ \_* del segnaposto, in genere riflette il nome dell'evento gestito dalla funzione.</span><span class="sxs-lookup"><span data-stu-id="3575b-107">The name of the function, represented below by the place holder *Event\_Handler\_Function\_Name*, typically reflects the name of the event that the function handles.</span></span> <span data-ttu-id="3575b-108">Ad esempio, la funzione che gestisce gli eventi di accesso potrebbe essere denominata: **WLEventLogon**.</span><span class="sxs-lookup"><span data-stu-id="3575b-108">For example, the function that handles logon events might be named: **WLEventLogon**.</span></span>

## <a name="syntax"></a><span data-ttu-id="3575b-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3575b-109">Syntax</span></span>


```C++
void Event_Handler_Function_Name(
  _In_ PWLX_NOTIFICATION_INFO pInfo
);
```



## <a name="parameters"></a><span data-ttu-id="3575b-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="3575b-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3575b-111">*pInfo* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3575b-111">*pInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3575b-112">Puntatore a una struttura [**di \_ \_ informazioni di notifica di WLX**](/windows/desktop/api/Winwlx/ns-winwlx-wlx_notification_info) che contiene i dettagli dell'evento.</span><span class="sxs-lookup"><span data-stu-id="3575b-112">A pointer to a [**WLX\_NOTIFICATION\_INFO**](/windows/desktop/api/Winwlx/ns-winwlx-wlx_notification_info) structure that contains the details of the event.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3575b-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3575b-113">Return value</span></span>

<span data-ttu-id="3575b-114">Questa funzione di callback non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="3575b-114">This callback function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="3575b-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="3575b-115">Remarks</span></span>

<span data-ttu-id="3575b-116">Se il gestore eventi deve creare processi figlio, deve chiamare la funzione [**CreateProcessAsUser ha**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) .</span><span class="sxs-lookup"><span data-stu-id="3575b-116">If your event handler needs to create child processes, it should call the [**CreateProcessAsUser**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) function.</span></span> <span data-ttu-id="3575b-117">In caso contrario, il nuovo processo verrà creato sul desktop di Winlogon, non sul desktop dell'utente.</span><span class="sxs-lookup"><span data-stu-id="3575b-117">Otherwise, the new process will be created on the Winlogon desktop, not the user's desktop.</span></span>

## <a name="examples"></a><span data-ttu-id="3575b-118">Esempio</span><span class="sxs-lookup"><span data-stu-id="3575b-118">Examples</span></span>

<span data-ttu-id="3575b-119">Nell'esempio seguente viene illustrato come implementare i gestori eventi per gli eventi Winlogon.</span><span class="sxs-lookup"><span data-stu-id="3575b-119">The following sample shows how to implement event handlers for Winlogon events.</span></span> <span data-ttu-id="3575b-120">Per semplicità, vengono visualizzate solo le implementazioni dei gestori degli eventi di accesso e di disconnessione.</span><span class="sxs-lookup"><span data-stu-id="3575b-120">For simplicity, only the implementations of the Logon and Logoff event handlers are shown.</span></span> <span data-ttu-id="3575b-121">È possibile implementare i gestori per il resto degli eventi esattamente allo stesso modo.</span><span class="sxs-lookup"><span data-stu-id="3575b-121">You can implement handlers for the rest of the events in exactly the same manner.</span></span>


```C++
// Copyright (C) Microsoft. All rights reserved. 
#include <windows.h>

// Here is the entrance function for the DLL.
BOOL WINAPI LibMain(HINSTANCE hInstance, DWORD dwReason, LPVOID lpReserved)
{
    switch (dwReason)
    {
        case DLL_PROCESS_ATTACH:
            {

             // Disable DLL_THREAD_ATTACH & DLL_THREAD_DETACH
             // notification calls. This is a performance optimization
             // for multithreaded applications that do not need 
             // thread-level notifications of attachment or
             // detachment.

            DisableThreadLibraryCalls (hInstance);
            }
            break;
    }

    return TRUE;
}

// Here is the event handler for the Winlogon Logon event.
void WLEventLogon (PWLX_NOTIFICATION_INFO pInfo)
{

    // Print the name of the handler to debug output.
    // You can replace this with more useful functionality.
    OutputDebugString (TEXT("NOTIFY:  Entering WLEventLogon.\r\n"));
}

// Here is the event handler for the Winlogon Logoff event.
void WLEventLogoff (PWLX_NOTIFICATION_INFO pInfo)
{

    // Print the name of the handler to debug output.
    // You can replace this with more useful functionality.
    OutputDebugString (TEXT("NOTIFY:  Entering WLEventLogff.\r\n"));
}
```



## <a name="requirements"></a><span data-ttu-id="3575b-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3575b-122">Requirements</span></span>



| <span data-ttu-id="3575b-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="3575b-123">Requirement</span></span> | <span data-ttu-id="3575b-124">Valore</span><span class="sxs-lookup"><span data-stu-id="3575b-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="3575b-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3575b-125">Minimum supported client</span></span><br/> | <span data-ttu-id="3575b-126">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="3575b-126">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="3575b-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3575b-127">Minimum supported server</span></span><br/> | <span data-ttu-id="3575b-128">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="3575b-128">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="3575b-129">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="3575b-129">End of client support</span></span><br/>    | <span data-ttu-id="3575b-130">Windows XP</span><span class="sxs-lookup"><span data-stu-id="3575b-130">Windows XP</span></span><br/>                                |
| <span data-ttu-id="3575b-131">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="3575b-131">End of server support</span></span><br/>    | <span data-ttu-id="3575b-132">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="3575b-132">Windows Server 2003</span></span><br/>                       |



 

