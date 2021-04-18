---
description: La classe CSeekingPassThru è un oggetto helper che crea oggetti CPosPassThru e CRendererPosPassThru.
ms.assetid: a748ea5c-d93f-4f80-9d2f-bef5a5c1c2fb
title: Classe CSeekingPassThru (Seekpt. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSeekingPassThru
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 273f9b6686c4455452924dc43628801fae5d518a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324663"
---
# <a name="cseekingpassthru-class"></a>Classe CSeekingPassThru

La `CSeekingPassThru` classe è un oggetto helper che crea oggetti [**CPosPassThru**](cpospassthru.md) e [**CRendererPosPassThru**](crendererpospassthru.md) .

Le classi **CPosPassThru** e **CRendererPosPassThru** sono oggetti helper che passano i comandi di ricerca upstream, quindi la `CSeekingPassThru` classe è un oggetto helper per la creazione di oggetti helper.

Non è necessario usare direttamente questa classe. Usare invece la funzione [**CreatePosPassThru**](createpospassthru.md) , che gestisce tutti i dettagli dell'uso di questa classe. Offre l'ulteriore vantaggio di caricare l'oggetto da Quartz.dll, riducendo in qualche modo le dimensioni del codice del filtro. Per ulteriori informazioni, vedere [**CPosPassThru**](cpospassthru.md).

La `CSeekingPassThru` classe espone l'interfaccia [**ISeekingPassThru**](/windows/desktop/api/Strmif/nn-strmif-iseekingpassthru) . Il metodo [**ISeekingPassThru:: init**](/windows/desktop/api/Strmif/nf-strmif-iseekingpassthru-init) Inizializza l'oggetto. Dopo che l'oggetto è stato inizializzato, il filtro può eseguire una query per le interfacce [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) e [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition) .



| Metodi pubblici                                                  | Descrizione                        |
|-----------------------------------------------------------------|------------------------------------|
| [**CSeekingPassThru**](cseekingpassthru-cseekingpassthru.md)   | Metodo del costruttore.                |
| [**~ CSeekingPassThru**](cseekingpassthru--cseekingpassthru.md) | Metodo del distruttore.                 |
| [**CreateInstance**](cseekingpassthru-createinstance.md)       | Crea un'istanza dell'oggetto. |
| Metodi ISeekingPassThru                                        | Descrizione                        |
| [**Init**](cseekingpassthru-init.md)                           | Inizializza l'oggetto.            |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Seekpt. h (include Streams. h)</dt> </dl>                                                                                    |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



 

 




