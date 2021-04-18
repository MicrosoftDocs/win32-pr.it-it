---
description: La tabella MsiPatchMetadata contiene informazioni su una patch Windows Installer necessaria per rimuovere la patch e utilizzata da installazione applicazioni.
ms.assetid: b1c30e16-6c91-451a-8b75-7ddbcefcc092
title: Tabella MsiPatchMetadata
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2642661a8f9dc067086926f8e993fc32c95a4a85
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319007"
---
# <a name="msipatchmetadata-table"></a>Tabella MsiPatchMetadata

La tabella MsiPatchMetadata contiene informazioni su una patch Windows Installer necessaria per rimuovere la patch e utilizzata da **Installazione applicazioni**.

Non è possibile rimuovere le patch installate senza la tabella presente nel database della patch (file con estensione msp) e non sono disponibili alcune informazioni da **Installazione applicazioni**. La tabella deve trovarsi nel database del file di correzione e non in una trasformazione della patch.

La tabella MsiPatchMetadata include le colonne seguenti.



| Colonna   | Tipo                         | Chiave | Nullable |
|----------|------------------------------|-----|----------|
| Company  | [Identificatore](identifier.md) | S   | S        |
| Proprietà | [Identificatore](identifier.md) | S   | N        |
| Valore    | [Text](text.md)             | N   | N        |



 

## <a name="columns"></a>Colonne

<dl> <dt>

<span id="Company"></span><span id="company"></span><span id="COMPANY"></span>Azienda
</dt> <dd>

Nome della società. Un campo vuoto (un valore null) indica che la riga contiene una delle proprietà dei metadati standard del Windows Installer. Per ulteriori informazioni, vedere la sezione Osservazioni di questo argomento.

Aggiungendo una riga alla tabella e immettendo il nome di una società in questo campo, è possibile aggiungere qualsiasi azienda per estendere il set di proprietà.

</dd> <dt>

<span id="Property"></span><span id="property"></span><span id="PROPERTY"></span>Proprietà
</dt> <dd>

Nome di una proprietà dei metadati.

</dd> <dt>

<span id="Value"></span><span id="value"></span><span id="VALUE"></span>Valore
</dt> <dd>

Valore della proprietà dei metadati. Non può mai essere null o una stringa vuota.

</dd> </dl>

## <a name="remarks"></a>Commenti

Disponibile in Windows Installer 3,0 e versioni successive.

Le righe della tabella MsiPatchMetadata che contengono un valore null nel campo CompanyName si riferiscono a una delle seguenti proprietà standard dei metadati del Windows Installer.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Proprietà</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>AllowRemoval</td>
<td>Indica se la patch è una patch non <a href="uninstallable-patches.md">installabile</a>. Se il campo del valore contiene 0 (zero), la patch non può essere rimossa. Se il campo del valore contiene uno (1), la patch è una patch non installabile. questa proprietà è registrata e il relativo valore può essere ottenuto tramite la funzione <a href="/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa"><strong>MsiGetPatchInfoEx</strong></a> . <br/></td>
</tr>
<tr class="even">
<td>ManufacturerName</td>
<td>Nome del produttore dell'applicazione.</td>
</tr>
<tr class="odd">
<td>MinorUpdateTargetRTM</td>
<td>Indica che la patch è destinata alla versione RTM del prodotto o alla patch di aggiornamento principale più recente. Creare questa proprietà facoltativa in patch di aggiornamento secondarie che contengono informazioni di sequenziazione per indicare che la patch rimuove tutte le patch fino alla versione RTM del prodotto o fino alla patch di aggiornamento principale più recente. Questa proprietà è disponibile in Windows Installer 3,1 e versioni successive. <br/></td>
</tr>
<tr class="even">
<td>TargetProductName</td>
<td>Nome dell'applicazione o del gruppo di applicazioni di destinazione.</td>
</tr>
<tr class="odd">
<td>MoreInfoURL</td>
<td>URL che fornisce informazioni specifiche per questa patch. Questa proprietà è registrata e il relativo valore può essere ottenuto tramite la funzione <a href="/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa"><strong>MsiGetPatchInfoEx</strong></a> . A partire da Windows XP con Service Pack 2 (SP2), questo valore può essere il collegamento di supporto per la patch visualizzata in <strong>Installazione applicazioni</strong>.<br/></td>
</tr>
<tr class="even">
<td>CreationTimeUTC</td>
<td>Ora di creazione del file con estensione msp nel formato mm-DD-YY HH: MM (mese-giorno-anno ora: minuto).</td>
</tr>
<tr class="odd">
<td>DisplayName</td>
<td>Titolo per la patch che è corretto per la visualizzazione pubblica. Questa proprietà è registrata e il relativo valore può essere ottenuto tramite la funzione <a href="/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa"><strong>MsiGetPatchInfoEx</strong></a> . A partire da Windows XP con SP2, questo valore corrisponde al nome della patch visualizzata in <strong>Installazione applicazioni</strong>.<br/></td>
</tr>
<tr class="even">
<td>Descrizione</td>
<td>Breve descrizione della patch.</td>
</tr>
<tr class="odd">
<td>Classificazione</td>
<td>Valore stringa che contiene la categoria arbitraria di aggiornamenti come definito dall'autore della patch. Gli autori delle patch possono ad esempio specificare che ogni patch deve essere classificata come hotfix, rollup della sicurezza, aggiornamento critico, aggiornamento, Service Pack o aggiornamento cumulativo. Questa proprietà è obbligatoria.</td>
</tr>
<tr class="even">
<td>OptimizeCA</td>
<td>Indica se il Windows Installer deve ignorare le azioni personalizzate durante l'applicazione della patch. In questo modo è possibile ridurre il tempo necessario per applicare la patch. Il valore della proprietà OptimizeCA può essere uno dei seguenti:<br/>
<ul>
<li>0: non viene ignorata alcuna azione personalizzata.</li>
<li>1-ignorare le azioni personalizzate di assegnazione di proprietà e directory. Il <a href="custom-action-type-35.md">tipo di azione personalizzata 35</a> e il <a href="custom-action-type-51.md">tipo di azione personalizzato 51</a> possono essere azioni personalizzate di assegnazione di proprietà e directory.</li>
<li>2-ignorare le azioni personalizzate immediate che non rientrano nelle assegnazioni di proprietà o directory. Le azioni personalizzate immediate non includono l'opzione msidbCustomActionTypeInScript nella colonna Type della <a href="customaction-table.md">tabella CustomAction</a>.</li>
<li>4-ignorare le azioni personalizzate eseguite all'interno dello script.</li>
</ul>
Il valore di OptimizeCA deve essere lo stesso per tutte le patch installate o non viene ignorata alcuna azione personalizzata. Se, ad esempio, vengono installate due patch e OptimizeCA è impostato rispettivamente sui valori 1 e 2, nessuna azione personalizzata verrà ignorata. <br/> I valori di OptimizeCA possono essere combinati quando si elaborano più nuove patch. Se tutte le patch hanno un 1 (uno) incluso nei valori, tutte le azioni personalizzate di assegnazione di proprietà e directory vengono ignorate. Se una patch ha il valore 3 (tre) per la proprietà e una patch ha il valore 1 (uno) per la proprietà, le azioni personalizzate di assegnazione di directory e proprietà vengono ignorate. Tuttavia, l'altra azione personalizzata immediata viene eseguita, perché non tutte le patch richieste vengono ignorate. <br/></td>
</tr>
<tr class="odd">
<td>OptimizedInstallMode</td>
<td>Se questa proprietà è impostata su 1 (una) in tutte le patch da applicare in una transazione, un'applicazione della patch viene ottimizzata, se possibile. Per altre informazioni, vedere <a href="patch-optimization.md">ottimizzazione della patch</a>. Disponibile a partire da Windows Installer 3,1.</td>
</tr>
</tbody>
</table>



 

## <a name="validation"></a>Convalida

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
</dl>

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Non supportato in Windows Installer 2,0 e versioni precedenti](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




