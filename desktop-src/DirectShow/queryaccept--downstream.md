---
description: QueryAccept (Downstream)
ms.assetid: 3ca30f62-c320-40ea-9bf5-022abad912c4
title: QueryAccept (Downstream)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87ec5c26209839f0dcd8351cc9a7ca84227faa2289d44d46c2c321fce0429e3f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119747736"
---
# <a name="queryaccept-downstream"></a>QueryAccept (Downstream)

Questo meccanismo consente a un pin di output di proporre un nuovo formato al peer downstream. Il nuovo formato non deve richiedere dimensioni del buffer maggiori. Il pin di output esegue le operazioni seguenti:

1.  Chiama [**IPin::QueryAccept**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept) o [**IPinConnection::D ynamicQueryAccept**](/windows/desktop/api/Strmif/nf-strmif-ipinconnection-dynamicqueryaccept) sul pin downstream per verificare se l'altro pin può accettare il nuovo tipo di supporto (vedere l'illustrazione, passaggio A).
2.  Se il valore restituito dal passaggio 1 è S OK, il segnaposto collega il tipo \_ di supporto all'esempio successivo. A tale scopo, chiama prima [**IMemAllocator::GetBuffer per**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-getbuffer) ottenere l'esempio (B). Chiama quindi [**IMediaSample::SetMediaType**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setmediatype) per collegare il tipo di supporto a tale esempio (C). Associando il tipo di supporto all'esempio, il filtro indica che il formato è stato modificato, a partire da tale esempio.
3.  Il pin recapita l'esempio (D).
4.  Quando il filtro downstream riceve l'esempio, chiama [**IMediaSample::GetMediaType**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getmediatype) per recuperare il nuovo tipo di supporto.

    ![queryaccept (downstream)](images/dynformat3.png)

Tutti i pin supportano il `QueryAccept` metodo . Tuttavia, questo metodo è leggermente ambiguo, perché un valore restituito di S OK non garantisce sempre che sia possibile modificare il formato mentre il \_ grafico è attivo. Alcuni filtri potrebbero restituire S \_ OK, ma rifiutare la modifica se il grafico è attivo. Il **metodo DynamicQueryAccept,** supportato da alcuni pin di input, definisce in modo esplicito S OK per indicare che il pin può modificare i formati \_ mentre è attivo. Se un pin di input supporta **l'interfaccia IPinConnection,** è necessario chiamare **DynamicQueryAccept** anziché `QueryAccept` .

Nella maggior parte dei casi, questo meccanismo non consente modifiche drastiche al formato, ad esempio la modifica della profondità dei bit. Una situazione in cui può essere usata è quando un decodificatore video passa da una tavolozza all'altra. I dettagli di base del formato rimangono gli stessi, ad esempio le dimensioni dell'immagine e la profondità in bit, ma il nuovo tipo di supporto ha un set diverso di voci della tavolozza.

**Nota sull'implementazione**

Nelle classi DirectShow di base, [**CBasePin::QueryAccept**](cbasepin-queryaccept.md) chiama il **metodo CheckMediaType,** che viene chiamato anche durante la connessione del pin iniziale. Nel caso di un filtro di trasformazione, il metodo **CheckMediaType** del pin di input deve sempre verificare se il pin di output è connesso e, in tal caso, se il tipo di supporto di input è compatibile con il tipo di supporto di output. Pertanto, questa implementazione sarà probabilmente valida per `QueryAccept` . In caso contrario, è necessario eseguire l'override per `QueryAccept` eseguire eventuali controlli aggiuntivi necessari. Si noti inoltre che la [**classe CTransformFilter**](ctransformfilter.md) incapsula questa logica all'interno **dei metodi CheckInputType** **e CheckTransform.** La [**classe CTransInPlaceFilter,**](ctransinplacefilter.md) d'altra parte, chiama sempre il filtro upstream o `QueryAccept` downstream successivo.

Il [**metodo CBaseInputPin::Receive**](cbaseinputpin-receive.md) verifica la presenza di un tipo di supporto nell'esempio in ingresso e, se presente, chiama **CheckMediaType**. Tuttavia, non aggiorna il membro **m \_ mt** del pin, che contiene il tipo di supporto corrente. Quando il filtro elabora l'esempio, è consigliabile controllare l'esempio per un tipo di supporto. Se è presente un nuovo tipo, è probabilmente necessario archiviarlo chiamando **SetMediaType** sul pin o impostando direttamente il valore **di m \_ mt.** D'altra parte, la [**classe CVideoTransformFilter,**](cvideotransformfilter.md) progettata per i filtri di trasformazione video, archivia il tipo di supporto quando cambia. Per informazioni dettagliate, vedere il codice [**sorgente per CVideoTransformFilter::Receive**](cvideotransformfilter-receive.md) nella DirectShow di classi di base.

In alcuni casi, è sufficiente passare la chiamata a valle, quindi collegare il tipo di supporto all'esempio di output e consentire al filtro downstream di `QueryAccept` gestire la modifica del formato.

 

 



