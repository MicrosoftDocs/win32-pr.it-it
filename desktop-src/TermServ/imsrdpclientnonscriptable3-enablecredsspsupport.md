---
title: Proprietà EnableCredSspSupport di IMsRdpClientNonScriptable3
description: Specifica o recupera un valore che indica se il provider del servizio di sicurezza delle credenziali (CredSSP) è abilitato per la connessione.
ms.assetid: 770da50b-2a93-4274-9b6f-c24c13f08549
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà EnableCredSspSupport
- Servizi Desktop remoto proprietà EnableCredSspSupport, interfaccia IMsRdpClientNonScriptable3
- Interfaccia IMsRdpClientNonScriptable3 Servizi Desktop remoto, proprietà EnableCredSspSupport
- Servizi Desktop remoto proprietà EnableCredSspSupport, interfaccia IMsRdpClientNonScriptable4
- Interfaccia IMsRdpClientNonScriptable4 Servizi Desktop remoto, proprietà EnableCredSspSupport
- Servizi Desktop remoto proprietà EnableCredSspSupport, interfaccia IMsRdpClientNonScriptable5
- Interfaccia IMsRdpClientNonScriptable5 Servizi Desktop remoto, proprietà EnableCredSspSupport
- Servizi Desktop remoto proprietà EnableCredSspSupport, oggetto MsRdpClient5
- Oggetto MsRdpClient5 Servizi Desktop remoto, proprietà EnableCredSspSupport
- Servizi Desktop remoto proprietà EnableCredSspSupport, oggetto MsRdpClient6
- Oggetto MsRdpClient6 Servizi Desktop remoto, proprietà EnableCredSspSupport
- Servizi Desktop remoto proprietà EnableCredSspSupport, oggetto MsRdpClient7
- Oggetto MsRdpClient7 Servizi Desktop remoto, proprietà EnableCredSspSupport
- Servizi Desktop remoto proprietà EnableCredSspSupport, oggetto MsRdpClient8
- Oggetto MsRdpClient8 Servizi Desktop remoto, proprietà EnableCredSspSupport
- Servizi Desktop remoto proprietà EnableCredSspSupport, oggetto MsRdpClient9
- Oggetto MsRdpClient9 Servizi Desktop remoto, proprietà EnableCredSspSupport
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable3.EnableCredSspSupport
- IMsRdpClientNonScriptable3.get_EnableCredSspSupport
- IMsRdpClientNonScriptable3.put_EnableCredSspSupport
- IMsRdpClientNonScriptable4.EnableCredSspSupport
- IMsRdpClientNonScriptable4.get_EnableCredSspSupport
- IMsRdpClientNonScriptable4.put_EnableCredSspSupport
- IMsRdpClientNonScriptable5.EnableCredSspSupport
- IMsRdpClientNonScriptable5.get_EnableCredSspSupport
- IMsRdpClientNonScriptable5.put_EnableCredSspSupport
- MsRdpClient5.EnableCredSspSupport
- MsRdpClient6.EnableCredSspSupport
- MsRdpClient7.EnableCredSspSupport
- MsRdpClient8.EnableCredSspSupport
- MsRdpClient9.EnableCredSspSupport
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e2330b800d15f95a7b59a01735de971dd4b212d6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119639"
---
# <a name="imsrdpclientnonscriptable3enablecredsspsupport-property"></a>Proprietà IMsRdpClientNonScriptable3:: EnableCredSspSupport

Specifica o recupera un valore che indica se il provider del servizio di sicurezza delle credenziali (CredSSP) è abilitato per la connessione.

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT put_EnableCredSspSupport(
  [in]  VARIANT_BOOL fEnableSupport
);

HRESULT get_EnableCredSspSupport(
  [out] VARIANT_BOOL *pfEnableSupport
);
```



## <a name="property-value"></a>Valore proprietà

Specifica se CredSSP è abilitato per questa connessione.

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

 

 





