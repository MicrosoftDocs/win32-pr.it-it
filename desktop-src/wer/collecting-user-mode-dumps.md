---
title: Raccolta di dump di User-Mode
description: A partire da Windows Server 2008 e Windows Vista con Service Pack 1 (SP1), è possibile configurare Segnalazione errori Windows (WER) in modo che i dump completi della modalità utente vengano raccolti e archiviati localmente dopo l'arresto anomalo di un'applicazione in modalità utente.
ms.assetid: 8dad892b-04df-4aeb-b6c4-82f7676d382a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b7b1e7850e84d9fa6c8d10953d23640b41b1bc6
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/17/2020
ms.locfileid: "103872338"
---
# <a name="collecting-user-mode-dumps"></a>Raccolta di dump di User-Mode

A partire da Windows Server 2008 e Windows Vista con Service Pack 1 (SP1), è possibile configurare Segnalazione errori Windows (WER) in modo che i dump completi della modalità utente vengano raccolti e archiviati localmente dopo l'arresto anomalo di un'applicazione in modalità utente. Questa funzionalità non supporta le applicazioni che eseguono una segnalazione di arresti anomali personalizzata, incluse le applicazioni .NET.

Per impostazione predefinita questa funzionalità non è abilitata. Per abilitare la funzionalità sono necessari i privilegi di amministratore. Per abilitare e configurare la funzionalità, usare i seguenti valori del registro di sistema nella chiave **HKEY \_ locale \_ \\ software \\ Microsoft \\ Windows \\ segnalazione errori Windows \\ LocalDumps** .

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th>Valore</th>
<th>Descrizione</th>
<th>Type</th>
<th>Valore predefinito</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>DumpFolder</strong></td>
<td>Percorso in cui archiviare i file di dump. Se non si usa il percorso predefinito, assicurarsi che la cartella contenga ACL che consentono al processo di arresto anomalo di scrivere i dati nella cartella. Per gli arresti anomali del servizio, il dump viene scritto in cartelle di profili specifiche del servizio a seconda dell'account di servizio utilizzato. Ad esempio, la cartella del profilo per i servizi di sistema è%WINDIR%\System32\Config\SystemProfile. Per i servizi di rete e locali, la cartella è%WINDIR%\ServiceProfiles.<br/></td>
<td>REG_EXPAND_SZ</td>
<td>%LOCALAPPDATA%\CrashDumps</td>
</tr>
<tr class="even">
<td><strong>DumpCount</strong></td>
<td>Numero massimo di file di dump nella cartella. Quando viene superato il valore massimo, il file di dump meno recente nella cartella verrà sostituito con il nuovo file di dump.</td>
<td>REG_DWORD</td>
<td>10</td>
</tr>
<tr class="odd">
<td><strong>DumpType</strong></td>
<td>Specificare uno dei seguenti tipi di dump:
<ul>
<li>0: dump personalizzato</li>
<li>1: dump minimo</li>
<li>2: dump completo</li>
</ul></td>
<td>REG_DWORD</td>
<td>1</td>
</tr>
<tr class="even">
<td><strong>CustomDumpFlags</strong></td>
<td>Opzioni di dump personalizzate da utilizzare. Questo valore viene utilizzato solo quando <strong>DumpType</strong> è impostato su 0.<br/> Le opzioni sono una combinazione bit per bit dei valori di enumerazione <a href="/windows/desktop/api/minidumpapiset/ne-minidumpapiset-minidump_type"><strong>MINIDUMP_TYPE</strong></a> .<br/></td>
<td>REG_DWORD</td>
<td><code>MiniDumpWithDataSegs | MiniDumpWithUnloadedModules | MiniDumpWithProcessThreadData.</code></td>
</tr>
</tbody>
</table>

>[!NOTE]
> Un dump di arresto anomalo del sistema non viene raccolto quando si imposta il [debug automatico per arresti anomali **dell'applicazione**](../debug/configuring-automatic-debugging.md#configuring-automatic-debugging-for-application-crashes) 

Questi valori del registro di sistema rappresentano le impostazioni globali. È anche possibile specificare impostazioni per applicazione che eseguono l'override delle impostazioni globali. Per creare un'impostazione per ogni applicazione, creare una nuova chiave per l'applicazione in **HKEY \_ Local \_ Machine \\ software \\ Microsoft \\ Windows \\ segnalazione errori Windows \\ LocalDumps** (ad esempio, **HKEY \_ Local \_ Machine \\ software \\ Microsoft \\ Windows \\ segnalazione errori Windows \\ LocalDumps \\MyApplication.exe**). Aggiungere le impostazioni di dump sotto la chiave **MyApplication.exe** . Se l'applicazione si arresta in modo anomalo, WER legge prima le impostazioni globali e quindi esegue l'override di qualsiasi impostazione con le impostazioni specifiche dell'applicazione.

Dopo l'arresto anomalo di un'applicazione e prima della terminazione, il sistema verificherà le impostazioni del registro di sistema per determinare se è necessario raccogliere un dump locale. Al termine della raccolta di dump, l'applicazione verrà terminata normalmente. Se l'applicazione supporta il ripristino, il dump locale viene raccolto prima che venga chiamato il callback di ripristino.

Questi dump sono configurati e controllati indipendentemente dal resto dell'infrastruttura di WER. È possibile usare la raccolta di dump locale anche se WER è disabilitato o se l'utente annulla la segnalazione di WER. Il dump locale può essere diverso dal dump inviato a Microsoft.

 

