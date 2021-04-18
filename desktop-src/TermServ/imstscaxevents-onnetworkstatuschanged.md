---
title: Metodo IMsTscAxEvents OnNetworkStatusChanged
description: Chiamato quando lo stato della rete è stato modificato. | Metodo IMsTscAxEvents OnNetworkStatusChanged
ms.assetid: 177A410E-2449-4FC7-8DE5-21F83A6DD028
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo OnNetworkStatusChanged
- Metodo OnNetworkStatusChanged Servizi Desktop remoto, interfaccia IMsTscAxEvents
- Interfaccia IMsTscAxEvents Servizi Desktop remoto, metodo OnNetworkStatusChanged
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnNetworkStatusChanged
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2b9bdcd7774493fcc54e1390ad199a6a56a7c51
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "106321185"
---
# <a name="imstscaxeventsonnetworkstatuschanged-method"></a>Metodo IMsTscAxEvents:: OnNetworkStatusChanged

Chiamato quando lo stato della rete è stato modificato.

## <a name="syntax"></a>Sintassi


```C++
void OnNetworkStatusChanged(
  [in] ULONG qualityLevel,
  [in] LONG  bandwidth,
  [in] LONG  rtt
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*qualityLevel* \[ in\]
</dt> <dd>

Specifica la nuova velocità di connessione. Si tratta di uno dei valori seguenti.

<dt>

1
</dt> <dd>

Inferiore a 512 kilobyte al secondo (KBps).

</dd> <dt>

2
</dt> <dd>

da 512 a 1.999 KBps.

</dd> <dt>

3
</dt> <dd>

da 2.000 a 9.999 KBps.

</dd> <dt>

4
</dt> <dd>

Maggiore o uguale a 10.000 KBps.

</dd> </dl> </dd> <dt>

*larghezza di banda* \[ in\]
</dt> <dd>

Specifica la larghezza di banda della connessione.

</dd> <dt>

*RTT* \[ in\]
</dt> <dd>

Specifica la latenza di connessione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 8<br/>                                                                   |
| Server minimo supportato<br/> | Windows Server 2012<br/>                                                         |
| Libreria dei tipi<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IMsTscAxEvents è definito come 336d5562-efa8-482e-8cb3-c5c0fc7a7db6<br/>           |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IMsTscAxEvents**](imstscaxevents-interface.md)
</dt> </dl>

 

 





