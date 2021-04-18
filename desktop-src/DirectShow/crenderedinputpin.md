---
description: La classe CRenderedInputPin è una classe di base per l'implementazione di un pin di input in un renderer.
ms.assetid: 644dc6ef-eefa-4dfa-a27e-cab690b6e1db
title: Classe CRenderedInputPin (Amextra. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRenderedInputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3fc00b4aa0ce1fc6c8a93fb2fbda2118ad6bb40e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328824"
---
# <a name="crenderedinputpin-class"></a>Classe CRenderedInputPin

![gerarchia di classi crenderedinputpin](images/rbase04.png)

La classe **CRenderedInputPin** è una classe di base per l'implementazione di un pin di input in un renderer. Questa classe è progettata per i filtri renderer che non derivano dalla classe [**CBaseRenderer**](cbaserenderer.md) . I filtri che derivano da **CBaseRenderer** devono usare la classe [**CRendererInputPin**](crendererinputpin.md) per il pin di input.

Per utilizzare questa classe, è necessario eseguire almeno le operazioni seguenti:

-   Dichiarare una nuova classe pin che eredita **CRenderedInputPin**.
-   Nella classe pin, dichiarare un oggetto sezione critica per mantenere il blocco di streaming. A questo scopo, è possibile usare la classe [**CCritSec**](ccritsec.md) . Per altre informazioni, vedere [thread e sezioni critiche](threads-and-critical-sections.md).
-   Eseguire l'override di [**CRenderedInputPin:: EndOfStream**](crenderedinputpin-endofstream.md) per mantenere il blocco di streaming.
-   Implementare i metodi [**IMemInputPin:: Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive), [**CBasePin:: CheckMediaType**](cbasepin-checkmediatype.md)e [**CBasePin:: GetMediaType**](cbasepin-getmediatype.md) .
-   Nel filtro implementare [**CBaseFilter:: GetPin**](cbasefilter-getpin.md) per restituire un'istanza della classe pin.

È possibile usare questa classe in un renderer con più di un pin di input. Questa classe eredita la classe [**CBaseInputPin**](cbaseinputpin.md) .



| Variabili membro protette                                            | Descrizione                                                                                                  |
|-----------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| [**\_bAtEndOfStream m**](crenderedinputpin-m-batendofstream.md)       | Indica se è stata raggiunta la fine del flusso.                                                         |
| [**\_bCompleteNotified m**](crenderedinputpin-m-bcompletenotified.md) | Indica se il pin ha inviato un evento [**EC \_ complete**](ec-complete.md) al gestore del grafico dei filtri. |
| Metodi pubblici                                                        | Descrizione                                                                                                  |
| [**Attivo**](crenderedinputpin-active.md)                            | Notifica al pin che il filtro è ora attivo.                                                              |
| [**CRenderedInputPin**](crenderedinputpin-crenderedinputpin.md)      | Metodo del costruttore.                                                                                          |
| [**Correre**](crenderedinputpin-run.md)                                  | Notifica al pin che il filtro è ora in esecuzione.                                                             |
| Metodi IPin                                                          | Descrizione                                                                                                  |
| [**EndFlush**](crenderedinputpin-endflush.md)                        | Termina un'operazione di svuotamento.                                                                                      |
| [**EndOfStream**](crenderedinputpin-endofstream.md)                  | Notifica al pin che non sono previsti dati aggiuntivi fino a quando il filtro non riceve un nuovo comando Run.            |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amextra. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



 

 




