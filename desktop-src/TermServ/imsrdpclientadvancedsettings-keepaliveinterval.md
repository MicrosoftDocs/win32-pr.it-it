---
title: Proprietà keepAliveInterval di IMsRdpClientAdvancedSettings
description: Specifica un intervallo, in millisecondi, in cui il client invia messaggi keep-alive al server.
ms.assetid: 0d1b7d8f-f81c-4591-bb08-adab307e87fe
ms.tgt_platform: multiple
keywords:
- Proprietà keepAliveInterval Servizi Desktop remoto
- Proprietà keepAliveInterval Servizi Desktop remoto , interfaccia IMsRdpClientAdvancedSettings
- Interfaccia IMsRdpClientAdvancedSettings Servizi Desktop remoto proprietà , keepAliveInterval
- Proprietà keepAliveInterval Servizi Desktop remoto, interfaccia IMsRdpClientAdvancedSettings2
- Interfaccia IMsRdpClientAdvancedSettings2 Servizi Desktop remoto proprietà , keepAliveInterval
- Proprietà keepAliveInterval Servizi Desktop remoto , interfaccia IMsRdpClientAdvancedSettings3
- Interfaccia IMsRdpClientAdvancedSettings3 Servizi Desktop remoto proprietà , keepAliveInterval
- Proprietà keepAliveInterval Servizi Desktop remoto , interfaccia IMsRdpClientAdvancedSettings4
- Interfaccia IMsRdpClientAdvancedSettings4 Servizi Desktop remoto proprietà , keepAliveInterval
- Proprietà keepAliveInterval Servizi Desktop remoto, interfaccia IMsRdpClientAdvancedSettings5
- Interfaccia IMsRdpClientAdvancedSettings5 Servizi Desktop remoto proprietà , keepAliveInterval
- Proprietà keepAliveInterval Servizi Desktop remoto , interfaccia IMsRdpClientAdvancedSettings6
- Interfaccia IMsRdpClientAdvancedSettings6 Servizi Desktop remoto proprietà , keepAliveInterval
- Proprietà keepAliveInterval Servizi Desktop remoto, interfaccia IMsRdpClientAdvancedSettings7
- Interfaccia IMsRdpClientAdvancedSettings7 Servizi Desktop remoto proprietà , keepAliveInterval
- Proprietà keepAliveInterval Servizi Desktop remoto , interfaccia IMsRdpClientAdvancedSettings8
- Interfaccia IMsRdpClientAdvancedSettings8 Servizi Desktop remoto , proprietà keepAliveInterval
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.keepAliveInterval
- IMsRdpClientAdvancedSettings.get_keepAliveInterval
- IMsRdpClientAdvancedSettings.put_keepAliveInterval
- IMsRdpClientAdvancedSettings2.keepAliveInterval
- IMsRdpClientAdvancedSettings2.get_keepAliveInterval
- IMsRdpClientAdvancedSettings2.put_keepAliveInterval
- IMsRdpClientAdvancedSettings3.keepAliveInterval
- IMsRdpClientAdvancedSettings3.get_keepAliveInterval
- IMsRdpClientAdvancedSettings3.put_keepAliveInterval
- IMsRdpClientAdvancedSettings4.keepAliveInterval
- IMsRdpClientAdvancedSettings4.get_keepAliveInterval
- IMsRdpClientAdvancedSettings4.put_keepAliveInterval
- IMsRdpClientAdvancedSettings5.keepAliveInterval
- IMsRdpClientAdvancedSettings5.get_keepAliveInterval
- IMsRdpClientAdvancedSettings5.put_keepAliveInterval
- IMsRdpClientAdvancedSettings6.keepAliveInterval
- IMsRdpClientAdvancedSettings6.get_keepAliveInterval
- IMsRdpClientAdvancedSettings6.put_keepAliveInterval
- IMsRdpClientAdvancedSettings7.keepAliveInterval
- IMsRdpClientAdvancedSettings7.get_keepAliveInterval
- IMsRdpClientAdvancedSettings7.put_keepAliveInterval
- IMsRdpClientAdvancedSettings8.keepAliveInterval
- IMsRdpClientAdvancedSettings8.get_keepAliveInterval
- IMsRdpClientAdvancedSettings8.put_keepAliveInterval
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1dad34455d1203fb353672b8ef3797866b8ad2aa8b5686f71f769eccc5f3c9ff
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120033301"
---
# <a name="imsrdpclientadvancedsettingskeepaliveinterval-property"></a>Proprietà IMsRdpClientAdvancedSettings::keepAliveInterval

Specifica un intervallo, in millisecondi, in cui il client invia messaggi keep-alive al server.

Un'impostazione di Criteri di gruppo che specifica se sono consentite connessioni client permanenti al server può eseguire l'override di questa impostazione di proprietà.

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT put_keepAliveInterval(
  [in]  LONG keepAliveInterval
);

HRESULT get_keepAliveInterval(
  [out] LONG *pkeepAliveInterval
);
```



## <a name="property-value"></a>Valore proprietà

Nuovo intervallo, espresso in millisecondi. Il valore predefinito della proprietà è zero, che disabilita i messaggi keep-alive. Il valore minimo valido di questa proprietà è 10.000, che rappresenta 10 secondi.

## <a name="error-codes"></a>Codici di errore

Restituisce **S \_ OK in** caso di esito positivo.

## <a name="remarks"></a>Commenti

Per altre informazioni sui Connessione Web Desktop remoto, vedere [Requisiti per Connessione Web Desktop remoto](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                        |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                                  |
| Libreria dei tipi<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>          |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>          |
| IID<br/>                      | IID \_ IMsRdpClientAdvancedSettings è definito come 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IMsRdpClientAdvancedSettings2**](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings3**](imstscadvancedsettings-interface.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings4**](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings5**](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings6**](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings7**](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings8**](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings**](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





