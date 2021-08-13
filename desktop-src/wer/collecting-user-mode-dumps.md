---
title: Raccolta di User-Mode dump
description: A partire da Windows Server 2008 e Windows Vista con Service Pack 1 (SP1), è possibile configurare Segnalazione errori Windows (WER) in modo che i dump completi in modalità utente siano raccolti e archiviati in locale dopo un arresto anomalo di un'applicazione in modalità utente.
ms.assetid: 8dad892b-04df-4aeb-b6c4-82f7676d382a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4597c4bf1fd583b647e7ad74b7f1cb2cd41be9c0118226d502932c61f481cedd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118442365"
---
# <a name="collecting-user-mode-dumps"></a>Raccolta di User-Mode dump

A partire da Windows Server 2008 e Windows Vista con Service Pack 1 (SP1), è possibile configurare Segnalazione errori Windows (WER) in modo che i dump completi in modalità utente siano raccolti e archiviati in locale dopo un arresto anomalo di un'applicazione in modalità utente. Le applicazioni che e funzionalità di segnalazione di arresti anomalo del sistema personalizzati, incluse le applicazioni .NET, non sono supportate da questa funzionalità.

Per impostazione predefinita questa funzionalità non è abilitata. L'abilitazione della funzionalità richiede privilegi di amministratore. Per abilitare e configurare la funzionalità, usare i valori del Registro di sistema seguenti nella chiave **HKEY \_ LOCAL MACHINE SOFTWARE microsoft Windows Segnalazione errori Windows \_ \\ \\ \\ \\ \\ LocalDumps.**

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
<td>Percorso in cui archiviare i file di dump. Se non si usa il percorso predefinito, assicurarsi che la cartella contenga elenchi di controllo di accesso che consentono al processo che si arresta in modo anomalo di scrivere dati nella cartella. Per gli arresti anomali del servizio, il dump viene scritto nelle cartelle del profilo specifiche del servizio a seconda dell'account del servizio usato. Ad esempio, la cartella del profilo per i servizi di sistema è %WINDIR%\System32\Config\SystemProfile. Per Servizi di rete e locali, la cartella è %WINDIR%\ServiceProfiles.<br/></td>
<td>REG_EXPAND_SZ</td>
<td>%LOCALAPPDATA%\CrashDumps</td>
</tr>
<tr class="even">
<td><strong>DumpCount</strong></td>
<td>Numero massimo di file di dump nella cartella. Quando viene superato il valore massimo, il file dump meno recente nella cartella verrà sostituito con il nuovo file dump.</td>
<td>REG_DWORD</td>
<td>10</td>
</tr>
<tr class="odd">
<td><strong>DumpType</strong></td>
<td>Specificare uno dei tipi di dump seguenti:
<ul>
<li>0: dump personalizzato</li>
<li>1: Minidump</li>
<li>2: Dump completo</li>
</ul></td>
<td>REG_DWORD</td>
<td>1</td>
</tr>
<tr class="even">
<td><strong>CustomDumpFlags</strong></td>
<td>Opzioni di dump personalizzate da utilizzare. Questo valore viene usato solo quando <strong>DumpType</strong> è impostato su 0.<br/> Le opzioni sono una combinazione bit per bit dei <a href="/windows/desktop/api/minidumpapiset/ne-minidumpapiset-minidump_type"><strong>MINIDUMP_TYPE</strong></a> di enumerazione.<br/></td>
<td>REG_DWORD</td>
 <td><code>0x00000121</code> (<code>MiniDumpWithDataSegs | MiniDumpWithUnloadedModules | MiniDumpWithProcessThreadData == 0x00000001 | 0x00000020 | 0x00000100)</code></td>
</tr>
</tbody>
</table>

>[!NOTE]
> Un dump di arresto anomalo del sistema non viene raccolto quando si imposta il [debug automatico per **l'arresto anomalo dell'applicazione.**](../debug/configuring-automatic-debugging.md#configuring-automatic-debugging-for-application-crashes) 

Questi valori del Registro di sistema rappresentano le impostazioni globali. È anche possibile specificare impostazioni per applicazione che sostituiscono le impostazioni globali. Per creare un'impostazione per applicazione, creare una nuova chiave per l'applicazione in **HKEY \_ LOCAL MACHINE Software Microsoft Windows Segnalazione errori Windows \_ \\ \\ \\ \\ \\ LocalDumps** (ad esempio, **HKEY LOCAL MACHINE Software \_ Microsoft Windows Segnalazione errori Windows \_ \\ \\ \\ \\ \\ LocalDumps \\MyApplication.exe**). Aggiungere le impostazioni di dump nella **chiaveMyApplication.exe** dump. Se l'applicazione si arresta in modo anomalo, WeR leggerà prima le impostazioni globali e quindi eseguirà l'override di qualsiasi impostazione con le impostazioni specifiche dell'applicazione.

Dopo l'arresto anomalo di un'applicazione e prima della chiusura, il sistema controlla le impostazioni del Registro di sistema per determinare se è necessario raccogliere un dump locale. Al termine della raccolta di dump, l'applicazione può terminare normalmente. Se l'applicazione supporta il ripristino, il dump locale viene raccolto prima che venga chiamato il callback di ripristino.

Questi dump vengono configurati e controllati indipendentemente dal resto dell'infrastruttura di WeR. È possibile usare la raccolta di dump locali anche se Segnalazione errori Windows è disabilitato o se l'utente annulla la segnalazione segnalazione errori Windows. Il dump locale può essere diverso dal dump inviato a Microsoft.

 

