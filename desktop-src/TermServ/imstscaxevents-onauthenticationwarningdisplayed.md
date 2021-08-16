---
title: Metodo IMsTscAxEvents OnAuthenticationWarningDisplayed
description: Chiamato prima che un controllo ActiveX visualizza una finestra di dialogo di autenticazione , ad esempio la finestra di dialogo di errore del certificato.
ms.assetid: ce307e5f-5e26-4041-bbd5-6871c0678da4
ms.tgt_platform: multiple
keywords:
- Metodo OnAuthenticationWarningDisplayed Servizi Desktop remoto
- Metodo OnAuthenticationWarningDisplayed Servizi Desktop remoto , interfaccia IMsTscAxEvents
- Interfaccia IMsTscAxEvents Servizi Desktop remoto , metodo OnAuthenticationWarningDisplayed
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnAuthenticationWarningDisplayed
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: df2de56a612c748db720e485d9f1e6e5750c9fc3281500dfddd751f41aed1641
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118854009"
---
# <a name="imstscaxeventsonauthenticationwarningdisplayed-method"></a>Metodo IMsTscAxEvents::OnAuthenticationWarningDisplayed

Chiamato prima che un controllo ActiveX visualizza una finestra di dialogo di autenticazione , ad esempio la finestra di dialogo di errore del certificato.

## <a name="syntax"></a>Sintassi


```C++
void OnAuthenticationWarningDisplayed();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Se necessario, è possibile usare la proprietà [**UIParentWindowHandle**](imsrdpclientnonscriptable2-uiparentwindowhandle.md) [**dell'interfaccia IMsRdpClientNonScriptable2**](imsrdpclientnonscriptable2.md) per garantire che la finestra di dialogo di autenticazione modale da visualizzare sia padre di una finestra specificata (potrebbe essere necessario per impedire agli utenti di usare altre finestre di dialogo mentre viene visualizzata la finestra di dialogo di autenticazione). Per impostazione predefinita, l'elemento padre è la ActiveX di controllo.

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

[**OnAuthenticationWarningDismissed**](imstscaxevents-onauthenticationwarningdismissed.md)
</dt> <dt>

[**UIParentWindowHandle**](imsrdpclientnonscriptable2-uiparentwindowhandle.md)
</dt> <dt>

[**IMsTscAxEvents**](imstscaxevents-interface.md)
</dt> </dl>

 

 





