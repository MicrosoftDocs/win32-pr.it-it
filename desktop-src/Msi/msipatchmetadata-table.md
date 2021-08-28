---
description: La tabella MsiPatchMetadata contiene informazioni su una patch Windows Installer necessaria per rimuovere la patch e che viene usata da Installazione applicazioni.
ms.assetid: b1c30e16-6c91-451a-8b75-7ddbcefcc092
title: Tabella MsiPatchMetadata
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ee71e25bf04a39d8d360c5977fad7ec72a8924b
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122469168"
---
# <a name="msipatchmetadata-table"></a>Tabella MsiPatchMetadata

La tabella MsiPatchMetadata contiene informazioni su una patch Windows Installer necessaria per rimuovere la patch e che viene usata da Installazione **applicazioni**.

Le patch installate senza questa tabella presente nel database delle patch (file con estensione msp) non possono essere rimosse e mancano alcune informazioni da Installazione **applicazioni**. La tabella deve essere nel database del file di patch e non in una trasformazione nella patch.

La tabella MsiPatchMetadata include le colonne seguenti.



| Colonna   | Tipo                         | Chiave | Nullable |
|----------|------------------------------|-----|----------|
| Company  | [Identificatore](identifier.md) | S   | S        |
| Proprietà | [Identificatore](identifier.md) | S   | N        |
| valore    | [Text](text.md)             | N   | N        |



 

## <a name="columns"></a>Colonne

<dl> <dt>

<span id="Company"></span><span id="company"></span><span id="COMPANY"></span>Azienda
</dt> <dd>

Nome della società. Un campo vuoto (valore Null) indica che la riga contiene una delle proprietà dei metadati standard del Windows Installer. Per altre informazioni, vedere la sezione Osservazioni di questo argomento.

Aggiungendo una riga alla tabella e immettendo il nome di una società in questo campo, è possibile aggiungere qualsiasi società per estendere il set di proprietà.

</dd> <dt>

<span id="Property"></span><span id="property"></span><span id="PROPERTY"></span>Proprietà
</dt> <dd>

Nome di una proprietà di metadati.

</dd> <dt>

<span id="Value"></span><span id="value"></span><span id="VALUE"></span>Valore
</dt> <dd>

Valore della proprietà dei metadati. Non può mai essere Null o una stringa vuota.

</dd> </dl>

## <a name="remarks"></a>Commenti

Disponibile in Windows Installer 3.0 e versioni successive.

Le righe nella tabella MsiPatchMetadata che contengono un valore Null nel campo CompanyName fanno riferimento a una delle proprietà dei metadati Windows installer standard seguenti.




| Proprietà | Descrizione | 
|----------|-------------|
| AllowRemoval | Indica se la patch è una patch <a href="uninstallable-patches.md">disinstallabile.</a> Se il campo del valore contiene 0 (zero), la patch non può essere rimossa. Se il campo del valore contiene una (1), la patch è una patch disinstallabile. Questa proprietà è registrata e il relativo valore può essere ottenuto usando la <a href="/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa"><strong>funzione MsiGetPatchInfoEx.</strong></a> <br /> | 
| ManufacturerName | Nome del produttore dell'applicazione. | 
| MinorUpdateTargetRTM | Indica che la patch è destinata alla versione RTM del prodotto o alla patch di aggiornamento principale più recente. Creare questa proprietà facoltativa nelle patch di aggiornamento secondarie che contengono informazioni di sequenziazione per indicare che la patch rimuove tutte le patch fino alla versione RTM del prodotto o fino alla patch di aggiornamento principale più recente. Questa proprietà è disponibile in Windows Installer 3.1 e versioni successive. <br /> | 
| TargetProductName | Nome dell'applicazione o del gruppo di applicazioni di destinazione. | 
| MoreInfoURL | URL che fornisce informazioni specifiche per questa patch. Questa proprietà è registrata e il relativo valore può essere ottenuto usando la <a href="/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa"><strong>funzione MsiGetPatchInfoEx.</strong></a> A partire Windows XP con Service Pack 2 (SP2), questo valore può essere il collegamento di supporto per la patch visualizzata in Installazione <strong>applicazioni</strong>.<br /> | 
| CreationTimeUTC | Ora di creazione del file msp sotto forma di mm-gg-aa HH:MM (mese-giorno-anno ora:minuto). | 
| DisplayName | Titolo per la patch che è possibile visualizzare pubblicamente. Questa proprietà è registrata e il relativo valore può essere ottenuto usando la <a href="/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa"><strong>funzione MsiGetPatchInfoEx.</strong></a> A partire Windows XP con SP2, questo valore è il nome della patch visualizzata in Installazione <strong>applicazioni</strong>.<br /> | 
| Descrizione | Breve descrizione della patch. | 
| Classificazione | Valore stringa che contiene la categoria arbitraria di aggiornamenti definita dall'autore della patch. Ad esempio, gli autori di patch possono specificare che ogni patch deve essere classificata come hotfix, rollup della sicurezza, aggiornamento critico, aggiornamento, Service Pack o aggiornamento cumulativo. Questa proprietà è obbligatoria. | 
| OptimizeCA | Indica se il programma di Windows deve ignorare le azioni personalizzate durante l'applicazione della patch. In questo modo è possibile ridurre il tempo necessario per applicare la patch. La proprietà OptimizeCA può avere uno dei valori seguenti:<br /><ul><li>0 : non ignorare le azioni personalizzate.</li><li>1 - Ignorare le azioni personalizzate di assegnazione di directory e proprietà. <a href="custom-action-type-35.md">Il tipo di azione personalizzata 35</a> e il tipo di azione <a href="custom-action-type-51.md">personalizzata 51</a> possono essere azioni personalizzate di assegnazione di proprietà e directory.</li><li>2 - Ignorare le azioni personalizzate immediate che non rientrano nelle assegnazioni di proprietà o directory. Le azioni personalizzate immediate non includono l'opzione msidbCustomActionTypeInScript nella colonna Tipo della <a href="customaction-table.md">tabella CustomAction</a>.</li><li>4 - Ignorare le azioni personalizzate eseguite all'interno dello script.</li></ul>Il valore di OptimizeCA deve essere lo stesso per tutte le patch installate o non viene ignorata alcuna azione personalizzata. Ad esempio, se vengono installate due patch e OptimizeCA è impostato rispettivamente sui valori 1 e 2, non viene ignorata alcuna azione personalizzata. <br /> I valori di OptimizeCA possono essere combinati durante l'elaborazione di più nuove patch. Se tutte le patch hanno un valore 1 (uno) incluso nei valori, tutte le azioni personalizzate di assegnazione di proprietà e directory vengono ignorate. Se una patch ha il valore 3 (tre) per la proprietà e una patch ha il valore 1 (uno) per la proprietà, le azioni personalizzate di assegnazione di directory e proprietà vengono ignorate. Tuttavia, le altre azioni personalizzate immediate vengono eseguite, perché non tutte le patch richieste vengono ignorate. <br /> | 
| OptimizedInstallMode | Se questa proprietà è impostata su 1 (una) in tutte le patch da applicare in una transazione, un'applicazione della patch viene ottimizzata, se possibile. Per altre informazioni, vedere <a href="patch-optimization.md">Ottimizzazione delle patch.</a> Disponibile a partire da Windows Installer 3.1. | 




 

## <a name="validation"></a>Convalida

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
</dl>

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Non supportato in Windows Installer 2.0 e versioni precedenti](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




