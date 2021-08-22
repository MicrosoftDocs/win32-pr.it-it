---
title: Metodo IMsTscAxEvents OnLoginComplete
description: Chiamato quando il controllo client ha eseguito correttamente l'accesso a un server host sessione Desktop remoto (Host sessione Desktop remoto), dopo la visualizzazione della finestra di dialogo Windows Accesso remoto.
ms.assetid: acb345a6-3153-4b8f-ac51-fe0c19fa750a
ms.tgt_platform: multiple
keywords:
- Metodo OnLoginComplete Servizi Desktop remoto
- Metodo OnLoginComplete Servizi Desktop remoto, interfaccia IMsTscAxEvents
- Interfaccia IMsTscAxEvents Servizi Desktop remoto , metodo OnLoginComplete
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
ms.openlocfilehash: d6c89b494a250652e054e245eb0de3267a860bec1a193c7dc953f93fd0800c2a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119138434"
---
# <a name="imstscaxeventsonlogincomplete-method"></a>Metodo IMsTscAxEvents::OnLoginComplete

Chiamato quando il controllo client ha eseguito correttamente l'accesso a un server host sessione Desktop remoto (Host sessione Desktop remoto), dopo la visualizzazione della finestra di dialogo Windows Accesso remoto.

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

Nell'esempio seguente viene illustrato come gestire questo evento usando Visual Basic di scripting. Il presupposto in questo esempio è che l'oggetto controllo sia denominato "MsRdpClient".

Per altre informazioni sui Connessione Web Desktop remoto, vedere [Requisiti per Connessione Web Desktop remoto](requirements-for-remote-desktop-web-connection.md).


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

 

 





