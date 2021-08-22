---
description: Restituisce l'elenco dei file di configurazione di backup salvati che possono essere ripristinati.
ms.assetid: 9487c50e-ef3b-425f-92ef-0614290e9af4
ms.tgt_platform: multiple
title: Metodo ListBackups della classe Control
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Control.ListBackups
api_type:
- COM
api_location:
- BEvtCol.exe
ms.openlocfilehash: ba6a3f042a6bd8f01e4bede00e22bda95ca28ebe7cc2beb33a12c6b49deba6bf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119589121"
---
# <a name="listbackups-method-of-the-control-class"></a>Metodo ListBackups della classe Control

Restituisce l'elenco dei file di configurazione di backup salvati che possono essere ripristinati.

## <a name="syntax"></a>Sintassi


```mof
void ListBackups(
  [out] Uint32 OriginalTimestampLow,
  [out] Uint32 OriginalTimestampHigh,
  [out] string Files[],
  [out] Uint32 FilesTimestampLow[],
  [out] Uint32 FilesTimestampHigh[]
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*OriginalTimestampLow* \[ Cambio\]
</dt> <dd>

Timestamp di quando è stata impostata la configurazione corrente (se ripristinata dal backup, conterrà il timestamp originale). Questa è la parte bassa di [**FILETIME.**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime)

</dd> <dt>

*OriginalTimestampHigh* \[ Cambio\]
</dt> <dd>

Timestamp di quando è stata impostata la configurazione corrente (se ripristinata dal backup, conterrà il timestamp originale). Questa è la parte più importante di [**FILETIME.**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime)

</dd> <dt>

*File* \[ Cambio\]
</dt> <dd>

Elenco dei file di backup disponibili, in ordine dal più recente al meno recente.

</dd> <dt>

*FilesTimestampLow* \[ Cambio\]
</dt> <dd>

Per ogni file di backup, timestamp di quando è stata impostata la relativa configurazione. Questa è la parte bassa di [**FILETIME.**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime)

</dd> <dt>

*FilesTimestampHigh* \[ Cambio\]
</dt> <dd>

Per ogni file di backup, timestamp di quando è stata impostata la relativa configurazione. Questa è la parte più importante di [**FILETIME.**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 10 solo app desktop\]<br/>                                                          |
| Server minimo supportato<br/> | Windows Server 2016<br/>                                                                       |
| Spazio dei nomi<br/>                | Root \\ Microsoft \\ Windows \\ BootEventCollector<br/>                                              |
| MOF<br/>                      | <dl> <dt>BootEventCollectorWMI.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>BEvtCol.exe</dt> </dl>               |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Control**](control.md)
</dt> </dl>

 

