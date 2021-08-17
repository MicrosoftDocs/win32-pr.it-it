---
title: Proprietà DisableConnectionBar IMsRdpClientNonScriptable5
description: Specifica se il controllo Desktop remoto ActiveX deve disabilitare la barra delle connessioni.
ms.assetid: 82c57b93-f976-43e6-97f9-3602bf97e466
ms.tgt_platform: multiple
keywords:
- Proprietà DisableConnectionBar Servizi Desktop remoto
- Proprietà DisableConnectionBar Servizi Desktop remoto, interfaccia IMsRdpClientNonScriptable5
- Interfaccia IMsRdpClientNonScriptable5 Servizi Desktop remoto , proprietà DisableConnectionBar
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable5.DisableConnectionBar
- IMsRdpClientNonScriptable5.put_DisableConnectionBar
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4f74fce650eb82514538eed7066b937c29f8618aba1eab7531f3bdb7e1127da5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119138744"
---
# <a name="imsrdpclientnonscriptable5disableconnectionbar-property"></a>Proprietà IMsRdpClientNonScriptable5::D isableConnectionBar

Specifica se il controllo Desktop remoto ActiveX deve disabilitare la barra delle connessioni. Se questa proprietà contiene **VARIANT \_ TRUE,** la barra di connessione deve essere disabilitata. Se questa proprietà contiene **VARIANT \_ FALSE,** la barra delle connessioni deve essere abilitata.

Questa proprietà è di sola scrittura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT put_DisableConnectionBar(
  [in] VARIANT_BOOL fDisableConnectionBar
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

 

 





