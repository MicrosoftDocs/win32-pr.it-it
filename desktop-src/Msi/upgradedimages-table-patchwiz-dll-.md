---
description: La tabella UpgradedImages contiene informazioni sulle immagini aggiornate del prodotto.
ms.assetid: f4ee2cc8-8a49-4e4a-b8cf-b4ae2bc7e753
title: Tabella UpgradedImages (Patchwiz.dll)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48dcecc94786cbe783f21e6e005b645586f2e894
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104348956"
---
# <a name="upgradedimages-table-patchwizdll"></a>Tabella UpgradedImages (Patchwiz.dll)

La tabella UpgradedImages contiene informazioni sulle immagini aggiornate del prodotto. L'immagine aggiornata deve essere un'immagine di configurazione completamente non compressa della versione più recente del prodotto, ad esempio un'immagine amministrativa o un'immagine di configurazione non compressa da un CD-ROM. Un pacchetto Windows Installer patch aggiorna un'immagine di destinazione in un'immagine aggiornata. La tabella UpgradedImages è obbligatoria nel database di creazione della patch (file con estensione PCP) e viene usata da [UiCreatePatchPackageEx](uicreatepatchpackageex--patchwiz-dll-.md).

Una tabella UpgradedImages contenente almeno un record è obbligatoria in ogni database di creazione della patch (file con estensione PCP). Questa tabella viene utilizzata da [UiCreatePatchPackageEx](uicreatepatchpackageex--patchwiz-dll-.md).

La tabella UpgradedImages include le colonne seguenti.



| Colonna       | Tipo | Chiave | Nullable |
|--------------|------|-----|----------|
| Aggiornato     | text | S   | N        |
| PercorsoMSI      | text |     | N        |
| PatchMsiPath | text |     | S        |
| SymbolPaths  | text |     | S        |
| Famiglia       | text |     | N        |



 

## <a name="columns"></a>Colonne

<dl> <dt>

<span id="Upgraded"></span><span id="upgraded"></span><span id="UPGRADED"></span>Aggiornato
</dt> <dd>

Il campo aggiornato è un identificatore arbitrario per connettere le immagini di destinazione a un'immagine aggiornata del prodotto.

</dd> <dt>

<span id="MsiPath"></span><span id="msipath"></span><span id="MSIPATH"></span>PercorsoMSI
</dt> <dd>

Questo campo specifica il percorso completo, incluso il nome del file, al percorso del file con estensione msi per l'immagine aggiornata. Si tratta del percorso dei file di origine per l'immagine aggiornata.

</dd> <dt>

<span id="PatchMsiPath"></span><span id="patchmsipath"></span><span id="PATCHMSIPATH"></span>PatchMsiPath
</dt> <dd>

Il patchMsiPath facoltativo punta a una copia modificata del database di installazione aggiornato che contiene la modifica aggiuntiva specifica per il processo di installazione della patch. Ad esempio, finestre di dialogo aggiuntive o azioni personalizzate condizionate nella proprietà [**patch**](patch.md) .

</dd> <dt>

<span id="SymbolPaths"></span><span id="symbolpaths"></span><span id="SYMBOLPATHS"></span>SymbolPaths
</dt> <dd>

Elenco delimitato da punti e virgola di cartelle in cui cercare i file di simboli che possono essere usati per ottimizzare la generazione della patch binaria. Si noti che non viene eseguita la ricerca nelle sottodirectory delle cartelle specificate in questo campo. Una patch binaria ottimizzata può essere più piccola. Visual C++ deve essere installato nel computer che genera la patch e utilizzato per creare i file di simboli. Questo campo è facoltativo e il programma di installazione crea una patch binaria anche se non è stato specificato alcun file di simboli o se i file di simboli non sono più disponibili per Patchwiz.dll.

</dd> <dt>

<span id="Family"></span><span id="family"></span><span id="FAMILY"></span>Famiglia
</dt> <dd>

Chiave esterna nella [tabella ImageFamilies](imagefamilies-table-patchwiz-dll-.md). Ogni immagine aggiornata deve appartenere a un solo gruppo.

</dd> </dl>

## <a name="remarks"></a>Commenti

Sebbene ogni immagine aggiornata possa essere raggruppata in una famiglia di immagini distinta, il raggruppamento di immagini aggiornate che condividono i file può rendere più piccolo il file con estensione msp.

Questa tabella accetta le variabili di ambiente come percorsi che iniziano con la versione 4,0 di Patchwiz.dll.

 

 



