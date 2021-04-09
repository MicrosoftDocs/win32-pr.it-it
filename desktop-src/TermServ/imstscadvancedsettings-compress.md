---
title: Proprietà Compress IMsTscAdvancedSettings
description: Specifica se la compressione è abilitata.
ms.assetid: 274774b3-0442-4a46-95f8-7857f885bfdb
ms.tgt_platform: multiple
keywords:
- Comprimi Servizi Desktop remoto proprietà
- Comprimi Servizi Desktop remoto proprietà, interfaccia IMsTscAdvancedSettings
- Interfaccia IMsTscAdvancedSettings Servizi Desktop remoto, proprietà Compress
- Comprimi Servizi Desktop remoto proprietà, interfaccia IMsRdpClientAdvancedSettings
- Interfaccia IMsRdpClientAdvancedSettings Servizi Desktop remoto, proprietà Compress
- Comprimi Servizi Desktop remoto proprietà, interfaccia IMsRdpClientAdvancedSettings2
- Interfaccia IMsRdpClientAdvancedSettings2 Servizi Desktop remoto, proprietà Compress
- Comprimi Servizi Desktop remoto proprietà, interfaccia IMsRdpClientAdvancedSettings3
- Interfaccia IMsRdpClientAdvancedSettings3 Servizi Desktop remoto, proprietà Compress
- Comprimi Servizi Desktop remoto proprietà, interfaccia IMsRdpClientAdvancedSettings4
- Interfaccia IMsRdpClientAdvancedSettings4 Servizi Desktop remoto, proprietà Compress
- Comprimi Servizi Desktop remoto proprietà, interfaccia IMsRdpClientAdvancedSettings5
- Interfaccia IMsRdpClientAdvancedSettings5 Servizi Desktop remoto, proprietà Compress
- Comprimi Servizi Desktop remoto proprietà, interfaccia IMsRdpClientAdvancedSettings6
- Interfaccia IMsRdpClientAdvancedSettings6 Servizi Desktop remoto, proprietà Compress
- Comprimi Servizi Desktop remoto proprietà, interfaccia IMsRdpClientAdvancedSettings7
- Interfaccia IMsRdpClientAdvancedSettings7 Servizi Desktop remoto, proprietà Compress
- Comprimi Servizi Desktop remoto proprietà, interfaccia IMsRdpClientAdvancedSettings8
- Interfaccia IMsRdpClientAdvancedSettings8 Servizi Desktop remoto, proprietà Compress
topic_type:
- apiref
api_name:
- IMsTscAdvancedSettings.Compress
- IMsTscAdvancedSettings.get_Compress
- IMsTscAdvancedSettings.put_Compress
- IMsRdpClientAdvancedSettings.Compress
- IMsRdpClientAdvancedSettings.get_Compress
- IMsRdpClientAdvancedSettings.put_Compress
- IMsRdpClientAdvancedSettings2.Compress
- IMsRdpClientAdvancedSettings2.get_Compress
- IMsRdpClientAdvancedSettings2.put_Compress
- IMsRdpClientAdvancedSettings3.Compress
- IMsRdpClientAdvancedSettings3.get_Compress
- IMsRdpClientAdvancedSettings3.put_Compress
- IMsRdpClientAdvancedSettings4.Compress
- IMsRdpClientAdvancedSettings4.get_Compress
- IMsRdpClientAdvancedSettings4.put_Compress
- IMsRdpClientAdvancedSettings5.Compress
- IMsRdpClientAdvancedSettings5.get_Compress
- IMsRdpClientAdvancedSettings5.put_Compress
- IMsRdpClientAdvancedSettings6.Compress
- IMsRdpClientAdvancedSettings6.get_Compress
- IMsRdpClientAdvancedSettings6.put_Compress
- IMsRdpClientAdvancedSettings7.Compress
- IMsRdpClientAdvancedSettings7.get_Compress
- IMsRdpClientAdvancedSettings7.put_Compress
- IMsRdpClientAdvancedSettings8.Compress
- IMsRdpClientAdvancedSettings8.get_Compress
- IMsRdpClientAdvancedSettings8.put_Compress
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c588784d9b06bd2e8e1605a96c8aa9fd157c10eb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964422"
---
# <a name="imstscadvancedsettingscompress-property"></a>Proprietà IMsTscAdvancedSettings:: Compress

Specifica se la compressione è abilitata.

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT put_Compress(
  [in]  LONG compress
);

HRESULT get_Compress(
  [out] LONG *pcompress
);
```



## <a name="property-value"></a>Valore proprietà

Impostare questo parametro su 0 per disabilitare la compressione o un valore diverso da zero per abilitare la compressione.

## <a name="error-codes"></a>Codici di errore

Restituisce **\_ OK** se ha esito positivo.

## <a name="remarks"></a>Commenti

Per ulteriori informazioni su Connessione Web Desktop remoto, vedere [requisiti per connessione Web Desktop remoto](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                  |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                            |
| Libreria dei tipi<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>    |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>    |
| IID<br/>                      | IID \_ IMsTscAdvancedSettings è definito come 809945cc-4b3b-4A92-a6b0-dbf9b5f2ef2d<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IMsRdpClientAdvancedSettings**](imsrdpclientadvancedsettings-interface.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings2**](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings3**](imsrdpclientadvancedsettings3.md)
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

[**IMsTscAdvancedSettings**](imstscadvancedsettings-interface.md)
</dt> </dl>

 

 





