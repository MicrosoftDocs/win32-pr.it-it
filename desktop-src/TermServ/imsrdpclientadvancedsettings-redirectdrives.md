---
title: Proprietà RedirectDrives di IMsRdpClientAdvancedSettings
description: Specifica se è consentito il reindirizzamento delle unità disco.
ms.assetid: 5ed4cd28-4a1f-4d3b-9f9d-bf44a8483209
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà RedirectDrives
- Servizi Desktop remoto proprietà RedirectDrives, interfaccia IMsRdpClientAdvancedSettings
- Interfaccia IMsRdpClientAdvancedSettings Servizi Desktop remoto, proprietà RedirectDrives
- Servizi Desktop remoto proprietà RedirectDrives, interfaccia IMsRdpClientAdvancedSettings2
- Interfaccia IMsRdpClientAdvancedSettings2 Servizi Desktop remoto, proprietà RedirectDrives
- Servizi Desktop remoto proprietà RedirectDrives, interfaccia IMsRdpClientAdvancedSettings3
- Interfaccia IMsRdpClientAdvancedSettings3 Servizi Desktop remoto, proprietà RedirectDrives
- Servizi Desktop remoto proprietà RedirectDrives, interfaccia IMsRdpClientAdvancedSettings4
- Interfaccia IMsRdpClientAdvancedSettings4 Servizi Desktop remoto, proprietà RedirectDrives
- Servizi Desktop remoto proprietà RedirectDrives, interfaccia IMsRdpClientAdvancedSettings5
- Interfaccia IMsRdpClientAdvancedSettings5 Servizi Desktop remoto, proprietà RedirectDrives
- Servizi Desktop remoto proprietà RedirectDrives, interfaccia IMsRdpClientAdvancedSettings6
- Interfaccia IMsRdpClientAdvancedSettings6 Servizi Desktop remoto, proprietà RedirectDrives
- Servizi Desktop remoto proprietà RedirectDrives, interfaccia IMsRdpClientAdvancedSettings7
- Interfaccia IMsRdpClientAdvancedSettings7 Servizi Desktop remoto, proprietà RedirectDrives
- Servizi Desktop remoto proprietà RedirectDrives, interfaccia IMsRdpClientAdvancedSettings8
- Interfaccia IMsRdpClientAdvancedSettings8 Servizi Desktop remoto, proprietà RedirectDrives
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.RedirectDrives
- IMsRdpClientAdvancedSettings.get_RedirectDrives
- IMsRdpClientAdvancedSettings.put_RedirectDrives
- IMsRdpClientAdvancedSettings2.RedirectDrives
- IMsRdpClientAdvancedSettings2.get_RedirectDrives
- IMsRdpClientAdvancedSettings2.put_RedirectDrives
- IMsRdpClientAdvancedSettings3.RedirectDrives
- IMsRdpClientAdvancedSettings3.get_RedirectDrives
- IMsRdpClientAdvancedSettings3.put_RedirectDrives
- IMsRdpClientAdvancedSettings4.RedirectDrives
- IMsRdpClientAdvancedSettings4.get_RedirectDrives
- IMsRdpClientAdvancedSettings4.put_RedirectDrives
- IMsRdpClientAdvancedSettings5.RedirectDrives
- IMsRdpClientAdvancedSettings5.get_RedirectDrives
- IMsRdpClientAdvancedSettings5.put_RedirectDrives
- IMsRdpClientAdvancedSettings6.RedirectDrives
- IMsRdpClientAdvancedSettings6.get_RedirectDrives
- IMsRdpClientAdvancedSettings6.put_RedirectDrives
- IMsRdpClientAdvancedSettings7.RedirectDrives
- IMsRdpClientAdvancedSettings7.get_RedirectDrives
- IMsRdpClientAdvancedSettings7.put_RedirectDrives
- IMsRdpClientAdvancedSettings8.RedirectDrives
- IMsRdpClientAdvancedSettings8.get_RedirectDrives
- IMsRdpClientAdvancedSettings8.put_RedirectDrives
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c83d24ae4ea4dae2760c1e468f4fa8b326a94c38
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743655"
---
# <a name="imsrdpclientadvancedsettingsredirectdrives-property"></a>Proprietà IMsRdpClientAdvancedSettings:: RedirectDrives

Specifica se è consentito il reindirizzamento delle unità disco.

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT put_RedirectDrives(
  [in]  VARIANT_BOOL redirectDrives
);

HRESULT get_RedirectDrives(
  [out] VARIANT_BOOL *predirectDrives
);
```



## <a name="property-value"></a>Valore proprietà

Impostare questo parametro su **Variant \_ true** per consentire il reindirizzamento o la **variante \_ false** in caso contrario. **Variante \_ TRUE** chiede all'utente di confermare la concessione del reindirizzamento al momento della connessione, per motivi di sicurezza.

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

 

 





