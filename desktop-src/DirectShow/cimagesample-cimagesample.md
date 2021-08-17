---
description: 'Costruttore CImageSample.CImageSample : metodo costruttore.'
ms.assetid: d7550c38-d728-41b2-80a6-20728abf6012
title: Costruttore CImageSample.CImageSample (Winutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageSample.CImageSample
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4eeb15ec42daed1fa835eff28a4953b223d9782859bfcc23b174dee8fee65019
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118402531"
---
# <a name="cimagesamplecimagesample-constructor"></a>Costruttore CImageSample.CImageSample

Metodo del costruttore.

## <a name="syntax"></a>Sintassi


```C++
CImageSample(
   CBaseAllocator *pAllocator,
   TCHAR          *pName,
   HRESULT        *phr,
   LPBYTE         pBuffer,
   LONG           length
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pAllocator* 
</dt> <dd>

Puntatore all'allocatore che ha creato questo esempio.

</dd> <dt>

*Pname* 
</dt> <dd>

Ignorato.

</dd> <dt>

*Phr* 
</dt> <dd>

Ignorato.

</dd> <dt>

*pBuffer* 
</dt> <dd>

Puntatore a un buffer di memoria allocato dal chiamante, di lunghezza *.* Il buffer deve contenere una bitmap GDI indipendente dal dispositivo (DIB).

</dd> <dt>

*length* 
</dt> <dd>

Lunghezza del buffer.

</dd> </dl>

## <a name="remarks"></a>Commenti

La [**classe CImageAllocator**](cimageallocator.md) crea un DIB usando un oggetto di mapping di file supportato dal file di paging del sistema operativo. L'handle per l'oggetto di mapping dei file viene archiviato nel **membro hMapping** della **struttura \_ DibData m.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Winutil.h (includere Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CImageSample**](cimagesample.md)
</dt> </dl>

 

 




