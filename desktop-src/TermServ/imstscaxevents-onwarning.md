---
title: Metodo IMsTscAxEvents OnWarning
description: Chiamato quando il controllo client rileva una condizione di errore non irreversibile.
ms.assetid: af43d3aa-0ae8-4721-b85d-bb043b20dc40
ms.tgt_platform: multiple
keywords:
- Metodo OnWarning Servizi Desktop remoto
- Metodo OnWarning Servizi Desktop remoto, interfaccia IMsTscAxEvents
- Interfaccia IMsTscAxEvents Servizi Desktop remoto , metodo OnWarning
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnWarning
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bbcebe5c86bb50913ba11d4485f30757f399467aa30730f8cd27de50e360c0cd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119657141"
---
# <a name="imstscaxeventsonwarning-method"></a>Metodo IMsTscAxEvents::OnWarning

Chiamato quando il controllo client rileva una condizione di errore non irreversibile.

## <a name="syntax"></a>Sintassi


```C++
void OnWarning(
  [in] long warningCode
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*warningCode* \[ Pollici\]
</dt> <dd>

Codice di errore.

<dt>

<span id="1"></span>

<span id="1"></span>**1**


</dt> <dd>

La cache bitmap è danneggiata.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Per altre informazioni sui Connessione Web Desktop remoto, vedere [Requisiti per Connessione Web Desktop remoto](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                               |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                         |
| Libreria dei tipi<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IMsTscAxEvents è definito come 336d5562-efa8-482e-8cb3-c5c0fc7a7db6<br/>           |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IMsTscAxEvents**](imstscaxevents-interface.md)
</dt> </dl>

 

 





