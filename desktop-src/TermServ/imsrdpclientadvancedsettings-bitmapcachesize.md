---
title: Proprietà BitmapCacheSize di IMsRdpClientAdvancedSettings
description: Dimensioni, in kilobyte, del file di cache bitmap utilizzato per le bitmap a 8 bit per pixel.
ms.assetid: a2a4b739-0fa3-4a76-87ae-3cba913b7703
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà BitmapCacheSize
- Servizi Desktop remoto proprietà BitmapCacheSize, interfaccia IMsRdpClientAdvancedSettings
- Interfaccia IMsRdpClientAdvancedSettings Servizi Desktop remoto, proprietà BitmapCacheSize
- Servizi Desktop remoto proprietà BitmapCacheSize, interfaccia IMsRdpClientAdvancedSettings2
- Interfaccia IMsRdpClientAdvancedSettings2 Servizi Desktop remoto, proprietà BitmapCacheSize
- Servizi Desktop remoto proprietà BitmapCacheSize, interfaccia IMsRdpClientAdvancedSettings3
- Interfaccia IMsRdpClientAdvancedSettings3 Servizi Desktop remoto, proprietà BitmapCacheSize
- Servizi Desktop remoto proprietà BitmapCacheSize, interfaccia IMsRdpClientAdvancedSettings4
- Interfaccia IMsRdpClientAdvancedSettings4 Servizi Desktop remoto, proprietà BitmapCacheSize
- Servizi Desktop remoto proprietà BitmapCacheSize, interfaccia IMsRdpClientAdvancedSettings5
- Interfaccia IMsRdpClientAdvancedSettings5 Servizi Desktop remoto, proprietà BitmapCacheSize
- Servizi Desktop remoto proprietà BitmapCacheSize, interfaccia IMsRdpClientAdvancedSettings6
- Interfaccia IMsRdpClientAdvancedSettings6 Servizi Desktop remoto, proprietà BitmapCacheSize
- Servizi Desktop remoto proprietà BitmapCacheSize, interfaccia IMsRdpClientAdvancedSettings7
- Interfaccia IMsRdpClientAdvancedSettings7 Servizi Desktop remoto, proprietà BitmapCacheSize
- Servizi Desktop remoto proprietà BitmapCacheSize, interfaccia IMsRdpClientAdvancedSettings8
- Interfaccia IMsRdpClientAdvancedSettings8 Servizi Desktop remoto, proprietà BitmapCacheSize
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.BitmapCacheSize
- IMsRdpClientAdvancedSettings.get_BitmapCacheSize
- IMsRdpClientAdvancedSettings.put_BitmapCacheSize
- IMsRdpClientAdvancedSettings2.BitmapCacheSize
- IMsRdpClientAdvancedSettings2.get_BitmapCacheSize
- IMsRdpClientAdvancedSettings2.put_BitmapCacheSize
- IMsRdpClientAdvancedSettings3.BitmapCacheSize
- IMsRdpClientAdvancedSettings3.get_BitmapCacheSize
- IMsRdpClientAdvancedSettings3.put_BitmapCacheSize
- IMsRdpClientAdvancedSettings4.BitmapCacheSize
- IMsRdpClientAdvancedSettings4.get_BitmapCacheSize
- IMsRdpClientAdvancedSettings4.put_BitmapCacheSize
- IMsRdpClientAdvancedSettings5.BitmapCacheSize
- IMsRdpClientAdvancedSettings5.get_BitmapCacheSize
- IMsRdpClientAdvancedSettings5.put_BitmapCacheSize
- IMsRdpClientAdvancedSettings6.BitmapCacheSize
- IMsRdpClientAdvancedSettings6.get_BitmapCacheSize
- IMsRdpClientAdvancedSettings6.put_BitmapCacheSize
- IMsRdpClientAdvancedSettings7.BitmapCacheSize
- IMsRdpClientAdvancedSettings7.get_BitmapCacheSize
- IMsRdpClientAdvancedSettings7.put_BitmapCacheSize
- IMsRdpClientAdvancedSettings8.BitmapCacheSize
- IMsRdpClientAdvancedSettings8.get_BitmapCacheSize
- IMsRdpClientAdvancedSettings8.put_BitmapCacheSize
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a38376bb0b06bd4efea36d3c4cad4e4aec0f35b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400457"
---
# <a name="imsrdpclientadvancedsettingsbitmapcachesize-property"></a>Proprietà IMsRdpClientAdvancedSettings:: BitmapCacheSize

Dimensioni, in kilobyte, del file di cache bitmap utilizzato per le bitmap a 8 bit per pixel.

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT put_BitmapCacheSize(
  [in]  LONG bitmapCacheSize
);

HRESULT get_BitmapCacheSize(
  [out] LONG *pbitmapCacheSize
);
```



## <a name="property-value"></a>Valore proprietà

Nuove dimensioni della cache, in kilobyte. I valori numerici validi sono compresi tra 1 e 32.

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

 

 





