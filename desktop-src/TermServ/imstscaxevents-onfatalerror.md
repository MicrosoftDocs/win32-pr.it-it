---
title: Metodo IMsTscAxEvents OnFatalError
description: Chiamato quando il controllo client rileva un errore irreversibile.
ms.assetid: 13a5eb2e-d847-4561-b30b-3f23a0579b4d
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo OnFatalError
- Metodo OnFatalError Servizi Desktop remoto, interfaccia IMsTscAxEvents
- Interfaccia IMsTscAxEvents Servizi Desktop remoto, metodo OnFatalError
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnFatalError
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 73402ac178bcb2ac3dc03c0adda092d3b49f6ba3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874077"
---
# <a name="imstscaxeventsonfatalerror-method"></a>Metodo IMsTscAxEvents:: OnFatalError

Chiamato quando il controllo client rileva un errore irreversibile.

## <a name="syntax"></a>Sintassi


```C++
void OnFatalError(
  [in] long errorCode
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

Codice errore  \[ in\]
</dt> <dd>

Indica il codice di errore.

<dt>

<span id="0"></span>

<span id="0"></span>**0**


</dt> <dd>

Si è verificato un errore sconosciuto.

</dd> <dt>

<span id="1"></span>

<span id="1"></span>**1**


</dt> <dd>

Codice di errore interno 1.

</dd> <dt>

<span id="2"></span>

<span id="2"></span>**2**


</dt> <dd>

Si è verificato un errore di memoria insufficiente.

</dd> <dt>

<span id="3"></span>

<span id="3"></span>**3**


</dt> <dd>

Si è verificato un errore di creazione della finestra.

</dd> <dt>

<span id="4"></span>

<span id="4"></span>**4**


</dt> <dd>

Codice di errore interno 2.

</dd> <dt>

<span id="5"></span>

<span id="5"></span>**5**


</dt> <dd>

Codice di errore interno 3. Lo stato non è valido.

</dd> <dt>

<span id="6"></span>

<span id="6"></span>**6**


</dt> <dd>

Codice di errore interno 4.

</dd> <dt>

<span id="7"></span>

<span id="7"></span>**7**


</dt> <dd>

Si è verificato un errore irreversibile durante la connessione client.

</dd> <dt>

<span id="100"></span>

<span id="100"></span>**100**


</dt> <dd>

Errore di inizializzazione Winsock.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

In risposta a questo evento, il contenitore Visualizza un messaggio di errore e si arresta.

Per ulteriori informazioni su Connessione Web Desktop remoto, vedere [requisiti per connessione Web Desktop remoto](requirements-for-remote-desktop-web-connection.md).

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

 

 





