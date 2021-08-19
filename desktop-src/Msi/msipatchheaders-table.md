---
description: La tabella MsiPatchHeaders contiene i flussi di intestazione di patch binari usati per la convalida delle patch.
ms.assetid: aefdd365-1681-43e4-8470-04a5d6efd993
title: Tabella MsiPatchHeaders
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1888a91da13923c4a9904c770df77cb24a5b8381c869a60895bb5ff49d23e6b1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118944494"
---
# <a name="msipatchheaders-table"></a>Tabella MsiPatchHeaders

La tabella MsiPatchHeaders contiene i flussi di intestazione di patch binari usati per la convalida delle patch.

La tabella MsiPatchHeaders viene usata quando le chiavi lunghe della tabella [File](file-table.md) causano un errore durante la generazione del flusso di intestazione patch nella [tabella Patch](patch-table.md). Ciò può essere dovuto alla limitazione del nome del flusso descritta in [Limitazioni OLE Flussi](ole-limitations-on-streams.md). In questo caso, la tabella Patch può fare riferimento alla tabella MsiPatchHeaders per creare il flusso di intestazione patch.

La tabella MsiPatchHeaders include le colonne seguenti.



| Colonna    | Tipo                         | Chiave | Nullable |
|-----------|------------------------------|-----|----------|
| StreamRef | [Identificatore](identifier.md) | S   | N        |
| Intestazione    | [Binario](binary.md)         | N   | N        |



 

## <a name="columns"></a>Colonne

<dl> <dt>

<span id="StreamRef"></span><span id="streamref"></span><span id="STREAMREF"></span>StreamRef
</dt> <dd>

Chiave primaria per la tabella che identifica in modo univoco una particolare intestazione di patch.

</dd> <dt>

<span id="Header"></span><span id="header"></span><span id="HEADER"></span>Intestazione
</dt> <dd>

Questa colonna è l'intestazione della patch del flusso binario usata per la convalida delle patch.

</dd> </dl>

## <a name="remarks"></a>Commenti

Questa tabella viene elaborata [dall'azione PatchFiles](patchfiles-action.md). Questa tabella viene in genere aggiunta al pacchetto di installazione da una trasformazione da un pacchetto patch. In genere non viene creato direttamente in un pacchetto di installazione.

## <a name="validation"></a>Convalida

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE29](ice29.md)  
</dl>

 

 



