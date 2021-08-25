---
description: Il processo di acquisizione è lo stesso per ognuna delle quattro interfacce NPP.
ms.assetid: f778aba5-8f66-4fc9-830b-f830c364da56
title: Processo di acquisizione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 51a6d82d721f0f85c6b1ab279d556aaad866f70fde7c8e422995cba5be513d8e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119889591"
---
# <a name="the-capture-process"></a>Processo di acquisizione

Il processo di acquisizione è lo stesso per ognuna delle quattro interfacce NPP. In ogni caso, il processo include:

-   Recupero dell'oggetto interfaccia NPP da usare
-   Connessione alla rete
-   Avvio e quindi arresto [ *dell'acquisizione*](c.md)
-   Disconnessione dalla rete

> [!Note]  
> Quando si ottiene l'oggetto interfaccia desiderato, assicurarsi di chiamare solo i metodi inclusi in tale interfaccia. La figura seguente mostra ogni interfaccia che fornisce metodi simili per l'acquisizione dei dati di rete. Viene restituito un errore se ci si connette alla rete con un'interfaccia e quindi si tenta di eseguire un'acquisizione usando i metodi di un'altra interfaccia.

 

Le illustrazioni seguenti illustrano due diversi modi in cui è possibile eseguire un'acquisizione. La prima figura illustra come eseguire una o più acquisizioni sequenziali, consentendo di creare un numero qualsiasi di acquisizioni indipendenti.

![acquisizione sequenziale](images/capt1.png)

Come illustrato in precedenza, dopo la connessione alla rete è possibile avviare e arrestare un'acquisizione tutte le volte che si desidera, avviando una nuova acquisizione e generando nuove statistiche ogni volta che si riavvia l'acquisizione. Ad esempio, per un'acquisizione ritardata che usa [**l'interfaccia IDelaydC,**](idelaydc.md) viene creato un nuovo [*file*](c.md) di acquisizione ogni volta che si riavvia l'acquisizione.

Tenere tuttavia presente che ogni volta che si riavvia il processo di acquisizione è necessario chiamare il metodo di configurazione appropriato per riconfigurare la connessione. Per consentire alla chiamata iniziale di avviare l'acquisizione, la connessione viene configurata dalla chiamata per connettersi alla rete.

La seconda figura mostra come è possibile eseguire una singola acquisizione sospensione e riavvio.

![acquisizione singola tramite sospensione e riavvio](images/capt2.png)

In questo caso, è possibile sospendere e riavviare un'acquisizione tutte le volte che si vuole. Con questo approccio, è possibile eseguire un'acquisizione i cui dati (e le relative statistiche correlate) vengono registrati come singola acquisizione. Ad esempio, per eseguire un'acquisizione ritardata usando [**l'interfaccia IDelaydC,**](idelaydc.md) tutte le informazioni di rete acquisite verranno salvate in un [*singolo file di acquisizione.*](c.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**CreateNPPInterface**](createnppinterface.md)
</dt> <dt>

[**IDelaydC::Configure**](idelaydc-configure.md)
</dt> <dt>

[**IDelaydC::Connessione**](idelaydc-connect.md)
</dt> <dt>

[**IDelaydC::D isconnect**](idelaydc-disconnect.md)
</dt> <dt>

[**IDelaydC::P ause**](idelaydc-pause.md)
</dt> <dt>

[**IDelaydC::Resume**](idelaydc-resume.md)
</dt> <dt>

[**IDelaydC::Start**](idelaydc-start.md)
</dt> <dt>

[**IDelaydC::Stop**](idelaydc-stop.md)
</dt> <dt>

[**IESP::Configure**](iesp-configure.md)
</dt> <dt>

[**IESP::Connessione**](iesp-connect.md)
</dt> <dt>

[**IESP::D isconnect**](iesp-disconnect.md)
</dt> <dt>

[**IESP::P ause**](iesp-pause.md)
</dt> <dt>

[**IESP::Resume**](iesp-resume.md)
</dt> <dt>

[**IESP::Start**](iesp-start.md)
</dt> <dt>

[**IESP::Stop**](iesp-stop.md)
</dt> <dt>

[**IRTC::Configure**](irtc-configure.md)
</dt> <dt>

[**IRTC::Connessione**](irtc-connect.md)
</dt> <dt>

[**IRTC::D isconnect**](irtc-disconnect.md)
</dt> <dt>

[**IRTC::P ause**](irtc-pause.md)
</dt> <dt>

[**IRTC::Resume**](irtc-resume.md)
</dt> <dt>

[**IRTC::Start**](irtc-start.md)
</dt> <dt>

[**IRTC::Stop**](irtc-stop.md)
</dt> <dt>

[**IStats::Configure**](istats-configure.md)
</dt> <dt>

[**IStats::Connessione**](istats-connect.md)
</dt> <dt>

[**IStats::D isconnect**](istats-disconnect.md)
</dt> <dt>

[**IStats::P ause**](istats-pause.md)
</dt> <dt>

[**IStats::Resume**](istats-resume.md)
</dt> <dt>

[**IStats::Start**](istats-start.md)
</dt> <dt>

[**IStats::Stop**](istats-stop.md)
</dt> </dl>

 

 



