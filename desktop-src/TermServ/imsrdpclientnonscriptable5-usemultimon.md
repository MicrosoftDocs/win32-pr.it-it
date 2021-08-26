---
title: Proprietà IMsRdpClientNonScriptable5 UseMultimon
description: Specifica se il Desktop remoto ActiveX deve usare più monitor.
ms.assetid: 7832E025-80F6-4B4B-9829-C2D2EF2D8C37
ms.tgt_platform: multiple
keywords:
- Proprietà UseMultimon Servizi Desktop remoto
- Interfaccia UseMultimon Servizi Desktop remoto , IMsRdpClientNonScriptable5
- Interfaccia IMsRdpClientNonScriptable5 Servizi Desktop remoto , proprietà UseMultimon
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable5.UseMultimon
- IMsRdpClientNonScriptable5.get_UseMultimon
- IMsRdpClientNonScriptable5.put_UseMultimon
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8335d4424931b38d5d967e3ad910785e68184668eceda79011ff2c213517a8eb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120033281"
---
# <a name="imsrdpclientnonscriptable5usemultimon-property"></a>Proprietà IMsRdpClientNonScriptable5::UseMultimon

Specifica se il Desktop remoto ActiveX deve usare più monitor. Se questa proprietà contiene **VARIANT \_ TRUE,** il controllo userà più monitor. Se questa proprietà contiene **VARIANT \_ FALSE,** il controllo non userà più monitor.

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT put_UseMultimon(
  [in]          VARIANT_BOOL fUseMultimon
);

HRESULT get_UseMultimon(
  [out, retval] VARIANT_BOOL *pfUseMultimon
);
```



## <a name="property-value"></a>Valore proprietà

Specifica il nuovo valore della proprietà.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7<br/>                                                                          |
| Server minimo supportato<br/> | Windows Server 2008 R2<br/>                                                             |
| Libreria dei tipi<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>        |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>        |
| IID<br/>                      | IID \_ IMsRdpClientNonScriptable5 è definito come 4f6996d5-d7b1-412c-b0ff-063718566907<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IMsRdpClientNonScriptable5**](imsrdpclientnonscriptable5.md)
</dt> </dl>

 

 





