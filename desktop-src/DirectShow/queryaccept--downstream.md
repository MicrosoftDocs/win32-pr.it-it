---
description: QueryAccept (downstream)
ms.assetid: 3ca30f62-c320-40ea-9bf5-022abad912c4
title: QueryAccept (downstream)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9015e0a246abb9fb996c0771e4bc935cccda054d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104563602"
---
# <a name="queryaccept-downstream"></a>QueryAccept (downstream)

Questo meccanismo consente a un pin di output di proporre un nuovo formato al peer downstream. Il nuovo formato non deve richiedere una dimensione del buffer maggiore. Il pin di output esegue le operazioni seguenti:

1.  Chiama [**Ipin:: QueryAccept**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept) o [**IPinConnection::D ynamicqueryaccept**](/windows/desktop/api/Strmif/nf-strmif-ipinconnection-dynamicqueryaccept) sul pin downstream, per verificare se l'altro pin può accettare il nuovo tipo di supporto (vedere la figura, passaggio A).
2.  Se il valore restituito dal passaggio 1 è \_ OK, il pin connette il tipo di supporto all'esempio successivo. A tale scopo, prima di tutto viene chiamato [**IMemAllocator:: GetBuffer**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-getbuffer) per ottenere l'esempio (B). Chiama quindi [**IMediaSample:: SetMediaType**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setmediatype) per alleghiare il tipo di supporto a tale esempio (C). Associando il tipo di supporto all'esempio, il filtro indica che il formato è stato modificato, a partire da tale esempio.
3.  Il pin recapita l'esempio (D).
4.  Quando il filtro downstream riceve l'esempio, chiama [**IMediaSample:: GetMediaType**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getmediatype) per recuperare il nuovo tipo di supporto.

    ![queryaccept (downstream)](images/dynformat3.png)

Tutti i pin supportano il `QueryAccept` metodo. Tuttavia, questo metodo è leggermente ambiguo, perché un valore restituito di S \_ OK non sempre garantisce che sia possibile modificare il formato quando il grafico è attivo. Alcuni filtri potrebbero restituire S \_ OK, ma rifiutare la modifica se il grafico è attivo. Il metodo **DynamicQueryAccept** , supportato da alcuni pin di input, definisce in modo esplicito S \_ OK per indicare che il pin può modificare i formati mentre è attivo. Se un pin di input supporta l'interfaccia **IPinConnection** , è necessario chiamare **DynamicQueryAccept** anziché `QueryAccept` .

Nella maggior parte dei casi, questo meccanismo non consente modifiche drastiche al formato, ad esempio la modifica della profondità dei bit. Una situazione in cui può essere utilizzata è quando un decodificatore video passa le tavolozze. I dettagli di base del formato rimanere invariati, ad esempio le dimensioni dell'immagine e la profondità del bit, ma il nuovo tipo di supporto presenta un set diverso di voci della tavolozza.

**Nota sull'implementazione**

Nelle classi base di DirectShow, [**CBasePin:: QueryAccept**](cbasepin-queryaccept.md) chiama il metodo **CheckMediaType** , che viene chiamato anche durante la connessione iniziale del PIN. Nel caso di un filtro di trasformazione, il metodo **CheckMediaType** del PIN di input deve sempre controllare se il pin di output è connesso e, in tal caso, se il tipo di supporto di input è compatibile con il tipo di supporto di output. Questa implementazione probabilmente sarà quindi valida per `QueryAccept` . In caso contrario, è necessario eseguire l'override `QueryAccept` di per eseguire tutti i controlli aggiuntivi necessari. Si noti inoltre che la classe [**CTransformFilter**](ctransformfilter.md) incapsula questa logica nei metodi **CheckInputType** e **CheckTransform** . La classe [**CTransInPlaceFilter**](ctransinplacefilter.md) , d'altra parte, chiama sempre `QueryAccept` sul filtro upstream o downstream successivo.

Il metodo [**CBaseInputPin:: Receive**](cbaseinputpin-receive.md) verifica la presenza di un tipo di supporto nell'esempio in ingresso e, se presente, chiama **CheckMediaType**. Tuttavia, non aggiorna il membro **\_ mt m** del PIN, che include il tipo di supporto corrente. Quando il filtro elabora l'esempio, è necessario controllare l'esempio per un tipo di supporto. Se è presente un nuovo tipo, probabilmente sarà necessario archiviarlo chiamando **SetMediaType** sul pin oppure impostando il valore di **m \_ mt** direttamente. D'altra parte, la classe [**CVideoTransformFilter**](cvideotransformfilter.md) , progettata per i filtri di trasformazione video, archivia il tipo di supporto quando viene modificato. Per informazioni dettagliate, vedere il codice sorgente per [**CVideoTransformFilter:: Receive**](cvideotransformfilter-receive.md) nella libreria di classi base DirectShow.

In alcuni casi, è possibile passare semplicemente la `QueryAccept` chiamata downstream, quindi alleghi il tipo di supporto all'esempio di output e consentire al filtro downstream di gestire la modifica del formato.

 

 



