---
description: Evoluzione del supporto MUI tra Windows versioni
ms.assetid: a3bda96e-6a54-41b3-88d3-9da88d7c0416
title: Evoluzione del supporto MUI tra Windows versioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57e08ff181cf34daa95710d5bf57a294703a88ef
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122467898"
---
# <a name="evolution-of-mui-support-across-windows-versions"></a>Evoluzione del supporto MUI tra Windows versioni

-   [Prima di Windows Vista](#before-windows-vista)
-   [Windows Vista e oltre](#windows-vista-and-beyond)
    -   [Sistema operativo indipendente dalla lingua/MUI](#a-language-neutralmui-operating-system)
    -   [Gli scenari di distribuzione sono completamente basati su MUI](#deployment-scenarios-are-fully-mui-based)
    -   [Distribuzione di una singola immagine](#single-image-deployment)
    -   [Modello di manutenzione migliorato](#improved-servicing-model)
    -   [Infrastruttura MUI](#mui-infrastructure)
    -   [Gestione del linguaggio](#language-management)
    -   [Gestione delle risorse](#resource-handling)

## <a name="before-windows-vista"></a>Prima di Windows Vista

Prima della versione di Windows Vista, Windows fornito con immagini in una sola lingua, il che significava che ogni versione localizzata di Windows conteneva una singola lingua per l'interfaccia utente. MUI era un componente aggiuntivo per la versione inglese del sistema operativo e i interfaccia utente multilingue Pack potevano essere aggiunti solo a determinate versioni in lingua inglese di Windows. Se installato nella versione inglese di Windows, MUI ha consentito di modificare la lingua dell'interfaccia utente del sistema operativo in base alle preferenze dei singoli utenti in una delle lingue supportate.

Il modello MUI Pack non ha esposto il supporto MUI per le applicazioni. Anche se gli sviluppatori potevano creare applicazioni multilingue, dovevano creare meccanismi personalizzati a tale scopo.

## <a name="windows-vista-and-beyond"></a>Windows Vista e oltre

Con Windows Vista, Microsoft ha effettuato un investimento significativo in MUI. Windows Vista è stato creato da zero su una piattaforma MUI. Anche se questo rappresenta un importante passo avanti nella strategia di localizzazione di Windows perché è un elemento chiave per consentire a Microsoft di fornire Windows in più lingue che mai, è innanzitutto un grande passo avanti per gli utenti e i clienti di Windows.

### <a name="a-language-neutralmui-operating-system"></a>Sistema operativo indipendente dalla lingua/MUI

La maggior parte dei file binari Windows Vista è conforme a MUI e i relativi dati localizzabili vengono archiviati separatamente dal codice. Ciò offre flessibilità, in quanto è possibile aggiungere dati linguistici diversi in qualsiasi momento.

### <a name="deployment-scenarios-are-fully-mui-based"></a>Gli scenari di distribuzione sono completamente basati su MUI

La progettazione della creazione di pacchetti e dell'installazione di Windows Vista è basata su MUI e tutti i dati localizzabili sono contenuti in pacchetti specifici della lingua e ogni language pack può essere distribuito in scenari diversi. Ad esempio, anche se i DVD per la vendita al dettaglio per Windows Vista contengono versioni in una sola lingua, gli utenti dell'edizione Ultimate possono scaricare Language Pack MUI aggiuntivi e cambiare lingua dell'interfaccia utente dal pannello di controllo Opzioni internazionali e della lingua.  Enterprise di licenza dell'edizione possono ottenere tutte le lingue e distribuirle.

### <a name="single-image-deployment"></a>Distribuzione di una singola immagine

Enterprise clienti e OEM possono ora ridurre il numero di immagini che devono gestire per distribuire applicazioni e Windows in computer con impostazioni locali diverse tramite la distribuzione di una singola immagine.

Con MUI in Windows Vista, un'immagine contenente più lingue può essere distribuita agli utenti di qualsiasi lingua e gli utenti possono determinare le proprie lingue preferite (all'interno dei criteri) durante l'installazione o l'esperienza iniziale "predefinita" con il computer. In particolare, gli OEM possono inserire molte lingue dell'interfaccia utente nei nuovi computer per consentire agli utenti di selezionarne una dal Centro attività iniziali. Di conseguenza, da un'immagine con più Language Pack, il programma di installazione visualizza un elenco delle lingue disponibili e consente agli utenti di selezionarne una. Tutte le impostazioni internazionali vengono quindi impostate in modo che corrispondano alla lingua o alle impostazioni locali selezionate.

### <a name="improved-servicing-model"></a>Modello di manutenzione migliorato

Lo stesso QFE o pacchetto di correzione della sicurezza può ora essere installato in qualsiasi sistema di linguaggio. Questo è fondamentale perché consente un turnaround più rapido delle correzioni per la sicurezza in particolare e consente a tutti gli utenti internazionali di trarre vantaggio dalla stessa disponibilità di tutte le correzioni per la sicurezza.

### <a name="mui-infrastructure"></a>Infrastruttura MUI

A partire da Windows Vista, sono disponibili API MUI per consentire agli sviluppatori di sfruttare i meccanismi MUI per le proprie applicazioni, senza dover creare logica personalizzata per la gestione delle risorse e la gestione del linguaggio.

### <a name="language-management"></a>Gestione del linguaggio

Le API MUI di base che forniscono funzionalità di gestione del linguaggio dell'interfaccia utente sono disponibili come parte dell'infrastruttura MUI. Per facilitare la gestione delle diverse impostazioni della lingua dell'interfaccia utente a livello di sistema, utente e applicazione, MUI le combina internamente in un unico elenco con priorità. MUI implementa quindi un meccanismo di fallback basato su questo elenco con priorità, consentendo soluzioni di localizzazione parziali, offrendo allo stesso tempo agli utenti un'esperienza linguistica appropriata, se non preferita, dell'interfaccia utente.

Ad esempio, un sistema che esegue la versione in spagnolo di Windows Vista con un Language Interface Pack (LIP) installato sul sistema operativo di base può supportare il comportamento seguente: il sistema tenterà di visualizzare prima le relative risorse in Spagna e, se queste risorse non sono disponibili in Catalogna, fornire all'utente le risorse in spagnolo.

### <a name="resource-handling"></a>Gestione delle risorse

Con l'infrastruttura MUI migliorata disponibile a partire da Windows Vista, le tecnologie di risorse più comuni sono abilitate per MUI. La tabella seguente fornisce dettagli aggiuntivi sul supporto per la gestione delle risorse disponibile in Windows Vista.




| Category | Supporto | 
|----------|---------|
| Tipi di risorsa supportati | <ul><li>Risorsa Win32/non gestita: .DLL/.EXE/. OCX</li><li>Registrazioni correlate alla shell</li><li>Risorse correlate alla gestione: registro eventi, file snap-in/MSC</li><li>WMI: MOF/MFL</li><li>Criteri di gruppo: ADMX/ADML</li><li>Gestione Resources.dll</li></ul> | 
| Strumenti di sviluppo | <ul><li>Per Win32: RC.exe, MUIRCT.exe e Visual Studio 2005 e versioni successive</li></ul> | 
| Supporto limitato per i tipi di risorse | <ul><li>File della Guida *.chm</li></ul> | 




 

 

 



