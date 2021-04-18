---
description: La tabella binaria include i dati binari per elementi come bitmap, animazioni e icone. La tabella binaria viene usata anche per archiviare i dati per le azioni personalizzate. Vedere limitazioni OLE sui flussi.
ms.assetid: 44c56407-df2e-4cbe-b7a3-b22e8d97eb03
title: Tabella binaria
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f4069c7e684e7d90c94b4b04f3d5839058f3570a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311014"
---
# <a name="binary-table"></a>Tabella binaria

La tabella binaria include i dati binari per elementi come bitmap, animazioni e icone. La tabella binaria viene usata anche per archiviare i dati per le azioni personalizzate. Vedere [limitazioni OLE sui flussi](ole-limitations-on-streams.md).

La tabella binaria contiene le colonne seguenti.



| Colonna | Tipo                         | Chiave | Nullable |
|--------|------------------------------|-----|----------|
| Nome   | [Identificatore](identifier.md) | S   | N        |
| Data   | [Binario](binary.md)         | N   | N        |



 

## <a name="columns"></a>Colonne

<dl> <dt>

<span id="Name"></span><span id="name"></span><span id="NAME"></span>Nome
</dt> <dd>

Chiave univoca che identifica i dati binari specifici. Se i dati binari sono per un controllo, la chiave viene visualizzata nella colonna di testo del controllo associato nella [tabella del controllo](control-table.md). Questa chiave deve essere univoca tra tutti i controlli che richiedono dati binari.

</dd> <dt>

<span id="Data"></span><span id="data"></span><span id="DATA"></span>Dati
</dt> <dd>

Dati binari non formattati.

</dd> </dl>

## <a name="validation"></a>Convalida

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE17](ice17.md)  
[ICE29](ice29.md)  
</dl>

 

 



