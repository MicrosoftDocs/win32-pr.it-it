---
title: Chiamata di procedura remota
description: Microsoft Remote Procedure Call (RPC) definisce una tecnologia potente per la creazione di programmi client/server distribuiti.
ms.assetid: 27c7c352-5fc1-47cf-99b1-fdf3eca986bc
keywords:
- RPC
- RPC (vedere Remote Procedure Call)
- RPC (Remote Procedure Call), pagina iniziale
- RPC RPC (Remote Procedure Call)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c3461116468bf1d686d1a5695924e5fe66007b35
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399540"
---
# <a name="remote-procedure-call"></a>Chiamata di procedura remota

## <a name="purpose"></a>Scopo

Microsoft Remote Procedure Call (RPC) definisce una tecnologia potente per la creazione di programmi client/server distribuiti. Gli stub e le librerie di runtime RPC gestiscono la maggior parte dei processi correlati alla comunicazione e ai protocolli di rete. In questo modo è possibile concentrarsi sui dettagli dell'applicazione anziché sui dettagli della rete.

## <a name="where-applicable"></a>Se applicabile

RPC può essere usato in tutte le applicazioni client/server basate su sistemi operativi Windows. Può essere usato anche per creare programmi client e server per ambienti di rete eterogenei che includono sistemi operativi come UNIX e Apple.

## <a name="developer-audience"></a>Sviluppatori

RPC è progettato per essere utilizzato dai programmatori C/C++. È necessaria una certa familiarità con il Microsoft Interface Definition Language (MIDL) e il compilatore MIDL.

## <a name="run-time-requirements"></a>Requisiti di runtime

Le librerie di runtime RPC sono incluse in Windows. I componenti dell'ambiente di sviluppo RPC vengono installati quando si installa il Software Development Kit (SDK) di Microsoft Windows. Per informazioni dettagliate, vedere [installazione dell'ambiente di programmazione RPC](installing-the-rpc-programming-environment.md).

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                                           | Descrizione                                                                                                                      |
|---------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| [Procedure di programmazione RPC migliori](best-rpc-programming-practices.md)<br/> | Indicazioni sulle procedure di programmazione RPC che consentono di creare le migliori applicazioni RPC possibili.<br/>                            |
| [Overview](overviews.md)<br/>                                            | Informazioni generali sull'incorporamento di RPC nelle applicazioni client/server.<br/>                                     |
| [Riferimento](reference.md)<br/>                                           | Documentazione di tipi, funzioni e costanti RPC.<br/>                                                                 |
| [Motore di recapito RPC](rpc-ndr-engine.md)<br/>                                 | Documentazione del motore di marshalling per i componenti RPC e DCOM, il motore di rappresentazione dei dati di rete RPC (NDR).<br/> |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Microsoft Interface Definition Language (MIDL)](/windows/desktop/Midl/midl-start-page)
</dt> </dl>

 

