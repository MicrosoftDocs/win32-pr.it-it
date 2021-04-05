---
title: Proprietà CanAutoReconnect di IMsRdpClientAdvancedSettings2
description: Specifica se il controllo client è in grado di riconnettersi automaticamente alla sessione corrente in caso di disconnessione di rete.
ms.assetid: 0a7ecf90-832b-4ec1-990b-7fe26ff134b1
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà CanAutoReconnect
- Servizi Desktop remoto proprietà CanAutoReconnect, interfaccia IMsRdpClientAdvancedSettings2
- Interfaccia IMsRdpClientAdvancedSettings2 Servizi Desktop remoto, proprietà CanAutoReconnect
- Servizi Desktop remoto proprietà CanAutoReconnect, interfaccia IMsRdpClientAdvancedSettings3
- Interfaccia IMsRdpClientAdvancedSettings3 Servizi Desktop remoto, proprietà CanAutoReconnect
- Servizi Desktop remoto proprietà CanAutoReconnect, interfaccia IMsRdpClientAdvancedSettings4
- Interfaccia IMsRdpClientAdvancedSettings4 Servizi Desktop remoto, proprietà CanAutoReconnect
- Servizi Desktop remoto proprietà CanAutoReconnect, interfaccia IMsRdpClientAdvancedSettings5
- Interfaccia IMsRdpClientAdvancedSettings5 Servizi Desktop remoto, proprietà CanAutoReconnect
- Servizi Desktop remoto proprietà CanAutoReconnect, interfaccia IMsRdpClientAdvancedSettings6
- Interfaccia IMsRdpClientAdvancedSettings6 Servizi Desktop remoto, proprietà CanAutoReconnect
- Servizi Desktop remoto proprietà CanAutoReconnect, interfaccia IMsRdpClientAdvancedSettings7
- Interfaccia IMsRdpClientAdvancedSettings7 Servizi Desktop remoto, proprietà CanAutoReconnect
- Servizi Desktop remoto proprietà CanAutoReconnect, interfaccia IMsRdpClientAdvancedSettings8
- Interfaccia IMsRdpClientAdvancedSettings8 Servizi Desktop remoto, proprietà CanAutoReconnect
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
ms.openlocfilehash: 0d8c8f4113c39b79783978252136c50d2111ed0c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103873337"
---
# <a name="imsrdpclientadvancedsettings2canautoreconnect-property"></a>Proprietà IMsRdpClientAdvancedSettings2:: CanAutoReconnect

Specifica se il controllo client è in grado di riconnettersi automaticamente alla sessione corrente in caso di disconnessione di rete.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT get_CanAutoReconnect(
  [out] VARIANT_BOOL *pfCanAutoReconnect
);
```



## <a name="property-value"></a>Valore proprietà

Riceve la **variante \_ true** se il controllo è in grado di riconnettersi automaticamente e **Variant \_ false** in caso contrario.

## <a name="error-codes"></a>Codici di errore

Se l'operazione ha esito positivo, restituire **S \_ OK** .

## <a name="remarks"></a>Commenti

Le situazioni in cui la riconnessione automatica potrebbe non essere abilitata includono quelle in cui un amministratore usa i criteri di gruppo per disabilitare autoreconnection e gli ambienti legacy che non supportano la riconnessione automatica.

Impossibile impostare questa proprietà quando il controllo è connesso.

Per ulteriori informazioni su Connessione Web Desktop remoto, vedere [requisiti per connessione Web Desktop remoto](requirements-for-remote-desktop-web-connection.md).

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

 

 





