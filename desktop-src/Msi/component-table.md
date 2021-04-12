---
description: La tabella Component elenca i componenti di e include le colonne seguenti.
ms.assetid: 069d64e9-106a-42b7-8dea-a44fc0c6e0cd
title: Tabella componenti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b721996767fa98209f0e13530f8f1bb1ba8cca07
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226450"
---
# <a name="component-table"></a>Tabella componenti

La tabella Component elenca i componenti di e include le colonne seguenti.



| Colonna      | Tipo                         | Chiave | Nullable |
|-------------|------------------------------|-----|----------|
| Componente   | [Identificatore](identifier.md) | S   | N        |
| ComponentId | [GUID](guid.md)             | N   | S        |
| Directory\_ | [Identificatore](identifier.md) | N   | N        |
| Attributi  | [Integer](integer.md)       | N   | N        |
| Condizione   | [Condition](condition.md)   | N   | S        |
| KeyPath     | [Identificatore](identifier.md) | N   | S        |



 

## <a name="columns"></a>Colonne

<dl> <dt>

<span id="Component"></span><span id="component"></span><span id="COMPONENT"></span>Componente
</dt> <dd>

Identifica il record del componente.

Chiave della tabella primaria.

</dd> <dt>

<span id="ComponentId"></span><span id="componentid"></span><span id="COMPONENTID"></span>ComponentId
</dt> <dd>

GUID di stringa univoco per il componente, la versione e la lingua.

Si noti che le lettere di questi GUID devono essere maiuscole. Utilità come GUIDGEN possono generare GUID contenenti lettere minuscole. Le lettere minuscole devono essere modificate in lettere maiuscole per rendere questi GUID del codice componente valido.

Se questa colonna è null, il programma di installazione non registra il componente e il componente non può essere rimosso o ripristinato dal programma di installazione. Questa operazione può essere eseguita intenzionalmente se il componente è necessario solo durante l'installazione, ad esempio un'azione personalizzata che pulisce i file temporanei o rimuove un prodotto obsoleto. Può anche essere utile quando si copiano i file di dati nel computer di un utente che non deve essere registrato.

</dd> <dt>

<span id="Directory_"></span><span id="directory_"></span><span id="DIRECTORY_"></span>Directory\_
</dt> <dd>

Chiave esterna di una voce nella [tabella di directory](directory-table.md). Si tratta di un nome di proprietà il cui valore contiene il percorso effettivo, che può essere impostato dall' [azione AppSearch](appsearch-action.md) o con l'impostazione predefinita ottenuta dalla tabella di directory.

Gli sviluppatori devono evitare di creare componenti che inseriscono i file in una delle cartelle dei profili utente. Questi file non sono disponibili per tutti gli utenti in situazioni multiutente e possono fare in modo che il programma di installazione possa visualizzare in modo permanente il componente in modo da richiedere il ripristino.

Chiave esterna per la colonna uno della tabella di directory.

</dd> <dt>

<span id="Attributes"></span><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributi
</dt> <dd>

Questa colonna contiene un flag di bit che specifica le opzioni per l'esecuzione remota. Aggiungere il bit indicato al valore totale nella colonna per includere un'opzione.

> [!Note]  
> Nel caso di un file con estensione msi scaricato da un percorso Web, i flag di attributo non devono essere impostati in modo da consentire l'esecuzione dall'origine di un componente. Si tratta di una limitazione del Windows Installer e può restituire uno stato della funzionalità di INSTALLSTATE \_ BADCONFIG.

 



<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th>Flag di bit</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><dl> <dt>0x0000</dt> <dt><strong>msidbComponentAttributesLocalOnly</strong></dt> <dt>0</dt> </dl> Impossibile eseguire il componente dall'origine. Impostare questo bit per tutti i componenti appartenenti a una funzionalità per impedire che la funzionalità venga eseguita da rete o da Run-from-source. Si noti che se una funzionalità non ha componenti, la funzionalità Visualizza sempre le opzioni Esegui da origine ed Esegui da computer come valide.<br/></td>
</tr>
<tr class="even">
<td><dl> <dt><strong>msidbComponentAttributesSourceOnly</strong></dt> <dt>1</dt> <dt>0x0001</dt> </dl> Il componente può essere eseguito solo dall'origine. Impostare questo bit per tutti i componenti appartenenti a una funzionalità per impedire che la funzionalità venga eseguita dal computer. Si noti che se una funzionalità non ha componenti, la funzionalità Visualizza sempre le opzioni Esegui da origine ed Esegui da computer come valide.<br/></td>
</tr>
<tr class="odd">
<td><dl> <dt><strong>msidbComponentAttributesOptional</strong></dt> <dt>2</dt> <dt>0x0002</dt> </dl> Il componente può essere eseguito localmente o dall'origine.<br/></td>
</tr>
<tr class="even">
<td><dl> <dt><strong>msidbComponentAttributesRegistryKeyPath</strong></dt> <dt>4</dt> <dt>0x0004</dt> </dl> Se questo bit è impostato, il valore nella colonna percorso chiave viene usato come chiave nella <a href="registry-table.md">tabella del registro di sistema</a>. Se il campo del valore del record corrispondente nella tabella del registro di sistema è null, il campo del nome del record non deve contenere &quot; + &quot; , &quot; - &quot; o &quot; * &quot; . Per ulteriori informazioni, vedere la descrizione del campo nome nella <a href="registry-table.md">tabella del registro di sistema</a>.<br/> L'impostazione di questo bit è consigliata per le voci del registro di sistema scritte nell'hive HKCU. Ciò garantisce che il programma di installazione scriva le voci del registro di sistema HKCU necessarie quando ci sono più utenti nello stesso computer.<br/></td>
</tr>
<tr class="odd">
<td><dl> <dt><strong>msidbComponentAttributesSharedDllRefCount</strong></dt> <dt>8</dt> <dt>0x0008</dt> </dl> Se questo bit è impostato, il programma di installazione incrementa il conteggio dei riferimenti nel registro di sistema delle DLL condivise del file di chiave del componente. Se questo bit non è impostato, il programma di installazione incrementa il conteggio dei riferimenti solo se il conteggio dei riferimenti esiste già.<br/></td>
</tr>
<tr class="even">
<td><dl> <dt><strong>msidbComponentAttributesPermanent</strong></dt> <dt>16</dt> <dt>0x0010</dt> </dl> Se questo bit è impostato, il programma di installazione non rimuove il componente durante una disinstallazione. Il programma di installazione registra un client di sistema aggiuntivo per il componente nelle impostazioni del registro di sistema Windows Installer.<br/></td>
</tr>
<tr class="odd">
<td><dl> <dt><strong>msidbComponentAttributesODBCDataSource</strong></dt> <dt>32</dt> <dt>0x0020</dt> </dl> Se questo bit è impostato, il valore nella colonna percorso chiave è una chiave nella <a href="odbcdatasource-table.md">tabella ODBCDataSource</a>.<br/></td>
</tr>
<tr class="even">
<td><dl> <dt><strong>msidbComponentAttributesTransitive</strong></dt> <dt>64</dt> <dt>0x0040</dt> </dl> Se questo bit è impostato, il programma di installazione rivaluterà il valore dell'istruzione nella colonna condizione durante una reinstallazione. Se il valore era in precedenza false e è stato modificato in true, il programma di installazione installerà il componente. Se il valore era in precedenza true e è stato modificato in false, il programma di installazione rimuove il componente anche se il componente dispone di altri prodotti come client.<br/> Questo bit deve essere impostato solo per i componenti transitivi. Vedere <a href="using-transitive-components.md">utilizzo dei componenti transitivi</a>.<br/></td>
</tr>
<tr class="odd">
<td><dl> <dt><strong>msidbComponentAttributesNeverOverwrite</strong></dt> <dt>128</dt> <dt>0x0080</dt> </dl> Se questo bit è impostato, il programma di installazione non installa o reinstalla il componente se è già presente un file di percorso della chiave o una voce del registro di sistema del percorso della chiave per il componente. L'applicazione esegue la registrazione come client del componente.<br/> Utilizzare questo flag solo per i componenti registrati dalla tabella del registro di sistema. Non usare questo flag per i componenti registrati dalle tabelle <a href="appid-table.md">AppID</a>, <a href="class-table.md">Class</a>, <a href="extension-table.md">Extension</a>, <a href="progid-table.md">ProgID</a>, <a href="mime-table.md">MIME</a>e <a href="verb-table.md">Verb</a>.<br/></td>
</tr>
<tr class="even">
<td><dl> <dt><strong>msidbComponentAttributes64bit</strong></dt> <dt>256</dt> <dt>0x0100</dt> </dl> Impostare questo bit per contrassegnare questo elemento come componente a 64 bit. Questo attributo semplifica l'installazione dei pacchetti che includono sia i componenti a 32 bit che quelli a 64 bit. Se questo bit non è impostato, il componente viene registrato come componente a 32 bit.<br/> Se si tratta di un componente a 64 bit che sostituisce un componente a 32 bit, impostare questo bit e assegnare un nuovo GUID nella colonna ComponentId.<br/></td>
</tr>
<tr class="odd">
<td><dl> <dt><strong>msidbComponentAttributesDisableRegistryReflection</strong></dt> <dt>512</dt> <dt>0x0200</dt> </dl> Impostare questo bit per disabilitare la <a href="/windows/desktop/WinProg64/registry-reflection">Reflection del registro</a> di sistema in tutte le chiavi del registro di sistema esistenti e nuove interessate da questo componente. Se questo bit è impostato, il Windows Installer chiama <a href="/windows/desktop/api/winreg/nf-winreg-regdisablereflectionkey"><strong>RegDisableReflectionKey</strong></a> su ogni chiave a cui accede il componente. Questo bit è disponibile con Windows Installer versione 4,0. Questo bit viene ignorato nei sistemi a 32 bit. Questo bit viene ignorato nelle versioni a 64 bit di Windows XP.<br/>
<blockquote>
[!Note]<br />
le applicazioni Windows a 32 bit in esecuzione nell'emulatore Windows a 64 bit (WOW64) fanno riferimento a una vista diversa del registro di sistema rispetto alle applicazioni a 64 bit. La reflection del registro di sistema copia alcuni valori del registro di sistema tra queste due visualizzazioni del registro
</blockquote>
<br/> <br/></td>
</tr>
<tr class="even">
<td><dl> <dt><strong>msidbComponentAttributesUninstallOnSupersedence</strong></dt> <dt>1024</dt> <dt>0x0400</dt> </dl> Impostare questo bit per un componente in un pacchetto di patch per evitare di lasciare i componenti orfani nel computer. Se viene installata una patch successiva contrassegnata con il valore <strong>msidbPatchSequenceSupersedeEarlier</strong> nella tabella <a href="msipatchsequence-table.md">MsiPatchSequence</a> per sostituire la prima patch, Windows Installer 4,5 e versioni successive possono annullare la registrazione e la disinstallazione dei componenti contrassegnati con il valore <strong>msidbComponentAttributesUninstallOnSupersedence</strong> . Se il componente non è contrassegnato con questo bit, l'installazione di una patch sostitutiva può rimanere dietro un componente inutilizzato nel computer.<br/> L'impostazione della proprietà <strong>MSIUNINSTALLSUPERSEDEDCOMPONENTS</strong> ha lo stesso effetto dell'impostazione di questo bit per tutti i componenti.<br/> <strong><a href="not-supported-in-windows-installer-4-0.md">Windows Installer 4,0 e versioni precedenti</a>:</strong> il valore <strong>msidbComponentAttributesUninstallOnSupersedence</strong> non è supportato e viene ignorato.<br/> <br/></td>
</tr>
<tr class="odd">
<td><dl> <dt><strong>msidbComponentAttributesShared</strong></dt> <dt>2048</dt> <dt>0x0800</dt> </dl> Se un componente è contrassegnato con questo valore di attributo in almeno un pacchetto installato nel sistema, il programma di installazione considera il componente come contrassegnato in tutti i pacchetti. Se viene disinstallato un pacchetto che condivide il componente contrassegnato, Windows Installer 4,5 può continuare a condividere la versione più recente del componente nel sistema, anche se la versione più recente è stata installata dal pacchetto in fase di disinstallazione. <br/> Se il criterio DisableSharedComponent è impostato su 1, nessun pacchetto ottiene la funzionalità del componente condiviso abilitata da questo bit.<br/> <strong><a href="not-supported-in-windows-installer-4-0.md">Windows Installer 4,0 e versioni precedenti</a>:</strong> il valore <strong>msidbComponentAttributesShared</strong> non è supportato e viene ignorato.<br/> <br/></td>
</tr>
</tbody>
</table>



 

</dd> <dt>

<span id="Condition"></span><span id="condition"></span><span id="CONDITION"></span>Condizione
</dt> <dd>

Questa colonna contiene un'istruzione condizionale che consente di controllare se un componente è installato. Se la condizione è null o restituisce true, il componente è abilitato. Se la condizione restituisce false, il componente è disabilitato e non è installato.

Il campo condizione Abilita o Disabilita un componente solo durante l' [azione CostFinalize secondo](costfinalize-action.md). Per abilitare o disabilitare un componente dopo CostFinalize secondo, è necessario usare un'azione personalizzata o [DoAction ControlEvent](doaction-controlevent.md) per chiamare [**MsiSetComponentState**](/windows/desktop/api/Msiquery/nf-msiquery-msisetcomponentstatea).

Si noti che, a meno che non sia impostato il bit transitivo nella colonna attributi per un componente, il componente rimane abilitato una volta installato anche se l'istruzione condizionale nella colonna condizione restituisce false in seguito a un'installazione di manutenzione successiva del prodotto.

La colonna Condition della tabella Component accetta espressioni condizionali contenenti riferimenti agli stati installati delle funzionalità e dei componenti. Per informazioni sulla sintassi delle istruzioni condizionali, vedere [sintassi dell'istruzione condizionale](conditional-statement-syntax.md).

</dd> <dt>

<span id="KeyPath"></span><span id="keypath"></span><span id="KEYPATH"></span>KeyPath
</dt> <dd>

Questo valore punta a un file o a una cartella appartenente al componente utilizzato dal programma di installazione per rilevare il componente. Due componenti non possono condividere lo stesso valore di percorso della chiave. Il valore in questa colonna è anche il percorso restituito dalla funzione [**MsiGetComponentPath**](/windows/desktop/api/Msi/nf-msi-msigetcomponentpatha) .

Se il valore non è null, il percorso delle chiavi è una chiave primaria nel [Registro di sistema](registry-table.md), [ODBCDataSource](odbcdatasource-table.md)o le [tabelle di file](file-table.md) a seconda del valore dell'attributo. Se il percorso della chiave è null, la cartella della colonna di directory \_ viene utilizzata come percorso della chiave.

Poiché le cartelle create dal programma di installazione vengono eliminate quando diventano vuote, è necessario creare una voce nella [tabella CreateFolder](createfolder-table.md) per installare un componente costituito da una cartella vuota.

Si noti che se un componente Windows Installer contiene una chiave del registro di sistema o un file protetto da [Protezione risorse di Windows](/windows/desktop/Wfp/windows-resource-protection-portal) (WRP) o da un file protetto da protezione file di Windows, questa risorsa deve essere utilizzata come percorso di chiave per il componente. In questo caso, Windows Installer non installa, aggiorna o rimuove il componente. Non includere risorse protette in un pacchetto di installazione. È invece consigliabile usare i [meccanismi di sostituzione delle risorse supportati](/windows/desktop/Wfp/supported-file-replacement-mechanisms) per protezione risorse di Windows. Per ulteriori informazioni, vedere [utilizzo di Windows Installer e protezione risorse di Windows](windows-resource-protection-on-windows-vista.md).

</dd> </dl>

## <a name="remarks"></a>Commenti

Per una descrizione della relazione tra componenti e funzionalità, vedere [tabella delle funzionalità](feature-table.md).

Il programma di installazione tiene traccia delle DLL condivise indipendentemente dal conteggio dei riferimenti alla DLL condivisa nel registro di sistema. Se nel registro di sistema è presente un conteggio dei riferimenti per una DLL condivisa, il programma di installazione incrementa sempre il numero durante l'installazione del file e lo decrementa quando viene disinstallato. Se **msidbComponentAttributesSharedDllRefCount**, non è impostato e il conteggio dei riferimenti non esiste già, il programma di installazione non ne creerà uno. Si noti che il conteggio dei riferimenti SharedDLLs nel registro di sistema viene incrementato per tutti i file installati nella cartella di sistema.

Se **msidbComponentAttributesSharedDllRefCount** non è impostato, un'altra applicazione può rimuovere il componente anche se è ancora necessario. Per vedere in che modo questo potrebbe verificarsi, si consideri lo scenario seguente:

-   Un'applicazione che usa il programma di installazione installa un componente condiviso.
-   Il bit **msidbComponentAttributesSharedDllRefCount** non è impostato e non è presente alcun conteggio dei riferimenti. Il programma di installazione non inizia quindi un conteggio dei riferimenti.
-   Un'applicazione legacy che condivide questo componente e non utilizza il programma di installazione viene installata.
-   L'applicazione legacy crea e incrementa un conteggio dei riferimenti per il componente condiviso.
-   L'applicazione legacy viene disinstallata.
-   Il conteggio dei riferimenti per il componente condiviso viene decrementato a zero e il componente viene rimosso.
-   L'applicazione che utilizza il programma di installazione non dispone più dell'accesso al componente.

Per evitare questo comportamento, impostare **msidbComponentAttributesSharedDllRefCount**.

Si noti che i componenti dei servizi di sistema non devono essere specificati come Run-from-source senza essere progettati in modo specifico per tale uso. Per ulteriori informazioni, vedere la [tabella ServiceInstall](serviceinstall-table.md) .

Si noti che gli attributi che abilitano l'installazione dell'esecuzione dall'origine non devono mai essere impostati per i componenti contenenti librerie a collegamento dinamico che passano alla cartella di sistema. Il motivo è che se lo stato di installazione del componente viene impostato su Run-from-source seguendo una funzionalità o impostando nell'interfaccia utente, le successive chiamate a **LoadLibrary** sulla dll avranno esito negativo.

Vedere anche [controllo degli Stati di selezione delle funzionalità](controlling-feature-selection-states.md).

## <a name="validation"></a>Convalida

<dl>

[ICE02](ice02.md)  
[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE07](ice07.md)  
[ICE08](ice08.md)  
[ICE09](ice09.md)  
[ICE18](ice18.md)  
[ICE19](ice19.md)  
[ICE21](ice21.md)  
[ICE30](ice30.md)  
[ICE32](ice32.md)  
[ICE35](ice35.md)  
[ICE38](ice38.md)  
[ICE41](ice41.md)  
[ICE42](ice42.md)  
[ICE43](ice43.md)  
[ICE46](ice46.md)  
[ICE50](ice50.md)  
[ICE54](ice54.md)  
[ICE57](ice57.md)  
[ICE59](ice59.md)  
[ICE62](ice62.md)  
[ICE67](ice67.md)  
[ICE76](ice76.md)  
[ICE79](ice79.md)  
[ICE80](ice80.md)  
[ICE83](ice83.md)  
[ICE86](ice86.md)  
[ICE88](ice88.md)  
[ICE91](ice91.md)  
[ICE92](ice92.md)  
[ICE97](ice97.md)  
</dl>

