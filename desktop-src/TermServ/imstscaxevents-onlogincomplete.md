---
title: Metodo IMsTscAxEvents OnLoginComplete
description: Chiamato quando il controllo client ha effettuato l'accesso a un server di host sessione Desktop remoto (host sessione Desktop remoto), dopo la visualizzazione della finestra di dialogo di accesso di Windows.
ms.assetid: acb345a6-3153-4b8f-ac51-fe0c19fa750a
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo OnLoginComplete
- Metodo OnLoginComplete Servizi Desktop remoto, interfaccia IMsTscAxEvents
- Interfaccia IMsTscAxEvents Servizi Desktop remoto, metodo OnLoginComplete
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnLoginComplete
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 74d6b63f74ed99c8af939bafdc8a55a41e33b404
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518057"
---
# <a name="imstscaxeventsonlogincomplete-method"></a>Metodo IMsTscAxEvents:: OnLoginComplete

Chiamato quando il controllo client ha effettuato l'accesso a un server di host sessione Desktop remoto (host sessione Desktop remoto), dopo la visualizzazione della finestra di dialogo di accesso di Windows.

## <a name="syntax"></a>Sintassi


```C++
void OnLoginComplete();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Implementare questo metodo nel sink di evento per ricevere la notifica che il controllo ha completato l'accesso.

## <a name="examples"></a>Esempio

Nell'esempio seguente viene illustrato come gestire questo evento utilizzando Visual Basic codice di scripting. Il presupposto in questo esempio è che l'oggetto controllo è denominato "MsRdpClient".

Per ulteriori informazioni su Connessione Web Desktop remoto, vedere [requisiti per connessione Web Desktop remoto](requirements-for-remote-desktop-web-connection.md).


```VB
Sub MsRdpClient.OnLoginComplete()
    Msgbox("Login has completed")
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

 

 





