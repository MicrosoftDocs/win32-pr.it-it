---
title: Informazioni sull'API Windows Deployment Services
description: Windows Servizi di distribuzione è una suite di componenti che consentono la distribuzione di sistemi operativi Windows, in particolare Windows Vista e versioni successive e Windows Server 2008 e versioni successive.
ms.assetid: 5742e51a-70e3-4607-bfb7-181362dfb168
keywords:
- Windows Servizi di Windows distribuzione , informazioni su
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58dd65f18c1628236358d61656c8c3b414d180e43166daa86dfa6562024252a2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120098681"
---
# <a name="about-the-windows-deployment-services-api"></a>Informazioni sull'API Windows Deployment Services

Windows Servizi di distribuzione è una suite di componenti che consentono la distribuzione di sistemi operativi Windows, in particolare Windows Vista e versioni successive e Windows Server 2008 e versioni successive. È possibile usarlo per configurare nuovi computer usando installazioni basate sulla rete.

Gli OEM, i system builder e i professionisti IT aziendali che cercano informazioni su come distribuire Windows in nuovi computer dovrebbero vedere le informazioni sulla soluzione WDS standard nella guida dettagliata all'aggiornamento di servizi di distribuzione di [Windows](/previous-versions/windows/it-pro/windows-vista/cc766320(v=ws.10)) e [Windows Automated Installation Kit (WAIK).](https://www.microsoft.com/download/details.aspx?id=10333)

Negli ambienti in cui non è possibile usare la soluzione WDS standard, l'API WDS consente l'accesso a livello di codice ad alcuni componenti wds.

-   Le [Windows server di Servizi](windows-deployment-services-server-functions.md) di distribuzione consentono l'accesso a livello di codice al server WDS Pre-Boot eXecution Environment (PXE). I componenti server WDS includono un server PXE e un server Trivial File Transfer Protocol (TFTP) per l'avvio di rete di un computer per caricare e installare un sistema operativo.
-   Le [Windows client di Servizi di distribuzione consentono](windows-deployment-services-client-functions.md) l'accesso a livello di codice al client WDS. I componenti client wds includono un'interfaccia utente grafica che viene eseguita all'interno dell'ambiente di preinstallazione di Windows (Windows PE) e comunica con i componenti server per selezionare e installare un'immagine del sistema operativo.
-   Non è disponibile alcuna API per i componenti di gestione wds. Questi componenti sono un set di strumenti che consentono di gestire il server, le immagini del sistema operativo e gli account computer client. Per altre informazioni sui componenti di gestione di WdS, vedere La guida dettagliata all'aggiornamento di [Windows Deployment Services](/previous-versions/windows/it-pro/windows-vista/cc766320(v=ws.10)).

WDS PXE Server è costituito da un server PXE e da un provider PXE. Il server PXE contiene la funzionalità di rete principale. Il server PXE supporta le interfacce plug-in note come provider PXE. Questo modello di provider consente lo sviluppo di soluzioni PXE personalizzate continuando a usare la base di codice di rete del server PXE di base.

-   Gli sviluppatori [](windows-deployment-services-server-functions.md) possono usare Windows Funzioni server di Servizi di distribuzione per scrivere una DLL per un provider personalizzato da sostituire o eseguire in combinazione con il livello BINL (Boot Information Negotiation Layer) standard in un server WDS. Ad esempio, il provider personalizzato può usare un file di testo come archivio dati anziché Active Directory.
-   Gli sviluppatori possono usare Windows [Funzioni](windows-deployment-services-server-functions.md) server di Servizi di distribuzione per scrivere un provider di filtri sequenziato prima di BINL o di qualsiasi altro provider PXE nell'elenco ordinato dei provider registrati. Il secondo provider quindi gestisce solo le richieste PXE selezionate, mentre il primo provider gestisce altre richieste. Ad esempio, questo può consentire al secondo provider registrato nell'elenco ordinato di offrire nuove funzionalità senza interrompere la soluzione WDS esistente implementata nel primo provider.

Il client WDS include un'interfaccia utente grafica che viene eseguita all'interno dell'ambiente di preinstallazione di Windows (Windows PE) e comunica con i componenti server per selezionare e installare un'immagine del sistema operativo. La libreria client WDS supporta lo sviluppo di applicazioni client personalizzate che possono usare un server WDS.

-   Gli sviluppatori possono usare le [Windows client](windows-deployment-services-client-functions.md) di Servizi di distribuzione per scrivere la propria applicazione client personalizzata che sostituisce il client WDS. Ad esempio, l'applicazione personalizzata può enumerare le immagini archiviate in un server WDS e inviare messaggi di stato dell'installazione al registro eventi del server PXE.

## <a name="windows-deployment-services-samples"></a>Windows Esempi di Servizi di distribuzione

Un provider PXE personalizzato di esempio, un provider di filtri e un'applicazione client WDS è disponibile in Microsoft Windows Software Development Kit (SDK), vedere [Microsoft Windows Software Development Kit (SDK)](https://developer.microsoft.com/windows/downloads/windows-10-sdk/).

È possibile scaricare online gli esempi di WDS seguenti nella raccolta [di codice desktop](https://github.com/microsoft/Windows-classic-samples).

<dl>

[Windows Esempio di provider di filtri di Servizi di distribuzione](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/WindowsDeploymentServices/FilterProvider)  
[Windows Esempio di enumerazione delle immagini di Servizi di distribuzione](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/WindowsDeploymentServices/ImageEnumeration)  
[Windows Esempio di consumer multicast di Servizi di distribuzione](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/WindowsDeploymentServices/Multicast/WdsProvider)  
[Windows Esempio di provider multicast di Servizi di distribuzione](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/WindowsDeploymentServices/Multicast/WdsProvider)  
[Windows Esempio di provider di Servizi di distribuzione](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/WindowsDeploymentServices/FilterProvider)  
[Windows Esempio di gestione trasporto di Servizi di distribuzione](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/WindowsDeploymentServices/Management/WDSTransportManager)  
</dl>

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso dell'API server di Servizi di distribuzione Windows](using-the-windows-deployment-services-server-api.md)
</dt> <dt>

[Uso dell'API client di Servizi di distribuzione Windows](using-the-windows-deployment-services-client-api.md)
</dt> </dl>

 

 