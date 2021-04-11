---
description: La tabella media descrive il set di dischi che costituiscono il supporto di origine per l'installazione.
ms.assetid: f9789f1d-35bf-40d6-9724-d5a160a0d06d
title: Tabella supporti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a59cd8bf864aa890891873ed92a39225c6eebdf
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "104351256"
---
# <a name="media-table"></a>Tabella supporti

La tabella media descrive il set di dischi che costituiscono il supporto di origine per l'installazione.

La tabella media contiene le colonne mostrate nella tabella seguente.



| Colonna       | Tipo                     | Chiave | Nullable |
|--------------|--------------------------|-----|----------|
| DiskId       | [Integer](integer.md)   | S   | N        |
| LastSequence | [Integer](integer.md)   | N   | N        |
| DiskPrompt   | [Text](text.md)         | N   | S        |
| CAB      | [CAB](cabinet.md)   | N   | S        |
| VolumeLabel  | [Text](text.md)         | N   | S        |
| Source (Sorgente)       | [Proprietà](property.md) | N   | S        |



 

## <a name="columns"></a>Colonne

<dl> <dt>

<span id="DiskId"></span><span id="diskid"></span><span id="DISKID"></span>DiskId
</dt> <dd>

Determina il tipo di ordinamento per la tabella. Questo numero deve essere maggiore o uguale a 1.

</dd> <dt>

<span id="LastSequence"></span><span id="lastsequence"></span><span id="LASTSEQUENCE"></span>LastSequence
</dt> <dd>

Numero di sequenza del file per l'ultimo file per questo supporto. I numeri nella colonna LastSequence specificano quali file della tabella [file](file-table.md) si trovano in un determinato disco di origine. Ogni disco di origine contiene tutti i file con numeri di sequenza (come illustrato nella colonna sequenza della tabella file) minore o uguale al valore nella colonna LastSequence e maggiore del valore LastSequence del disco precedente (o maggiore di 0, per la prima voce nella tabella Media). Questo numero deve essere non negativo. il limite massimo è 32767 file. Per ulteriori informazioni sulla creazione di un pacchetto di Windows Installer con più file, vedere Creazione di [un pacchetto di grandi dimensioni](authoring-a-large-package.md).

</dd> <dt>

<span id="DiskPrompt"></span><span id="diskprompt"></span><span id="DISKPROMPT"></span>DiskPrompt
</dt> <dd>

Nome del disco, che in genere è il testo visibile stampato sul disco. Questo testo localizzabile viene usato per richiedere all'utente quando è necessario inserire il disco.

</dd> <dt>

<span id="Cabinet"></span><span id="cabinet"></span><span id="CABINET"></span>CAB
</dt> <dd>

Nome del file CAB se alcuni o tutti i file archiviati nel supporto vengono compressi in un file CAB. Se non viene utilizzato alcun cabinet, questa colonna deve essere vuota. Il nome del file CAB deve usare la sintassi del tipo di dati [CAB](cabinet.md) . Windows Installer richiede sempre un'origine valida per ripristinare i file inclusi nei file CAB incorporati. Quando Windows Installer installa un pacchetto contenente un file CAB incorporato, una copia del file CAB può essere salvata dal sistema. Non è possibile utilizzare questa copia per ripristinare il file CAB. Per conservare spazio su disco, utilizzare file CAB esterni anziché file CAB incorporati.

</dd> <dt>

<span id="VolumeLabel"></span><span id="volumelabel"></span><span id="VOLUMELABEL"></span>VolumeLabel
</dt> <dd>

Etichetta attribuita al volume. Si tratta dell'etichetta del volume restituita dalla funzione [**GetVolumeInformation**](/windows/win32/api/fileapi/nf-fileapi-getvolumeinformationa) . Se la proprietà [**SourceDir**](sourcedir.md) fa riferimento a un volume rimovibile (floppy o CD-ROM), questa etichetta del volume viene utilizzata per verificare che il disco appropriato si trovi nell'unità prima di tentare di installare i file. La voce in questa colonna deve corrispondere all'etichetta del volume del supporto fisico.

</dd> <dt>

<span id="Source"></span><span id="source"></span><span id="SOURCE"></span>Origine
</dt> <dd>

Questo campo viene usato solo con l'applicazione di patch e in caso contrario viene lasciato vuoto. Una trasformazione patch può immettere una proprietà che rappresenta il percorso del file CAB contenente i file della patch o i nuovi file aggiunti dalla patch. Per questi file è necessario specificare un'origine diversa, perché l'origine del pacchetto di patch può essere archiviata separatamente dall'origine del prodotto. Se il campo cabinet è vuoto, il programma di installazione ignorerà il valore in questa colonna. Se questo campo è vuoto, il programma di installazione usa il valore della proprietà [**SourceDir**](sourcedir.md) come origine del file CAB.

</dd> </dl>

## <a name="remarks"></a>Commenti

Se il nome del cabinet è preceduto da un simbolo di cancelletto ( \# ), i file che fanno riferimento a questo record della tabella multimediale vengono compressi in un file CAB archiviato nel database come flusso separato.

Per ulteriori informazioni su come aggiungere i file CAB alle tabelle di file e alle tabelle multimediali, vedere [utilizzo di archivi e origini compresse](using-cabinets-and-compressed-sources.md).

Windows Installer richiede che il file con estensione msi si trovi nel primo disco del supporto rimovibile (CD, DVD o floppy) usato per l'installazione del prodotto.

**Determinazione del SourceMode**

La proprietà [**riepilogo Conteggio parole**](word-count-summary.md) determina la modalità di origine per l'installazione corrente. Se questa proprietà è impostata su 2 o 3, viene utilizzata un'installazione del cabinet. In questa modalità, si presuppone che i file CAB esistano nella directory indicata dalla proprietà [**SourceDir**](sourcedir.md) . Se il valore del tipo di origine è 0 o 1, si presuppone che tutti i file di origine esistano nell'albero la cui radice è indicata dalla proprietà **SourceDir** .

Si noti che questo si applica solo ai file della tabella file che non dispongono del set di bit compresso o non compresso nella colonna attributi. Questi bit eseguono l'override del valore della proprietà [**riepilogo Conteggio parole**](word-count-summary.md) per determinare se un determinato file viene compresso o decompresso.

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

 

 
