---
title: Metodo IMsTscAxEvents OnAuthenticationWarningDismissed
description: Chiamato dopo che un ActiveX visualizza una finestra di dialogo di autenticazione, ad esempio la finestra di dialogo di errore del certificato.
ms.assetid: bf5dbe4a-9129-47b3-9808-ed09d9010099
ms.tgt_platform: multiple
keywords:
- Metodo OnAuthenticationWarningDismissed Servizi Desktop remoto
- Metodo OnAuthenticationWarningDismissed Servizi Desktop remoto, interfaccia IMsTscAxEvents
- Interfaccia IMsTscAxEvents Servizi Desktop remoto , metodo OnAuthenticationWarningDismissed
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnAuthenticationWarningDismissed
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a55af8450160e271e96c53d4d5a9d4390393ab7880d2c2bb143cf0e6a1cb3bb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120125231"
---
# <a name="imstscaxeventsonauthenticationwarningdismissed-method"></a>Metodo IMsTscAxEvents::OnAuthenticationWarningDismissed

Chiamato dopo che un ActiveX visualizza una finestra di dialogo di autenticazione, ad esempio la finestra di dialogo di errore del certificato.

## <a name="syntax"></a>Sintassi


```C++
void OnAuthenticationWarningDismissed();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Se necessario, è possibile usare la proprietà [**UIParentWindowHandle**](imsrdpclientnonscriptable2-uiparentwindowhandle.md) dell'interfaccia [**IMsRdpClientNonScriptable2**](imsrdpclientnonscriptable2.md) per ripristinare qualsiasi elemento padre che potrebbe essere stato eseguito nel metodo [**OnAuthenticationWarningDisplayed.**](imstscaxevents-onauthenticationwarningdisplayed.md)

Per altre informazioni sui Connessione Web Desktop remoto, vedere [Requisiti per Connessione Web Desktop remoto](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                               |
| Server minimo supportato<br/> | Windows Server 2008, Windows Server 2008 con SP1<br/>                           |
| Libreria dei tipi<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IMsTscAxEvents è definito come 336d5562-efa8-482e-8cb3-c5c0fc7a7db6<br/>           |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**OnAuthenticationWarningDisplayed**](imstscaxevents-onauthenticationwarningdisplayed.md)
</dt> <dt>

[**UIParentWindowHandle**](imsrdpclientnonscriptable2-uiparentwindowhandle.md)
</dt> <dt>

[**IMsTscAxEvents**](imstscaxevents-interface.md)
</dt> </dl>

 

 





