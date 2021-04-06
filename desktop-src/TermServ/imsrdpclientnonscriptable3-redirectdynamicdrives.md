---
title: Proprietà RedirectDynamicDrives di IMsRdpClientNonScriptable3
description: Specifica o recupera un valore che indica se le unità Plug and Play (PnP) associate in modo dinamico che vengono enumerate in una sessione sono disponibili per il reindirizzamento.
ms.assetid: 11eb19fc-9711-4293-8054-f7975dadb492
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà RedirectDynamicDrives
- Servizi Desktop remoto proprietà RedirectDynamicDrives, interfaccia IMsRdpClientNonScriptable3
- Interfaccia IMsRdpClientNonScriptable3 Servizi Desktop remoto, proprietà RedirectDynamicDrives
- Servizi Desktop remoto proprietà RedirectDynamicDrives, interfaccia IMsRdpClientNonScriptable4
- Interfaccia IMsRdpClientNonScriptable4 Servizi Desktop remoto, proprietà RedirectDynamicDrives
- Servizi Desktop remoto proprietà RedirectDynamicDrives, interfaccia IMsRdpClientNonScriptable5
- Interfaccia IMsRdpClientNonScriptable5 Servizi Desktop remoto, proprietà RedirectDynamicDrives
- Servizi Desktop remoto proprietà RedirectDynamicDrives, oggetto MsRdpClient5
- Oggetto MsRdpClient5 Servizi Desktop remoto, proprietà RedirectDynamicDrives
- Servizi Desktop remoto proprietà RedirectDynamicDrives, oggetto MsRdpClient6
- Oggetto MsRdpClient6 Servizi Desktop remoto, proprietà RedirectDynamicDrives
- Servizi Desktop remoto proprietà RedirectDynamicDrives, oggetto MsRdpClient7
- Oggetto MsRdpClient7 Servizi Desktop remoto, proprietà RedirectDynamicDrives
- Servizi Desktop remoto proprietà RedirectDynamicDrives, oggetto MsRdpClient8
- Oggetto MsRdpClient8 Servizi Desktop remoto, proprietà RedirectDynamicDrives
- Servizi Desktop remoto proprietà RedirectDynamicDrives, oggetto MsRdpClient9
- Oggetto MsRdpClient9 Servizi Desktop remoto, proprietà RedirectDynamicDrives
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable3.RedirectDynamicDrives
- IMsRdpClientNonScriptable3.get_RedirectDynamicDrives
- IMsRdpClientNonScriptable3.put_RedirectDynamicDrives
- IMsRdpClientNonScriptable4.RedirectDynamicDrives
- IMsRdpClientNonScriptable4.get_RedirectDynamicDrives
- IMsRdpClientNonScriptable4.put_RedirectDynamicDrives
- IMsRdpClientNonScriptable5.RedirectDynamicDrives
- IMsRdpClientNonScriptable5.get_RedirectDynamicDrives
- IMsRdpClientNonScriptable5.put_RedirectDynamicDrives
- MsRdpClient5.RedirectDynamicDrives
- MsRdpClient6.RedirectDynamicDrives
- MsRdpClient7.RedirectDynamicDrives
- MsRdpClient8.RedirectDynamicDrives
- MsRdpClient9.RedirectDynamicDrives
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b19c0e6e20f7f73481f6f2ecbc50ab0eda512ded
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743647"
---
# <a name="imsrdpclientnonscriptable3redirectdynamicdrives-property"></a>Proprietà IMsRdpClientNonScriptable3:: RedirectDynamicDrives

Specifica o recupera un valore che indica se le unità Plug and Play (PnP) associate in modo dinamico che vengono enumerate in una sessione sono disponibili per il reindirizzamento.

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT put_RedirectDynamicDrives(
  [in]  VARIANT_BOOL fRedirectDynamicDrives
);

HRESULT get_RedirectDynamicDrives(
  [out] VARIANT_BOOL *pfRedirectDynamicDrives
);
```



## <a name="property-value"></a>Valore proprietà

Specifica se le unità PnP associate in modo dinamico enumerate in una sessione sono disponibili per il reindirizzamento.

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

 

 





