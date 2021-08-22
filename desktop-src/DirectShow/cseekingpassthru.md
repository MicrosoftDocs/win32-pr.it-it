---
description: La classe CSeekingPassThru è un oggetto helper che crea oggetti CPosPassThru e CRendererPosPassThru.
ms.assetid: a748ea5c-d93f-4f80-9d2f-bef5a5c1c2fb
title: Classe CSeekingPassThru (Seekpt.h)
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
ms.openlocfilehash: 3ffb8436623cb5ba5f415ceb8bbdafe00e22487da2bbfaba5d02ee4c8f189c10
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118953770"
---
# <a name="cseekingpassthru-class"></a>Classe CSeekingPassThru

La `CSeekingPassThru` classe è un oggetto helper che crea oggetti [**CPosPassThru**](cpospassthru.md) e [**CRendererPosPassThru.**](crendererpospassthru.md)

Le **classi CPosPassThru** e **CRendererPosPassThru** sono oggetti helper che passano i comandi di ricerca a monte, quindi la classe è un oggetto helper per la creazione di `CSeekingPassThru` oggetti helper.

Non è necessario usare direttamente questa classe. Usare invece la [**funzione CreatePosPassThru,**](createpospassthru.md) che gestisce tutti i dettagli dell'uso di questa classe. Ha l'ulteriore vantaggio di caricare l'oggetto da Quartz.dll, riducendo in qualche modo le dimensioni del codice del filtro. Per altre informazioni, vedere [**CPosPassThru**](cpospassthru.md).

La `CSeekingPassThru` classe espone [**l'interfaccia ISeekingPassThru.**](/windows/desktop/api/Strmif/nn-strmif-iseekingpassthru) Il [**metodo ISeekingPassThru::Init**](/windows/desktop/api/Strmif/nf-strmif-iseekingpassthru-init) inizializza l'oggetto . Dopo l'inizializzazione dell'oggetto, il filtro può eseguire una query per le [**interfacce IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) e [**IMediaPosition.**](/windows/desktop/api/Control/nn-control-imediaposition)



| Metodi pubblici                                                  | Descrizione                        |
|-----------------------------------------------------------------|------------------------------------|
| [**CSeekingPassThru**](cseekingpassthru-cseekingpassthru.md)   | Metodo del costruttore.                |
| [**~CSeekingPassThru**](cseekingpassthru--cseekingpassthru.md) | Metodo del distruttore.                 |
| [**CreateInstance**](cseekingpassthru-createinstance.md)       | Crea un'istanza dell'oggetto . |
| Metodi di ISeekingPassThru                                        | Descrizione                        |
| [**Init**](cseekingpassthru-init.md)                           | Inizializza l'oggetto.            |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Seekpt.h (includere Flussi.h)</dt> </dl>                                                                                    |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



 

 




