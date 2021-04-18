---
title: Proprietà MinutesToIdleTimeout di IMsRdpClientAdvancedSettings
description: Specifica il periodo di tempo massimo, in minuti, durante il quale il client deve rimanere connesso senza l'input dell'utente. Se il tempo specificato scade, il controllo chiama il metodo IMsTscAxEvents OnIdleTimeoutNotification.
ms.assetid: 709238ea-45f8-4bdc-9bbe-019d54ca27bf
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà MinutesToIdleTimeout
- Servizi Desktop remoto proprietà MinutesToIdleTimeout, interfaccia IMsRdpClientAdvancedSettings
- Interfaccia IMsRdpClientAdvancedSettings Servizi Desktop remoto, proprietà MinutesToIdleTimeout
- Servizi Desktop remoto proprietà MinutesToIdleTimeout, interfaccia IMsRdpClientAdvancedSettings2
- Interfaccia IMsRdpClientAdvancedSettings2 Servizi Desktop remoto, proprietà MinutesToIdleTimeout
- Servizi Desktop remoto proprietà MinutesToIdleTimeout, interfaccia IMsRdpClientAdvancedSettings3
- Interfaccia IMsRdpClientAdvancedSettings3 Servizi Desktop remoto, proprietà MinutesToIdleTimeout
- Servizi Desktop remoto proprietà MinutesToIdleTimeout, interfaccia IMsRdpClientAdvancedSettings4
- Interfaccia IMsRdpClientAdvancedSettings4 Servizi Desktop remoto, proprietà MinutesToIdleTimeout
- Servizi Desktop remoto proprietà MinutesToIdleTimeout, interfaccia IMsRdpClientAdvancedSettings5
- Interfaccia IMsRdpClientAdvancedSettings5 Servizi Desktop remoto, proprietà MinutesToIdleTimeout
- Servizi Desktop remoto proprietà MinutesToIdleTimeout, interfaccia IMsRdpClientAdvancedSettings6
- Interfaccia IMsRdpClientAdvancedSettings6 Servizi Desktop remoto, proprietà MinutesToIdleTimeout
- Servizi Desktop remoto proprietà MinutesToIdleTimeout, interfaccia IMsRdpClientAdvancedSettings7
- Interfaccia IMsRdpClientAdvancedSettings7 Servizi Desktop remoto, proprietà MinutesToIdleTimeout
- Servizi Desktop remoto proprietà MinutesToIdleTimeout, interfaccia IMsRdpClientAdvancedSettings8
- Interfaccia IMsRdpClientAdvancedSettings8 Servizi Desktop remoto, proprietà MinutesToIdleTimeout
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.MinutesToIdleTimeout
- IMsRdpClientAdvancedSettings.get_MinutesToIdleTimeout
- IMsRdpClientAdvancedSettings.put_MinutesToIdleTimeout
- IMsRdpClientAdvancedSettings2.MinutesToIdleTimeout
- IMsRdpClientAdvancedSettings2.get_MinutesToIdleTimeout
- IMsRdpClientAdvancedSettings2.put_MinutesToIdleTimeout
- IMsRdpClientAdvancedSettings3.MinutesToIdleTimeout
- IMsRdpClientAdvancedSettings3.get_MinutesToIdleTimeout
- IMsRdpClientAdvancedSettings3.put_MinutesToIdleTimeout
- IMsRdpClientAdvancedSettings4.MinutesToIdleTimeout
- IMsRdpClientAdvancedSettings4.get_MinutesToIdleTimeout
- IMsRdpClientAdvancedSettings4.put_MinutesToIdleTimeout
- IMsRdpClientAdvancedSettings5.MinutesToIdleTimeout
- IMsRdpClientAdvancedSettings5.get_MinutesToIdleTimeout
- IMsRdpClientAdvancedSettings5.put_MinutesToIdleTimeout
- IMsRdpClientAdvancedSettings6.MinutesToIdleTimeout
- IMsRdpClientAdvancedSettings6.get_MinutesToIdleTimeout
- IMsRdpClientAdvancedSettings6.put_MinutesToIdleTimeout
- IMsRdpClientAdvancedSettings7.MinutesToIdleTimeout
- IMsRdpClientAdvancedSettings7.get_MinutesToIdleTimeout
- IMsRdpClientAdvancedSettings7.put_MinutesToIdleTimeout
- IMsRdpClientAdvancedSettings8.MinutesToIdleTimeout
- IMsRdpClientAdvancedSettings8.get_MinutesToIdleTimeout
- IMsRdpClientAdvancedSettings8.put_MinutesToIdleTimeout
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8b5e42258ed670ac0323723cafe7b2792f8c5bd6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301311"
---
# <a name="imsrdpclientadvancedsettingsminutestoidletimeout-property"></a>Proprietà IMsRdpClientAdvancedSettings:: MinutesToIdleTimeout

Specifica il periodo di tempo massimo, in minuti, durante il quale il client deve rimanere connesso senza l'input dell'utente. Se il tempo specificato scade, il controllo chiama il metodo [**IMsTscAxEvents:: OnIdleTimeoutNotification**](imstscaxevents-onidletimeoutnotification.md) .

È possibile utilizzare questa proprietà in una situazione in cui è necessario disconnettere una sessione inattiva. ad esempio, in un ambiente chiosco multimediale.

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT put_MinutesToIdleTimeout(
  [in]  LONG minutesToIdleTimeout
);

HRESULT get_MinutesToIdleTimeout(
  [out] LONG *pminutesToIdleTimeout
);
```



## <a name="property-value"></a>Valore proprietà

Nuova ora, in minuti. Il valore predefinito è zero, che disabilita la funzionalità. Il valore massimo è 240, che rappresenta 4 ore.

## <a name="error-codes"></a>Codici di errore

Restituisce **\_ OK** se ha esito positivo.

## <a name="remarks"></a>Commenti

Per ulteriori informazioni su Connessione Web Desktop remoto, vedere [requisiti per connessione Web Desktop remoto](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                        |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                                  |
| Libreria dei tipi<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>          |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>          |
| IID<br/>                      | IID \_ IMsRdpClientAdvancedSettings è definito come 3c65b4ab-12b3-465b-aCD4-b8dad3bff9e2<br/> |



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

 

 





