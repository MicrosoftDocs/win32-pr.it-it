---
description: Il metodo GetMediaPositionInterface recupera i puntatori dell'interfaccia IMediaPosition e IMediaSeeking del filtro.
ms.assetid: aeca4484-cecc-4d07-aa77-56221ff75699
title: Metodo CBaseRenderer. GetMediaPositionInterface (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.GetMediaPositionInterface
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3d41d777b88f0e18ae1510c32b7e89024ea7bdd9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325521"
---
# <a name="cbaserenderergetmediapositioninterface-method"></a>CBaseRenderer. GetMediaPositionInterface, metodo

Il `GetMediaPositionInterface` metodo recupera i puntatori dell'interfaccia [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition) e [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) del filtro.

## <a name="syntax"></a>Sintassi


```C++
virtual HRESULT GetMediaPositionInterface(
   REFIID riid,
   void   **ppv
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*riid* 
</dt> <dd>

Identificatore di riferimento dell'interfaccia.

</dd> <dt>

*PPV* 
</dt> <dd>

Indirizzo di una variabile che riceve il puntatore a interfaccia.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore **HRESULT** . I valori possibili includono quelli mostrati nella tabella seguente.



| Codice restituito                                                                                   | Descrizione                         |
|-----------------------------------------------------------------------------------------------|-------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>          | Esito positivo.<br/>                 |
| <dl> <dt>**E \_ OutOfMemory**</dt> </dl> | Memoria insufficiente.<br/>     |
| <dl> <dt>**E \_ NOinterface**</dt> </dl> | Interfaccia non supportata.<br/> |



 

## <a name="remarks"></a>Commenti

Il filtro delega tutti i comandi di ricerca a un oggetto [**CRendererPosPassThru**](crendererpospassthru.md) , che li passa a upstream. Questo metodo crea l'oggetto **CRendererPosPassThru** , se non esiste ancora, ed esegue una query per l'interfaccia richiesta.

La variabile membro [**CBaseRenderer:: m \_ pPosition**](cbaserenderer-m-pposition.md) archivia un puntatore all'oggetto **CRendererPosPassThru** .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Renbase. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseRenderer**](cbaserenderer.md)
</dt> </dl>

 

 




