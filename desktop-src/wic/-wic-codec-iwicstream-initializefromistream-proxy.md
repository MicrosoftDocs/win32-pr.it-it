---
description: Funzione proxy per il metodo InitializeFromIStream.
ms.assetid: 3ab780bb-7fe7-4abe-9ea7-86f54ea15d91
title: IWICStream_InitializeFromIStream_Proxy funzione
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICStream_InitializeFromIStream_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 491a2a67881929eba86dc317645161dee28ee9062d01fee63a9f6d4a7995cf72
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120056561"
---
# <a name="iwicstream_initializefromistream_proxy-function"></a>Funzione proxy IWICStream \_ \_ InitializeFromIStream

Funzione proxy per il [**metodo InitializeFromIStream.**](/windows/desktop/api/Wincodec/nf-wincodec-iwicstream-initializefromistream)

## <a name="syntax"></a>Sintassi


```C++
HRESULT IWICStream_InitializeFromIStream_Proxy(
  _In_ IWICStream *THIS_PTR,
  _In_ IStream    *pIStream
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*QUESTO \_ PTR* \[ in\]
</dt> <dd>

Tipo: **[ **IWICStream**](/windows/desktop/api/Wincodec/nn-wincodec-iwicstream)\***

Puntatore a [**questo oggetto IWICStream.**](/windows/desktop/api/Wincodec/nn-wincodec-iwicstream)

</dd> <dt>

*pIStream* \[ Pollici\]
</dt> <dd>

Tipo: **[IStream](/windows/desktop/api/objidl/nn-objidl-istream)\***

Flusso di inizializzazione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **HRESULT**

Se questa funzione ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un **codice di errore HRESULT.**

## <a name="remarks"></a>Osservazioni

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows XP con SP2, Windows solo app desktop di Vista \[\]<br/>                                                                                              |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                                                                                                             |
| DLL<br/>                      | <dl> <dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt> </dl> |



 

