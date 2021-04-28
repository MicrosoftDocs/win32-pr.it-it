---
description: Costruttore CSeekingPassThru.CSeekingPassThru - Metodo costruttore.
ms.assetid: e31253fc-b365-4414-9dee-906d4c41d16e
title: Costruttore CSeekingPassThru.CSeekingPassThru (Seekpt.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSeekingPassThru.CSeekingPassThru
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: cab9d6329f5175c96a3bfc5962ca5a555fe62b5d
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085379"
---
# <a name="cseekingpassthrucseekingpassthru-constructor"></a>Costruttore CSeekingPassThru.CSeekingPassThru

Metodo del costruttore.

## <a name="syntax"></a>Sintassi


```C++
CSeekingPassThru(
   const TCHAR     *pName,
         LPUNKNOWN pUnk,
         HRESULT   *phr
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Pname* 
</dt> <dd>

Stringa contenente il nome dell'oggetto. Per [**altre informazioni, vedere CBaseObject.**](cbaseobject.md)

</dd> <dt>

*Punk* 
</dt> <dd>

Puntatore al proprietario di questo oggetto. Se l'oggetto è aggregato, passare un puntatore all'interfaccia **IUnknown dell'oggetto** aggregatore. In caso contrario, impostare questo parametro su **NULL.**

</dd> <dt>

*Phr* 
</dt> <dd>

Puntatore a un **valore HRESULT.** Ignorato.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Seekpt.h (include Streams.h)</dt> </dl>                                                                                    |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CSeekingPassThru**](cseekingpassthru.md)
</dt> </dl>

 

 




