---
title: Proprietà IMsRdpClientNonScriptable5 RemoteMonitorLayoutMatchesLocal
description: Specifica se il layout del monitoraggio remoto è identico al layout del monitor locale.
ms.assetid: 8F3C6650-870C-417C-82FC-E145FC360012
ms.tgt_platform: multiple
keywords:
- Proprietà RemoteMonitorLayoutMatchesLocal Servizi Desktop remoto
- Proprietà RemoteMonitorLayoutMatchesLocal Servizi Desktop remoto, interfaccia IMsRdpClientNonScriptable5
- Interfaccia IMsRdpClientNonScriptable5 Servizi Desktop remoto , proprietà RemoteMonitorLayoutMatchesLocal
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable5.RemoteMonitorLayoutMatchesLocal
- IMsRdpClientNonScriptable5.get_RemoteMonitorLayoutMatchesLocal
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 235879a80e7e2a90207ee9b7852e73a26874c0961d7394fa80f2cf85e7452362
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119138724"
---
# <a name="imsrdpclientnonscriptable5remotemonitorlayoutmatcheslocal-property"></a>Proprietà IMsRdpClientNonScriptable5::RemoteMonitorLayoutMatchesLocal

Specifica se il layout del monitoraggio remoto è identico al layout del monitor locale. Se questa proprietà contiene **VARIANT \_ TRUE,** il layout del monitoraggio remoto è identico al layout del monitoraggio locale. Se questa proprietà contiene **VARIANT \_ FALSE,** i monitoraggi remoti e locali hanno layout diversi.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT get_RemoteMonitorLayoutMatchesLocal(
  [out, retval] VARIANT_BOOL *pfRemoteMatchesLocal
);
```



## <a name="property-value"></a>Valore proprietà

Riceve il valore della proprietà.

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

 

 





