---
title: ORPC_DBG_BUFFER struttura
description: La struttura BUFFER DBG ORPC è il formato di buffer usato per il marshalling dei dati RPC ai metodi \_ \_ dell'interfaccia IOrpcDebugNotify.
ms.assetid: 444cd3b8-bc7b-425d-9ccc-04fd6c7393b2
keywords:
- ORPC_DBG_BUFFER struttura COM
- PORPC_DBG_BUFFER struttura com
topic_type:
- apiref
api_name:
- ORPC_DBG_BUFFER
api_location:
- N/A
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7cb1f83cfcbe673cd2d5701e57ae1e94d4e04b59b845cd9ec7b617077da24bb0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118310257"
---
# <a name="orpc_dbg_buffer-structure"></a>Struttura BUFFER \_ DBG ORPC \_

La **struttura BUFFER \_ DBG \_ ORPC** è il formato di buffer usato per il marshalling dei dati RPC ai metodi [**dell'interfaccia IOrpcDebugNotify.**](iorpcdebugnotify.md)

## <a name="syntax"></a>Sintassi


```C++
typedef struct _ORPC_DBG_BUFFER {
  DWORD alwaysOrSometimes;
  BYTE  verMajor;
  BYTE  verMinor;
  DWORD cbRemaining;
  GUID  guidSemantic;
  union {
    BOOL   fStopOnOtherSide;
    USHORT wDebuggingOpCode;
    USHORT cExtent;
    BYTE   padding[2];
    struct {
      ULONG cb;
      GUID  guidExtent;
      BYTE  *rgbData;
    };
  };
} ORPC_DBG_BUFFER, *PORPC_DBG_BUFFER;
```



## <a name="members"></a>Members

<dl> <dt>

**alwaysOrSometimes**
</dt> <dd>

Valore che controlla la generazione del debugger. **alwaysOrSometimes** può essere uno dei valori seguenti:



| Valore                                                                                                                                                                                                                                                                   | Significato                                                                                                                                                                                                                                        |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="ORPC_DEBUG_ALWAYS"></span><span id="orpc_debug_always"></span><dl> <dt>**ORPC \_ DEBUG \_ ALWAYS**</dt> <dt>0X00000000</dt> </dl>                              | Se impostata, COM genererà sempre la notifica client o server sul ricevitore.<br/>                                                                                                                                                    |
| <span id="ORPC_DEBUG_IF_HOOK_ENABLED"></span><span id="orpc_debug_if_hook_enabled"></span><dl> <dt>**ORPC \_ DEBUG \_ IF HOOK ENABLED \_ \_ 0X00000001**</dt> <dt></dt> </dl> | Se impostata, COM genererà la notifica client o server sul ricevitore solo se il debug COM è stato abilitato chiamando [**DllDebugObjectRPCHook**](dlldebugobjectrpchook.md) in tale processo con **fTrace** impostato su **TRUE.** <br/> |



 

</dd> <dt>

**verMajor**
</dt> <dd>

Numero di versione principale della specifica del formato dati.

</dd> <dt>

**verMinor**
</dt> <dd>

Numero di versione secondaria della specifica del formato dati.

</dd> <dt>

**cbRemaining**
</dt> <dd>

Numero di byte, inclusi **cbRemaining**, che seguono in questa struttura .

</dd> <dt>

**guidSemantic**
</dt> <dd>

GUID che determina i membri dell'unione presenti di seguito. **guidSemantic** può assumere uno dei valori seguenti:



| Valore                                                                                                           | Significato                                                                                                                                                                                      |
|-----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>9CADE560-8F43-101A-B07B-00DD01113F11</dt> </dl> | Determina se l'esecuzione di un'unica istruzione deve essere eseguita dal debugger. Di seguito è presente solo il membro **fStopOnOtherSide** dell'unione.<br/>                                             |
| <dl> <dt>D62AEDFA-57EA-11ce-A964-00AA006C3706</dt> </dl> | Determina se i dati con marshalling RPC e i codici operativo di debug vengono passati al ricevitore. Tutti i membri dell'unione sono presenti di seguito, ad eccezione di **fStopOnOtherSide**.<br/> |



 

</dd> <dt>

**fStopOnOtherSide**
</dt> <dd>

Se **TRUE,** l'esecuzione di un'istruzione alla volta viene eseguita dal debugger e deve uscire dal server e continuare l'esecuzione una volta raggiunto l'altro lato. In caso contrario, non viene eseguita una singola istruzione e l'esecuzione del debugger si arresta sull'altro lato.

</dd> <dt>

**wDebuggingOpCode**
</dt> <dd>

Valore che consente di impostare una serie di operazioni. **wDebuggingOpCode** può assumere uno dei valori seguenti:



| Valore                                                                             | Significato                                                                                              |
|-----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| <dl> <dt>0x0000</dt> </dl> | Nessuna operazione.<br/>                                                                             |
| <dl> <dt>0x0001</dt> </dl> | Se impostata, la semantica a passaggio singolo è identica a **fStopOnOtherSide** se impostata su **TRUE.**<br/> |



 

</dd> <dt>

**cExtent**
</dt> <dd>

Imbottitura. Non usare.

</dd> <dt>

**padding**
</dt> <dd>

Imbottitura. Non usare.

</dd> <dt>

**Cb**
</dt> <dd>

Dimensioni, in byte, dei dati in **rgbData.**

</dd> <dt>

**guidExtent**
</dt> <dd>

GUID **che** determina il tipo di dati in **rgbData.** **guidExtent** può assumere uno dei valori seguenti:



| Valore                                                                                                           | Significato                                                   |
|-----------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| <dl> <dt>53199051-57EB-11ce-A964-00AA006C3706</dt> </dl> | **rgbData è** un puntatore a interfaccia con marshalling.<br/> |



 

</dd> <dt>

**rgbData**
</dt> <dd>

Buffer **BYTE** utilizzato per passare dati COM con marshalling RPC tra i debugger client e server. Il contenuto di **rgbData** è determinato dal **GUID** in **guidExtent.**



| GuidExtent Value                     | Contenuto di rgbData                                                                                                                                                                                                                                    |
|--------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 53199051-57EB-11ce-A964-00AA006C3706 | Puntatore a interfaccia con marshalling che risulta dalla chiamata [**a CoMarshalInterface.**](/windows/desktop/api/combaseapi/nf-combaseapi-comarshalinterface) Il puntatore di cui è stato marshalling viene convertito nel puntatore di interfaccia corrispondente [**usando CoUnmarshalInterface.**](/windows/desktop/api/combaseapi/nf-combaseapi-counmarshalinterface) |



 

</dd> </dl>

## <a name="remarks"></a>Commenti

Questi membri di questa struttura hanno un allineamento a 1 byte e vengono sempre trasmessi nell'ordine dei byte little endian.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                     |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                           |
| Intestazione<br/>                   | <dl> <dt>N/D</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ORPC \_ DBG \_ ALL**](orpc-dbg-all.md)
</dt> <dt>

[**ARGOMENTI \_ ORPC INIT \_**](orpc-init-args.md)
</dt> <dt>

[**DllDebugObjectRPCHook**](dlldebugobjectrpchook.md)
</dt> <dt>

[**IOrpcDebugNotify**](iorpcdebugnotify.md)
</dt> </dl>

 

 





