---
title: Strumento compilatore WsUtil
description: Lo strumento compilatore di servizi Web Windows, WsUtil.exe, supporta il modello di servizio e la serializzazione dei tipi di dati. Elabora documenti WSDL, XML Schema e criteri e genera intestazioni e file di origine C.
ms.assetid: 7fc3f1bd-ead2-4095-9592-d2ad88d56e7a
keywords:
- Servizi Web dello strumento del compilatore WsUtil per Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa83da50888fcf2d66fac7fb00b3a31ae2919738
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/04/2020
ms.locfileid: "103963577"
---
# <a name="wsutil-compiler-tool"></a>Strumento compilatore WsUtil

Lo strumento compilatore di servizi Web Windows, WsUtil.exe, supporta il [modello di servizio](service-model-layer-overview.md) e la [serializzazione](serialization.md) dei tipi di dati. Elabora documenti WSDL, XML Schema e criteri e genera intestazioni e file di origine C. Questo strumento è simile allo strumento compilatore WSDL per il codice gestito, ma è invece destinato al codice nativo.

Per supportare il [modello di servizio](service-model-layer-overview.md), WsUtil.exe genera intestazioni da usare sia per il client che per il servizio. Genera il file proxy C per il lato client e i file stub C per il lato del servizio, in base alle esigenze.

Per supportare la [serializzazione](serialization.md), il compilatore genera intestazioni per le descrizioni di elementi per le definizioni di elementi globali e tutte le informazioni relative alla definizione dei tipi nei file proxy utilizzati dal motore di serializzazione.


Per le opzioni della riga di comando per l'elaborazione di file WSDL, file di XML Schema e file di criteri del servizio Web, vedere gli argomenti seguenti:

-   [Strumento compilatore servizio Web](web-service-compiler-tool.md)
-   [WSDL e contratti di servizio](wsdl-support.md)
-   [Supporto degli schemi](schema-support.md)
-   [Supporto dei criteri](policy-support.md)

## <a name="security"></a>Sicurezza

Quando si usa WsUtil, tenere presente i problemi seguenti e osservare le precauzioni appropriate:

-   Wsutil non recupera i metadati XML sulla rete e WSUTIL non risolve le istruzioni Import e/o include nei file di metadati di input. Wsutil apre e legge i file di criteri WSDL, XSD e. I metadati XML non sono resistenti alle manomissioni. Assicurarsi di usare solo i file WSDL, XSD e Policy acquisiti da un'origine attendibile e assicurarsi di proteggere i file dalla manomissione prima e dopo l'uso. Esaminare attentamente il contenuto dei file di input e verificare che il contenuto dei file sia sicuro per l'utilizzo nell'applicazione. Wsutil.exe non esegue alcuna verifica dell'autenticità dei file di metadati.
-   Wsutil genera file di intestazione e Stub, che non sono resistenti alle manomissioni. È necessario impostare i diritti di accesso a livello corretti per i file di origine generati da wsutil.exe per impedire l'accesso unauthoritized a tali file. Wsutil usa System. IO. StreamWriter per creare i file di output.
-   Gli utenti devono tenere presente che WSUTIL può sovrascrivere i file locali e devono prestare attenzione a specificare nomi e directory sicuri per i file di output usando l'opzione/out.
-   Wsutil o wsutilhelper.dll caricati in wsutil.exe, possono terminare in modo imprevisto o utilizzare una grande quantità di risorse di sistema quando sono sotto attacco o durante l'elaborazione di una quantità molto elevata di metadati di input. Lo strumento è progettato per essere utilizzato in fase di sviluppo. solo questo strumento deve essere utilizzato solo come strumento per la fase di sviluppo. Potrebbe non essere possibile utilizzare il livello intermedio per elaborare le informazioni sui criteri.
-   Wsutilhelper.dll DLL Helper viene caricata in wsutil.exe gestite per elaborare le informazioni sui criteri. Assicurarsi che non esistano file binari dannosi con lo stesso nome di file nel percorso binario. Analogamente, l'utente deve assicurarsi che nell'ambiente di compilazione il percorso binario sia configurato correttamente, in modo che non esistano file binari dannosi con lo stesso nome "wsutil.exe".
-   Wsutil genera l'annotazione SAL per le operazioni e i campi della struttura, quando possibile. L'utente dei file generati da WSUTIL deve seguire il requisito specificato tramite l'annotazione SAL.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Panoramica del livello del modello di servizio](service-model-layer-overview.md)
</dt> <dt>

[Serializzazione](serialization.md)
</dt> <dt>

[Strumento compilatore servizio Web](web-service-compiler-tool.md)
</dt> <dt>

[Supporto WSDL](wsdl-support.md)
</dt> <dt>

[Supporto degli schemi](schema-support.md)
</dt> <dt>

[Supporto dei criteri](policy-support.md)
</dt> </dl>

 

 




