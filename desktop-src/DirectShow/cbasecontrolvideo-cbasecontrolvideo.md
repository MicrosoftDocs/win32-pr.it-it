---
description: Costruttore CBaseControlVideo.CBaseControlVideo - Metodo costruttore.
ms.assetid: 925c6c45-0990-4044-aca1-34f343f438b5
title: Costruttore CBaseControlVideo.CBaseControlVideo (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.CBaseControlVideo
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 389c05b5254326d2966799b857107e79792610e9
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096349"
---
# <a name="cbasecontrolvideocbasecontrolvideo-constructor"></a>Costruttore CBaseControlVideo.CBaseControlVideo

Metodo del costruttore.

## <a name="syntax"></a>Sintassi


```C++
CBaseControlVideo(
   CBaseFilter *pFilter,
   CCritSec    *pInterfaceLock,
   TCHAR       *pName,
   LPUNKNOWN   pUnk,
   HRESULT     *phr
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pFilter* 
</dt> <dd>

Puntatore all'oggetto filtro multimediale proprietario.

</dd> <dt>

*pInterfaceLock* 
</dt> <dd>

Puntatore alla sezione critica da usare per il blocco.

</dd> <dt>

*Pname* 
</dt> <dd>

Puntatore alla descrizione dell'oggetto.

</dd> <dt>

*Punk* 
</dt> <dd>

Puntatore **all'interfaccia IUnknown** di controllo, se l'oggetto fa parte di un'aggregazione; in caso contrario, deve essere **NULL.**

</dd> <dt>

*Phr* 
</dt> <dd>

Puntatore a una variabile che riceve un valore HRESULT che indica l'esito positivo o negativo del metodo del costruttore.

</dd> </dl>

## <a name="remarks"></a>Commenti

L'oggetto implementa [**l'interfaccia di controllo IBasicVideo.**](/windows/desktop/api/Control/nn-control-ibasicvideo)

Tutti i metodi di interfaccia [**di IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) implementati da questa classe richiedono che il filtro sia connesso correttamente. Per questo motivo, alla classe viene passato un pin con cui eseguire la sincronizzazione. Ogni volta che viene chiamato un metodo di interfaccia, l'oggetto determina che il pin è ancora connesso.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Ctlutil.h (include Streams.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseControlVideo**](cbasecontrolvideo.md)
</dt> </dl>

 

 




