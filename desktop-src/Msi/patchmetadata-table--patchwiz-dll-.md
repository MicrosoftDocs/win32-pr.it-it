---
description: La tabella PatchMetadata contiene informazioni su una patch Windows installer necessaria per rimuovere una patch e che viene usata da Installazione applicazioni.
ms.assetid: 09a06de4-0713-4e92-ab29-f34f6c94b677
title: Tabella PatchMetadata (PATCHWIZ.DLL)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af760fbe286cf37cdb3aefe389ee8d09d7a759d3
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122475447"
---
# <a name="patchmetadata-table-patchwizdll"></a>Tabella PatchMetadata (PATCHWIZ.DLL)

La tabella PatchMetadata contiene informazioni su una patch Windows installer necessaria per rimuovere una patch e che viene usata da Installazione applicazioni. Tutte le proprietà nella tabella PatchMetadata vengono aggiunte alla tabella [MsiPatchMetadata](msipatchmetadata-table.md) del file con estensione msp per una patch.

La tabella PatchMetadata è necessaria nei file delle proprietà di creazione delle patch (file con estensione pcp) con minimumRequiredMsiVersion uguale a 300 nella tabella [delle proprietà](properties-table-patchwiz-dll-.md). La tabella è facoltativa se MinimumRequiredMsiVersion non è uguale a 300.

La tabella PatchMetadata include le colonne seguenti.



| Colonna   | Tipo | Chiave | Nullable |
|----------|------|-----|----------|
| Company  | text | S   | S        |
| Proprietà | text | S   | N        |
| valore    | text |     | S        |



 

### <a name="columns"></a>Colonne

<dl> <dt>

<span id="Company"></span><span id="company"></span><span id="COMPANY"></span>Azienda
</dt> <dd>

Nome della società. Un campo vuoto (valore Null) indica che questa riga contiene una delle proprietà dei metadati standard. Una società può estendere il set di proprietà aggiungendo una riga alla tabella e immettendo il nome di una società in questo campo.

</dd> <dt>

<span id="Property"></span><span id="property"></span><span id="PROPERTY"></span>Proprietà
</dt> <dd>

Nome di una proprietà di metadati. Le proprietà AllowRemoval, ManufacturerName, TargetProductName, MoreInfoURL, DisplayName, Description e Classification sono obbligatorie nella tabella PatchMetadata . Questo campo deve contenere una delle proprietà di metadati standard seguenti se il campo Company è vuoto (valore Null).




| Proprietà | Descrizione | 
|----------|-------------|
| AllowRemoval | Valore intero che indica se la patch è una patch <a href="uninstallable-patches.md">disinstallabile.</a> Se il campo Valore contiene 0 (zero), la patch non può essere rimossa. Se il campo Valore contiene 1 (uno), la patch è una patch disinstallabile. Questa proprietà è obbligatoria. Questa proprietà è registrata e il relativo valore può essere ottenuto usando la <a href="/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa"><strong>funzione MsiGetPatchInfoEx.</strong></a><br /> | 
| ManufacturerName | Valore stringa contenente il nome del produttore dell'applicazione. Questa proprietà è obbligatoria. | 
| MinorUpdateTargetRTM | Indica che la patch è destinata alla versione RTM del prodotto o alla patch di aggiornamento principale più recente. Creare questa proprietà facoltativa nelle patch di aggiornamento secondarie che contengono informazioni di sequenziazione per indicare che la patch rimuove tutte le patch fino alla versione RTM del prodotto o fino alla patch di aggiornamento principale più recente. Questa proprietà è disponibile a partire da Windows Installer 3.1.<blockquote>[!Note]<br />Per richiedere che Windows Installer 3.1 sia installato per applicare la patch, impostare la proprietà MinimumRequiredMsiVersion su 310 nella tabella delle proprietà del file con estensione pcp. <a href="properties-table-patchwiz-dll-.md"></a></blockquote><br /><br /> | 
| TargetProductName | Valore stringa che contiene il nome dell'applicazione o del gruppo di applicazioni di destinazione. Questa proprietà è obbligatoria. | 
| MoreInfoURL | Valore stringa che contiene un URL che punta alle informazioni per questa patch. Questa proprietà obbligatoria viene registrata e il relativo valore può essere ottenuto usando la <a href="/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa"><strong>funzione MsiGetPatchInfoEx.</strong></a> A partire Windows XP con Service Pack 2 (SP2), questo valore può essere il collegamento di supporto per la patch visualizzata in Installazione applicazioni.<br /> | 
| CreationTimeUTC | Valore stringa che contiene l'ora di creazione del file msp nel formato mm-gg-yy HH:MM (mese-giorno-anno ora:minuto). Questa proprietà è facoltativa. | 
| DisplayName | Valore stringa che contiene il titolo della patch adatto per la visualizzazione pubblica. Questa proprietà è obbligatoria. Questa proprietà è registrata e il relativo valore può essere ottenuto usando la <a href="/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa"><strong>funzione MsiGetPatchInfoEx.</strong></a> A partire da Windows XP con SP2, questo valore è il nome della patch visualizzata in Installazione applicazioni a partire da Windows XP con SP2.<br /> | 
| Descrizione | Valore stringa che contiene una breve descrizione della patch. Questa proprietà è obbligatoria. | 
| Classificazione | Valore stringa che contiene la categoria arbitraria di aggiornamenti definita dall'autore della patch. Ad esempio, gli autori di patch possono specificare che ogni patch deve essere classificata come hotfix, rollup della sicurezza, aggiornamento critico, aggiornamento, Service Pack o aggiornamento cumulativo. Questa proprietà è obbligatoria. | 
| OptimizedInstallMode | Se questa proprietà è impostata su 1 (una) in tutte le patch da applicare in una transazione, l'applicazione della patch viene ottimizzata, se possibile. Per informazioni, vedere <a href="patch-optimization.md">Ottimizzazione delle patch.</a> Disponibile a partire da Windows Installer 3.1. | 




 

</dd> <dt>

<span id="Value"></span><span id="value"></span><span id="VALUE"></span>Valore
</dt> <dd>

Valore della proprietà dei metadati. Non può mai essere Null o una stringa vuota. Questo valore può essere localizzato.

</dd> </dl>

### <a name="remarks"></a>Commenti

Disponibile a partire da Windows Installer 3.0.

Tutte le proprietà scritte nella tabella PatchMetadata vengono aggiunte alla tabella MsiPatchMetadata del file msp. Le proprietà AllowRemoval, MoreInfoURL e DisplayName sono registrate e sono accessibili tramite [**MsiGetPatchInfoEx**](/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa).

 

 




