---
title: Proprietà GrabFocusOnConnect di IMsRdpClientAdvancedSettings
description: Specifica se il controllo client deve avere lo stato attivo durante la connessione.
ms.assetid: c67fc284-6e07-4749-84bf-70c0ae4d1b2b
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà GrabFocusOnConnect
- Servizi Desktop remoto proprietà GrabFocusOnConnect, interfaccia IMsRdpClientAdvancedSettings
- Interfaccia IMsRdpClientAdvancedSettings Servizi Desktop remoto, proprietà GrabFocusOnConnect
- Servizi Desktop remoto proprietà GrabFocusOnConnect, interfaccia IMsRdpClientAdvancedSettings2
- Interfaccia IMsRdpClientAdvancedSettings2 Servizi Desktop remoto, proprietà GrabFocusOnConnect
- Servizi Desktop remoto proprietà GrabFocusOnConnect, interfaccia IMsRdpClientAdvancedSettings3
- Interfaccia IMsRdpClientAdvancedSettings3 Servizi Desktop remoto, proprietà GrabFocusOnConnect
- Servizi Desktop remoto proprietà GrabFocusOnConnect, interfaccia IMsRdpClientAdvancedSettings4
- Interfaccia IMsRdpClientAdvancedSettings4 Servizi Desktop remoto, proprietà GrabFocusOnConnect
- Servizi Desktop remoto proprietà GrabFocusOnConnect, interfaccia IMsRdpClientAdvancedSettings5
- Interfaccia IMsRdpClientAdvancedSettings5 Servizi Desktop remoto, proprietà GrabFocusOnConnect
- Servizi Desktop remoto proprietà GrabFocusOnConnect, interfaccia IMsRdpClientAdvancedSettings6
- Interfaccia IMsRdpClientAdvancedSettings6 Servizi Desktop remoto, proprietà GrabFocusOnConnect
- Servizi Desktop remoto proprietà GrabFocusOnConnect, interfaccia IMsRdpClientAdvancedSettings7
- Interfaccia IMsRdpClientAdvancedSettings7 Servizi Desktop remoto, proprietà GrabFocusOnConnect
- Servizi Desktop remoto proprietà GrabFocusOnConnect, interfaccia IMsRdpClientAdvancedSettings8
- Interfaccia IMsRdpClientAdvancedSettings8 Servizi Desktop remoto, proprietà GrabFocusOnConnect
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.GrabFocusOnConnect
- IMsRdpClientAdvancedSettings.get_GrabFocusOnConnect
- IMsRdpClientAdvancedSettings.put_GrabFocusOnConnect
- IMsRdpClientAdvancedSettings2.GrabFocusOnConnect
- IMsRdpClientAdvancedSettings2.get_GrabFocusOnConnect
- IMsRdpClientAdvancedSettings2.put_GrabFocusOnConnect
- IMsRdpClientAdvancedSettings3.GrabFocusOnConnect
- IMsRdpClientAdvancedSettings3.get_GrabFocusOnConnect
- IMsRdpClientAdvancedSettings3.put_GrabFocusOnConnect
- IMsRdpClientAdvancedSettings4.GrabFocusOnConnect
- IMsRdpClientAdvancedSettings4.get_GrabFocusOnConnect
- IMsRdpClientAdvancedSettings4.put_GrabFocusOnConnect
- IMsRdpClientAdvancedSettings5.GrabFocusOnConnect
- IMsRdpClientAdvancedSettings5.get_GrabFocusOnConnect
- IMsRdpClientAdvancedSettings5.put_GrabFocusOnConnect
- IMsRdpClientAdvancedSettings6.GrabFocusOnConnect
- IMsRdpClientAdvancedSettings6.get_GrabFocusOnConnect
- IMsRdpClientAdvancedSettings6.put_GrabFocusOnConnect
- IMsRdpClientAdvancedSettings7.GrabFocusOnConnect
- IMsRdpClientAdvancedSettings7.get_GrabFocusOnConnect
- IMsRdpClientAdvancedSettings7.put_GrabFocusOnConnect
- IMsRdpClientAdvancedSettings8.GrabFocusOnConnect
- IMsRdpClientAdvancedSettings8.get_GrabFocusOnConnect
- IMsRdpClientAdvancedSettings8.put_GrabFocusOnConnect
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0e7fb04c00bd7aaaf4de1252d961206ffee0e6b9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302464"
---
# <a name="imsrdpclientadvancedsettingsgrabfocusonconnect-property"></a>Proprietà IMsRdpClientAdvancedSettings:: GrabFocusOnConnect

Specifica se il controllo client deve avere lo stato attivo durante la connessione. Il controllo non tenterà di acquisire lo stato attivo da una finestra in esecuzione in un processo diverso.

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT put_GrabFocusOnConnect(
  [in]  VARIANT_BOOL fGrabFocusOnConnect
);

HRESULT get_GrabFocusOnConnect(
  [out] VARIANT_BOOL pfGrabFocusOnConnect
);
```



## <a name="property-value"></a>Valore proprietà

Impostare questo parametro su **Variant \_ false** per disabilitare la funzionalità o la **variante \_ true** per abilitare la funzionalità. L'impostazione di questa proprietà su **Variant \_ false** impedisce al controllo di catturare lo stato attivo durante la connessione.

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

 

 





