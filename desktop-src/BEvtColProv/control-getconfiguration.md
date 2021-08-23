---
description: Leggere la configurazione attiva dell'agente di raccolta.
ms.assetid: ea26142d-5dcd-466d-b9df-5349f58a190f
ms.tgt_platform: multiple
title: Metodo GetConfiguration della classe Control
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Control.GetConfiguration
api_type:
- COM
api_location:
- BEvtCol.exe
ms.openlocfilehash: a877b4ae061b6568b877d9b8ee65b8d9b0380a012d7fdba28408ad4bfcae7030
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119579721"
---
# <a name="getconfiguration-method-of-the-control-class"></a>Metodo GetConfiguration della classe Control

Leggere la configurazione attiva dell'agente di raccolta.

## <a name="syntax"></a>Sintassi


```mof
Uint32 GetConfiguration(
  [out] Uint32 TimestampLow,
  [out] Uint32 TimestampHigh
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*TimestampLow* \[ Cambio\]
</dt> <dd>

Quando questo metodo viene restituito, questo parametro contiene i bit di ordine basso di un timestamp che indica quando è stata impostata la configurazione.

</dd> <dt>

*TimestampHigh* \[ Cambio\]
</dt> <dd>

Quando questo metodo viene restituito, questo parametro contiene i bit più elevati di un timestamp che indica quando è stata impostata la configurazione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

<dl> <dt>


</dt> <dd>

0

Errore

</dd> <dt>


</dt> <dd>

1

Operazione completata

</dd> </dl>

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

 

 




