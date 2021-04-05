---
title: Proprietà PinConnectionBar di IMsRdpClientAdvancedSettings
description: Specifica lo stato della barra di connessione dell'interfaccia utente.
ms.assetid: b1f9cb02-3ee3-4574-a874-2584b0d5b47e
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà PinConnectionBar
- Servizi Desktop remoto proprietà PinConnectionBar, interfaccia IMsRdpClientAdvancedSettings
- Interfaccia IMsRdpClientAdvancedSettings Servizi Desktop remoto, proprietà PinConnectionBar
- Servizi Desktop remoto proprietà PinConnectionBar, interfaccia IMsRdpClientAdvancedSettings2
- Interfaccia IMsRdpClientAdvancedSettings2 Servizi Desktop remoto, proprietà PinConnectionBar
- Servizi Desktop remoto proprietà PinConnectionBar, interfaccia IMsRdpClientAdvancedSettings3
- Interfaccia IMsRdpClientAdvancedSettings3 Servizi Desktop remoto, proprietà PinConnectionBar
- Servizi Desktop remoto proprietà PinConnectionBar, interfaccia IMsRdpClientAdvancedSettings4
- Interfaccia IMsRdpClientAdvancedSettings4 Servizi Desktop remoto, proprietà PinConnectionBar
- Servizi Desktop remoto proprietà PinConnectionBar, interfaccia IMsRdpClientAdvancedSettings5
- Interfaccia IMsRdpClientAdvancedSettings5 Servizi Desktop remoto, proprietà PinConnectionBar
- Servizi Desktop remoto proprietà PinConnectionBar, interfaccia IMsRdpClientAdvancedSettings6
- Interfaccia IMsRdpClientAdvancedSettings6 Servizi Desktop remoto, proprietà PinConnectionBar
- Servizi Desktop remoto proprietà PinConnectionBar, interfaccia IMsRdpClientAdvancedSettings7
- Interfaccia IMsRdpClientAdvancedSettings7 Servizi Desktop remoto, proprietà PinConnectionBar
- Servizi Desktop remoto proprietà PinConnectionBar, interfaccia IMsRdpClientAdvancedSettings8
- Interfaccia IMsRdpClientAdvancedSettings8 Servizi Desktop remoto, proprietà PinConnectionBar
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.PinConnectionBar
- IMsRdpClientAdvancedSettings.get_PinConnectionBar
- IMsRdpClientAdvancedSettings.put_PinConnectionBar
- IMsRdpClientAdvancedSettings2.PinConnectionBar
- IMsRdpClientAdvancedSettings2.get_PinConnectionBar
- IMsRdpClientAdvancedSettings2.put_PinConnectionBar
- IMsRdpClientAdvancedSettings3.PinConnectionBar
- IMsRdpClientAdvancedSettings3.get_PinConnectionBar
- IMsRdpClientAdvancedSettings3.put_PinConnectionBar
- IMsRdpClientAdvancedSettings4.PinConnectionBar
- IMsRdpClientAdvancedSettings4.get_PinConnectionBar
- IMsRdpClientAdvancedSettings4.put_PinConnectionBar
- IMsRdpClientAdvancedSettings5.PinConnectionBar
- IMsRdpClientAdvancedSettings5.get_PinConnectionBar
- IMsRdpClientAdvancedSettings5.put_PinConnectionBar
- IMsRdpClientAdvancedSettings6.PinConnectionBar
- IMsRdpClientAdvancedSettings6.get_PinConnectionBar
- IMsRdpClientAdvancedSettings6.put_PinConnectionBar
- IMsRdpClientAdvancedSettings7.PinConnectionBar
- IMsRdpClientAdvancedSettings7.get_PinConnectionBar
- IMsRdpClientAdvancedSettings7.put_PinConnectionBar
- IMsRdpClientAdvancedSettings8.PinConnectionBar
- IMsRdpClientAdvancedSettings8.get_PinConnectionBar
- IMsRdpClientAdvancedSettings8.put_PinConnectionBar
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0da294d933026194d7307a7fa0a175575761809e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103873341"
---
# <a name="imsrdpclientadvancedsettingspinconnectionbar-property"></a>IMsRdpClientAdvancedSettings::P proprietà inConnectionBar

Specifica lo stato della barra di connessione dell'interfaccia utente.

Questa proprietà restituisce **E \_ NOTIMPL** se il contenitore chiama il metodo [**IObjectSafety:: SetInterfaceSafetyOptions**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768225(v=vs.85)) .

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT put_PinConnectionBar(
  [in]  VARIANT_BOOL fPinConnectionBar
);

HRESULT get_PinConnectionBar(
  [out] VARIANT_BOOL *pfPinConnectionBar
);
```



## <a name="property-value"></a>Valore proprietà

Impostando questa proprietà su **Variant \_ true** , lo stato viene impostato su "abbassato", ovvero invisibile per l'utente e non disponibile per l'input. **Variante \_ FALSE** imposta lo stato su "Raised" e disponibile per l'input dell'utente.

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

 

