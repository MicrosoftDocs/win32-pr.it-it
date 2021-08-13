---
description: La tabella Binary contiene i dati binari per elementi quali bitmap, animazioni e icone. La tabella binaria viene usata anche per archiviare i dati per le azioni personalizzate. Vedere Limitazioni OLE in Flussi.
ms.assetid: 44c56407-df2e-4cbe-b7a3-b22e8d97eb03
title: Tabella binaria
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a70750193b1dc147a9b2b4cfa01bbea410f0e44b7c03f16bd1c992f118a4f0e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118638805"
---
# <a name="binary-table"></a>Tabella binaria

La tabella Binary contiene i dati binari per elementi quali bitmap, animazioni e icone. La tabella binaria viene usata anche per archiviare i dati per le azioni personalizzate. Vedere [Limitazioni OLE in Flussi](ole-limitations-on-streams.md).

La tabella Binary include le colonne seguenti.



| Colonna | Tipo                         | Chiave | Nullable |
|--------|------------------------------|-----|----------|
| Nome   | [Identificatore](identifier.md) | S   | N        |
| Dati   | [Binario](binary.md)         | N   | N        |



 

## <a name="columns"></a>Colonne

<dl> <dt>

<span id="Name"></span><span id="name"></span><span id="NAME"></span>Nome
</dt> <dd>

Chiave univoca che identifica i dati binari specifici. Se i dati binari sono relativi a un controllo , la chiave viene visualizzata nella colonna Text del controllo associato nella [tabella Control](control-table.md). Questa chiave deve essere univoca tra tutti i controlli che richiedono dati binari.

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

 

 



