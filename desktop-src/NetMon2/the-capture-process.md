---
description: Il processo di acquisizione è lo stesso per ognuna delle quattro interfacce di NPP.
ms.assetid: f778aba5-8f66-4fc9-830b-f830c364da56
title: Processo di acquisizione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e0ca1987266b7e042713f1d1c292cf63d5e3ccf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104571101"
---
# <a name="the-capture-process"></a>Processo di acquisizione

Il processo di acquisizione è lo stesso per ognuna delle quattro interfacce di NPP. In ogni caso, il processo include:

-   Recupero dell'oggetto dell'interfaccia NPP da usare
-   Connessione alla rete
-   Avvio e arresto dell' [ *acquisizione*](c.md)
-   Disconnessione dalla rete

> [!Note]  
> Quando si ottiene l'oggetto interfaccia desiderato, assicurarsi di chiamare solo i metodi inclusi in tale interfaccia. Nell'illustrazione seguente viene mostrata ogni interfaccia che fornisce metodi simili per l'acquisizione dei dati di rete. Viene restituito un errore se ci si connette alla rete con un'interfaccia e quindi si prova a eseguire un'acquisizione usando i metodi di un'altra interfaccia.

 

Le illustrazioni seguenti illustrano due modi diversi per eseguire un'acquisizione. Nella prima figura viene illustrato come eseguire una o più acquisizioni sequenziali, consentendo di creare un numero qualsiasi di acquisizioni indipendenti.

![acquisizione sequenziale](images/capt1.png)

Come illustrato sopra, dopo la connessione alla rete è possibile avviare e arrestare un'acquisizione il numero di volte desiderato, avviando una nuova acquisizione e generando nuove statistiche ogni volta che si riavvia l'acquisizione. Ad esempio, per un'acquisizione ritardata tramite l'interfaccia [**IDelaydC**](idelaydc.md) , viene creato un nuovo [*file di acquisizione*](c.md) ogni volta che viene riavviata l'acquisizione.

Tuttavia, tenere presente che ogni volta che si riavvia il processo di acquisizione è necessario chiamare il metodo Configure appropriato per riconfigurare la connessione. Per la chiamata iniziale per avviare l'acquisizione, la connessione viene configurata dalla chiamata per connettersi alla rete.

La seconda illustrazione mostra come eseguire una singola acquisizione sospendendo e riavviando.

![acquisizione singola mediante sospensione e riavvio](images/capt2.png)

In questo caso, è possibile sospendere e riavviare un'acquisizione tutte le volte che si desidera. Con questo approccio, è possibile eseguire un'acquisizione i cui dati (e le relative statistiche) vengono registrati come una singola acquisizione. Per eseguire un'acquisizione ritardata tramite l'interfaccia [**IDelaydC**](idelaydc.md) , ad esempio, tutte le informazioni di rete acquisite vengono salvate in un unico [*file di acquisizione*](c.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**CreateNPPInterface**](createnppinterface.md)
</dt> <dt>

[**IDelaydC:: Configure**](idelaydc-configure.md)
</dt> <dt>

[**IDelaydC:: Connect**](idelaydc-connect.md)
</dt> <dt>

[**IDelaydC::D la connessione**](idelaydc-disconnect.md)
</dt> <dt>

[**IDelaydC::P ause**](idelaydc-pause.md)
</dt> <dt>

[**IDelaydC:: Resume**](idelaydc-resume.md)
</dt> <dt>

[**IDelaydC:: Start**](idelaydc-start.md)
</dt> <dt>

[**IDelaydC:: Stop**](idelaydc-stop.md)
</dt> <dt>

[**IESP:: Configure**](iesp-configure.md)
</dt> <dt>

[**IESP:: Connect**](iesp-connect.md)
</dt> <dt>

[**IESP::D la connessione**](iesp-disconnect.md)
</dt> <dt>

[**IESP::P ause**](iesp-pause.md)
</dt> <dt>

[**IESP:: Resume**](iesp-resume.md)
</dt> <dt>

[**IESP:: Start**](iesp-start.md)
</dt> <dt>

[**IESP:: Stop**](iesp-stop.md)
</dt> <dt>

[**IRTC:: Configure**](irtc-configure.md)
</dt> <dt>

[**IRTC:: Connect**](irtc-connect.md)
</dt> <dt>

[**IRTC::D la connessione**](irtc-disconnect.md)
</dt> <dt>

[**IRTC::P ause**](irtc-pause.md)
</dt> <dt>

[**IRTC:: Resume**](irtc-resume.md)
</dt> <dt>

[**IRTC:: Start**](irtc-start.md)
</dt> <dt>

[**IRTC:: Stop**](irtc-stop.md)
</dt> <dt>

[**IStats:: Configure**](istats-configure.md)
</dt> <dt>

[**IStats:: Connect**](istats-connect.md)
</dt> <dt>

[**IStats::D la connessione**](istats-disconnect.md)
</dt> <dt>

[**IStats::P ause**](istats-pause.md)
</dt> <dt>

[**IStats:: Resume**](istats-resume.md)
</dt> <dt>

[**IStats:: Start**](istats-start.md)
</dt> <dt>

[**IStats:: Stop**](istats-stop.md)
</dt> </dl>

 

 



