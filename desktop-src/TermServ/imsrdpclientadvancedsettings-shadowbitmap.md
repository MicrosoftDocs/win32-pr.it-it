---
title: Proprietà ShadowBitmap di IMsRdpClientAdvancedSettings
description: Specifica se devono essere utilizzate le bitmap Shadow.
ms.assetid: b329e367-7579-466d-877a-16253f85e5a2
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto Proprietà ShadowBitmap
- Servizi Desktop remoto Proprietà ShadowBitmap, interfaccia IMsRdpClientAdvancedSettings
- Interfaccia IMsRdpClientAdvancedSettings Servizi Desktop remoto, Proprietà ShadowBitmap
- Servizi Desktop remoto Proprietà ShadowBitmap, interfaccia IMsRdpClientAdvancedSettings2
- Interfaccia IMsRdpClientAdvancedSettings2 Servizi Desktop remoto, Proprietà ShadowBitmap
- Servizi Desktop remoto Proprietà ShadowBitmap, interfaccia IMsRdpClientAdvancedSettings3
- Interfaccia IMsRdpClientAdvancedSettings3 Servizi Desktop remoto, Proprietà ShadowBitmap
- Servizi Desktop remoto Proprietà ShadowBitmap, interfaccia IMsRdpClientAdvancedSettings4
- Interfaccia IMsRdpClientAdvancedSettings4 Servizi Desktop remoto, Proprietà ShadowBitmap
- Servizi Desktop remoto Proprietà ShadowBitmap, interfaccia IMsRdpClientAdvancedSettings5
- Interfaccia IMsRdpClientAdvancedSettings5 Servizi Desktop remoto, Proprietà ShadowBitmap
- Servizi Desktop remoto Proprietà ShadowBitmap, interfaccia IMsRdpClientAdvancedSettings6
- Interfaccia IMsRdpClientAdvancedSettings6 Servizi Desktop remoto, Proprietà ShadowBitmap
- Servizi Desktop remoto Proprietà ShadowBitmap, interfaccia IMsRdpClientAdvancedSettings7
- Interfaccia IMsRdpClientAdvancedSettings7 Servizi Desktop remoto, Proprietà ShadowBitmap
- Servizi Desktop remoto Proprietà ShadowBitmap, interfaccia IMsRdpClientAdvancedSettings8
- Interfaccia IMsRdpClientAdvancedSettings8 Servizi Desktop remoto, Proprietà ShadowBitmap
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.ShadowBitmap
- IMsRdpClientAdvancedSettings.get_ShadowBitmap
- IMsRdpClientAdvancedSettings.put_ShadowBitmap
- IMsRdpClientAdvancedSettings2.ShadowBitmap
- IMsRdpClientAdvancedSettings2.get_ShadowBitmap
- IMsRdpClientAdvancedSettings2.put_ShadowBitmap
- IMsRdpClientAdvancedSettings3.ShadowBitmap
- IMsRdpClientAdvancedSettings3.get_ShadowBitmap
- IMsRdpClientAdvancedSettings3.put_ShadowBitmap
- IMsRdpClientAdvancedSettings4.ShadowBitmap
- IMsRdpClientAdvancedSettings4.get_ShadowBitmap
- IMsRdpClientAdvancedSettings4.put_ShadowBitmap
- IMsRdpClientAdvancedSettings5.ShadowBitmap
- IMsRdpClientAdvancedSettings5.get_ShadowBitmap
- IMsRdpClientAdvancedSettings5.put_ShadowBitmap
- IMsRdpClientAdvancedSettings6.ShadowBitmap
- IMsRdpClientAdvancedSettings6.get_ShadowBitmap
- IMsRdpClientAdvancedSettings6.put_ShadowBitmap
- IMsRdpClientAdvancedSettings7.ShadowBitmap
- IMsRdpClientAdvancedSettings7.get_ShadowBitmap
- IMsRdpClientAdvancedSettings7.put_ShadowBitmap
- IMsRdpClientAdvancedSettings8.ShadowBitmap
- IMsRdpClientAdvancedSettings8.get_ShadowBitmap
- IMsRdpClientAdvancedSettings8.put_ShadowBitmap
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fc6c43862b498fe5828d2746666c5e414de4c71e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475232"
---
# <a name="imsrdpclientadvancedsettingsshadowbitmap-property"></a>Proprietà IMsRdpClientAdvancedSettings:: ShadowBitmap

\[Questa proprietà non è supportata. A partire da Windows Server 2008 e Windows 7, le chiamate a **ShadowBitmap** restituiscono sempre **S \_ false**.\]

Specifica se devono essere utilizzate le bitmap Shadow.

Le bitmap Shadow sono sempre disabilitate in modalità schermo intero, pertanto questa proprietà non ha alcun effetto in modalità schermo intero.

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT put_ShadowBitmap(
  [in]  LONG shadowBitmap
);

HRESULT get_ShadowBitmap(
  [out] LONG *pshadowBitmap
);
```



## <a name="property-value"></a>Valore proprietà

Impostare questo parametro su 0 per disabilitare la funzionalità o un valore diverso da zero per abilitare la funzionalità. La disabilitazione di questa funzionalità consente in genere di migliorare le prestazioni, ma può generare artefatti quando si disegnano schermate.

## <a name="remarks"></a>Commenti

Per ulteriori informazioni su Connessione Web Desktop remoto, vedere [requisiti per connessione Web Desktop remoto](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                        |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                       |
| Fine del supporto client<br/>    | Windows Vista<br/>                                                                        |
| Fine del supporto server<br/>    | Nessuno supportato<br/>                                                                       |
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

 

 





