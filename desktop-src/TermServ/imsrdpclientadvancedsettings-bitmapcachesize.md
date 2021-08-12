---
title: Proprietà BitmapCacheSize IMsRdpClientAdvancedSettings
description: Dimensioni, in kilobyte, del file della cache bitmap usato per bitmap a 8 bit per pixel.
ms.assetid: a2a4b739-0fa3-4a76-87ae-3cba913b7703
ms.tgt_platform: multiple
keywords:
- Proprietà BitmapCacheSize Servizi Desktop remoto
- Proprietà BitmapCacheSize Servizi Desktop remoto, interfaccia IMsRdpClientAdvancedSettings
- Interfaccia IMsRdpClientAdvancedSettings Servizi Desktop remoto , proprietà BitmapCacheSize
- Proprietà BitmapCacheSize Servizi Desktop remoto, interfaccia IMsRdpClientAdvancedSettings2
- Interfaccia IMsRdpClientAdvancedSettings2 Servizi Desktop remoto , proprietà BitmapCacheSize
- Proprietà BitmapCacheSize Servizi Desktop remoto, interfaccia IMsRdpClientAdvancedSettings3
- Interfaccia IMsRdpClientAdvancedSettings3 Servizi Desktop remoto , proprietà BitmapCacheSize
- Proprietà BitmapCacheSize Servizi Desktop remoto, interfaccia IMsRdpClientAdvancedSettings4
- Interfaccia IMsRdpClientAdvancedSettings4 Servizi Desktop remoto , proprietà BitmapCacheSize
- Proprietà BitmapCacheSize Servizi Desktop remoto, interfaccia IMsRdpClientAdvancedSettings5
- Interfaccia IMsRdpClientAdvancedSettings5 Servizi Desktop remoto , proprietà BitmapCacheSize
- Proprietà BitmapCacheSize Servizi Desktop remoto, interfaccia IMsRdpClientAdvancedSettings6
- Interfaccia IMsRdpClientAdvancedSettings6 Servizi Desktop remoto , proprietà BitmapCacheSize
- Proprietà BitmapCacheSize Servizi Desktop remoto, interfaccia IMsRdpClientAdvancedSettings7
- Interfaccia IMsRdpClientAdvancedSettings7 Servizi Desktop remoto , proprietà BitmapCacheSize
- Proprietà BitmapCacheSize Servizi Desktop remoto, interfaccia IMsRdpClientAdvancedSettings8
- Interfaccia IMsRdpClientAdvancedSettings8 Servizi Desktop remoto , proprietà BitmapCacheSize
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
ms.openlocfilehash: af56056cbdd62bb041ba9ab08e83a4f09e69037a3f9bd6799fa0c0facc9da75e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118609052"
---
# <a name="imsrdpclientadvancedsettingsbitmapcachesize-property"></a>Proprietà IMsRdpClientAdvancedSettings::BitmapCacheSize

Dimensioni, in kilobyte, del file della cache bitmap usato per bitmap a 8 bit per pixel.

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

Nuove dimensioni della cache, in kilobyte. I valori numerici validi sono compresi tra 1 e 32 inclusi.

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

 

 





