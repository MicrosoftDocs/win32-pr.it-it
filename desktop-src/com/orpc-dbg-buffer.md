---
title: Struttura ORPC_DBG_BUFFER
description: La \_ struttura del \_ buffer dbg ORPC è il formato del buffer usato per i dati RPC con marshalling nei metodi dell'interfaccia IOrpcDebugNotify.
ms.assetid: 444cd3b8-bc7b-425d-9ccc-04fd6c7393b2
keywords:
- COM struttura ORPC_DBG_BUFFER
- Puntatore a struttura PORPC_DBG_BUFFER COM
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
ms.openlocfilehash: 4dc42251b928207a2b009a18c1d88e94dcf1492a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301283"
---
# <a name="orpc_dbg_buffer-structure"></a>\_Struttura del \_ buffer dbg ORPC

La struttura del **\_ \_ buffer dbg ORPC** è il formato del buffer usato per i dati RPC con marshalling nei metodi dell'interfaccia [**IOrpcDebugNotify**](iorpcdebugnotify.md) .

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
| <span id="ORPC_DEBUG_ALWAYS"></span><span id="orpc_debug_always"></span><dl> <dt>**ORPC \_ DEBUG \_ sempre**</dt> <dt>0x00000000</dt> </dl>                              | Se impostato, COM genererà sempre la notifica del client o del server sul ricevitore.<br/>                                                                                                                                                    |
| <span id="ORPC_DEBUG_IF_HOOK_ENABLED"></span><span id="orpc_debug_if_hook_enabled"></span><dl> <dt>**ORPC \_ DEBUG \_ se l' \_ hook è \_ abilitato**</dt> <dt>0x00000001</dt> </dl> | Se impostato, COM genererà solo la notifica client o server sul ricevitore se è stato abilitato il debug COM chiamando [**DllDebugObjectRPCHook**](dlldebugobjectrpchook.md) in tale processo con **FTrace** impostato su **true**. <br/> |



 

</dd> <dt>

**verMajor**
</dt> <dd>

Numero di versione principale della specifica del formato dati.

</dd> <dt>

**VersioneSecondaria**
</dt> <dd>

Numero della versione secondaria della specifica del formato dati.

</dd> <dt>

**cbRemaining**
</dt> <dd>

Numero di byte, inclusi **cbRemaining**, che seguono la struttura.

</dd> <dt>

**guidSemantic**
</dt> <dd>

GUID che determina i membri dell'Unione presenti sotto. **guidSemantic** può assumere uno dei valori seguenti:



| Valore                                                                                                           | Significato                                                                                                                                                                                      |
|-----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>9CADE560-8F43-101A-B07B-00DD01113F11</dt> </dl> | Determina se il debugger deve eseguire l'esecuzione singola. Di seguito è disponibile solo il membro **fStopOnOtherSide** dell'Unione.<br/>                                             |
| <dl> <dt>D62AEDFA-57EA-11ce-A964-00AA006C3706</dt> </dl> | Determina se i dati e i codici operativi di debug RPC vengono passati al ricevitore. Tutti i membri dell'Unione sono presenti di seguito, ad eccezione di **fStopOnOtherSide**.<br/> |



 

</dd> <dt>

**fStopOnOtherSide**
</dt> <dd>

Se il valore è **true**, il debugger esegue un'istruzione/routine singola e deve uscire dal server e continuare l'esecuzione una volta raggiunto l'altro lato. In caso contrario, l'esecuzione di un singolo passo non viene eseguita e l'esecuzione del debugger si interrompe sull'altro lato.

</dd> <dt>

**wDebuggingOpCode**
</dt> <dd>

Valore che consente di specificare una di una serie di operazioni. **wDebuggingOpCode** può assumere uno dei valori seguenti:



| Valore                                                                             | Significato                                                                                              |
|-----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| <dl> <dt>0x0000</dt> </dl> | Nessuna operazione.<br/>                                                                             |
| <dl> <dt>0x0001</dt> </dl> | Se impostata, la semantica del singolo passaggio è identica a **fStopOnOtherSide** quando è impostata su **true**.<br/> |



 

</dd> <dt>

**cExtent**
</dt> <dd>

Imbottitura. Non usare.

</dd> <dt>

**padding**
</dt> <dd>

Imbottitura. Non usare.

</dd> <dt>

**CB**
</dt> <dd>

Dimensioni in byte dei dati in **rgbData**.

</dd> <dt>

**guidExtent**
</dt> <dd>

**GUID** che determina il tipo di dati in **rgbData**. **guidExtent** può assumere uno dei valori seguenti:



| Valore                                                                                                           | Significato                                                   |
|-----------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| <dl> <dt>53199051-57EB-11ce-A964-00AA006C3706</dt> </dl> | **rgbData** è un puntatore a interfaccia con marshalling.<br/> |



 

</dd> <dt>

**rgbData**
</dt> <dd>

Buffer di **byte** utilizzato per passare i dati com con marshalling RPC tra i debugger client e server. Il contenuto di **rgbData** è determinato dal **GUID** in **guidExtent**.



| Valore guidExtent                     | contenuto di rgbData                                                                                                                                                                                                                                    |
|--------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 53199051-57EB-11ce-A964-00AA006C3706 | Puntatore a un'interfaccia con marshalling risultante dalla chiamata a [**CoMarshalInterface**](/windows/desktop/api/combaseapi/nf-combaseapi-comarshalinterface). Il puntatore di marshalling viene convertito nel puntatore a interfaccia corrispondente utilizzando [**CoUnmarshalInterface**](/windows/desktop/api/combaseapi/nf-combaseapi-counmarshalinterface). |



 

</dd> </dl>

## <a name="remarks"></a>Commenti

I membri di questa struttura hanno un allineamento a 1 byte e vengono sempre trasmessi nell'ordine dei byte little-endian.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                     |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                           |
| Intestazione<br/>                   | <dl> <dt>N/D</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ORPC \_ dbg \_ All**](orpc-dbg-all.md)
</dt> <dt>

[**\_argomenti init \_ ORPC**](orpc-init-args.md)
</dt> <dt>

[**DllDebugObjectRPCHook**](dlldebugobjectrpchook.md)
</dt> <dt>

[**IOrpcDebugNotify**](iorpcdebugnotify.md)
</dt> </dl>

 

 





