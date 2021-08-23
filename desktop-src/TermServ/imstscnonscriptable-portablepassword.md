---
title: Proprietà IMsTscNonScriptable PortablePassword
description: Questa proprietà non è più disponibile per l'uso. | Proprietà IMsTscNonScriptable PortablePassword
ms.assetid: 8d831ed3-1f4a-41a9-b283-507c5d9eea22
ms.tgt_platform: multiple
keywords:
- Proprietà PortablePassword Servizi Desktop remoto
- Proprietà PortablePassword Servizi Desktop remoto, interfaccia IMsTscNonScriptable
- Interfaccia IMsTscNonScriptable Servizi Desktop remoto , proprietà PortablePassword
- Proprietà PortablePassword Servizi Desktop remoto , oggetto MsTscAx
- Oggetto MsTscAx Servizi Desktop remoto , proprietà PortablePassword
- Proprietà PortablePassword Servizi Desktop remoto, interfaccia IMsRdpClientNonScriptable
- Interfaccia IMsRdpClientNonScriptable Servizi Desktop remoto , proprietà PortablePassword
- Proprietà PortablePassword Servizi Desktop remoto, interfaccia IMsRdpClientNonScriptable2
- Interfaccia IMsRdpClientNonScriptable2 Servizi Desktop remoto , proprietà PortablePassword
- Proprietà PortablePassword Servizi Desktop remoto, interfaccia IMsRdpClientNonScriptable3
- Interfaccia IMsRdpClientNonScriptable3 Servizi Desktop remoto , proprietà PortablePassword
- Proprietà PortablePassword Servizi Desktop remoto, interfaccia IMsRdpClientNonScriptable4
- Interfaccia IMsRdpClientNonScriptable4 Servizi Desktop remoto , proprietà PortablePassword
- Proprietà PortablePassword Servizi Desktop remoto, interfaccia IMsRdpClientNonScriptable5
- Interfaccia IMsRdpClientNonScriptable5 Servizi Desktop remoto , proprietà PortablePassword
topic_type:
- apiref
api_name:
- IMsTscNonScriptable.PortablePassword
- IMsTscNonScriptable.get_PortablePassword
- IMsTscNonScriptable.put_PortablePassword
- MsTscAx.PortablePassword
- IMsRdpClientNonScriptable.PortablePassword
- IMsRdpClientNonScriptable.get_PortablePassword
- IMsRdpClientNonScriptable.put_PortablePassword
- IMsRdpClientNonScriptable2.PortablePassword
- IMsRdpClientNonScriptable2.get_PortablePassword
- IMsRdpClientNonScriptable2.put_PortablePassword
- IMsRdpClientNonScriptable3.PortablePassword
- IMsRdpClientNonScriptable3.get_PortablePassword
- IMsRdpClientNonScriptable3.put_PortablePassword
- IMsRdpClientNonScriptable4.PortablePassword
- IMsRdpClientNonScriptable4.get_PortablePassword
- IMsRdpClientNonScriptable4.put_PortablePassword
- IMsRdpClientNonScriptable5.PortablePassword
- IMsRdpClientNonScriptable5.get_PortablePassword
- IMsRdpClientNonScriptable5.put_PortablePassword
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fad57f972d3f33f199a3908f1c088f889fa7a56933878cd616feadd418f9424f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119512041"
---
# <a name="imstscnonscriptableportablepassword-property"></a>Proprietà IMsTscNonScriptable::P ortablePassword

Questa proprietà non è più disponibile per l'uso.

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT put_PortablePassword(
  [in]  BSTR newPortablePassVal
);

HRESULT get_PortablePassword(
  [out] BSTR *pPortablePass
);
```



## <a name="property-value"></a>Valore proprietà

Nuova parte della password, in formato codificato portabile.

## <a name="error-codes"></a>Codici di errore

Restituisce **E \_ NOTIMPL.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                              |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                              |
| Fine del supporto client<br/>    | Nessuno supportato<br/>                                                              |
| Fine del supporto server<br/>    | Nessuno supportato<br/>                                                              |
| Libreria dei tipi<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IMsTscNonScriptable IID è definito \_ come c1e6743a-41c1-4a74-832a-0dd06c1c7a0e<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IMsRdpClientNonScriptable**](imsrdpclientnonscriptable-interface.md)
</dt> <dt>

[**IMsRdpClientNonScriptable2**](imsrdpclientnonscriptable2.md)
</dt> <dt>

[**IMsRdpClientNonScriptable3**](imsrdpclientnonscriptable3.md)
</dt> <dt>

[**IMsRdpClientNonScriptable4**](imsrdpclientnonscriptable4.md)
</dt> <dt>

[**IMsRdpClientNonScriptable5**](imsrdpclientnonscriptable5.md)
</dt> <dt>

[**IMsTscNonScriptable**](imstscnonscriptable-interface.md)
</dt> </dl>

 

 





