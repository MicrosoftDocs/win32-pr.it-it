---
description: La tabella ODBCSourceAttribute contiene informazioni sugli attributi delle origini dati.
ms.assetid: 8ee50fd7-507e-484f-9a16-de5449470562
title: Tabella ODBCSourceAttribute
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d52dd9636ac19eae0fb3a9e41d1a1c8389753e5d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525771"
---
# <a name="odbcsourceattribute-table"></a>Tabella ODBCSourceAttribute

La tabella ODBCSourceAttribute contiene informazioni sugli attributi delle origini dati.

La tabella ODBCSourceAttribute include le colonne seguenti.



| Colonna       | Tipo                         | Chiave | Nullable |
|--------------|------------------------------|-----|----------|
| DataSource\_ | [Identificatore](identifier.md) | S   | N        |
| Attributo    | [Text](text.md)             | S   | N        |
| Valore        | [Formattato](formatted.md)   | N   | S        |



 

## <a name="columns"></a>Colonne

<dl> <dt>

<span id="DataSource_"></span><span id="datasource_"></span><span id="DATASOURCE_"></span>DataSource\_
</dt> <dd>

Nome del token interno per l'origine dati. Chiave primaria per la tabella.

</dd> <dt>

<span id="Attribute"></span><span id="attribute"></span><span id="ATTRIBUTE"></span>Attributo
</dt> <dd>

Nome dell'attributo dell'origine dati. Chiave primaria per la tabella.

</dd> <dt>

<span id="Value"></span><span id="value"></span><span id="VALUE"></span>Valore
</dt> <dd>

Valore stringa localizzabile per l'attributo.

</dd> </dl>

## <a name="remarks"></a>Commenti

Le azioni [InstallODBC](installodbc-action.md) e [RemoveODBC](removeodbc-action.md) nelle [*tabelle di sequenza*](s-gly.md) elaborano le informazioni contenute in questa tabella. Per informazioni sull'utilizzo di *tabelle di sequenza*, vedere [utilizzo di una tabella di sequenza](using-a-sequence-table.md).

## <a name="validation"></a>Convalida

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
[ICE46](ice46.md)  
</dl>

 

 



