---
description: Questo argomento riepiloga le principali considerazioni sulla programmazione da tenere presenti quando si aggiungono funzionalità MUI alle applicazioni.
ms.assetid: 10064f5c-5563-44f8-afb5-c6c77991e13c
title: Sviluppo di applicazioni MUI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32cc647069577a2ff3b137573b85308aa66e685df2310c2ea01973d19d1dc0d0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119822771"
---
# <a name="development-of-mui-applications"></a>Sviluppo di applicazioni MUI

Questo argomento riepiloga le principali considerazioni sulla programmazione da tenere presenti quando si aggiungono funzionalità MUI alle applicazioni.

## <a name="requirements-for-a-mui-application"></a>Requisiti per un'applicazione MUI

La funzionalità MUI viene applicata solo alla localizzazione di un'applicazione completamente globalizzata, creata usando un processo denominato internazionalizzazione del software. Microsoft [Go Global Developer Center](https://msdn.microsoft.com/goglobal) offre un'ampia gamma di documentazione correlata che consente di progettare, compilare e distribuire applicazioni pronte per il mondo. Questi documenti consentono di valutare in che modo le caratteristiche dei diversi linguaggi umani possono influire sulla progettazione del software. Si noti che il portale fornisce anche un archivio completo delle colonne Dr. International.

L'applicazione MUI può essere eseguita con qualsiasi lingua o impostazione locale e l'utente può richiedere qualsiasi lingua per cui l'applicazione include il supporto. Pertanto, l'applicazione deve codificare il testo dell'interfaccia utente per supportare la più ampia gamma possibile di lingue. La cosa più importante da ricordare è usare [Unicode](unicode.md) per gestire tutta l'elaborazione del testo. Per altre informazioni sulla globalizzazione con Unicode, vedere Microsoft [Go Global Developer Center](https://msdn.microsoft.com/goglobal).

## <a name="supported-programming-environments"></a>Ambienti di programmazione supportati

È possibile aggiungere funzionalità MUI a un'applicazione form Win32 globalizzata o a un'applicazione console, come descritto in questo SDK. È anche possibile creare applicazioni gestite usando .NET Framework, che è compatibile con MUI. Per altre informazioni, vedere [Sviluppo .NET.](/previous-versions/ff361664(v=vs.100))

## <a name="user-interface-language-settings"></a>Interfaccia utente lingua Impostazioni

Quando si pianifica l'applicazione MUI, è innanzitutto necessario decidere le lingue per l'interfaccia utente e il modo in cui presentarle all'utente. L'applicazione può supportare le lingue in uno dei modi seguenti:

-   Seguire le impostazioni della lingua di sistema. Si supponga che le lingue dell'interfaccia utente preferite dall'utente e le lingue dell'interfaccia utente preferite dal sistema, insieme, rappresentino le lingue disponibili per l'utente. Usare il meccanismo di fallback del caricatore di risorse per la selezione della lingua.
-   Impostare le impostazioni della lingua specifiche dell'applicazione. Supportare lingue specifiche e presentare un meccanismo di selezione all'utente.

## <a name="resource-creation"></a>Creazione di risorse

In questa sezione vengono descritte le possibilità di creazione delle risorse della lingua dell'interfaccia utente per l'applicazione. Per altre informazioni, vedere [Preparazione delle risorse](preparing-resources.md).

> [!Note]  
> Nei sistemi operativi Windows Vista vengono in genere create applicazioni localizzate a lingua singola statiche e separate con le lingue supportate dalle sezioni delle risorse incluse nei file eseguibili. Questo tipo di implementazione è in gran parte obsoleto ed è consigliabile scegliere una delle altre tecniche di creazione delle risorse descritte in questa sezione, supportate per Windows Vista e versioni successive. L'applicazione può quindi essere eseguita nei sistemi operativi Windows Vista precedenti usando [**LoadMUILibrary**](/windows/desktop/api/Muiload/nf-muiload-loadmuilibrarya).

 

### <a name="use-of-a-single-language-in-a-resource-dll-mui-resource-technology"></a>Uso di una singola lingua in una DLL di risorse (tecnologia delle risorse MUI)

Un'implementazione di risorse DLL satellite standard viene usata da molte applicazioni Microsoft. In questo caso, viene usato un file eseguibile principale per l'applicazione MUI e viene creata una DLL di risorse per ogni lingua supportata. L'uso di una DLL satellite si applica alle applicazioni eseguite in qualsiasi Windows operativo. Come descritto in [Gestione risorse MUI,](mui-resource-management.md)la tecnologia delle risorse MUI supporta una variazione nell'implementazione della DLL satellite standard.

### <a name="use-of-multiple-languages-in-a-resource-dll"></a>Uso di più lingue in una DLL di risorse

È possibile scegliere di creare un file eseguibile principale per l'applicazione MUI e una DLL di risorse per le risorse associate alle lingue supportate. Le copie dello stesso identificatore di risorsa sono definite nel file di risorse della lingua di base (estensione RC) in tag di lingua diversi per tutte le lingue supportate.

### <a name="use-of-an-application-specific-resource-mechanism"></a>Uso di un meccanismo Application-Specific risorse

È possibile pianificare l'applicazione MUI per l'uso di un meccanismo di risorse personalizzato. In questo caso, l'applicazione gestisce il caricamento delle risorse in modo specializzato.

## <a name="resource-localization"></a>Localizzazione delle risorse

Per supportare le lingue dell'interfaccia utente per l'applicazione MUI, è necessario che le risorse della lingua sono localizzate. MUI supporta due tipi di localizzazione, come descritto nella tabella seguente.



| Tipo di localizzazione       | Descrizione                                                                                                                                                                                                                                                                |
|-------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Localizzazione pre-compilazione  | Richiedere la localizzazione prima di compilare l'applicazione e le risorse specifiche della lingua. Il file di risorse della lingua di base per le lingue dell'interfaccia utente supportate viene copiato e rinominato per ogni lingua supportata e le copie vengono fornite ai localizzatori in base alle esigenze. |
| Localizzazione post-compilazione | Richiedere la localizzazione dopo aver compilato il file eseguibile e la DLL di risorse per l'applicazione. In questo caso, viene fornita una copia della DLL della risorsa a ogni localizzatore.                                                                                                     |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni interfaccia utente multilingue](about-multilingual-user-interface.md)
</dt> </dl>

 

 
