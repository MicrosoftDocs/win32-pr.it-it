---
title: Proprietà UseMultimon di IMsRdpClientNonScriptable5
description: Specifica se il controllo ActiveX Desktop remoto deve usare più monitor.
ms.assetid: 7832E025-80F6-4B4B-9829-C2D2EF2D8C37
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà UseMultimon
- Servizi Desktop remoto proprietà UseMultimon, interfaccia IMsRdpClientNonScriptable5
- Interfaccia IMsRdpClientNonScriptable5 Servizi Desktop remoto, proprietà UseMultimon
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
ms.openlocfilehash: 941a2991ef5591176cd2508bbb6a097fecabebf0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964508"
---
# <a name="imsrdpclientnonscriptable5usemultimon-property"></a>Proprietà IMsRdpClientNonScriptable5:: UseMultimon

Specifica se il controllo ActiveX Desktop remoto deve usare più monitor. Se questa proprietà contiene la **variante \_ true**, il controllo utilizzerà più monitoraggi. Se questa proprietà contiene la **variante \_ false**, il controllo non utilizzerà più monitoraggi.

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
| IID<br/>                      | IID \_ IMsRdpClientNonScriptable5 è definito come 4f6996d5-d7b1-412C-b0ff-063718566907<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IMsRdpClientNonScriptable5**](imsrdpclientnonscriptable5.md)
</dt> </dl>

 

 





