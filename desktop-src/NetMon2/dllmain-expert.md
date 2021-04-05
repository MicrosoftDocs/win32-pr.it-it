---
description: L'esperto implementa la funzione DllMain. Il sistema operativo chiama DllMain per ottenere un handle per un'istanza dell'esperto.
ms.assetid: 38593ba0-dc37-4620-bb49-2e50c3d9ea3c
title: Funzione di callback dell'esperto DllMain (Process. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DllMain
api_type:
- UserDefined
api_location:
- process.h
ms.openlocfilehash: 914f50b75e83fdc67448770b32ac8d0f8e8ab656
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103882914"
---
# <a name="dllmain-expert-callback-function"></a>Funzione di callback Expert DllMain

L'esperto implementa la funzione [**DllMain**](/windows/desktop/Dlls/dllmain) . Il sistema operativo chiama **DllMain** per ottenere un handle per un'istanza dell'esperto.

## <a name="syntax"></a>Sintassi


```C++
BOOL WINAPI DllMain(
  _Out_ HINSTANCE hInstance,
  _In_  ULONG     ulReason,
        LPVOID    Reserved
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*HINSTANCE* \[ out\]
</dt> <dd>

Handle per un'istanza dell'esperto.

Se l'esperto utilizza l'interfaccia utente di Network Monitor, il valore *HINSTANCE* deve essere archiviato in una variabile globale. Questo approccio è necessario solo quando il valore del parametro *ulReason* è impostato su dll \_ Process \_ Connetti.

</dd> <dt>

*ulReason* \[ in\]
</dt> <dd>

Indicatore del motivo per cui è stata chiamata la funzione. Il valore DLL \_ processo di \_ connessione (che si applica quando la dll viene caricata per la prima volta) indica che l'esperto deve salvare il valore *HINSTANCE* in una variabile globale.

Con qualsiasi altro valore, tutte le chiamate alla funzione [**DllMain**](/windows/desktop/Dlls/dllmain) possono essere ignorate. Per un elenco di tutti i flag possibili impostati dal sistema operativo, vedere **DllMain**.

</dd> <dt>

*Reserved* 
</dt> <dd>

Il parametro non è in uso.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è **true**.

Se la funzione ha esito negativo, il valore restituito è **false**.

## <a name="remarks"></a>Commenti

Il sistema operativo chiama la funzione dell'esperto **DllMain** quando un processo carica o Scarica la dll di esperti. La funzione Expert **DllMain** deve essere esportata solo se l'esperto dispone di un'interfaccia utente per la visualizzazione della configurazione o dei risultati, quindi solo per la restituzione del valore *HINSTANCE* corretto.

La funzione dell'esperto **DllMain** è basata sulla funzione [**DllMain**](/windows/desktop/Dlls/dllmain) della libreria a collegamento dinamico.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                           |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                 |
| Intestazione<br/>                   | <dl> <dt>Elabora. h</dt> </dl> |



 

