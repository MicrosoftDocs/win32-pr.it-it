---
description: La tabella TargetImages contiene informazioni sulle immagini di destinazione del prodotto. Un pacchetto Windows Installer patch aggiorna un'immagine di destinazione in un'immagine aggiornata.
ms.assetid: 4681715e-9918-4d7b-8f33-1cca2bb34eb7
title: Tabella TargetImages (Patchwiz.dll)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4bbb8e7bae92fbc25b217808aaae709f079d65dd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103885094"
---
# <a name="targetimages-table-patchwizdll"></a>Tabella TargetImages (Patchwiz.dll)

La tabella TargetImages contiene informazioni sulle immagini di destinazione del prodotto. Un pacchetto Windows Installer patch aggiorna un'immagine di destinazione in un'immagine aggiornata.

Una tabella TargetImages contenente almeno un record è obbligatoria in ogni database di creazione della patch (file con estensione PCP). Questa tabella viene utilizzata dalla funzione [UiCreatePatchPackage](uicreatepatchpackage-patchwiz-dll-.md) .

La tabella TargetImages include le colonne seguenti.



| Colonna                | Tipo    | Chiave | Nullable |
|-----------------------|---------|-----|----------|
| Destinazione                | text    | S   | N        |
| PercorsoMSI               | text    |     | N        |
| SymbolPaths           | text    |     | S        |
| Aggiornato              | text    |     | N        |
| JSON                 | numero intero |     | N        |
| ProductValidateFlags  | text    |     | S        |
| IgnoreMissingSrcFiles | numero intero |     | N        |



 

## <a name="columns"></a>Colonne

<dl> <dt>

<span id="Target"></span><span id="target"></span><span id="TARGET"></span>Destinazione
</dt> <dd>

Identificatore per un'immagine di destinazione. Il pacchetto patch aggiorna l'immagine di destinazione specificata in questa colonna all'immagine aggiornata specificata nella colonna aggiornata. Per ogni immagine aggiornata sono disponibili una o più immagini di destinazione. L'immagine di destinazione deve essere un'immagine di configurazione completamente non compressa del prodotto, ad esempio un'immagine amministrativa o un'immagine di installazione non compressa in un CD-ROM. Si noti che la funzione [UiCreatePatchPackageEx](uicreatepatchpackageex--patchwiz-dll-.md) non genera patch binarie per i file nei file CAB. Il valore di questo campo viene usato con il valore nel campo aggiornato per generare i nomi delle trasformazioni che il programma di installazione aggiunge al pacchetto di patch.

</dd> <dt>

<span id="MsiPath"></span><span id="msipath"></span><span id="MSIPATH"></span>PercorsoMSI
</dt> <dd>

Questo campo specifica il percorso completo, incluso il nome del file, al percorso del file con estensione msi per l'immagine di destinazione. Si tratta del percorso dei file di origine per l'immagine di destinazione.

</dd> <dt>

<span id="SymbolPaths"></span><span id="symbolpaths"></span><span id="SYMBOLPATHS"></span>SymbolPaths
</dt> <dd>

Elenco delimitato da punti e virgola di cartelle in cui cercare i file di simboli che possono essere usati per ottimizzare la generazione della patch binaria. Si noti che non viene eseguita la ricerca nelle sottodirectory delle cartelle specificate in questo campo. Una patch binaria ottimizzata può essere più piccola. Microsoft Visual C++ deve essere installato nel computer che genera la patch e utilizzato per creare i file di simboli. Questo campo è facoltativo e il programma di installazione crea una patch binaria anche se non è stato specificato alcun file di simboli o se i file di simboli non sono più disponibili per Patchwiz.dll.

</dd> <dt>

<span id="Upgraded"></span><span id="upgraded"></span><span id="UPGRADED"></span>Aggiornato
</dt> <dd>

Chiave esterna per la colonna aggiornata della [tabella UpgradedImages](upgradedimages-table-patchwiz-dll-.md). La funzione [UiCreatePatchPackageEx](uicreatepatchpackageex--patchwiz-dll-.md) ignora tutte le immagini aggiornate a cui non viene fatto riferimento da almeno un record della tabella TargetImages.

</dd> <dt>

<span id="Order"></span><span id="order"></span><span id="ORDER"></span>Ordine
</dt> <dd>

Ordine relativo dell'immagine di destinazione. Poiché è possibile applicare patch a più destinazioni a un'immagine aggiornata, il campo Order fornisce un mezzo per sequenziare le trasformazioni nell'elenco delle trasformazioni delle patch. In genere, l'ordine è dall'immagine meno recente a quella più recente.

</dd> <dt>

<span id="ProductValidateFlags"></span><span id="productvalidateflags"></span><span id="PRODUCTVALIDATEFLAGS"></span>ProductValidateFlags
</dt> <dd>

Il campo ProductValidateFlags viene usato per specificare il controllo del prodotto per evitare l'applicazione di trasformazioni irrilevanti. Il valore immesso in questo campo deve essere un Integer esadecimale a 8 cifre e uno dei valori validi per il parametro *iValidation* della funzione [**MsiCreateTransformSummaryInfo**](/windows/desktop/api/Msiquery/nf-msiquery-msicreatetransformsummaryinfoa) . Il valore predefinito è 0x00000922, che è uguale a **MSITRANSFORM \_ Validate \_ UPDATEVERSION**  +  **MSITRANSFORM \_ Validate \_ NEWEQUALBASEVERSION**  +  **MSITRANSFORM \_ Validate \_** UPGRADECODE  +  **MSITRANSFORM \_ Validate \_ Product**.

</dd> <dt>

<span id="IgnoreMissingSrcFiles"></span><span id="ignoremissingsrcfiles"></span><span id="IGNOREMISSINGSRCFILES"></span>IgnoreMissingSrcFiles
</dt> <dd>

Se questo campo è impostato su un valore diverso da zero, i file mancanti nell'immagine di destinazione vengono ignorati dal programma di installazione e rimangono invariati durante l'applicazione di patch. Ciò consente di apportare le patch senza richiedere l'intera immagine; sono necessari solo i file modificati del prodotto e il file con estensione msi. Questo può ridurre il tempo necessario per generare la patch.

> [!Note]  
> Non usare il valore IgnoreMissingSrcFiles con TrustMsi impostato su 1 nella [tabella Properties](properties-table-patchwiz-dll-.md).

 

</dd> </dl>

## <a name="remarks"></a>Commenti

Questa tabella accetta le variabili di ambiente come percorsi che iniziano con la versione 4,0 di Patchwiz.dll.

 

 



