---
description: La tabella ODBCAttribute contiene informazioni sugli attributi dei driver Open Database Connectivity (ODBC) e dei traduttori.
ms.assetid: 82fd83d4-22dd-4641-807b-d2b263918e4c
title: Tabella ODBCAttribute
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e31e67cde1625812d1c5b8af7dc3bd24347891d3a769e24deeb02db7cc44396
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118943179"
---
# <a name="odbcattribute-table"></a>Tabella ODBCAttribute

La tabella ODBCAttribute contiene informazioni sugli attributi dei driver Open Database Connectivity (ODBC) e dei traduttori.

La tabella ODBCAttribute include le colonne seguenti.



| Colonna    | Tipo                         | Chiave | Nullable |
|-----------|------------------------------|-----|----------|
| Driver\_  | [Identificatore](identifier.md) | S   | N        |
| Attributo | [Text](text.md)             | S   | N        |
| Valore     | [Formattato](formatted.md)   | N   | S        |



 

## <a name="columns"></a>Colonne

<dl> <dt>

<span id="Driver_"></span><span id="driver_"></span><span id="DRIVER_"></span>autista\_
</dt> <dd>

Nome del token interno per un driver. Chiave primaria per la tabella. Chiave esterna nella [tabella ODBCDriver](odbcdriver-table.md).

</dd> <dt>

<span id="Attribute"></span><span id="attribute"></span><span id="ATTRIBUTE"></span>Attributo
</dt> <dd>

Nome dell'attributo del driver. Chiave primaria per la tabella.

</dd> <dt>

<span id="Value"></span><span id="value"></span><span id="VALUE"></span>Valore
</dt> <dd>

Valore stringa localizzabile per l'attributo.

</dd> </dl>

## <a name="remarks"></a>Commenti

Le [azioni InstallODBC](installodbc-action.md) [e RemoveODBC](removeodbc-action.md) nelle tabelle [*di sequenza*](s-gly.md) elaborano le informazioni in questa tabella. Per informazioni sull'uso *delle tabelle di sequenza,* vedere [Uso di una tabella di sequenza](using-a-sequence-table.md).

## <a name="validation"></a>Convalida

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
[ICE46](ice46.md)  
</dl>

 

 



