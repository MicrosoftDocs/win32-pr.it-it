---
description: La tabella ReserveCost è una tabella facoltativa che consente all'autore di riservare una quantità di spazio su disco in qualsiasi directory che dipende dallo stato di installazione di un componente.
ms.assetid: 371e72f1-40a2-4ed2-b0ab-33840075ff47
title: Tabella ReserveCost
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5f593fd11789cd2304385b97e96e50a009fbde0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103967734"
---
# <a name="reservecost-table"></a>Tabella ReserveCost

La tabella ReserveCost è una tabella facoltativa che consente all'autore di riservare una quantità di spazio su disco in qualsiasi directory che dipende dallo stato di installazione di un componente.

La tabella ReserveCost include le colonne seguenti.



| Colonna        | Tipo                               | Chiave | Nullable |
|---------------|------------------------------------|-----|----------|
| ReserveKey    | [Identificatore](identifier.md)       | S   | N        |
| Componente\_   | [Identificatore](identifier.md)       | N   | N        |
| ReserveFolder | [Identificatore](identifier.md)       | N   | S        |
| ReserveLocal  | [DoubleInteger](doubleinteger.md) | N   | N        |
| ReserveSource | [DoubleInteger](doubleinteger.md) | N   | N        |



 

## <a name="columns"></a>Colonne

<dl> <dt>

<span id="ReserveKey"></span><span id="reservekey"></span><span id="RESERVEKEY"></span>ReserveKey
</dt> <dd>

Chiave primaria che identifica in modo univoco una voce della tabella ReserveCost.

</dd> <dt>

<span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Componente\_
</dt> <dd>

Chiave esterna per la colonna uno della tabella dei [componenti](component-table.md) . Riserva una quantità di spazio specificata se il componente deve essere installato.

</dd> <dt>

<span id="ReserveFolder"></span><span id="reservefolder"></span><span id="RESERVEFOLDER"></span>ReserveFolder
</dt> <dd>

Questa colonna contiene il nome di una proprietà che rappresenta il percorso completo della directory di destinazione. Questo nome di proprietà è in genere il nome di una directory nella tabella di [directory](directory-table.md) o il nome di un set di proprietà ottenuto utilizzando l'azione [AppSearch](appsearch-action.md) . In questo modo viene aggiunta la quantità di spazio su disco specificata in ReserveLocal o ReserveSource al costo del volume del dispositivo che contiene la directory.

</dd> <dt>

<span id="ReserveLocal"></span><span id="reservelocal"></span><span id="RESERVELOCAL"></span>ReserveLocal
</dt> <dd>

Numero di byte di spazio su disco da riservare se il componente collegato è installato per l'esecuzione in locale.

</dd> <dt>

<span id="ReserveSource"></span><span id="reservesource"></span><span id="RESERVESOURCE"></span>ReserveSource
</dt> <dd>

Numero di byte di spazio su disco da riservare se il componente collegato è installato per l'esecuzione dall'origine.

</dd> </dl>

## <a name="remarks"></a>Commenti

Il mantenimento dei costi in questo modo può essere utile per gli autori che desiderano garantire che una quantità minima di spazio su disco sarà disponibile al termine dell'installazione. Questo spazio su disco, ad esempio, potrebbe essere riservato ai documenti utente o ai file dell'applicazione, ad esempio i file di indice, che vengono creati solo dopo l'avvio dell'applicazione dopo l'installazione.

È possibile utilizzare la tabella ReserveCost per abilitare azioni personalizzate per specificare un costo approssimativo per tutti i file, le voci del registro di sistema o altri elementi che l'azione personalizzata potrebbe installare. Le azioni personalizzate che aggiungono voci alla tabella ReserveCost devono essere sequenziate tra le azioni [CostInitialize](costinitialize-action.md) e [filecost](filecost-action.md) . Questa operazione è necessaria per l'azione filecost per inizializzare correttamente il costo di tutti i componenti interessati dalle voci nella tabella ReserveCost.

## <a name="validation"></a>Convalida

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
</dl>

 

 



