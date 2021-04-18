---
title: Proprietà BinaryPassword di IMsTscNonScriptable
description: Questa proprietà non è più disponibile per l'utilizzo. | Proprietà BinaryPassword di IMsTscNonScriptable
ms.assetid: b3be7323-a75f-4ec2-9d58-e8ff3338d6ff
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà BinaryPassword
- Servizi Desktop remoto proprietà BinaryPassword, interfaccia IMsTscNonScriptable
- Interfaccia IMsTscNonScriptable Servizi Desktop remoto, proprietà BinaryPassword
- Servizi Desktop remoto proprietà BinaryPassword, oggetto MsTscAx
- Oggetto MsTscAx Servizi Desktop remoto, proprietà BinaryPassword
- Servizi Desktop remoto proprietà BinaryPassword, interfaccia IMsRdpClientNonScriptable
- Interfaccia IMsRdpClientNonScriptable Servizi Desktop remoto, proprietà BinaryPassword
- Servizi Desktop remoto proprietà BinaryPassword, interfaccia IMsRdpClientNonScriptable2
- Interfaccia IMsRdpClientNonScriptable2 Servizi Desktop remoto, proprietà BinaryPassword
- Servizi Desktop remoto proprietà BinaryPassword, interfaccia IMsRdpClientNonScriptable3
- Interfaccia IMsRdpClientNonScriptable3 Servizi Desktop remoto, proprietà BinaryPassword
- Servizi Desktop remoto proprietà BinaryPassword, interfaccia IMsRdpClientNonScriptable4
- Interfaccia IMsRdpClientNonScriptable4 Servizi Desktop remoto, proprietà BinaryPassword
- Servizi Desktop remoto proprietà BinaryPassword, interfaccia IMsRdpClientNonScriptable5
- Interfaccia IMsRdpClientNonScriptable5 Servizi Desktop remoto, proprietà BinaryPassword
topic_type:
- apiref
api_name:
- IMsTscNonScriptable.BinaryPassword
- IMsTscNonScriptable.get_BinaryPassword
- IMsTscNonScriptable.put_BinaryPassword
- MsTscAx.BinaryPassword
- IMsRdpClientNonScriptable.BinaryPassword
- IMsRdpClientNonScriptable.get_BinaryPassword
- IMsRdpClientNonScriptable.put_BinaryPassword
- IMsRdpClientNonScriptable2.BinaryPassword
- IMsRdpClientNonScriptable2.get_BinaryPassword
- IMsRdpClientNonScriptable2.put_BinaryPassword
- IMsRdpClientNonScriptable3.BinaryPassword
- IMsRdpClientNonScriptable3.get_BinaryPassword
- IMsRdpClientNonScriptable3.put_BinaryPassword
- IMsRdpClientNonScriptable4.BinaryPassword
- IMsRdpClientNonScriptable4.get_BinaryPassword
- IMsRdpClientNonScriptable4.put_BinaryPassword
- IMsRdpClientNonScriptable5.BinaryPassword
- IMsRdpClientNonScriptable5.get_BinaryPassword
- IMsRdpClientNonScriptable5.put_BinaryPassword
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a1d6eab2a3902968ef4d4c953a8da8b9c884a497
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "106321325"
---
# <a name="imstscnonscriptablebinarypassword-property"></a>Proprietà IMsTscNonScriptable:: BinaryPassword

Questa proprietà non è più disponibile per l'utilizzo.

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT put_BinaryPassword(
  [in]  BSTR newPassword
);

HRESULT get_BinaryPassword(
  [out] BSTR *pBinaryPassword
);
```



## <a name="property-value"></a>Valore proprietà

Nuova parte della password, in formato con codifica binaria.

## <a name="error-codes"></a>Codici di errore

Restituisce **E \_ NOTIMPL**.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                              |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                              |
| Fine del supporto client<br/>    | Nessuno supportato<br/>                                                              |
| Fine del supporto server<br/>    | Nessuno supportato<br/>                                                              |
| Libreria dei tipi<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IID \_ IMsTscNonScriptable è definito come c1e6743a-41C1-4a74-832a-0dd06c1c7a0e<br/> |



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

 

 





