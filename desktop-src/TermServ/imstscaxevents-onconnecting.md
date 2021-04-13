---
title: Metodo OnConnection IMsTscAxEvents
description: Chiamato quando il controllo client inizia a connettersi a un server in risposta a una chiamata a IMsTscAx Connect.
ms.assetid: c5e367a8-126a-48bb-bc94-1063f77e8239
ms.tgt_platform: multiple
keywords:
- Metodo OnConnection Servizi Desktop remoto
- Servizi Desktop remoto del metodo OnConnection, interfaccia IMsTscAxEvents
- Interfaccia IMsTscAxEvents Servizi Desktop remoto, metodo OnConnection
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnConnecting
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2004fde83b79aff7b7c5082562de94f943eacb25
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400232"
---
# <a name="imstscaxeventsonconnecting-method"></a>Metodo IMsTscAxEvents:: OnConnection

Chiamato quando il controllo client inizia a connettersi a un server in risposta a una chiamata a [**IMsTscAx:: Connect**](imstscax-connect.md).

## <a name="syntax"></a>Sintassi


```C++
void OnConnecting();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Implementare questo metodo nel sink di evento per ricevere la notifica che il controllo ha iniziato la connessione.

## <a name="examples"></a>Esempio

Nell'esempio seguente viene illustrato come gestire questo evento con Visual Basic codice di scripting. Il presupposto in questo esempio è che l'oggetto controllo è denominato "MsRdpClient".

Per ulteriori informazioni su Connessione Web Desktop remoto, vedere [requisiti per connessione Web Desktop remoto](requirements-for-remote-desktop-web-connection.md).


```VB
Sub MsRdpClient.OnConnecting()
    Msgbox("Connecting")
End sub
```



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

 

 





