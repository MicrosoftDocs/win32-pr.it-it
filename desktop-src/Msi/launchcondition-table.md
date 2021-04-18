---
description: La tabella LaunchCondition viene utilizzata dall'azione LaunchConditions. Contiene un elenco di condizioni che devono essere soddisfatte per poter iniziare l'installazione.
ms.assetid: 6e550cc7-c479-417e-ab89-882d8fece4e1
title: Tabella LaunchCondition
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d67834f058575dde297454480040028ef9c5732
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307255"
---
# <a name="launchcondition-table"></a>Tabella LaunchCondition

La tabella LaunchCondition viene utilizzata dall' [azione LaunchConditions](launchconditions-action.md). Contiene un elenco di condizioni che devono essere soddisfatte per poter iniziare l'installazione.

La tabella LaunchCondition include le colonne seguenti.



| Colonna      | Tipo                       | Chiave | Nullable |
|-------------|----------------------------|-----|----------|
| Condizione   | [Condition](condition.md) | S   | N        |
| Descrizione | [Formattato](formatted.md) | N   | N        |



 

## <a name="columns"></a>Colonne

<dl> <dt>

<span id="Condition"></span><span id="condition"></span><span id="CONDITION"></span>Condizione
</dt> <dd>

Espressione che deve restituire true per iniziare l'installazione.

</dd> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Descrizione
</dt> <dd>

Testo localizzabile da visualizzare quando la condizione ha esito negativo e l'installazione deve essere terminata.

</dd> </dl>

## <a name="remarks"></a>Commenti

Non è possibile garantire l'ordine di valutazione delle condizioni di avvio mediante la creazione della tabella. Se è necessario controllare l'ordine in cui vengono valutate le condizioni, è necessario eseguire questa operazione usando il tipo di azione personalizzata 19 azioni personalizzate nell'installazione.

## <a name="validation"></a>Convalida

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE46](ice46.md)  
[ICE79](ice79.md)  
[ICE86](ice86.md)  
</dl>

 

 



