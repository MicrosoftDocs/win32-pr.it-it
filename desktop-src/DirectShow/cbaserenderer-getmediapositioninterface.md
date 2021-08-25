---
description: Il metodo GetMediaPositionInterface recupera i puntatori di interfaccia IMediaPosition e IMediaSeeking del filtro.
ms.assetid: aeca4484-cecc-4d07-aa77-56221ff75699
title: Metodo CBaseRenderer.GetMediaPositionInterface (Renbase.h)
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
ms.openlocfilehash: 12e15b297f78b3386ae9ad31e749858bad14b87e59e938ac02a3cf3a9ca002a9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119872331"
---
# <a name="cbaserenderergetmediapositioninterface-method"></a>Metodo CBaseRenderer.GetMediaPositionInterface

Il metodo recupera i puntatori di interfaccia `GetMediaPositionInterface` [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition) e [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) del filtro.

## <a name="syntax"></a>Sintassi


```C++
virtual HRESULT GetMediaPositionInterface(
   REFIID riid,
   void   **ppv
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Riid* 
</dt> <dd>

Identificatore di riferimento dell'interfaccia.

</dd> <dt>

*Ppv* 
</dt> <dd>

Indirizzo di una variabile che riceve il puntatore a interfaccia.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un **valore HRESULT.** I valori possibili includono quelli illustrati nella tabella seguente.



| Codice restituito                                                                                   | Descrizione                         |
|-----------------------------------------------------------------------------------------------|-------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Operazione completata.<br/>                 |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Memoria insufficiente.<br/>     |
| <dl> <dt>**E \_ NOINTERFACE**</dt> </dl> | Interfaccia non supportata.<br/> |



 

## <a name="remarks"></a>Commenti

Il filtro delega tutti i comandi di ricerca a un oggetto [**CRendererPosPassThru,**](crendererpospassthru.md) che li passa a monte. Questo metodo crea **l'oggetto CRendererPosPassThru,** se non esiste ancora, ed esegue una query per l'interfaccia richiesta.

La [**variabile membro CBaseRenderer::m \_ pPosition**](cbaserenderer-m-pposition.md) archivia un puntatore all'oggetto **CRendererPosPassThru.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Renbase.h (includere Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseRenderer**](cbaserenderer.md)
</dt> </dl>

 

 




