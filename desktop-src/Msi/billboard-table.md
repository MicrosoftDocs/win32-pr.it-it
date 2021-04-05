---
description: Nella tabella Billboard sono elencati i controlli dei tabelloni visualizzati nell'interfaccia utente completa.
ms.assetid: bb8c1d7c-aa1d-43cc-9fb4-3a0ad75c4615
title: Tabella Billboard
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65a561eb629e07b25437d6e5ce12b58bb0d7dd20
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103967256"
---
# <a name="billboard-table"></a>Tabella Billboard

Nella tabella Billboard sono elencati i [controlli dei tabelloni](billboard-control.md) visualizzati nell'interfaccia utente completa.

La tabella Billboard contiene le colonne seguenti.



| Colonna    | Tipo                         | Chiave | Nullable |
|-----------|------------------------------|-----|----------|
| Billboard | [Identificatore](identifier.md) | S   | N        |
| Funzionalità\_ | [Identificatore](identifier.md) | N   | N        |
| Azione    | [Identificatore](identifier.md) | N   | S        |
| Ordering  | [Integer](integer.md)       | N   | S        |



 

## <a name="columns"></a>Colonne

<dl> <dt>

<span id="Billboard"></span><span id="billboard"></span><span id="BILLBOARD"></span>Billboard
</dt> <dd>

Nome del [controllo Billboard](billboard-control.md).

</dd> <dt>

<span id="Feature_"></span><span id="feature_"></span><span id="FEATURE_"></span>Funzionalità\_
</dt> <dd>

Chiave esterna per la prima colonna della tabella delle [funzionalità](feature-table.md). Il tabellone viene visualizzato solo se questa funzionalità è in fase di installazione.

</dd> <dt>

<span id="Action"></span><span id="action"></span><span id="ACTION"></span>Azione
</dt> <dd>

Nome di un'azione. Il tabellone viene visualizzato durante i messaggi di stato ricevuti da questa azione.

</dd> <dt>

<span id="Ordering"></span><span id="ordering"></span><span id="ORDERING"></span>Ordinare
</dt> <dd>

Se è presente più di un Billboard corrispondente a un'azione, questi vengono visualizzati nell'ordine definito da questa colonna. Questo numero deve essere non negativo.

</dd> </dl>

## <a name="validation"></a>Convalida

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
[ICE95](ice95.md)  
</dl>

 

 



