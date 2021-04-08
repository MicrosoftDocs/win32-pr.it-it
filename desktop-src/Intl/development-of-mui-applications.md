---
description: In questo argomento vengono riepilogate le considerazioni di programmazione principali da tenere presenti quando si aggiunge la funzionalità MUI alle applicazioni.
ms.assetid: 10064f5c-5563-44f8-afb5-c6c77991e13c
title: Sviluppo di applicazioni MUI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb4a3278b4cc70969c1aa968de895d99fd3363a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103884577"
---
# <a name="development-of-mui-applications"></a>Sviluppo di applicazioni MUI

In questo argomento vengono riepilogate le considerazioni di programmazione principali da tenere presenti quando si aggiunge la funzionalità MUI alle applicazioni.

## <a name="requirements-for-a-mui-application"></a>Requisiti per un'applicazione MUI

La funzionalità MUI viene applicata solo alla localizzazione di un'applicazione completamente globalizzata, creata utilizzando un processo denominato internazionalizzazione software. Microsoft [go Global Developer Center](https://msdn.microsoft.com/goglobal) offre un'ampia gamma di documentazione correlata che consente di progettare, compilare e distribuire applicazioni internazionali. Questi documenti consentono di valutare il modo in cui le caratteristiche dei diversi linguaggi umani possono influenzare la progettazione del software. Si noti che il portale fornisce anche un archivio completo delle colonne di ripristino di emergenza.

L'applicazione MUI può essere eseguita in qualsiasi lingua o impostazione locale e l'utente può richiedere qualsiasi lingua per la quale l'applicazione includa il supporto. Pertanto, l'applicazione deve codificare il testo dell'interfaccia utente per supportare la più ampia gamma di linguaggi possibile. L'aspetto più importante da ricordare è usare [Unicode](unicode.md) per gestire tutta l'elaborazione del testo. Per ulteriori informazioni sulla globalizzazione mediante Unicode, vedere Microsoft [go Global Developer Center](https://msdn.microsoft.com/goglobal).

## <a name="supported-programming-environments"></a>Ambienti di programmazione supportati

È possibile aggiungere la funzionalità MUI a un'applicazione console o un'applicazione console Win32 globalizzata, come descritto in questo SDK. Inoltre, è possibile creare applicazioni gestite utilizzando .NET Framework, compatibile con MUI. Per ulteriori informazioni, vedere [sviluppo di .NET](/previous-versions/ff361664(v=vs.100)).

## <a name="user-interface-language-settings"></a>Impostazioni della lingua dell'interfaccia utente

Quando si pianifica l'applicazione MUI, è necessario innanzitutto decidere le lingue per l'interfaccia utente e il modo in cui presentarle all'utente. L'applicazione può supportare le lingue in uno dei modi seguenti:

-   Seguire le impostazioni della lingua del sistema. Si supponga che le lingue dell'interfaccia utente preferite dall'utente e le lingue dell'interfaccia utente preferite dal sistema, insieme, rappresentino le lingue disponibili per l'utente. Usare il meccanismo di fallback del caricatore di risorse per la selezione della lingua.
-   Apportare le impostazioni della lingua specifica dell'applicazione. Supportare linguaggi specifici e presentare un meccanismo di selezione all'utente.

## <a name="resource-creation"></a>Creazione di risorse

In questa sezione vengono descritte le possibilità per la creazione delle risorse di lingua dell'interfaccia utente per l'applicazione. Per ulteriori informazioni, vedere [preparazione delle risorse](preparing-resources.md).

> [!Note]  
> Nei sistemi operativi precedenti a Windows Vista, in genere si creano applicazioni localizzate in un unico linguaggio in pacchetto statiche e separate con le lingue supportate dalle sezioni delle risorse incluse nei file eseguibili. Questo tipo di implementazione è ampiamente obsoleto ed è consigliabile scegliere una delle altre tecniche di creazione delle risorse descritte in questa sezione, supportate per Windows Vista e versioni successive. L'applicazione può quindi essere eseguita nei sistemi operativi precedenti a Windows Vista mediante l'uso di [**LoadMUILibrary**](/windows/desktop/api/Muiload/nf-muiload-loadmuilibrarya).

 

### <a name="use-of-a-single-language-in-a-resource-dll-mui-resource-technology"></a>Uso di un singolo linguaggio in una DLL di risorse (tecnologia delle risorse MUI)

Un'implementazione della risorsa DLL satellite standard viene utilizzata da numerose applicazioni Microsoft. In questo caso, viene usato un file eseguibile di base per l'applicazione MUI e viene creata una DLL di risorse per ogni lingua supportata. L'uso di una DLL satellite si applica alle applicazioni eseguite in qualsiasi sistema operativo Windows. Come descritto in [gestione delle risorse MUI](mui-resource-management.md), la tecnologia delle risorse MUI supporta una variante nell'implementazione della DLL satellite standard.

### <a name="use-of-multiple-languages-in-a-resource-dll"></a>Uso di più lingue in una DLL di risorse

È possibile scegliere di creare un file eseguibile di base per l'applicazione MUI e una DLL di risorse per le risorse associate alle lingue supportate. Le copie dello stesso identificatore di risorsa vengono definite nel file di risorse della lingua di base (estensione RC) con tag di lingua diversi per tutte le lingue supportate.

### <a name="use-of-an-application-specific-resource-mechanism"></a>Uso di un meccanismo di risorse Application-Specific

È possibile pianificare l'applicazione MUI per l'uso di un meccanismo di risorse personalizzato. In questo caso, l'applicazione gestisce il caricamento delle risorse in modo specifico.

## <a name="resource-localization"></a>Localizzazione delle risorse

Per supportare le lingue dell'interfaccia utente per l'applicazione MUI, è necessario che siano localizzate le risorse della lingua. MUI supporta due tipi di localizzazione, come descritto nella tabella seguente.



| Tipo di localizzazione       | Descrizione                                                                                                                                                                                                                                                                |
|-------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Localizzazione pre-compilazione  | Richiedere la localizzazione prima di compilare l'applicazione e le risorse specifiche della lingua. Il file di risorse della lingua di base per le lingue dell'interfaccia utente supportate viene copiato e rinominato per ogni lingua supportata e le copie vengono fornite ai localizzatori come richiesto. |
| Localizzazione post-compilazione | Richiedere la localizzazione dopo aver compilato il file eseguibile e la DLL di risorse per l'applicazione. In questo caso, per ogni localizzatore viene fornita una copia della DLL della risorsa.                                                                                                     |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni sull'interfaccia utente multilingue](about-multilingual-user-interface.md)
</dt> </dl>

 

 
