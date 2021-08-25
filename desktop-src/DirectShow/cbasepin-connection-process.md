---
description: Processo di connessione CBasePin
ms.assetid: 4b3a9023-0267-4caa-9d89-88237009df05
title: Processo di connessione CBasePin
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6134c9094e00ea43c5e4bb9f92c9132287fab3c16f98d56497affc8c1015bd6a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119916787"
---
# <a name="cbasepin-connection-process"></a>Processo di connessione CBasePin

Questa sezione descrive come la [**classe CBasePin**](cbasepin.md) implementa il processo di connessione del pin.

Gestione filtri Graph avvia tutte le connessioni pin. Chiama il metodo [**IPin::Connessione**](/windows/desktop/api/Strmif/nf-strmif-ipin-connect) del pin di output, specificando il pin di input. Il pin di output completa la connessione chiamando il metodo [**IPin::ReceiveConnection del**](/windows/desktop/api/Strmif/nf-strmif-ipin-receiveconnection) pin di input. Il pin di input può accettare o rifiutare la connessione.

Gestione filtri Graph può anche specificare un tipo di supporto per la connessione. In tal caso, i pin provano a connettersi a tale tipo. In caso contrario, i pin devono negoziare il tipo. Filter Graph Manager può anche specificare  un tipo di supporto parziale, che ha il valore GUID NULL per il tipo principale, il \_ sottotipo o il tipo di formato. In tal caso, i pin tentano di trovare la corrispondenza con le parti del tipo di supporto specificate. il valore GUID \_ NULL funge da carattere jolly.

Il [**metodo CBasePin::Connessione**](cbasepin-connect.md) inizia verificando che il pin possa accettare una connessione. Ad esempio, verifica che il pin non sia già connesso. Delega il resto del processo di connessione al [**metodo CBasePin::AgreeMediaType.**](cbasepin-agreemediatype.md) Tutto ciò che segue viene eseguito **da AgreeMediaType.**

Se il tipo di supporto è completamente specificato, il pin chiama il metodo [**CBasePin::AttemptConnection**](cbasepin-attemptconnection.md) per tentare la connessione. In caso contrario, prova i tipi di supporti nell'ordine seguente:

1.  Tipi preferiti del pin di input.
2.  Tipi preferiti del pin di output.

È possibile invertire questo ordine impostando il flag [**CBasePin::m \_ bTryMyTypesFirst**](cbasepin-m-btrymytypesfirst.md) su **TRUE.**

In ogni caso, il pin chiama [**IPin::EnumMediaTypes**](/windows/desktop/api/Strmif/nf-strmif-ipin-enummediatypes) per enumerare i tipi di supporti. Questo metodo recupera un oggetto enumeratore, che viene passato al [**metodo CBasePin::TryMediaTypes.**](cbasepin-trymediatypes.md) Il **metodo TryMediaTypes** scorre in ciclo ogni tipo di supporto e chiama [**AttemptConnection**](cbasepin-attemptconnection.md) per ogni tipo.

All'interno [**del metodo AttemptConnection,**](cbasepin-attemptconnection.md) il pin di output chiama i metodi seguenti:

-   Chiama [**CBasePin::CheckConnect**](cbasepin-checkconnect.md) su se stesso per verificare se il pin di input è appropriato.
-   Chiama [**CBasePin::CheckMediaType**](cbasepin-checkmediatype.md) su se stesso per convalidare il tipo di supporto.
-   Chiama [**IPin::ReceiveConnection**](/windows/desktop/api/Strmif/nf-strmif-ipin-receiveconnection) sul pin di input. Il pin di input usa questo metodo per determinare se deve accettare la connessione.
-   Chiama [**CBasePin::CompleteConnect**](cbasepin-completeconnect.md) su se stesso per completare la connessione.

Tenere presente quanto segue:

-   [**CheckConnect**](cbasepin-checkconnect.md) è un metodo virtuale. Nella classe di base questo metodo controlla se le direzioni del segnaposto sono compatibili. I pin di output devono connettersi ai pin di input e viceversa. La classe pin derivata in genere esegue l'override di questo metodo per eseguire altri controlli. Ad esempio, potrebbe eseguire una query sull'altro pin per un'interfaccia necessaria per la connessione. Se la classe derivata esegue l'override **di CheckConnect,** deve chiamare anche il [**metodo CBasePin.**](cbasepin.md)
-   [**CheckMediaType**](cbasepin-checkmediatype.md) è un metodo virtuale puro che la classe derivata deve implementare.
-   [**CompleteConnect**](cbasepin-completeconnect.md) è un metodo virtuale che non esegue alcuna operazione nella classe di base. Le classi derivate possono eseguire l'override di questo metodo per eseguire qualsiasi lavoro aggiuntivo necessario per completare la connessione, ad esempio la scelta di un allocatore di memoria.

Se uno di questi passaggi ha esito negativo, il pin di output chiama il metodo [**CBasePin::BreakConnect**](cbasepin-breakconnect.md) per annullare i passaggi esempi [**da CheckConnect.**](cbasepin-checkconnect.md)

Il metodo [**ReceiveConnection del**](cbasepin-receiveconnection.md) pin di input chiama i metodi [**CheckConnect,**](cbasepin-checkconnect.md) [**CheckMediaType**](cbasepin-checkmediatype.md)e [**CompleteConnect del**](cbasepin-completeconnect.md) pin di input. Se uno di questi errori ha esito negativo, anche il tentativo di connessione ha esito negativo.

Il diagramma seguente illustra il processo di connessione in [**CBasePin:**](cbasepin.md)

![Processo di connessione cbasepin](images/cbasepin-connect.png)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**CBasePin**](cbasepin.md)
</dt> </dl>

 

 



