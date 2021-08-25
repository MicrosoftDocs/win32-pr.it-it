---
title: Architettura degli oggetti collegabili
description: Architettura degli oggetti collegabili
ms.assetid: 69949a3b-3ab8-4054-84d8-9256fbf39c7b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1215b013c3db751e90b07ed21d5f897ef0332000ce2cd2b3b167cbe86798927
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119993957"
---
# <a name="architecture-of-connectable-objects"></a>Architettura degli oggetti collegabili

L'oggetto collegabile è solo una parte dell'architettura complessiva degli oggetti collegabili. Questa tecnologia include gli elementi seguenti:

-   **Oggetto collegabile.** Implementa [**l'interfaccia IConnectionPointContainer.**](/windows/desktop/api/OCIdl/nn-ocidl-iconnectionpointcontainer) crea almeno un oggetto punto di connessione. definisce un'interfaccia in uscita per il client.
-   **Client.** Esegue una query sull'oggetto [**per IConnectionPointContainer**](/windows/desktop/api/OCIdl/nn-ocidl-iconnectionpointcontainer) per determinare se l'oggetto è collegabile; crea un oggetto sink per implementare l'interfaccia in uscita definita dall'oggetto collegabile.
-   **Oggetto sink.** Implementa l'interfaccia in uscita. utilizzato per stabilire una connessione all'oggetto collegabile.
-   **Oggetto punto di connessione.** Implementa [**l'interfaccia IConnectionPoint**](/windows/desktop/api/OCIdl/nn-ocidl-iconnectionpoint) e gestisce la connessione con il sink del client.

Le relazioni tra client, oggetto collegabile, punto di connessione e sink sono illustrate nel diagramma seguente:

![Diagramma che mostra i punti di connessione tra il client e l'oggetto collegabile.](images/1cd44fec-5d2c-4427-846b-ccab7ec0b08a.png)

Prima che l'oggetto punto di connessione chiami i metodi nell'interfaccia sink nel passaggio 3 del diagramma precedente, deve [**eseguire QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) per l'interfaccia specifica richiesta, anche se il puntatore è già stato passato nella chiamata del passaggio 2 al [**metodo Advise.**](/windows/desktop/api/OCIdl/nf-ocidl-iconnectionpoint-advise)

Anche due oggetti enumeratore sono coinvolti in questa architettura, anche se non sono illustrati nell'illustrazione. Uno viene creato da un metodo in [**IConnectionPointContainer**](/windows/desktop/api/OCIdl/nn-ocidl-iconnectionpointcontainer) per enumerare i punti di connessione all'interno dell'oggetto collegabile. L'altro viene creato da un metodo in [**IConnectionPoint per**](/windows/desktop/api/OCIdl/nn-ocidl-iconnectionpoint) enumerare le connessioni attualmente stabilite a tale punto di connessione. Un punto di connessione può supportare più interfacce sink connesse e deve scorrere l'elenco delle connessioni ogni volta che effettua una chiamata al metodo su tale interfaccia. Questo processo è noto come multicast.

Quando si lavora con oggetti collegabili, è importante comprendere che l'oggetto collegabile, ogni punto di connessione, ogni sink e tutti gli enumeratori sono oggetti separati con implementazioni [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) separate, conteggi dei riferimenti separati e durate separate. Un client che usa questi oggetti è sempre responsabile del rilascio di tutti i conteggi dei riferimenti di cui è proprietario.

> [!Note]  
> Un oggetto collegabile può supportare più client e più sink all'interno di un client. Analogamente, un sink può essere connesso a più di un oggetto collegabile.

 

I passaggi per stabilire una connessione tra un client e un oggetto collegabile sono i seguenti:

1.  Il client esegue una query [**per IConnectionPointContainer**](/windows/desktop/api/OCIdl/nn-ocidl-iconnectionpointcontainer) sull'oggetto per determinare se l'oggetto è collegabile. Se questa chiamata ha esito positivo, il client contiene un puntatore all'interfaccia **IConnectionPointContainer** sull'oggetto collegabile e il contatore dei riferimenti all'oggetto collegabile è stato incrementato. In caso contrario, l'oggetto non è collegabile e non supporta le interfacce in uscita.
2.  Se l'oggetto è collegabile, il client tenta quindi di ottenere un puntatore [**all'interfaccia IConnectionPoint**](/windows/desktop/api/OCIdl/nn-ocidl-iconnectionpoint) in un punto di connessione all'interno dell'oggetto collegabile. Esistono due metodi per ottenere questo puntatore, sia in [**IConnectionPointContainer::FindConnectionPoint**](/windows/desktop/api/OCIdl/nf-ocidl-iconnectionpointcontainer-findconnectionpoint) che in [**IConnectionPointContainer::EnumConnectionPoints**](/windows/desktop/api/OCIdl/nf-ocidl-iconnectionpointcontainer-enumconnectionpoints). Se si usa **EnumConnectionPoints,** sono necessari alcuni passaggi aggiuntivi. Per altre [informazioni, vedere Uso di IConnectionPointContainer.](using-iconnectionpointcontainer.md) In caso di esito positivo, l'oggetto collegabile e il client supportano entrambi la stessa interfaccia in uscita. L'oggetto collegabile lo definisce e lo chiama e il client lo implementa. Il client può quindi comunicare tramite il punto di connessione all'interno dell'oggetto collegabile.
3.  Il client chiama quindi [**Advise**](/windows/desktop/api/OCIdl/nf-ocidl-iconnectionpoint-advise) sul punto di connessione per stabilire una connessione tra l'interfaccia sink e il punto di connessione dell'oggetto. Dopo questa chiamata, il punto di connessione dell'oggetto contiene un puntatore all'interfaccia in uscita nel sink.
4.  Il codice [**all'interno**](/windows/desktop/api/OCIdl/nf-ocidl-iconnectionpoint-advise) di Advise chiama [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) sul puntatore a interfaccia passato, richiedendo l'identificatore di interfaccia specifico a cui si connette.
5.  L'oggetto chiama i metodi sull'interfaccia del sink in base alle esigenze, usando il puntatore mantenuto dal relativo punto di connessione.
6.  Il client chiama [**Unadvise per**](/windows/desktop/api/OCIdl/nf-ocidl-iconnectionpoint-unadvise) terminare la connessione. Il client chiama **quindi IConnectionPoint::Release** per liberare il blocco sul punto di connessione e, di conseguenza, anche l'oggetto principale collegabile. Il client deve anche chiamare **IConnectionPointContainer::Release** per liberare spazio sull'oggetto principale collegabile.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Interfacce a oggetti collegabili](connectable-object-interfaces.md)
</dt> </dl>

 

 




