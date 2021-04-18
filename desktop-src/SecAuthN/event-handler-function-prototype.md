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
# <a name="event-handler-function-prototype-callback-function"></a>Funzione di callback del prototipo di funzione del gestore eventi

\[Le funzioni del prototipo del gestore eventi non sono più disponibili per l'uso a partire da Windows Server 2008 e Windows Vista. \]

Le funzioni del prototipo del gestore eventi vengono usate per tutte le funzioni che gestiscono gli eventi di notifica [*Winlogon*](/windows/desktop/SecGloss/w-gly) . Nome della funzione, rappresentato di seguito dal nome della funzione del *\_ gestore eventi \_ \_* del segnaposto, in genere riflette il nome dell'evento gestito dalla funzione. Ad esempio, la funzione che gestisce gli eventi di accesso potrebbe essere denominata: **WLEventLogon**.

## <a name="syntax"></a>Sintassi


```C++
void Event_Handler_Function_Name(
  _In_ PWLX_NOTIFICATION_INFO pInfo
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pInfo* \[ in\]
</dt> <dd>

Puntatore a una struttura [**di \_ \_ informazioni di notifica di WLX**](/windows/desktop/api/Winwlx/ns-winwlx-wlx_notification_info) che contiene i dettagli dell'evento.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione di callback non restituisce un valore.

## <a name="remarks"></a>Commenti

Se il gestore eventi deve creare processi figlio, deve chiamare la funzione [**CreateProcessAsUser ha**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) . In caso contrario, il nuovo processo verrà creato sul desktop di Winlogon, non sul desktop dell'utente.

## <a name="examples"></a>Esempio

Nell'esempio seguente viene illustrato come implementare i gestori eventi per gli eventi Winlogon. Per semplicità, vengono visualizzate solo le implementazioni dei gestori degli eventi di accesso e di disconnessione. È possibile implementare i gestori per il resto degli eventi esattamente allo stesso modo.


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
| Client minimo supportato<br/> | \[Solo app desktop Windows XP\]<br/>          |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/> |
| Fine del supporto client<br/>    | Windows XP<br/>                                |
| Fine del supporto server<br/>    | Windows Server 2003<br/>                       |



 

