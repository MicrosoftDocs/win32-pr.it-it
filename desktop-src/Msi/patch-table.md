---
description: La tabella Patch specifica il file che deve ricevere una particolare patch e il percorso fisico dei file patch nelle immagini dei supporti.
ms.assetid: 1b624702-de25-4b1a-9dac-21f359ee97f7
title: Tabella patch
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a9e5f41f206557589bf0b90d9ffb125a80d05d39ce809dc01a8e687a21045475
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119558461"
---
# <a name="patch-table"></a>Tabella patch

La tabella Patch specifica il file che deve ricevere una particolare patch e il percorso fisico dei file patch nelle immagini dei supporti.

La tabella Patch contiene le colonne seguenti.



| Colonna      | Tipo                               | Chiave | Nullable |
|-------------|------------------------------------|-----|----------|
| file\_      | [Identificatore](identifier.md)       | S   | N        |
| Sequenza    | [Integer](integer.md)             | S   | N        |
| PatchSize   | [DoubleInteger](doubleinteger.md) | N   | N        |
| Attributi  | [Integer](integer.md)             | N   | N        |
| Intestazione      | [Binario](binary.md)               | N   | S        |
| StreamRef\_ | [Identificatore](identifier.md)       | N   | S        |



 

## <a name="columns"></a>Colonne

<dl> <dt>

<span id="File_"></span><span id="file_"></span><span id="FILE_"></span>File\_
</dt> <dd>

La patch viene applicata al file specificato dall'identificatore in questa colonna. Si tratta di una chiave primaria per la tabella ed è una chiave esterna per la [tabella File](file-table.md).

</dd> <dt>

<span id="Sequence"></span><span id="sequence"></span><span id="SEQUENCE"></span>Sequenza
</dt> <dd>

Si tratta della posizione del file di patch nell'ordine di sequenza dei file nelle immagini multimediali. L'ordine di sequenza deve corrispondere all'ordine dei file nel file CAB del pacchetto patch. Si tratta di una chiave primaria per questa tabella. Il limite massimo è 32767 file. Per creare un pacchetto di Windows Installer con più file, vedere Creazione di un pacchetto [di grandi dimensioni.](authoring-a-large-package.md)

</dd> <dt>

<span id="PatchSize"></span><span id="patchsize"></span><span id="PATCHSIZE"></span>PatchSize
</dt> <dd>

Questa colonna indica le dimensioni della patch in byte scritti come long integer.

</dd> <dt>

<span id="Attributes"></span><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributi
</dt> <dd>

Intero contenente flag di bit che rappresentano gli attributi patch. Inserire il valore 1 in questa colonna per indicare che l'errore di applicazione della patch non è irreversibile.



| Costante                         | Valore esadecimale | Decimal | Descrizione                                                          |
|----------------------------------|-------------|---------|----------------------------------------------------------------------|
| (nessuna)                           | 0x000       | 0       | La mancata applicazione di questa patch è un errore irreversibile.                        |
| **msidbPatchAttributesNonVital** | 0x001       | 1       | Indica che l'errore di applicazione della patch non è irreversibile. |



 

</dd> <dt>

<span id="Header"></span><span id="header"></span><span id="HEADER"></span>Intestazione
</dt> <dd>

Questa colonna è l'intestazione della patch del flusso binario usata per la convalida delle patch. Questa colonna deve essere Null se la colonna StreamRef \_ non è Null. In questo caso, il flusso di intestazione della patch viene archiviato nella tabella [MsiPatchHeaders](msipatchheaders-table.md) per superare la limitazione del nome del flusso descritta in [Limitazioni OLE Flussi](ole-limitations-on-streams.md).

</dd> <dt>

<span id="StreamRef_"></span><span id="streamref_"></span><span id="STREAMREF_"></span>StreamRef\_
</dt> <dd>

Chiave esterna nella tabella MsiPatchHeaders che specifica la riga che contiene il flusso di intestazione patch.

</dd> </dl>

## <a name="remarks"></a>Commenti

Questa tabella viene elaborata [dall'azione PatchFiles](patchfiles-action.md). Viene in genere aggiunto al pacchetto di installazione da una trasformazione da un pacchetto patch. In genere non viene creato direttamente in un pacchetto di installazione.

## <a name="validation"></a>Convalida

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE29](ice29.md)  
[ICE45](ice45.md)  
</dl>

 

 



