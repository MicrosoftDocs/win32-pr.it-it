---
title: Proprietà CanAutoReconnect di IMsRdpClientAdvancedSettings2
description: Specifica se il controllo client è in grado di riconnettersi automaticamente alla sessione corrente in caso di disconnessione dalla rete.
ms.assetid: 0a7ecf90-832b-4ec1-990b-7fe26ff134b1
ms.tgt_platform: multiple
keywords:
- Proprietà CanAutoReconnect Servizi Desktop remoto
- Proprietà CanAutoReconnect Servizi Desktop remoto, interfaccia IMsRdpClientAdvancedSettings2
- Interfaccia IMsRdpClientAdvancedSettings2 Servizi Desktop remoto proprietà , CanAutoReconnect
- Proprietà CanAutoReconnect Servizi Desktop remoto, interfaccia IMsRdpClientAdvancedSettings3
- Interfaccia IMsRdpClientAdvancedSettings3 Servizi Desktop remoto , proprietà CanAutoReconnect
- Proprietà CanAutoReconnect Servizi Desktop remoto, interfaccia IMsRdpClientAdvancedSettings4
- Interfaccia IMsRdpClientAdvancedSettings4 Servizi Desktop remoto proprietà , CanAutoReconnect
- Proprietà CanAutoReconnect Servizi Desktop remoto, interfaccia IMsRdpClientAdvancedSettings5
- Interfaccia IMsRdpClientAdvancedSettings5 Servizi Desktop remoto proprietà , CanAutoReconnect
- Proprietà CanAutoReconnect Servizi Desktop remoto, interfaccia IMsRdpClientAdvancedSettings6
- Interfaccia IMsRdpClientAdvancedSettings6 Servizi Desktop remoto proprietà , CanAutoReconnect
- Proprietà CanAutoReconnect Servizi Desktop remoto, interfaccia IMsRdpClientAdvancedSettings7
- Interfaccia IMsRdpClientAdvancedSettings7 Servizi Desktop remoto proprietà , CanAutoReconnect
- Proprietà CanAutoReconnect Servizi Desktop remoto, interfaccia IMsRdpClientAdvancedSettings8
- Interfaccia IMsRdpClientAdvancedSettings8 Servizi Desktop remoto , proprietà CanAutoReconnect
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings2.CanAutoReconnect
- IMsRdpClientAdvancedSettings2.get_CanAutoReconnect
- IMsRdpClientAdvancedSettings3.CanAutoReconnect
- IMsRdpClientAdvancedSettings3.get_CanAutoReconnect
- IMsRdpClientAdvancedSettings4.CanAutoReconnect
- IMsRdpClientAdvancedSettings4.get_CanAutoReconnect
- IMsRdpClientAdvancedSettings5.CanAutoReconnect
- IMsRdpClientAdvancedSettings5.get_CanAutoReconnect
- IMsRdpClientAdvancedSettings6.CanAutoReconnect
- IMsRdpClientAdvancedSettings6.get_CanAutoReconnect
- IMsRdpClientAdvancedSettings7.CanAutoReconnect
- IMsRdpClientAdvancedSettings7.get_CanAutoReconnect
- IMsRdpClientAdvancedSettings8.CanAutoReconnect
- IMsRdpClientAdvancedSettings8.get_CanAutoReconnect
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 20d64ac732af45e935ddef8d0436bc2b9173854394c55bcc19c085dec5926e31
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119001419"
---
# <a name="imsrdpclientadvancedsettings2canautoreconnect-property"></a>Proprietà IMsRdpClientAdvancedSettings2::CanAutoReconnect

Specifica se il controllo client è in grado di riconnettersi automaticamente alla sessione corrente in caso di disconnessione dalla rete.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT get_CanAutoReconnect(
  [out] VARIANT_BOOL *pfCanAutoReconnect
);
```



## <a name="property-value"></a>Valore proprietà

Riceve **VARIANT \_ TRUE se** il controllo è in grado di riconnettersi automaticamente e VARIANT FALSE in **\_ caso** contrario.

## <a name="error-codes"></a>Codici di errore

Restituisce **S \_ OK in** caso di esito positivo.

## <a name="remarks"></a>Commenti

Le situazioni in cui la riconnessione automatica potrebbe non essere abilitata includono quelle in cui un amministratore usa Criteri di gruppo per disabilitare la riconnessione automatica e gli ambienti legacy che non supportano la riconnessione automatica.

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

 

 





