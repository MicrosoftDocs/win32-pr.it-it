---
title: Strumento del compilatore WsUtil
description: Lo Windows compilatore di servizi Web, WsUtil.exe, supporta il modello di servizio e la serializzazione dei tipi di dati. Elabora wsdl, XML Schema e documenti di criteri e genera intestazioni C e file di origine.
ms.assetid: 7fc3f1bd-ead2-4095-9592-d2ad88d56e7a
keywords:
- Servizi Web dello strumento compilatore WsUtil per Windows
- WWSAPI
- Wws
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a9a4e5761a068e991463451595c410c01f868d4d3e6c9df6ab25a7cb232d678
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119324901"
---
# <a name="wsutil-compiler-tool"></a>Strumento del compilatore WsUtil

Lo Windows compilatore di servizi Web, WsUtil.exe, supporta il modello [di](service-model-layer-overview.md) servizio e la [serializzazione](serialization.md) dei tipi di dati. Elabora wsdl, XML Schema e documenti di criteri e genera intestazioni C e file di origine. Questo strumento è simile allo strumento del compilatore WSDL per il codice gestito, ma è invece destinato al codice nativo.

Per supportare [il modello di servizio](service-model-layer-overview.md), WsUtil.exe genera intestazioni da usare sia per il client che per il servizio. Genera il file proxy C per il lato client e i file stub C per il lato servizio, in base alle esigenze.

Per supportare [la](serialization.md)serializzazione , il compilatore genera intestazioni per le descrizioni degli elementi per le definizioni di elementi globali e tutte le informazioni sulla definizione del tipo nei file proxy utilizzati dal motore di serializzazione.


Per le opzioni della riga di comando per l'elaborazione di file WSDL, xml schema e file di criteri del servizio Web, vedere gli argomenti seguenti:

-   [Strumento compilatore di servizi Web](web-service-compiler-tool.md)
-   [WSDL e contratti di servizio](wsdl-support.md)
-   [Supporto degli schemi](schema-support.md)
-   [Supporto dei criteri](policy-support.md)

## <a name="security"></a>Sicurezza

Quando si usa WsUtil, tenere presenti i problemi seguenti e osservare le precauzioni appropriate:

-   Wsutil non recupera metadati XML in rete e wsutil non risolve le istruzioni import e/o include nei file di metadati di input. Wsutil apre e legge i file wsdl, xsd e dei criteri. I metadati XML non sono anti-manomissione. Assicurarsi di usare solo file wsdl, xsd e di criteri da un'origine attendibile e assicurarsi di proteggere i file da eventuali manomissioni prima e dopo averli utilizzati. Esaminare attentamente il contenuto dei file di input e verificare che il contenuto dei file sia sicuro per l'uso nell'applicazione. Wsutil.exe non esegue alcuna verifica dell'autenticità dei file di metadati.
-   Wsutil genera file di intestazione e stub, che non sono anti-manomissione. È necessario impostare i diritti di accesso di livello corretti per i file di origine generati wsutil.exe per impedire l'accesso non autenticato a tali file. Wsutil usa System.IO.StreamWriter per creare i file di output.
-   Gli utenti devono tenere presente che Wsutil può sovrascrivere i file locali e devono prestare attenzione a specificare directory e nomi di file sicuri per i file di output usando l'opzione /out.
-   Wsutil o wsutilhelper.dll caricato in wsutil.exe, può terminare in modo imprevisto o utilizzare una grande quantità di risorse di sistema in caso di attacco o durante l'elaborazione di una quantità molto grande di metadati di input. Lo strumento è progettato per essere usato solo in fase di sviluppo. Questo strumento deve essere usato solo come strumento in fase di sviluppo. Potrebbe non essere sicuro usarlo nel livello intermedio per elaborare le informazioni sui criteri.
-   Wsutilhelper.dll dll helper viene caricata in una libreria wsutil.exe per elaborare le informazioni sui criteri. L'utente deve assicurarsi che non esista alcun file binario dannoso con lo stesso nome file nel percorso binario. Analogamente, l'utente deve assicurarsi che nell'ambiente di compilazione il percorso binario sia configurato correttamente e che non esista alcun file binario dannoso con lo stesso nome "wsutil.exe".
-   Wsutil genera l'annotazione SAL per le operazioni e i campi di struttura quando possibile. L'utente dei file generati da wsutil deve seguire il requisito specificato tramite l'annotazione SAL.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Panoramica del livello del modello di servizio](service-model-layer-overview.md)
</dt> <dt>

[Serializzazione](serialization.md)
</dt> <dt>

[Strumento compilatore di servizi Web](web-service-compiler-tool.md)
</dt> <dt>

[Supporto WSDL](wsdl-support.md)
</dt> <dt>

[Supporto degli schemi](schema-support.md)
</dt> <dt>

[Supporto dei criteri](policy-support.md)
</dt> </dl>

 

 




