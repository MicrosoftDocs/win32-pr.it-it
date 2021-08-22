---
description: Le funzioni prototipo del gestore eventi vengono usate per tutte le funzioni che gestiscono gli eventi di notifica Winlogon.
ms.assetid: 99b91e80-5e4e-4119-89aa-c0a80fce69e3
title: Funzione di callback Del prototipo di funzione del gestore eventi
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
ms.openlocfilehash: df6670e852ccd12fd2bed1d0c188aa0252c9b3afbcb899cf9480b7011d08625d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119008229"
---
# <a name="event-handler-function-prototype-callback-function"></a>Funzione di callback Del prototipo di funzione del gestore eventi

\[Le funzioni prototipo del gestore eventi non sono più disponibili per l'uso a Windows Server 2008 e Windows Vista. \]

Le funzioni prototipo del gestore eventi vengono usate per tutte le funzioni che gestiscono [*gli eventi di notifica Winlogon.*](/windows/desktop/SecGloss/w-gly) Il nome della funzione, rappresentato di seguito dal segnaposto Nome funzione gestore eventi, riflette in genere il nome dell'evento gestito dalla funzione. *\_ \_ \_* Ad esempio, la funzione che gestisce gli eventi di accesso potrebbe essere denominata **WLEventLogon**.

## <a name="syntax"></a>Sintassi


```C++
void Event_Handler_Function_Name(
  _In_ PWLX_NOTIFICATION_INFO pInfo
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pInfo* \[ Pollici\]
</dt> <dd>

Puntatore a una [**struttura WLX \_ NOTIFICATION \_ INFO**](/windows/desktop/api/Winwlx/ns-winwlx-wlx_notification_info) che contiene i dettagli dell'evento.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione di callback non restituisce un valore.

## <a name="remarks"></a>Commenti

Se il gestore eventi deve creare processi figlio, deve chiamare la [**funzione CreateProcessAsUser.**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) In caso contrario, il nuovo processo verrà creato sul desktop Winlogon, non sul desktop dell'utente.

## <a name="examples"></a>Esempio

L'esempio seguente illustra come implementare i gestori eventi per gli eventi Winlogon. Per semplicità, vengono visualizzate solo le implementazioni dei gestori eventi Logon e Logoff. È possibile implementare gestori per il resto degli eventi esattamente nello stesso modo.


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



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop XP\]<br/>          |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/> |
| Fine del supporto client<br/>    | Windows XP<br/>                                |
| Fine del supporto server<br/>    | Windows Server 2003<br/>                       |



 

