---
title: Proprietà BitmapPeristence di IMsTscAdvancedSettings
description: Specifica se la memorizzazione nella cache bitmap è abilitata.
ms.assetid: 8cabeae8-26bc-4d33-82cc-47bb201d79b6
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà BitmapPeristence
- Servizi Desktop remoto proprietà BitmapPeristence, interfaccia IMsTscAdvancedSettings
- Interfaccia IMsTscAdvancedSettings Servizi Desktop remoto, proprietà BitmapPeristence
- Servizi Desktop remoto proprietà BitmapPeristence, interfaccia IMsRdpClientAdvancedSettings
- Interfaccia IMsRdpClientAdvancedSettings Servizi Desktop remoto, proprietà BitmapPeristence
- Servizi Desktop remoto proprietà BitmapPeristence, interfaccia IMsRdpClientAdvancedSettings2
- Interfaccia IMsRdpClientAdvancedSettings2 Servizi Desktop remoto, proprietà BitmapPeristence
- Servizi Desktop remoto proprietà BitmapPeristence, interfaccia IMsRdpClientAdvancedSettings3
- Interfaccia IMsRdpClientAdvancedSettings3 Servizi Desktop remoto, proprietà BitmapPeristence
- Servizi Desktop remoto proprietà BitmapPeristence, interfaccia IMsRdpClientAdvancedSettings4
- Interfaccia IMsRdpClientAdvancedSettings4 Servizi Desktop remoto, proprietà BitmapPeristence
- Servizi Desktop remoto proprietà BitmapPeristence, interfaccia IMsRdpClientAdvancedSettings5
- Interfaccia IMsRdpClientAdvancedSettings5 Servizi Desktop remoto, proprietà BitmapPeristence
- Servizi Desktop remoto proprietà BitmapPeristence, interfaccia IMsRdpClientAdvancedSettings6
- Interfaccia IMsRdpClientAdvancedSettings6 Servizi Desktop remoto, proprietà BitmapPeristence
- Servizi Desktop remoto proprietà BitmapPeristence, interfaccia IMsRdpClientAdvancedSettings7
- Interfaccia IMsRdpClientAdvancedSettings7 Servizi Desktop remoto, proprietà BitmapPeristence
- Servizi Desktop remoto proprietà BitmapPeristence, interfaccia IMsRdpClientAdvancedSettings8
- Interfaccia IMsRdpClientAdvancedSettings8 Servizi Desktop remoto, proprietà BitmapPeristence
topic_type:
- apiref
api_name:
- IMsTscAdvancedSettings.BitmapPeristence
- IMsTscAdvancedSettings.get_BitmapPeristence
- IMsTscAdvancedSettings.put_BitmapPeristence
- IMsRdpClientAdvancedSettings.BitmapPeristence
- IMsRdpClientAdvancedSettings.get_BitmapPeristence
- IMsRdpClientAdvancedSettings.put_BitmapPeristence
- IMsRdpClientAdvancedSettings2.BitmapPeristence
- IMsRdpClientAdvancedSettings2.get_BitmapPeristence
- IMsRdpClientAdvancedSettings2.put_BitmapPeristence
- IMsRdpClientAdvancedSettings3.BitmapPeristence
- IMsRdpClientAdvancedSettings3.get_BitmapPeristence
- IMsRdpClientAdvancedSettings3.put_BitmapPeristence
- IMsRdpClientAdvancedSettings4.BitmapPeristence
- IMsRdpClientAdvancedSettings4.get_BitmapPeristence
- IMsRdpClientAdvancedSettings4.put_BitmapPeristence
- IMsRdpClientAdvancedSettings5.BitmapPeristence
- IMsRdpClientAdvancedSettings5.get_BitmapPeristence
- IMsRdpClientAdvancedSettings5.put_BitmapPeristence
- IMsRdpClientAdvancedSettings6.BitmapPeristence
- IMsRdpClientAdvancedSettings6.get_BitmapPeristence
- IMsRdpClientAdvancedSettings6.put_BitmapPeristence
- IMsRdpClientAdvancedSettings7.BitmapPeristence
- IMsRdpClientAdvancedSettings7.get_BitmapPeristence
- IMsRdpClientAdvancedSettings7.put_BitmapPeristence
- IMsRdpClientAdvancedSettings8.BitmapPeristence
- IMsRdpClientAdvancedSettings8.get_BitmapPeristence
- IMsRdpClientAdvancedSettings8.put_BitmapPeristence
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a543d24b200d8fa484939d5ffeabfeeac0b5f73f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104479031"
---
# <a name="imstscadvancedsettingsbitmapperistence-property"></a>Proprietà IMsTscAdvancedSettings:: BitmapPeristence

Specifica se la memorizzazione nella cache bitmap è abilitata. La memorizzazione nella cache persistente può migliorare le prestazioni, ma richiede ulteriore spazio su disco.

> [!Note]  
> L'errore di ortografia nel nome della proprietà e il relativo parametro si trova nella versione rilasciata del controllo.

 

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT put_BitmapPeristence(
  [in]  LONG bitmapPeristence
);

HRESULT get_BitmapPeristence(
  [out] LONG *pbitmapPeristence
);
```



## <a name="property-value"></a>Valore proprietà

Impostare questo parametro su 0 per disabilitare la memorizzazione nella cache o un valore diverso da zero per abilitare la memorizzazione nella cache.

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

 

 





