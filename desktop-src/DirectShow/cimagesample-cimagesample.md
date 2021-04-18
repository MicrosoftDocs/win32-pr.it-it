---
description: Metodo del costruttore.
ms.assetid: d7550c38-d728-41b2-80a6-20728abf6012
title: Costruttore CImageSample. CImageSample (Winutil. h)
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
ms.openlocfilehash: 805be59cfc899b6461fa8c761eebb5821118640f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325058"
---
# <a name="cimagesamplecimagesample-constructor"></a>Costruttore CImageSample. CImageSample

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

Puntatore all'allocatore che ha creato l'esempio.

</dd> <dt>

*pName* 
</dt> <dd>

Ignorato.

</dd> <dt>

*PHR* 
</dt> <dd>

Ignorato.

</dd> <dt>

*pBuffer* 
</dt> <dd>

Puntatore a un buffer di memoria allocato dal chiamante, della *lunghezza* della dimensione. Il buffer deve contenere una bitmap indipendente dal dispositivo (DIB) GDI.

</dd> <dt>

*length* 
</dt> <dd>

Lunghezza del buffer.

</dd> </dl>

## <a name="remarks"></a>Commenti

La classe [**CImageAllocator**](cimageallocator.md) crea una DIB usando un oggetto di mapping dei file supportato dal file di paging del sistema operativo. L'handle per l'oggetto di mapping dei file viene archiviato nel membro **hMapping** della struttura **m \_ DibData** .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>WinUtil. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CImageSample**](cimagesample.md)
</dt> </dl>

 

 




