---
title: Proprietà RedirectDynamicDevices di IMsRdpClientNonScriptable3
description: Specifica o recupera un valore che indica se i dispositivi PnP (dynamicly Attached Plug and Play) enumerati in una sessione sono disponibili per il reindirizzamento.
ms.assetid: 8cc5d6a4-108b-4505-8937-f6e790a5c2ba
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà RedirectDynamicDevices
- Servizi Desktop remoto proprietà RedirectDynamicDevices, interfaccia IMsRdpClientNonScriptable3
- Interfaccia IMsRdpClientNonScriptable3 Servizi Desktop remoto, proprietà RedirectDynamicDevices
- Servizi Desktop remoto proprietà RedirectDynamicDevices, interfaccia IMsRdpClientNonScriptable4
- Interfaccia IMsRdpClientNonScriptable4 Servizi Desktop remoto, proprietà RedirectDynamicDevices
- Servizi Desktop remoto proprietà RedirectDynamicDevices, interfaccia IMsRdpClientNonScriptable5
- Interfaccia IMsRdpClientNonScriptable5 Servizi Desktop remoto, proprietà RedirectDynamicDevices
- Servizi Desktop remoto proprietà RedirectDynamicDevices, oggetto MsRdpClient5
- Oggetto MsRdpClient5 Servizi Desktop remoto, proprietà RedirectDynamicDevices
- Servizi Desktop remoto proprietà RedirectDynamicDevices, oggetto MsRdpClient6
- Oggetto MsRdpClient6 Servizi Desktop remoto, proprietà RedirectDynamicDevices
- Servizi Desktop remoto proprietà RedirectDynamicDevices, oggetto MsRdpClient7
- Oggetto MsRdpClient7 Servizi Desktop remoto, proprietà RedirectDynamicDevices
- Servizi Desktop remoto proprietà RedirectDynamicDevices, oggetto MsRdpClient8
- Oggetto MsRdpClient8 Servizi Desktop remoto, proprietà RedirectDynamicDevices
- Servizi Desktop remoto proprietà RedirectDynamicDevices, oggetto MsRdpClient9
- Oggetto MsRdpClient9 Servizi Desktop remoto, proprietà RedirectDynamicDevices
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable3.RedirectDynamicDevices
- IMsRdpClientNonScriptable3.get_RedirectDynamicDevices
- IMsRdpClientNonScriptable3.put_RedirectDynamicDevices
- IMsRdpClientNonScriptable4.RedirectDynamicDevices
- IMsRdpClientNonScriptable4.get_RedirectDynamicDevices
- IMsRdpClientNonScriptable4.put_RedirectDynamicDevices
- IMsRdpClientNonScriptable5.RedirectDynamicDevices
- IMsRdpClientNonScriptable5.get_RedirectDynamicDevices
- IMsRdpClientNonScriptable5.put_RedirectDynamicDevices
- MsRdpClient5.RedirectDynamicDevices
- MsRdpClient6.RedirectDynamicDevices
- MsRdpClient7.RedirectDynamicDevices
- MsRdpClient8.RedirectDynamicDevices
- MsRdpClient9.RedirectDynamicDevices
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 75224d26034e606a7a46943a02845280a092c3b5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740399"
---
# <a name="imsrdpclientnonscriptable3redirectdynamicdevices-property"></a>Proprietà IMsRdpClientNonScriptable3:: RedirectDynamicDevices

Specifica o recupera un valore che indica se i dispositivi PnP (dynamicly Attached Plug and Play) enumerati in una sessione sono disponibili per il reindirizzamento.

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT put_RedirectDynamicDevices(
  [in]  VARIANT_BOOL fRedirectDynamicDevices
);

HRESULT get_RedirectDynamicDevices(
  [out] VARIANT_BOOL *pfRedirectDynamicDevices
);
```



## <a name="property-value"></a>Valore proprietà

Specifica se i dispositivi PnP collegati in modo dinamico enumerati durante una sessione sono disponibili per il reindirizzamento.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                      |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                                |
| Libreria dei tipi<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>        |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>        |
| IID<br/>                      | IID \_ IMsRdpClientNonScriptable3 è definito come b3378d90-0728-45c7-8ed7-b6159fb92219<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IMsRdpClientNonScriptable4**](imsrdpclientnonscriptable4.md)
</dt> <dt>

[**IMsRdpClientNonScriptable5**](imsrdpclientnonscriptable5.md)
</dt> <dt>

[**IMsRdpClientNonScriptable3**](imsrdpclientnonscriptable3.md)
</dt> </dl>

 

 





