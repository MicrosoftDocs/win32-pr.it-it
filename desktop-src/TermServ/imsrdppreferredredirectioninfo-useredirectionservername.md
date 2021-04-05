---
title: Proprietà UseRedirectionServerName di IMsRdpPreferredRedirectionInfo
description: Ottiene e imposta un valore che indica se utilizzare il nome del server di reindirizzamento.
ms.assetid: D2239600-D75D-40FB-A6D0-4C7C4C5163E3
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà UseRedirectionServerName
- Servizi Desktop remoto proprietà UseRedirectionServerName, interfaccia IMsRdpPreferredRedirectionInfo
- Interfaccia IMsRdpPreferredRedirectionInfo Servizi Desktop remoto, proprietà UseRedirectionServerName
topic_type:
- apiref
api_name:
- IMsRdpPreferredRedirectionInfo.UseRedirectionServerName
- IMsRdpPreferredRedirectionInfo.get_UseRedirectionServerName
- IMsRdpPreferredRedirectionInfo.put_UseRedirectionServerName
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d1635273078a2d09ca01c219ebf7eaa482eeb7a4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740759"
---
# <a name="imsrdppreferredredirectioninfouseredirectionservername-property"></a>Proprietà IMsRdpPreferredRedirectionInfo:: UseRedirectionServerName

Ottiene e imposta un valore che indica se utilizzare il nome del server di reindirizzamento.

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT put_UseRedirectionServerName(
  [in]  VARIANT_BOOL UseRedirectionServerName
);

HRESULT get_UseRedirectionServerName(
  [out] VARIANT_BOOL *UseRedirectionServerName
);
```



## <a name="property-value"></a>Valore proprietà

Indica se utilizzare il nome del server di reindirizzamento.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 8<br/>                                                                              |
| Server minimo supportato<br/> | Windows Server 2012<br/>                                                                    |
| Libreria dei tipi<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>            |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>            |
| IID<br/>                      | IID \_ IMsRdpPreferredRedirectionInfo è definito come FDD029F9-9574-4def-8529-64B521CCCAA4<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IMsRdpPreferredRedirectionInfo**](imsrdppreferredredirectioninfo.md)
</dt> </dl>

 

 





