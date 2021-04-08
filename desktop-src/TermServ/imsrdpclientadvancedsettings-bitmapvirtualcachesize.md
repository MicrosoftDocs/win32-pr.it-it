---
title: Proprietà BitmapVirtualCacheSize di IMsRdpClientAdvancedSettings
description: Specifica le dimensioni in megabyte del file di cache bitmap persistente da utilizzare per il colore a 8 bit per pixel.
ms.assetid: 4efcabd2-8671-40a3-ad12-af0b2b6e495a
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà BitmapVirtualCacheSize
- Servizi Desktop remoto proprietà BitmapVirtualCacheSize, interfaccia IMsRdpClientAdvancedSettings
- Interfaccia IMsRdpClientAdvancedSettings Servizi Desktop remoto, proprietà BitmapVirtualCacheSize
- Servizi Desktop remoto proprietà BitmapVirtualCacheSize, interfaccia IMsRdpClientAdvancedSettings2
- Interfaccia IMsRdpClientAdvancedSettings2 Servizi Desktop remoto, proprietà BitmapVirtualCacheSize
- Servizi Desktop remoto proprietà BitmapVirtualCacheSize, interfaccia IMsRdpClientAdvancedSettings3
- Interfaccia IMsRdpClientAdvancedSettings3 Servizi Desktop remoto, proprietà BitmapVirtualCacheSize
- Servizi Desktop remoto proprietà BitmapVirtualCacheSize, interfaccia IMsRdpClientAdvancedSettings4
- Interfaccia IMsRdpClientAdvancedSettings4 Servizi Desktop remoto, proprietà BitmapVirtualCacheSize
- Servizi Desktop remoto proprietà BitmapVirtualCacheSize, interfaccia IMsRdpClientAdvancedSettings5
- Interfaccia IMsRdpClientAdvancedSettings5 Servizi Desktop remoto, proprietà BitmapVirtualCacheSize
- Servizi Desktop remoto proprietà BitmapVirtualCacheSize, interfaccia IMsRdpClientAdvancedSettings6
- Interfaccia IMsRdpClientAdvancedSettings6 Servizi Desktop remoto, proprietà BitmapVirtualCacheSize
- Servizi Desktop remoto proprietà BitmapVirtualCacheSize, interfaccia IMsRdpClientAdvancedSettings7
- Interfaccia IMsRdpClientAdvancedSettings7 Servizi Desktop remoto, proprietà BitmapVirtualCacheSize
- Servizi Desktop remoto proprietà BitmapVirtualCacheSize, interfaccia IMsRdpClientAdvancedSettings8
- Interfaccia IMsRdpClientAdvancedSettings8 Servizi Desktop remoto, proprietà BitmapVirtualCacheSize
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.BitmapVirtualCacheSize
- IMsRdpClientAdvancedSettings.get_BitmapVirtualCacheSize
- IMsRdpClientAdvancedSettings.put_BitmapVirtualCacheSize
- IMsRdpClientAdvancedSettings2.BitmapVirtualCacheSize
- IMsRdpClientAdvancedSettings2.get_BitmapVirtualCacheSize
- IMsRdpClientAdvancedSettings2.put_BitmapVirtualCacheSize
- IMsRdpClientAdvancedSettings3.BitmapVirtualCacheSize
- IMsRdpClientAdvancedSettings3.get_BitmapVirtualCacheSize
- IMsRdpClientAdvancedSettings3.put_BitmapVirtualCacheSize
- IMsRdpClientAdvancedSettings4.BitmapVirtualCacheSize
- IMsRdpClientAdvancedSettings4.get_BitmapVirtualCacheSize
- IMsRdpClientAdvancedSettings4.put_BitmapVirtualCacheSize
- IMsRdpClientAdvancedSettings5.BitmapVirtualCacheSize
- IMsRdpClientAdvancedSettings5.get_BitmapVirtualCacheSize
- IMsRdpClientAdvancedSettings5.put_BitmapVirtualCacheSize
- IMsRdpClientAdvancedSettings6.BitmapVirtualCacheSize
- IMsRdpClientAdvancedSettings6.get_BitmapVirtualCacheSize
- IMsRdpClientAdvancedSettings6.put_BitmapVirtualCacheSize
- IMsRdpClientAdvancedSettings7.BitmapVirtualCacheSize
- IMsRdpClientAdvancedSettings7.get_BitmapVirtualCacheSize
- IMsRdpClientAdvancedSettings7.put_BitmapVirtualCacheSize
- IMsRdpClientAdvancedSettings8.BitmapVirtualCacheSize
- IMsRdpClientAdvancedSettings8.get_BitmapVirtualCacheSize
- IMsRdpClientAdvancedSettings8.put_BitmapVirtualCacheSize
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb652c0f235cf7438b49e68a544188ac4622acad
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048088"
---
# <a name="imsrdpclientadvancedsettingsbitmapvirtualcachesize-property"></a>Proprietà IMsRdpClientAdvancedSettings:: BitmapVirtualCacheSize

Specifica le dimensioni in megabyte del file di cache bitmap persistente da utilizzare per il colore a 8 bit per pixel.

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT put_BitmapVirtualCacheSize(
  [in]  LONG bitmapVirtualCacheSize
);

HRESULT get_BitmapVirtualCacheSize(
  [out] LONG *pbitmapVirtualCacheSize
);
```



## <a name="property-value"></a>Valore proprietà

Nuove dimensioni della cache. I valori validi sono compresi tra 1 e 32. Si noti che la dimensione massima per tutti i file della cache virtuale è 128 MB.

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

[**BitmapVirtualCache16BppSize**](imsrdpclientadvancedsettings-bitmapvirtualcache16bppsize.md)
</dt> <dt>

[**BitmapVirtualCache24BppSize**](imsrdpclientadvancedsettings-bitmapvirtualcache24bppsize.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings**](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





