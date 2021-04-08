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
ms.openlocfilehash: e29cd7b17c634250f56cbafcf86379449ac88199
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103877218"
---
# <a name="ldrdllnotification-callback-function"></a>Funzione di callback LdrDllNotification

\[Questa funzione può essere modificata o rimossa da Windows senza ulteriore preavviso.\]

Funzione di callback di notifica specificata con la funzione [**LdrRegisterDllNotification**](ldrregisterdllnotification.md) . Il caricatore chiama questa funzione quando una DLL viene caricata per la prima volta.

**Avviso:** Non è sicuro che la funzione di callback delle notifiche chiami le funzioni in qualsiasi DLL.

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

*NotificationReason* \[ in\]
</dt> <dd>

Motivo per cui è stata chiamata la funzione di callback di notifica. Questo parametro può avere uno dei valori seguenti.



| Valore                                                                                                                                                                                                                                                                                        | Significato                                                                                                                               |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <span id="LDR_DLL_NOTIFICATION_REASON_LOADED"></span><span id="ldr_dll_notification_reason_loaded"></span><dl> <dt>**LDR \_ \_Motivo della notifica dll \_ \_ caricato**</dt> <dt>1</dt> </dl>       | La DLL è stata caricata. Il parametro *NotificationData* punta a una struttura di **\_ \_ \_ \_ dati di notifica caricata dalla dll LDR** . <br/>     |
| <span id="LDR_DLL_NOTIFICATION_REASON_UNLOADED"></span><span id="ldr_dll_notification_reason_unloaded"></span><dl> <dt>**LDR \_ \_Motivo della notifica dll \_ \_ scaricato**</dt> <dt>2</dt> </dl> | La DLL è stata scaricata. Il parametro *NotificationData* punta a una struttura di dati di **\_ \_ \_ notifica non \_ caricata della dll LDR** . <br/> |



 

</dd> <dt>

*NotificationData* \[ in\]
</dt> <dd>

Puntatore a un'Unione di **\_ \_ notifiche della dll LDR** costante che contiene i dati di notifica. Questa Unione presenta la definizione seguente:

``` syntax
typedef union _LDR_DLL_NOTIFICATION_DATA {
    LDR_DLL_LOADED_NOTIFICATION_DATA Loaded;
    LDR_DLL_UNLOADED_NOTIFICATION_DATA Unloaded;
} LDR_DLL_NOTIFICATION_DATA, *PLDR_DLL_NOTIFICATION_DATA;
```

La **struttura \_ \_ \_ \_ dei dati di notifica caricati della dll LDR** presenta la seguente definizione:

``` syntax
typedef struct _LDR_DLL_LOADED_NOTIFICATION_DATA {
    ULONG Flags;                    //Reserved.
    PCUNICODE_STRING FullDllName;   //The full path name of the DLL module.
    PCUNICODE_STRING BaseDllName;   //The base file name of the DLL module.
    PVOID DllBase;                  //A pointer to the base address for the DLL in memory.
    ULONG SizeOfImage;              //The size of the DLL image, in bytes.
} LDR_DLL_LOADED_NOTIFICATION_DATA, *PLDR_DLL_LOADED_NOTIFICATION_DATA;
```

La **struttura \_ \_ \_ \_ dei dati di notifica di LDR dll non caricata** presenta la seguente definizione:

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

La funzione di callback delle notifiche viene chiamata prima che venga eseguita la connessione dinamica.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>       |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**LdrRegisterDllNotification**](ldrregisterdllnotification.md)
</dt> <dt>

[**LdrUnregisterDllNotification**](ldrunregisterdllnotification.md)
</dt> </dl>

 

 




