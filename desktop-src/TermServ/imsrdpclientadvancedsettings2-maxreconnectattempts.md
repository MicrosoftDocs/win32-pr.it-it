---
title: Proprietà IMsRdpClientAdvancedSettings2 MaxReconnectAttempts
description: Specifica il numero di volte in cui provare a riconnettersi durante la riconnessione automatica.
ms.assetid: 24bfd3b6-d2de-4e46-8b5f-a4702c18a93c
ms.tgt_platform: multiple
keywords:
- Proprietà MaxReconnectAttempts Servizi Desktop remoto
- Proprietà MaxReconnectAttempts Servizi Desktop remoto , interfaccia IMsRdpClientAdvancedSettings2
- Interfaccia IMsRdpClientAdvancedSettings2 Servizi Desktop remoto , proprietà MaxReconnectAttempts
- Proprietà MaxReconnectAttempts Servizi Desktop remoto , interfaccia IMsRdpClientAdvancedSettings3
- Interfaccia IMsRdpClientAdvancedSettings3 Servizi Desktop remoto , proprietà MaxReconnectAttempts
- Proprietà MaxReconnectAttempts Servizi Desktop remoto , interfaccia IMsRdpClientAdvancedSettings4
- Interfaccia IMsRdpClientAdvancedSettings4 Servizi Desktop remoto , proprietà MaxReconnectAttempts
- Proprietà MaxReconnectAttempts Servizi Desktop remoto , interfaccia IMsRdpClientAdvancedSettings5
- Interfaccia IMsRdpClientAdvancedSettings5 Servizi Desktop remoto , proprietà MaxReconnectAttempts
- Proprietà MaxReconnectAttempts Servizi Desktop remoto, interfaccia IMsRdpClientAdvancedSettings6
- Interfaccia IMsRdpClientAdvancedSettings6 Servizi Desktop remoto , proprietà MaxReconnectAttempts
- Proprietà MaxReconnectAttempts Servizi Desktop remoto, interfaccia IMsRdpClientAdvancedSettings7
- Interfaccia IMsRdpClientAdvancedSettings7 Servizi Desktop remoto , proprietà MaxReconnectAttempts
- Proprietà MaxReconnectAttempts Servizi Desktop remoto, interfaccia IMsRdpClientAdvancedSettings8
- Interfaccia IMsRdpClientAdvancedSettings8 Servizi Desktop remoto , proprietà MaxReconnectAttempts
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings2.MaxReconnectAttempts
- IMsRdpClientAdvancedSettings2.get_MaxReconnectAttempts
- IMsRdpClientAdvancedSettings2.put_MaxReconnectAttempts
- IMsRdpClientAdvancedSettings3.MaxReconnectAttempts
- IMsRdpClientAdvancedSettings3.get_MaxReconnectAttempts
- IMsRdpClientAdvancedSettings3.put_MaxReconnectAttempts
- IMsRdpClientAdvancedSettings4.MaxReconnectAttempts
- IMsRdpClientAdvancedSettings4.get_MaxReconnectAttempts
- IMsRdpClientAdvancedSettings4.put_MaxReconnectAttempts
- IMsRdpClientAdvancedSettings5.MaxReconnectAttempts
- IMsRdpClientAdvancedSettings5.get_MaxReconnectAttempts
- IMsRdpClientAdvancedSettings5.put_MaxReconnectAttempts
- IMsRdpClientAdvancedSettings6.MaxReconnectAttempts
- IMsRdpClientAdvancedSettings6.get_MaxReconnectAttempts
- IMsRdpClientAdvancedSettings6.put_MaxReconnectAttempts
- IMsRdpClientAdvancedSettings7.MaxReconnectAttempts
- IMsRdpClientAdvancedSettings7.get_MaxReconnectAttempts
- IMsRdpClientAdvancedSettings7.put_MaxReconnectAttempts
- IMsRdpClientAdvancedSettings8.MaxReconnectAttempts
- IMsRdpClientAdvancedSettings8.get_MaxReconnectAttempts
- IMsRdpClientAdvancedSettings8.put_MaxReconnectAttempts
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2e3ff5875e55de54ddf454dd8d3e283fd77be42ae1c54474fc4acdaaef8a55ae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117757357"
---
# <a name="imsrdpclientadvancedsettings2maxreconnectattempts-property"></a>Proprietà IMsRdpClientAdvancedSettings2::MaxReconnectAttempts

Specifica il numero di volte in cui provare a riconnettersi durante la riconnessione automatica.

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT put_MaxReconnectAttempts(
  [in]  LONG MaxReconnectAttempts
);

HRESULT get_MaxReconnectAttempts(
  [out] LONG *pMaxReconnectAttempts
);
```



## <a name="property-value"></a>Valore proprietà

Nuovo numero di tentativi. I valori validi sono compresi tra 0 e 200 inclusi.

## <a name="error-codes"></a>Codici di errore

Restituisce **S \_ OK in** caso di esito positivo.

## <a name="remarks"></a>Commenti

Questa proprietà non può essere impostata quando il controllo è connesso.

Per altre informazioni sui Connessione Web Desktop remoto, vedere [Requisiti per Connessione Web Desktop remoto](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                         |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                                   |
| Libreria dei tipi<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| IID<br/>                      | IID \_ IMsRdpClientAdvancedSettings2 è definito come 9ac42117-2b76-4320-aa44-0e616ab8437b<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

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

[**IMsRdpClientAdvancedSettings2**](imsrdpclientadvancedsettings2.md)
</dt> </dl>

 

 





