---
description: Restituisce l'elenco dei file di configurazione del backup salvati che è possibile ripristinare.
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
ms.openlocfilehash: 858fb7ee38b7875426ae31172618ad8ac60510ed
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104125838"
---
# <a name="listbackups-method-of-the-control-class"></a>Metodo ListBackups della classe Control

Restituisce l'elenco dei file di configurazione del backup salvati che è possibile ripristinare.

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

*OriginalTimestampLow* \[ out\]
</dt> <dd>

Timestamp di quando è stata impostata la configurazione corrente, se ripristinata dal backup, conterrà il timestamp originale. Questa è la parte bassa di [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).

</dd> <dt>

*OriginalTimestampHigh* \[ out\]
</dt> <dd>

Timestamp di quando è stata impostata la configurazione corrente, se ripristinata dal backup, conterrà il timestamp originale. Si tratta della parte superiore di [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).

</dd> <dt>

*File* \[ out\]
</dt> <dd>

Elenco di file di backup disponibili, in ordine dal più recente al meno recente.

</dd> <dt>

*FilesTimestampLow* \[ out\]
</dt> <dd>

Per ogni file di backup, il timestamp di quando è stata impostata la configurazione. Questa è la parte bassa di [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).

</dd> <dt>

*FilesTimestampHigh* \[ out\]
</dt> <dd>

Per ogni file di backup, il timestamp di quando è stata impostata la configurazione. Si tratta della parte superiore di [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows 10\]<br/>                                                          |
| Server minimo supportato<br/> | Windows Server 2016<br/>                                                                       |
| Spazio dei nomi<br/>                | Radice \\ Microsoft \\ Windows \\ BootEventCollector<br/>                                              |
| MOF<br/>                      | <dl> <dt>BootEventCollectorWMI. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>BEvtCol.exe</dt> </dl>               |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Control**](control.md)
</dt> </dl>

 

