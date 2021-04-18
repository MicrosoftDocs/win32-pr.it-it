---
description: Nella tabella ODBCDataSource sono elencate le origini dati appartenenti all'installazione.
ms.assetid: dea28324-e48d-49e8-a4d2-309f7e7cb4b0
title: Tabella ODBCDataSource
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 819eecc671c75fa11db6e4a2706a511c2758ad00
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308179"
---
# <a name="odbcdatasource-table"></a>Tabella ODBCDataSource

Nella tabella ODBCDataSource sono elencate le origini dati appartenenti all'installazione.

La tabella ODBCDataSource include le colonne seguenti.



| Colonna            | Tipo                         | Chiave | Nullable |
|-------------------|------------------------------|-----|----------|
| DataSource        | [Identificatore](identifier.md) | S   | N        |
| Componente\_       | [Identificatore](identifier.md) | N   | N        |
| Descrizione       | [Text](text.md)             | N   | N        |
| DriverDescription | [Text](text.md)             | N   | N        |
| Registrazione      | [Integer](integer.md)       | N   | N        |



 

## <a name="columns"></a>Colonne

<dl> <dt>

<span id="DataSource"></span><span id="datasource"></span><span id="DATASOURCE"></span>DataSource
</dt> <dd>

Nome del token interno per l'origine dati. Chiave primaria per la tabella.

</dd> <dt>

<span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Componente\_
</dt> <dd>

Chiave esterna nella [tabella dei componenti](component-table.md).

</dd> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Descrizione
</dt> <dd>

Descrizione registrata per questa origine dati. Questo valore non può essere localizzato. Le descrizioni delle origini dati ODBC non possono superare la \_ lunghezza massima del \_ DSN SQL \_ .

</dd> <dt>

<span id="DriverDescription"></span><span id="driverdescription"></span><span id="DRIVERDESCRIPTION"></span>DriverDescription
</dt> <dd>

Driver associato che può essere preesistente. Questo valore non può essere localizzato.

</dd> <dt>

<span id="Registration"></span><span id="registration"></span><span id="REGISTRATION"></span>Registrazione
</dt> <dd>

Questo campo specifica il tipo di registrazione per l'origine dati.



| Costante                                      | Valore esadecimale | Decimal | Descrizione                            |
|-----------------------------------------------|-------------|---------|----------------------------------------|
| **msidbODBCDataSourceRegistrationPerMachine** | 0x000       | 0       | L'origine dati è registrata per computer. |
| **msidbODBCDataSourceRegistrationPerUser**    | 0x001       | 1       | L'origine dati è registrata per utente.    |



 

</dd> </dl>

## <a name="remarks"></a>Commenti

Le azioni [InstallODBC](installodbc-action.md) e [RemoveODBC](removeodbc-action.md) nelle [*tabelle di sequenza*](s-gly.md) elaborano le informazioni contenute in questa tabella. Per informazioni sull'utilizzo di *tabelle di sequenza*, vedere [utilizzo di una tabella di sequenza](using-a-sequence-table.md).

## <a name="validation"></a>Convalida

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
[ICE45](ice45.md)  
[ICE98](ice98.md)  
</dl>

 

 



