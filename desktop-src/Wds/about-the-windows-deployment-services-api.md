---
title: Informazioni sull'API di servizi di distribuzione Windows
description: Servizi di distribuzione Windows (WDS) è una suite di componenti che consentono la distribuzione di sistemi operativi Windows, in particolare Windows Vista e versioni successive e Windows Server 2008 e versioni successive.
ms.assetid: 5742e51a-70e3-4607-bfb7-181362dfb168
keywords:
- Servizi di distribuzione Windows servizi di distribuzione Windows, informazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eac4a904765f58ccf995c5bbc0a9413f8eb4d13c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103963144"
---
# <a name="about-the-windows-deployment-services-api"></a>Informazioni sull'API di servizi di distribuzione Windows

Servizi di distribuzione Windows (WDS) è una suite di componenti che consentono la distribuzione di sistemi operativi Windows, in particolare Windows Vista e versioni successive e Windows Server 2008 e versioni successive. È possibile usarlo per configurare nuovi computer con installazioni basate su rete.

Gli OEM, i System Builder e i professionisti IT aziendali che cercano informazioni su come distribuire Windows nei nuovi computer dovrebbero visualizzare le informazioni sulla soluzione WDS standard nella [Guida dettagliata all'aggiornamento di servizi di distribuzione Windows](/previous-versions/windows/it-pro/windows-vista/cc766320(v=ws.10)) e [Windows Automated Installation Kit (WAIK)](https://www.microsoft.com/download/details.aspx?id=10333).

Negli ambienti in cui non è possibile usare la soluzione WDS standard, l'API WDS consente l'accesso programmatico ad alcuni componenti di WDS.

-   Le [funzioni server di servizi di distribuzione Windows](windows-deployment-services-server-functions.md) forniscono l'accesso a livello di codice al server di pre-boot Execution Environment WDS (PXE). I componenti server WDS includono un server PXE e un server TFTP (Trivial File Transfer Protocol) per l'avvio di rete di un computer per caricare e installare un sistema operativo.
-   Le [funzioni client di servizi di distribuzione Windows](windows-deployment-services-client-functions.md) forniscono l'accesso a livello di codice al client WDS. I componenti client di WDS includono un'interfaccia utente grafica che viene eseguita nell'ambiente di preinstallazione di Windows (Windows PE) e comunica con i componenti server per selezionare e installare un'immagine del sistema operativo.
-   Non è disponibile alcuna API per i componenti di gestione WDS. Questi componenti sono un set di strumenti che è possibile utilizzare per gestire il server, le immagini del sistema operativo e gli account dei computer client. Per ulteriori informazioni sui componenti di gestione WDS, vedere [la guida dettagliata all'aggiornamento di servizi di distribuzione Windows](/previous-versions/windows/it-pro/windows-vista/cc766320(v=ws.10)).

Il server PXE WDS è costituito da un server PXE e da un provider PXE. Il server PXE contiene la funzionalità di rete principale. Il server PXE supporta le interfacce plug-in note come provider PXE. Questo modello di provider consente lo sviluppo di soluzioni PXE personalizzate continuando a utilizzare la base di codice di rete del server PXE principale.

-   Gli sviluppatori possono utilizzare le [funzioni server di servizi di distribuzione Windows](windows-deployment-services-server-functions.md) per scrivere una dll per un provider personalizzato da sostituire o eseguire in combinazione con il livello standard di Boot Information Negotiation (BINL) in un server WDS. Il provider personalizzato, ad esempio, può utilizzare un file di testo come archivio dati anziché Active Directory.
-   Gli sviluppatori possono utilizzare le [funzioni server di servizi di distribuzione Windows](windows-deployment-services-server-functions.md) per scrivere un provider di filtri sequenziato prima di BINL o di qualsiasi altro provider PXE nell'elenco ordinato di provider registrati. Il secondo provider quindi solo i servizi richieste PXE selezionate, mentre il primo provider gestisce altre richieste. Questo può, ad esempio, abilitare il secondo provider registrato nell'elenco ordinato per offrire nuove funzionalità senza compromettere la soluzione WDS esistente implementata nel primo provider.

Il client WDS include un'interfaccia utente grafica che viene eseguita nell'ambiente di preinstallazione di Windows (Windows PE) e comunica con i componenti server per selezionare e installare un'immagine del sistema operativo. La libreria client WDS supporta lo sviluppo di applicazioni client personalizzate che possono usare un server WDS.

-   Gli sviluppatori possono utilizzare le [funzioni client di servizi di distribuzione Windows](windows-deployment-services-client-functions.md) per scrivere un'applicazione client personalizzata che sostituisce il client WDS. Ad esempio, l'applicazione personalizzata può enumerare le immagini archiviate in un server WDS e inviare i messaggi di stato dell'installazione al registro eventi del server PXE.

## <a name="windows-deployment-services-samples"></a>Esempi di servizi di distribuzione Windows

Un provider PXE personalizzato di esempio, un provider di filtri e un'applicazione client WDS sono disponibili nel Software Development Kit (SDK) di Microsoft Windows, vedere [Microsoft Windows Software Development Kit (SDK)](https://developer.microsoft.com/windows/downloads/windows-10-sdk/).

È possibile scaricare gli esempi di WDS seguenti online nella [raccolta di codice desktop](https://github.com/microsoft/Windows-classic-samples).

<dl>

[Esempio di provider di filtri di servizi di distribuzione Windows](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/WindowsDeploymentServices/FilterProvider)  
[Esempio di enumerazione di immagini di servizi di distribuzione Windows](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/WindowsDeploymentServices/ImageEnumeration)  
[Esempio di consumer multicast di servizi di distribuzione Windows](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/WindowsDeploymentServices/Multicast/WdsProvider)  
[Esempio di provider multicast di servizi di distribuzione Windows](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/WindowsDeploymentServices/Multicast/WdsProvider)  
[Esempio di provider di servizi di distribuzione Windows](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/WindowsDeploymentServices/FilterProvider)  
[Esempio di gestione trasporto di servizi di distribuzione Windows](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/WindowsDeploymentServices/Management/WDSTransportManager)  
</dl>

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso dell'API server di Servizi di distribuzione Windows](using-the-windows-deployment-services-server-api.md)
</dt> <dt>

[Uso dell'API client di Servizi di distribuzione Windows](using-the-windows-deployment-services-client-api.md)
</dt> </dl>

 

 