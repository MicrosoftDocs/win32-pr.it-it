---
description: La tabella TargetImages contiene informazioni sulle immagini di destinazione del prodotto. Un Windows di patch del programma di installazione aggiorna un'immagine di destinazione in un'immagine aggiornata.
ms.assetid: 4681715e-9918-4d7b-8f33-1cca2bb34eb7
title: Tabella TargetImages (Patchwiz.dll)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec35a9090f89e93e807cda9429ae48d8cc28d175acc4c83e97150e3a98ce5fb3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119893591"
---
# <a name="targetimages-table-patchwizdll"></a>Tabella TargetImages (Patchwiz.dll)

La tabella TargetImages contiene informazioni sulle immagini di destinazione del prodotto. Un Windows di patch del programma di installazione aggiorna un'immagine di destinazione in un'immagine aggiornata.

In ogni database di creazione delle patch (file con estensione pcp) è necessaria una tabella TargetImages contenente almeno un record. Questa tabella viene usata dalla [funzione UiCreatePatchPackage.](uicreatepatchpackage-patchwiz-dll-.md)

La tabella TargetImages include le colonne seguenti.



| Colonna                | Tipo    | Chiave | Nullable |
|-----------------------|---------|-----|----------|
| Destinazione                | text    | S   | N        |
| MsiPath               | text    |     | N        |
| SymbolPaths           | text    |     | S        |
| Aggiornato              | text    |     | N        |
| JSON                 | numero intero |     | N        |
| ProductValidateFlags  | text    |     | S        |
| IgnoreMissingSrcFiles | numero intero |     | N        |



 

## <a name="columns"></a>Colonne

<dl> <dt>

<span id="Target"></span><span id="target"></span><span id="TARGET"></span>bersaglio
</dt> <dd>

Identificatore per un'immagine di destinazione. Il pacchetto patch aggiorna l'immagine di destinazione specificata in questa colonna all'immagine aggiornata specificata nella colonna Aggiornato. Sono disponibili una o più immagini di destinazione per ogni immagine aggiornata. L'immagine di destinazione deve essere un'immagine di installazione completamente non compressa del prodotto, ad esempio un'immagine amministrativa o un'immagine di installazione non compressa in un CD-ROM. Si noti che [la funzione UiCreatePatchPackageEx](uicreatepatchpackageex--patchwiz-dll-.md) non genera patch binarie per i file in archivi. Il valore in questo campo viene usato con il valore nel campo Aggiornato per generare i nomi delle trasformazioni aggiunte dal programma di installazione al pacchetto di patch.

</dd> <dt>

<span id="MsiPath"></span><span id="msipath"></span><span id="MSIPATH"></span>MsiPath
</dt> <dd>

Questo campo specifica il percorso completo, incluso il nome del file, del percorso .msi file per l'immagine di destinazione. Si tratta del percorso dei file di origine per l'immagine di destinazione.

</dd> <dt>

<span id="SymbolPaths"></span><span id="symbolpaths"></span><span id="SYMBOLPATHS"></span>SymbolPaths
</dt> <dd>

Elenco delimitato da punti e virgola di cartelle in cui cercare i file di simboli che possono essere usati per ottimizzare la generazione della patch binaria. Si noti che le sottodirectory delle cartelle specificate in questo campo non vengono cercate. Una patch binaria ottimizzata può essere più piccola. Microsoft Visual C++ essere installato nel computer che genera la patch e usato per creare i file di simboli. Questo campo è facoltativo e il programma di installazione crea una patch binaria anche se non viene specificato alcun file di simboli o se i file di simboli non sono più Patchwiz.dll.

</dd> <dt>

<span id="Upgraded"></span><span id="upgraded"></span><span id="UPGRADED"></span>Aggiornato
</dt> <dd>

Chiave esterna per la colonna Upgraded della [tabella UpgradedImages](upgradedimages-table-patchwiz-dll-.md). La [funzione UiCreatePatchPackageEx](uicreatepatchpackageex--patchwiz-dll-.md) ignora qualsiasi immagine aggiornata a cui non fa riferimento almeno un record della tabella TargetImages.

</dd> <dt>

<span id="Order"></span><span id="order"></span><span id="ORDER"></span>Ordine
</dt> <dd>

Ordine relativo dell'immagine di destinazione. Poiché è possibile applicare patch a più destinazioni a un'immagine aggiornata, il campo Order (Ordine) consente di sequenziare le trasformazioni nell'elenco delle trasformazioni patch. In genere, l'ordine è dall'immagine meno recente alla più recente.

</dd> <dt>

<span id="ProductValidateFlags"></span><span id="productvalidateflags"></span><span id="PRODUCTVALIDATEFLAGS"></span>ProductValidateFlags
</dt> <dd>

Il campo ProductValidateFlags viene usato per specificare il controllo del prodotto per evitare di applicare trasformazioni irrilevanti. Il valore immesso in questo campo deve essere un numero intero esadecimale di 8 cifre e uno dei valori validi per il *parametro iValidation* della [**funzione MsiCreateTransformSummaryInfo.**](/windows/desktop/api/Msiquery/nf-msiquery-msicreatetransformsummaryinfoa) Il valore predefinito è 0x00000922 uguale a **MSITRANSFORM \_ VALIDATE \_ UPDATEVERSION**  +  **MSITRANSFORM \_ VALIDATE \_ NEWEQUALBASEVERSION**  +  **MSITRANSFORM \_ VALIDATE \_ UPGRADECODE**  +  **MSITRANSFORM \_ VALIDATE \_ PRODUCT**.

</dd> <dt>

<span id="IgnoreMissingSrcFiles"></span><span id="ignoremissingsrcfiles"></span><span id="IGNOREMISSINGSRCFILES"></span>IgnoreMissingSrcFiles
</dt> <dd>

Se questo campo è impostato su un valore diverso da zero, i file mancanti nell'immagine di destinazione vengono ignorati dal programma di installazione e lasciati invariati durante l'applicazione delle patch. In questo modo è possibile applicare patch senza richiedere l'intera immagine. sono necessari solo i file modificati del prodotto e .msi file. Ciò può ridurre il tempo necessario per generare la patch.

> [!Note]  
> Non usare il valore IgnoreMissingSrcFiles con TrustMsi impostato su 1 nella [tabella delle proprietà](properties-table-patchwiz-dll-.md).

 

</dd> </dl>

## <a name="remarks"></a>Commenti

Questa tabella accetta le variabili di ambiente come percorsi che iniziano con la versione 4.0 Patchwiz.dll.

 

 



