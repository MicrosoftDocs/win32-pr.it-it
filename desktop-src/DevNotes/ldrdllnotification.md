---
description: Funzione di callback di notifica specificata con la funzione LdrRegisterDllNotification.
ms.assetid: 12202797-c80c-4fa3-9cc4-dcb1a9f01551
title: Funzione di callback LdrDllNotification
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LdrDllNotification
- PLDR_DLL_NOTIFICATION_FUNCTION
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: e1e9bea21cd4e21ca7549ce34343b42c50b293471e69576d7c1164f92a371c62
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118004106"
---
# <a name="ldrdllnotification-callback-function"></a>Funzione di callback LdrDllNotification

\[Questa funzione può essere modificata o rimossa da Windows senza preavviso.\]

Funzione di callback di notifica specificata con la [**funzione LdrRegisterDllNotification.**](ldrregisterdllnotification.md) Il caricatore chiama questa funzione quando viene caricata per la prima volta una DLL.

**Avviso:** Non è sicuro che la funzione di callback di notifica chiami le funzioni in qualsiasi DLL.

## <a name="syntax"></a>Sintassi


```C++
VOID CALLBACK LdrDllNotification(
  _In_     ULONG                       NotificationReason,
  _In_     PCLDR_DLL_NOTIFICATION_DATA NotificationData,
  _In_opt_ PVOID                       Context
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*NotificationReason* \[ Pollici\]
</dt> <dd>

Motivo per cui è stata chiamata la funzione di callback di notifica. Questo parametro può avere uno dei valori seguenti.



| Valore                                                                                                                                                                                                                                                                                        | Significato                                                                                                                               |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <span id="LDR_DLL_NOTIFICATION_REASON_LOADED"></span><span id="ldr_dll_notification_reason_loaded"></span><dl> <dt>**LDR \_ MOTIVO \_ NOTIFICA \_ DLL \_ CARICATO**</dt> <dt>1</dt> </dl>       | La DLL è stata caricata. Il *parametro NotificationData* punta a una struttura **LDR DLL \_ \_ LOADED NOTIFICATION \_ \_ DATA.** <br/>     |
| <span id="LDR_DLL_NOTIFICATION_REASON_UNLOADED"></span><span id="ldr_dll_notification_reason_unloaded"></span><dl> <dt>**LDR \_ MOTIVO \_ NOTIFICA DLL NON \_ \_ CARICATO**</dt> <dt>2</dt> </dl> | La DLL è stata scaricata. Il *parametro NotificationData* punta a una struttura **LDR DLL \_ \_ UNLOADED NOTIFICATION \_ \_ DATA.** <br/> |



 

</dd> <dt>

*NotificationData* \[ Pollici\]
</dt> <dd>

Puntatore a una costante **LDR \_ DLL \_ NOTIFICATION** union che contiene i dati di notifica. Questa unione ha la definizione seguente:

``` syntax
typedef union _LDR_DLL_NOTIFICATION_DATA {
    LDR_DLL_LOADED_NOTIFICATION_DATA Loaded;
    LDR_DLL_UNLOADED_NOTIFICATION_DATA Unloaded;
} LDR_DLL_NOTIFICATION_DATA, *PLDR_DLL_NOTIFICATION_DATA;
```

La **struttura LDR \_ DLL \_ LOADED NOTIFICATION \_ \_ DATA** ha la definizione seguente:

``` syntax
typedef struct _LDR_DLL_LOADED_NOTIFICATION_DATA {
    ULONG Flags;                    //Reserved.
    PCUNICODE_STRING FullDllName;   //The full path name of the DLL module.
    PCUNICODE_STRING BaseDllName;   //The base file name of the DLL module.
    PVOID DllBase;                  //A pointer to the base address for the DLL in memory.
    ULONG SizeOfImage;              //The size of the DLL image, in bytes.
} LDR_DLL_LOADED_NOTIFICATION_DATA, *PLDR_DLL_LOADED_NOTIFICATION_DATA;
```

La **struttura LDR \_ DLL \_ UNLOADED NOTIFICATION \_ \_ DATA** ha la definizione seguente:

``` syntax
typedef struct _LDR_DLL_UNLOADED_NOTIFICATION_DATA {
    ULONG Flags;                    //Reserved.
    PCUNICODE_STRING FullDllName;   //The full path name of the DLL module.
    PCUNICODE_STRING BaseDllName;   //The base file name of the DLL module.
    PVOID DllBase;                  //A pointer to the base address for the DLL in memory.
    ULONG SizeOfImage;              //The size of the DLL image, in bytes.
} LDR_DLL_UNLOADED_NOTIFICATION_DATA, *PLDR_DLL_UNLOADED_NOTIFICATION_DATA;
```

</dd> <dt>

*Contesto* \[ in, facoltativo\]
</dt> <dd>

Puntatore ai dati di contesto per la funzione di callback.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione di callback non restituisce un valore.

## <a name="remarks"></a>Commenti

La funzione di callback di notifica viene chiamata prima che venga eseguito il collegamento dinamico.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>       |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**LdrRegisterDllNotification**](ldrregisterdllnotification.md)
</dt> <dt>

[**LdrUnregisterDllNotification**](ldrunregisterdllnotification.md)
</dt> </dl>

 

 




