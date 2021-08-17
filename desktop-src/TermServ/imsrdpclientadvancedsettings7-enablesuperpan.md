---
title: Proprietà EnableSuperPan di IMsRdpClientAdvancedSettings7
description: Specifica o recupera un valore booleano che indica se SuperPan è abilitato o disabilitato.
ms.assetid: 0d0ef89e-75f5-460a-ad55-01f8d9478df5
ms.tgt_platform: multiple
keywords:
- Proprietà EnableSuperPan Servizi Desktop remoto
- Proprietà EnableSuperPan Servizi Desktop remoto, interfaccia IMsRdpClientAdvancedSettings7
- Interfaccia IMsRdpClientAdvancedSettings7 Servizi Desktop remoto , proprietà EnableSuperPan
- Proprietà EnableSuperPan Servizi Desktop remoto, interfaccia IMsRdpClientAdvancedSettings8
- Interfaccia IMsRdpClientAdvancedSettings8 Servizi Desktop remoto , proprietà EnableSuperPan
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings7.EnableSuperPan
- IMsRdpClientAdvancedSettings7.get_EnableSuperPan
- IMsRdpClientAdvancedSettings7.put_EnableSuperPan
- IMsRdpClientAdvancedSettings8.EnableSuperPan
- IMsRdpClientAdvancedSettings8.get_EnableSuperPan
- IMsRdpClientAdvancedSettings8.put_EnableSuperPan
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dd48fbb42f65e42b0cdeee3560c93361c49283eecfa4ee3a792a19f6081b07b4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117757343"
---
# <a name="imsrdpclientadvancedsettings7enablesuperpan-property"></a>Proprietà IMsRdpClientAdvancedSettings7::EnableSuperPan

Specifica o recupera un valore booleano che indica se SuperPan è abilitato o disabilitato. SuperPan è una funzionalità che consente a un utente di spostarsi facilmente in un desktop remoto in modalità schermo intero, quando le dimensioni del desktop remoto sono maggiori delle dimensioni della finestra del client corrente. Invece di usare le barre di scorrimento per spostarsi sul desktop, l'utente può puntare al bordo della finestra e il desktop remoto scorrerà automaticamente in tale direzione. SuperPan non supporta più monitor.

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT put_EnableSuperPan(
  [in]          VARIANT_BOOL fEnableSuperPan
);

HRESULT get_EnableSuperPan(
  [out, retval] VARIANT_BOOL *pfEnableSuperPan
);
```



## <a name="property-value"></a>Valore proprietà

Valore **VARIANT \_ BOOL** che specifica se SuperPan è abilitato. Il valore **VARIANT \_ TRUE specifica** che SuperPan è abilitato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7<br/>                                                                             |
| Server minimo supportato<br/> | Windows Server 2008 R2<br/>                                                                |
| Libreria dei tipi<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| IID<br/>                      | IID \_ IMsRdpClientAdvancedSettings7 è definito come 26036036-4010-4578-8091-0db9a1edf9c3<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IMsRdpClientAdvancedSettings8**](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings7**](imsrdpclientadvancedsettings7.md)
</dt> </dl>

 

 





