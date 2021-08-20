---
title: Proprietà BitmapPersistence IMsRdpClientAdvancedSettings
description: Specifica se deve essere utilizzata la memorizzazione nella cache delle bitmap persistenti. La memorizzazione nella cache persistente può migliorare le prestazioni, ma richiede spazio su disco aggiuntivo.
ms.assetid: ffaa9277-9dd7-4b2a-9de5-009b7e8766bc
ms.tgt_platform: multiple
keywords:
- Proprietà BitmapPersistence Servizi Desktop remoto
- Proprietà BitmapPersistence Servizi Desktop remoto, interfaccia IMsRdpClientAdvancedSettings
- Interfaccia IMsRdpClientAdvancedSettings Servizi Desktop remoto , proprietà BitmapPersistence
- Proprietà BitmapPersistence Servizi Desktop remoto, interfaccia IMsRdpClientAdvancedSettings2
- Interfaccia IMsRdpClientAdvancedSettings2 Servizi Desktop remoto proprietà , BitmapPersistence
- Proprietà BitmapPersistence Servizi Desktop remoto, interfaccia IMsRdpClientAdvancedSettings3
- Interfaccia IMsRdpClientAdvancedSettings3 Servizi Desktop remoto proprietà , BitmapPersistence
- Proprietà BitmapPersistence Servizi Desktop remoto, interfaccia IMsRdpClientAdvancedSettings4
- Interfaccia IMsRdpClientAdvancedSettings4 Servizi Desktop remoto proprietà , BitmapPersistence
- Proprietà BitmapPersistence Servizi Desktop remoto, interfaccia IMsRdpClientAdvancedSettings5
- Interfaccia IMsRdpClientAdvancedSettings5 Servizi Desktop remoto proprietà , BitmapPersistence
- Proprietà BitmapPersistence Servizi Desktop remoto, interfaccia IMsRdpClientAdvancedSettings6
- Interfaccia IMsRdpClientAdvancedSettings6 Servizi Desktop remoto proprietà , BitmapPersistence
- Proprietà BitmapPersistence Servizi Desktop remoto, interfaccia IMsRdpClientAdvancedSettings7
- Interfaccia IMsRdpClientAdvancedSettings7 Servizi Desktop remoto proprietà , BitmapPersistence
- Proprietà BitmapPersistence Servizi Desktop remoto, interfaccia IMsRdpClientAdvancedSettings8
- Interfaccia IMsRdpClientAdvancedSettings8 Servizi Desktop remoto proprietà , BitmapPersistence
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.BitmapPersistence
- IMsRdpClientAdvancedSettings.get_BitmapPersistence
- IMsRdpClientAdvancedSettings.put_BitmapPersistence
- IMsRdpClientAdvancedSettings2.BitmapPersistence
- IMsRdpClientAdvancedSettings2.get_BitmapPersistence
- IMsRdpClientAdvancedSettings2.put_BitmapPersistence
- IMsRdpClientAdvancedSettings3.BitmapPersistence
- IMsRdpClientAdvancedSettings3.get_BitmapPersistence
- IMsRdpClientAdvancedSettings3.put_BitmapPersistence
- IMsRdpClientAdvancedSettings4.BitmapPersistence
- IMsRdpClientAdvancedSettings4.get_BitmapPersistence
- IMsRdpClientAdvancedSettings4.put_BitmapPersistence
- IMsRdpClientAdvancedSettings5.BitmapPersistence
- IMsRdpClientAdvancedSettings5.get_BitmapPersistence
- IMsRdpClientAdvancedSettings5.put_BitmapPersistence
- IMsRdpClientAdvancedSettings6.BitmapPersistence
- IMsRdpClientAdvancedSettings6.get_BitmapPersistence
- IMsRdpClientAdvancedSettings6.put_BitmapPersistence
- IMsRdpClientAdvancedSettings7.BitmapPersistence
- IMsRdpClientAdvancedSettings7.get_BitmapPersistence
- IMsRdpClientAdvancedSettings7.put_BitmapPersistence
- IMsRdpClientAdvancedSettings8.BitmapPersistence
- IMsRdpClientAdvancedSettings8.get_BitmapPersistence
- IMsRdpClientAdvancedSettings8.put_BitmapPersistence
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c1dc22347941d71cec7002fef8841f95b548075070c221ddd21c9d331aab8c5d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118353458"
---
# <a name="imsrdpclientadvancedsettingsbitmappersistence-property"></a>Proprietà IMsRdpClientAdvancedSettings::BitmapPersistence

Specifica se deve essere utilizzata la memorizzazione nella cache delle bitmap persistenti. La memorizzazione nella cache persistente può migliorare le prestazioni, ma richiede spazio su disco aggiuntivo.

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT put_BitmapPersistence(
  [in]  LONG bitmapPeristence
);

HRESULT get_BitmapPersistence(
  [out] LONG *pbitmapPeristence
);
```



## <a name="property-value"></a>Valore proprietà

Impostare questo parametro su 0 per disabilitare la memorizzazione nella cache o su un valore diverso da zero per abilitare la memorizzazione nella cache.

> [!Note]  
> L'errore di ortografia nel nome del parametro si trova nella versione rilasciata del controllo.

 

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

 

 





