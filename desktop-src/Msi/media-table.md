---
description: La tabella Supporti descrive il set di dischi che costituiscono il supporto di origine per l'installazione.
ms.assetid: f9789f1d-35bf-40d6-9724-d5a160a0d06d
title: Tabella supporti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29939553e64fb6558aa6480fb69b7beab208a4ccb3e2c9ce55c4d8fcbfc18cc9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117805096"
---
# <a name="media-table"></a>Tabella supporti

La tabella Supporti descrive il set di dischi che costituiscono il supporto di origine per l'installazione.

La tabella Media contiene le colonne mostrate nella tabella seguente.



| Colonna       | Tipo                     | Chiave | Nullable |
|--------------|--------------------------|-----|----------|
| DiskId       | [Integer](integer.md)   | S   | N        |
| LastSequence | [Integer](integer.md)   | N   | N        |
| DiskPrompt   | [Text](text.md)         | N   | S        |
| armadietto      | [armadietto](cabinet.md)   | N   | S        |
| VolumeLabel  | [Text](text.md)         | N   | S        |
| Source (Sorgente)       | [Proprietà](property.md) | N   | S        |



 

## <a name="columns"></a>Colonne

<dl> <dt>

<span id="DiskId"></span><span id="diskid"></span><span id="DISKID"></span>DiskId
</dt> <dd>

Determina l'ordinamento per la tabella. Questo numero deve essere uguale o maggiore di 1.

</dd> <dt>

<span id="LastSequence"></span><span id="lastsequence"></span><span id="LASTSEQUENCE"></span>LastSequence
</dt> <dd>

Numero di sequenza del file per l'ultimo file per questo supporto. I numeri nella colonna LastSequence specificano quali file della tabella [File](file-table.md) si trovano in un disco di origine specifico. Ogni disco di origine contiene tutti i file con numeri di sequenza (come illustrato nella colonna Sequenza della tabella File) minore o uguale al valore nella colonna LastSequence e maggiore del valore LastSequence del disco precedente (o maggiore di 0, per la prima voce della tabella Media). Questo numero deve essere non negativo. il limite massimo è 32767 file. Per altre informazioni sulla creazione di un pacchetto Windows Installer con più file, vedere [Creazione di un pacchetto di grandi dimensioni.](authoring-a-large-package.md)

</dd> <dt>

<span id="DiskPrompt"></span><span id="diskprompt"></span><span id="DISKPROMPT"></span>DiskPrompt
</dt> <dd>

Nome del disco, che in genere è il testo visibile stampato sul disco. Questo testo localizzabile viene usato per richiedere all'utente quando è necessario inserire questo disco.

</dd> <dt>

<span id="Cabinet"></span><span id="cabinet"></span><span id="CABINET"></span>armadietto
</dt> <dd>

Nome del file CAB se alcuni o tutti i file archiviati nel supporto vengono compressi in un file CAB. Se non viene usato alcun cabinet, questa colonna deve essere vuota. Il nome dell'cabinet deve usare la sintassi del [tipo di dati Cabinet.](cabinet.md) Windows Il programma di installazione richiede sempre un'origine valida per ripristinare i file inclusi nei file CAB incorporati. Quando Windows programma di installazione installa un pacchetto contenente un file CAB incorporato, una copia del file CAB può essere salvata dal sistema. Questa copia non può essere usata per ripristinare il file CAB. Per risparmiare spazio su disco, usare file CAB esterni anziché file CAB incorporati.

</dd> <dt>

<span id="VolumeLabel"></span><span id="volumelabel"></span><span id="VOLUMELABEL"></span>VolumeLabel
</dt> <dd>

Etichetta attribuita al volume. Si tratta dell'etichetta di volume restituita [**dalla funzione GetVolumeInformation.**](/windows/win32/api/fileapi/nf-fileapi-getvolumeinformationa) Se la proprietà [**SourceDir**](sourcedir.md) fa riferimento a un volume rimovibile (floppy o CD-ROM), questa etichetta di volume viene usata per verificare che il disco appropriato si trova nell'unità prima di provare a installare i file. La voce in questa colonna deve corrispondere all'etichetta di volume del supporto fisico.

</dd> <dt>

<span id="Source"></span><span id="source"></span><span id="SOURCE"></span>fonte
</dt> <dd>

Questo campo viene usato solo dall'applicazione di patch e in caso contrario viene lasciato vuoto. Una trasformazione patch può immettere qui una proprietà che rappresenta il percorso del file CAB contenente i file di patch o i nuovi file aggiunti dalla patch. È necessario specificare un'origine diversa per questi file perché l'origine del pacchetto di patch può essere archiviata separatamente dall'origine del prodotto. Se il campo Cabinet è vuoto, il programma di installazione ignora il valore in questa colonna. Se questo campo è vuoto, il programma di installazione usa il valore della [**proprietà SourceDir**](sourcedir.md) come origine del file CAB.

</dd> </dl>

## <a name="remarks"></a>Commenti

Se il nome dell'archivio è preceduto da un simbolo di numero ( ), i file che fanno riferimento a questo record della tabella Media vengono archiviati in un file CAB archiviato all'interno del database come \# flusso separato.

Per altre informazioni su come aggiungere file CAB alle tabelle File e Media, vedere [Using Cabinets and Compressed Sources](using-cabinets-and-compressed-sources.md).

Windows Il programma di installazione richiede .msi file di installazione sul primo disco dei supporti rimovibili (CD, DVD o floppy) usati per l'installazione del prodotto.

**Determinazione di SourceMode**

La [**proprietà Riepilogo conteggio**](word-count-summary.md) parole determina la modalità di origine per l'installazione corrente. Se questa proprietà è impostata su 2 o 3, viene utilizzata un'installazione cab. In questa modalità si presuppone che i file CAB esistano nella directory indicata dalla [**proprietà SourceDir.**](sourcedir.md) Se il valore di Tipo di origine è 0 o 1, si presuppone che tutti i file di origine esistano nell'albero la cui radice è indicata dalla **proprietà SourceDir.**

Si noti che questo si applica solo ai file nella tabella File per i cui bit compressi o non compressi non sono impostati nella colonna attributes. Questi bit eseguono l'override del valore [**della proprietà Riepilogo**](word-count-summary.md) conteggio parole quando determinano se un determinato file è compresso o non compresso.

## <a name="validation"></a>Convalida

<dl>

[ICE03](ice03.md)  
[ICE04](ice04.md)  
[ICE06](ice06.md)  
[ICE35](ice35.md)  
[ICE58](ice58.md)  
[ICE71](ice71.md)  
[ICE81](ice81.md)  
</dl>

 

 
