---
description: La tabella MsiPatchHeaders include i flussi di intestazione della patch binaria usati per la convalida delle patch.
ms.assetid: aefdd365-1681-43e4-8470-04a5d6efd993
title: Tabella MsiPatchHeaders
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a3fa4e037a31f3e913f13ff9c96735ed6760dc4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104231863"
---
# <a name="msipatchheaders-table"></a>Tabella MsiPatchHeaders

La tabella MsiPatchHeaders include i flussi di intestazione della patch binaria usati per la convalida delle patch.

La tabella MsiPatchHeaders viene utilizzata quando le chiavi della [tabella di file](file-table.md) lunghi generano un errore durante la generazione del flusso dell'intestazione patch nella [tabella patch](patch-table.md). Questo problema può essere dovuto alla limitazione del nome del flusso descritta in [limitazioni OLE sui flussi](ole-limitations-on-streams.md). In questo caso, la tabella delle patch può fare riferimento alla tabella MsiPatchHeaders per creare il flusso dell'intestazione della patch.

La tabella MsiPatchHeaders include le colonne seguenti.



| Colonna    | Tipo                         | Chiave | Nullable |
|-----------|------------------------------|-----|----------|
| StreamRef | [Identificatore](identifier.md) | S   | N        |
| Intestazione    | [Binario](binary.md)         | N   | N        |



 

## <a name="columns"></a>Colonne

<dl> <dt>

<span id="StreamRef"></span><span id="streamref"></span><span id="STREAMREF"></span>StreamRef
</dt> <dd>

Chiave primaria per la tabella che identifica in modo univoco una particolare intestazione patch.

</dd> <dt>

<span id="Header"></span><span id="header"></span><span id="HEADER"></span>Intestazione
</dt> <dd>

Questa colonna è l'intestazione patch del flusso binario utilizzata per la convalida delle patch.

</dd> </dl>

## <a name="remarks"></a>Commenti

Questa tabella viene elaborata dall' [azione PatchFiles](patchfiles-action.md). Questa tabella viene in genere aggiunta al pacchetto di installazione da una trasformazione da un pacchetto di patch. Non viene in genere creato direttamente in un pacchetto di installazione.

## <a name="validation"></a>Convalida

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE29](ice29.md)  
</dl>

 

 



