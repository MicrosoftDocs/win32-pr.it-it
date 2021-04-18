---
description: La classe CRendererPosPassThru gestisce i comandi Seek per i filtri renderer, passandoli upstream al filtro successivo.
ms.assetid: 7b532177-939c-4cb7-a6fa-c0133f65c768
title: Classe CRendererPosPassThru (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRendererPosPassThru
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7154dde8adefdb3292107e9c33d7b6a2b54f6af0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327193"
---
# <a name="crendererpospassthru-class"></a>Classe CRendererPosPassThru

![gerarchia di classi crendererpospassthru](images/cutil14.png)

La `CRendererPosPassThru` classe gestisce i comandi Seek per i filtri renderer, passandoli upstream al filtro successivo.

Questa classe deriva dalla classe [**CPosPassThru**](cpospassthru.md) . Viene aggiunto il supporto per la memorizzazione nella cache dei timestamp degli esempi Man mano che arrivano. Usare questa classe nello stesso modo della classe **CPosPassThru** . Per informazioni dettagliate, vedere la documentazione di **CPosPassThru** .

Il filtro renderer deve aggiornare i `CRendererPosPassThru` timestamp memorizzati nella cache dell'oggetto, come indicato di seguito:

-   Per ogni esempio che il filtro riceve, chiamare il metodo [**CRendererPosPassThru:: RegisterMediaTime**](crendererpospassthru-registermediatime.md) .
-   Quando il filtro viene arrestato o riceve una chiamata **EndFlush** , chiamare il metodo [**CRendererPosPassThru:: ResetMediaTime**](crendererpospassthru-resetmediatime.md) .
-   Quando il filtro riceve una notifica di fine flusso, chiamare il metodo [**CRendererPosPassThru:: EOS**](crendererpospassthru-eos.md) .

Per un esempio di come usare questa classe, vedere il codice sorgente di [**CBaseRenderer**](cbaserenderer.md) .



| Metodi pubblici                                                            | Descrizione                                                         |
|---------------------------------------------------------------------------|---------------------------------------------------------------------|
| [**CRendererPosPassThru**](crendererpospassthru-crendererpospassthru.md) | Metodo del costruttore.                                                 |
| [**GetMediaTime**](crendererpospassthru-getmediatime.md)                 | Recupera i timestamp sull'esempio corrente.                    |
| [**RegisterMediaTime**](crendererpospassthru-registermediatime.md)       | Memorizza nella cache i timestamp dell'esempio corrente.                     |
| [**ResetMediaTime**](crendererpospassthru-resetmediatime.md)             | Reimposta i timestamp memorizzati nella cache su zero.                              |
| [**EOS**](crendererpospassthru-eos.md)                                   | Aggiorna i timestamp memorizzati nella cache dopo una notifica di fine del flusso. |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Ctlutil. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



 

 




