---
description: Processo di connessione CBasePin
ms.assetid: 4b3a9023-0267-4caa-9d89-88237009df05
title: Processo di connessione CBasePin
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1441b0daba58857e00da0139d3312fb277287fc2
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103965643"
---
# <a name="cbasepin-connection-process"></a>Processo di connessione CBasePin

In questa sezione viene descritto il modo in cui la classe [**CBasePin**](cbasepin.md) implementa il processo di connessione del PIN.

Il gestore del grafico del filtro avvia tutte le connessioni pin. Chiama il metodo [**Ipin:: Connect**](/windows/desktop/api/Strmif/nf-strmif-ipin-connect) del PIN di output, specificando il pin di input. Il pin di output completa la connessione chiamando il metodo [**Ipin:: ReceiveConnection**](/windows/desktop/api/Strmif/nf-strmif-ipin-receiveconnection) del PIN di input. Il pin di input può accettare o rifiutare la connessione.

Il gestore del grafo del filtro può inoltre specificare un tipo di supporto per la connessione. In tal caso, i pin tentano di connettersi a tale tipo. In caso contrario, i pin devono negoziare il tipo. Il gestore del grafico del filtro può inoltre specificare un tipo di supporto *parziale* , il cui valore GUID è \_ null per il tipo principale, il sottotipo o il tipo di formato. In tal caso, i pin tentano di trovare la corrispondenza con qualsiasi parte del tipo di supporto specificato. il valore null del GUID \_ funge da carattere jolly.

Il metodo [**CBasePin:: Connect**](cbasepin-connect.md) inizia verificando che il pin possa accettare una connessione. Ad esempio, verifica che il PIN non sia già connesso. Delega il resto del processo di connessione al metodo [**CBasePin:: AgreeMediaType**](cbasepin-agreemediatype.md) . Tutti gli elementi seguenti vengono eseguiti da **AgreeMediaType**.

Se il tipo di supporto è completamente specificato, il pin chiama il metodo [**CBasePin:: AttemptConnection**](cbasepin-attemptconnection.md) per tentare la connessione. In caso contrario, tenta i tipi di supporto nell'ordine seguente:

1.  Tipi preferiti del PIN di input.
2.  Tipi preferiti del PIN di output.

È possibile invertire questo ordine impostando il flag [**CBasePin:: m \_ BTryMyTypesFirst**](cbasepin-m-btrymytypesfirst.md) su **true**.

In ogni caso, il pin chiama [**Ipin:: EnumMediaTypes**](/windows/desktop/api/Strmif/nf-strmif-ipin-enummediatypes) per enumerare i tipi di supporto. Questo metodo recupera un oggetto enumeratore, che viene passato al metodo [**CBasePin:: TryMediaTypes**](cbasepin-trymediatypes.md) . Il metodo **TryMediaTypes** esegue il ciclo di ogni tipo di supporto e chiama [**AttemptConnection**](cbasepin-attemptconnection.md) per ogni tipo.

All'interno del metodo [**AttemptConnection**](cbasepin-attemptconnection.md) , il pin di output chiama i metodi seguenti:

-   Viene chiamato [**CBasePin:: CheckConnect**](cbasepin-checkconnect.md) per verificare se il pin di input è adatto.
-   Viene chiamato [**CBasePin:: CheckMediaType**](cbasepin-checkmediatype.md) su se stesso per convalidare il tipo di supporto.
-   Chiama [**Ipin:: ReceiveConnection**](/windows/desktop/api/Strmif/nf-strmif-ipin-receiveconnection) sul pin di input. Il pin di input usa questo metodo per determinare se deve accettare la connessione.
-   Viene chiamato [**CBasePin:: CompleteConnect**](cbasepin-completeconnect.md) per completare la connessione.

Tenere presente quanto segue:

-   [**CheckConnect**](cbasepin-checkconnect.md) è un metodo virtuale. Nella classe di base, questo metodo controlla se le direzioni del pin sono compatibili. I pin di output devono connettersi ai pin di input e viceversa. La classe pin derivata eseguirà in genere l'override di questo metodo per eseguire altri controlli. Ad esempio, potrebbe eseguire una query sull'altro pin per un'interfaccia necessaria per la connessione. Se la classe derivata esegue l'override di **CheckConnect**, deve chiamare anche il metodo [**CBasePin**](cbasepin.md) .
-   [**CheckMediaType**](cbasepin-checkmediatype.md) è un metodo virtuale puro, che deve essere implementato dalla classe derivata.
-   [**CompleteConnect**](cbasepin-completeconnect.md) è un metodo virtuale che non esegue alcuna operazione nella classe di base. Le classi derivate possono eseguire l'override di questo metodo per eseguire operazioni aggiuntive necessarie per completare la connessione, ad esempio per decidere un allocatore di memoria.

Se uno di questi passaggi ha esito negativo, il pin di output chiama il metodo [**CBasePin:: BreakConnect**](cbasepin-breakconnect.md) per annullare tutti i passaggi eseguiti da [**CheckConnect**](cbasepin-checkconnect.md).

Il metodo [**ReceiveConnection**](cbasepin-receiveconnection.md) del PIN di input chiama i metodi [**CheckConnect**](cbasepin-checkconnect.md), [**CheckMediaType**](cbasepin-checkmediatype.md)e [**CompleteConnect**](cbasepin-completeconnect.md) del PIN di input. Se uno di questi errori, anche il tentativo di connessione non riesce.

Il diagramma seguente illustra il processo di connessione in [**CBasePin**](cbasepin.md):

![processo di connessione CBasePin](images/cbasepin-connect.png)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**CBasePin**](cbasepin.md)
</dt> </dl>

 

 



