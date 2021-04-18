---
description: Evoluzione del supporto MUI nelle versioni di Windows
ms.assetid: a3bda96e-6a54-41b3-88d3-9da88d7c0416
title: Evoluzione del supporto MUI nelle versioni di Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b896c3651cbea3eef8f2d2021194742f24818f2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313835"
---
# <a name="evolution-of-mui-support-across-windows-versions"></a>Evoluzione del supporto MUI nelle versioni di Windows

-   [Prima di Windows Vista](#before-windows-vista)
-   [Windows Vista e versioni successive](#windows-vista-and-beyond)
    -   [Sistema operativo indipendente dalla lingua/MUI](#a-language-neutralmui-operating-system)
    -   [Gli scenari di distribuzione sono completamente basati su MUI](#deployment-scenarios-are-fully-mui-based)
    -   [Distribuzione con immagine singola](#single-image-deployment)
    -   [Modello di manutenzione migliorato](#improved-servicing-model)
    -   [Infrastruttura MUI](#mui-infrastructure)
    -   [Gestione della lingua](#language-management)
    -   [Gestione delle risorse](#resource-handling)

## <a name="before-windows-vista"></a>Prima di Windows Vista

Prima della versione di Windows Vista, Windows veniva fornito con immagini in linguaggio singolo, il che significava che ogni versione localizzata di Windows conteneva una sola lingua per la relativa interfaccia utente. MUI era un componente aggiuntivo della versione in lingua inglese del sistema operativo e i pacchetti dell'interfaccia utente multilingue potevano essere aggiunti solo a determinate versioni in lingua inglese di Windows. Quando è installato nella versione inglese di Windows, MUI ha consentito la modifica della lingua dell'interfaccia utente del sistema operativo in base alle preferenze dei singoli utenti a una delle lingue supportate.

Il modello di MUI Pack non ha esposto il supporto MUI per le applicazioni. Sebbene gli sviluppatori potessero creare applicazioni multilingue, avrebbero dovuto creare i propri meccanismi a tale scopo.

## <a name="windows-vista-and-beyond"></a>Windows Vista e versioni successive

Con Windows Vista, Microsoft ha realizzato un investimento significativo in MUI. Windows Vista è stato creato in base a una piattaforma MUI. Sebbene questo rappresenti un importante progresso nella strategia di localizzazione di Windows, poiché si tratta di una chiave fondamentale per Microsoft per fornire Windows in più lingue, è prima di tutto un ottimo progresso per utenti e clienti di Windows.

### <a name="a-language-neutralmui-operating-system"></a>Sistema operativo indipendente dalla lingua/MUI

La maggior parte dei file binari di Windows Vista sono conformi a MUI e i relativi dati localizzabili vengono archiviati separatamente dal codice. Questo offre flessibilità, in quanto è possibile aggiungere dati di lingua diversi in qualsiasi momento.

### <a name="deployment-scenarios-are-fully-mui-based"></a>Gli scenari di distribuzione sono completamente basati su MUI

La progettazione per la creazione di pacchetti e l'installazione di Windows Vista è basata su MUI e tutti i dati localizzabili sono inclusi in pacchetti specifici della lingua e ogni Language Pack può essere distribuito in scenari diversi. Ad esempio, anche se i DVD finali di Windows Vista contengono versioni in linguaggio singolo, gli utenti dell'edizione Ultimate possono scaricare Language Pack MUI aggiuntivi e possono cambiare lingua dell'interfaccia utente dal pannello di controllo **Opzioni internazionali e della lingua** . I licenziatari di Enterprise Edition ottengono tutte le lingue e possono distribuirli.

### <a name="single-image-deployment"></a>Distribuzione con immagine singola

I clienti aziendali e gli OEM possono ora ridurre il numero di immagini che è necessario gestire per distribuire Windows e le applicazioni nei computer in diverse impostazioni locali tramite la distribuzione di un'immagine singola.

Con MUI in Windows Vista, un'immagine contenente più lingue può essere distribuita a tutti gli utenti del linguaggio e gli utenti possono determinare le proprie lingue preferite (entro i criteri) durante l'installazione o l'esperienza iniziale "predefinita" con il computer. In particolare, gli OEM possono inserire molte lingue dell'interfaccia utente nei nuovi computer per consentire agli utenti di selezionarne una dal centro di benvenuto. Quindi, da un'immagine con più Language Pack, il programma di installazione visualizzerà un elenco di lingue disponibili e consentirà agli utenti di selezionarne uno. Tutte le impostazioni internazionali vengono quindi impostate in base alla lingua o alle impostazioni locali selezionate.

### <a name="improved-servicing-model"></a>Modello di manutenzione migliorato

È ora possibile installare lo stesso QFE o il pacchetto di correzione della sicurezza in qualsiasi sistema di linguaggio. Questo è fondamentale perché consente un ritorno più rapido delle correzioni di sicurezza in particolare e consente a tutti gli utenti internazionali di trarre vantaggio dalla stessa disponibilità di tutte le correzioni di sicurezza.

### <a name="mui-infrastructure"></a>Infrastruttura MUI

A partire da Windows Vista, le API MUI sono disponibili per consentire agli sviluppatori di sfruttare i meccanismi MUI per le proprie applicazioni, senza dover creare logica personalizzata per la gestione delle risorse e la gestione del linguaggio.

### <a name="language-management"></a>Gestione della lingua

Le API MUI di base che forniscono funzionalità di gestione della lingua dell'interfaccia utente sono disponibili come parte dell'infrastruttura MUI. Per semplificare la gestione delle diverse impostazioni della lingua dell'interfaccia utente a livello di sistema, utente e applicazione, MUI li combina internamente in un unico elenco con priorità. MUI implementa quindi un meccanismo di fallback basato su questo elenco in ordine di priorità, consentendo soluzioni di localizzazione parziali offrendo agli utenti un'esperienza di lingua dell'interfaccia utente appropriata, se non preferita.

Ad esempio, un sistema che esegue la versione spagnola di Windows Vista con un LIP (Language Interface Pack) Catalano installato sul sistema operativo di base può supportare il comportamento seguente: il sistema tenterà e visualizzerà prima le risorse in catalano e, se queste risorse non sono disponibili in Catalano, fornire all'utente risorse per lo spagnolo.

### <a name="resource-handling"></a>Gestione delle risorse

Con l'infrastruttura MUI migliorata disponibile a partire da Windows Vista, la maggior parte delle tecnologie delle risorse comuni è abilitata per MUI. Nella tabella seguente vengono forniti ulteriori dettagli sul supporto per la gestione delle risorse disponibile in Windows Vista.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Category</th>
<th>Supporto</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Tipi di risorsa supportati</td>
<td><ul>
<li>Risorsa Win32/non gestita:. DLL/. EXE/. OCX</li>
<li>Registrazioni correlate alla shell</li>
<li>Risorse correlate alla gestione: log eventi, file di snap-in/MSC</li>
<li>WMI: MOF/MFL</li>
<li>Criteri di gruppo: ADMX/ADML</li>
<li>Resources.dll gestite</li>
</ul></td>
</tr>
<tr class="even">
<td>Strumenti di sviluppo</td>
<td><ul>
<li>Per Win32: RC.exe, MUIRCT.exe e Visual Studio 2005 e versioni successive</li>
</ul></td>
</tr>
<tr class="odd">
<td>Supporto per tipi di risorse limitati</td>
<td><ul>
<li>file della guida *. chm</li>
</ul></td>
</tr>
</tbody>
</table>



 

 

 



