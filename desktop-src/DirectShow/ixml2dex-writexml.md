---
description: Il metodo WriteXML converte una sequenza temporale in una stringa XML.
ms.assetid: 1039c6fc-b2ba-4052-90b6-b7468b94c071
title: Metodo IXml2Dex::WriteXML (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IXml2Dex.WriteXML
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: a5285faad36f83dbab693c63a0c96ca2b1d2b6a25220bb601a9527aac9dc5ac1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120051291"
---
# <a name="ixml2dexwritexml-method"></a>Metodo IXml2Dex::WriteXML

> [!Note]  
> \[Deprecato. Questa API potrebbe essere rimossa dalle versioni future di Windows.\]

 

Il `WriteXML` metodo converte una sequenza temporale in una stringa XML.

## <a name="syntax"></a>Sintassi


```C++
HRESULT WriteXML(
   IUnknown *pTimeline,
   BSTR     *pbstrXML
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pTimeline* 
</dt> <dd>

Puntatore all'interfaccia **IUnknown dell'oggetto** sequenza temporale.

</dd> <dt>

*pbstrXML* 
</dt> <dd>

Puntatore a una variabile di tipo BSTR che riceve la stringa XML che descrive la sequenza temporale.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce S \_ OK in caso di esito positivo. Se la memoria non è sufficiente per la conversione, restituisce E \_ OUTOFMEMORY. In caso contrario, restituisce un altro codice di errore.

## <a name="remarks"></a>Commenti

Il metodo alloca memoria per la stringa. L'applicazione deve **chiamare SysFreeString** per liberare la memoria.

> [!Note]  
> Il file di intestazione Qedit.h non è compatibile con le intestazioni Direct3D successive alla versione 7.

 

> [!Note]  
> Per ottenere Qedit.h, scaricare [Microsoft Windows SDK Update per Windows Vista e .NET Framework 3.0.](https://msdn.microsoft.com/windowsvista/bb980924.aspx) Qedit.h non è disponibile in Microsoft Windows SDK per Windows 7 e .NET Framework 3.5 Service Pack 1.

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------------------------------------------|
| Versione<br/> | Internet Explorer 4.0 o versione successiva<br/>                                               |
| Intestazione<br/>  | <dl> <dt>Qedit.h</dt> </dl>      |
| Libreria<br/> | <dl> <dt>Strmiids.lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IXml2Dex**](ixml2dex.md)
</dt> <dt>

[Codici di errore e di esito positivo](error-and-success-codes.md)
</dt> </dl>

 

 




