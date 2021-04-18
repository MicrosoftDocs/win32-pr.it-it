---
title: Proprietà TransportType di IMsRdpClientAdvancedSettings
description: Specifica il tipo di trasporto utilizzato dal client.
ms.assetid: 752f5fbc-eb5a-48eb-8750-fc25c8a2f024
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto Proprietà TransportType
- Servizi Desktop remoto Proprietà TransportType, interfaccia IMsRdpClientAdvancedSettings
- Interfaccia IMsRdpClientAdvancedSettings Servizi Desktop remoto, Proprietà TransportType
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.TransportType
- IMsRdpClientAdvancedSettings.get_TransportType
- IMsRdpClientAdvancedSettings.put_TransportType
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0664e0c792725dc112baf786d63c5175eb450dcc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106300994"
---
# <a name="imsrdpclientadvancedsettingstransporttype-property"></a>Proprietà IMsRdpClientAdvancedSettings:: TransportType

Specifica il tipo di trasporto utilizzato dal client. Questa proprietà non viene utilizzata dal controllo ActiveX Desktop remoto.

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT put_TransportType(
  [in]  LONG transportType
);

HRESULT get_TransportType(
  [out] LONG *ptransportType
);
```



## <a name="property-value"></a>Valore proprietà

Imposta il tipo di trasporto. Questo metodo può avere esito positivo, ma il valore impostato non viene mai utilizzato dal controllo ActiveX Desktop remoto.

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

[**IMsRdpClientAdvancedSettings**](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





