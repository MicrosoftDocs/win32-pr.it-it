---
description: La tabella ODBCDriver elenca i driver ODBC che appartengono all'installazione.
ms.assetid: 3518b370-0652-4b54-8057-9871365d5e8c
title: Tabella ODBCDriver
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3257f3eec5b60191df727d156572293489aa1956
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525782"
---
# <a name="odbcdriver-table"></a>Tabella ODBCDriver

La tabella ODBCDriver elenca i driver ODBC che appartengono all'installazione.

La tabella ODBCDriver include le colonne seguenti.



| Colonna      | Tipo                         | Chiave | Nullable |
|-------------|------------------------------|-----|----------|
| Driver      | [Identificatore](identifier.md) | S   | N        |
| Componente\_ | [Identificatore](identifier.md) | N   | N        |
| Descrizione | [Text](text.md)             | N   | N        |
| file\_      | [Identificatore](identifier.md) | N   | N        |
| \_Installazione file | [Identificatore](identifier.md) | N   | S        |



 

## <a name="columns"></a>Colonne

<dl> <dt>

<span id="Driver"></span><span id="driver"></span><span id="DRIVER"></span>Driver
</dt> <dd>

Nome del token interno per il driver. Chiave primaria per la tabella

</dd> <dt>

<span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Componente\_
</dt> <dd>

Chiave esterna nella tabella dei componenti.

</dd> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Descrizione
</dt> <dd>

Descrizione registrata per il driver ODBC. Questo valore non può essere localizzato.

</dd> <dt>

<span id="File_"></span><span id="file_"></span><span id="FILE_"></span>File\_
</dt> <dd>

File DLL per i driver elencati nella colonna driver. La \_ colonna file è una chiave esterna nella [tabella file](file-table.md). Il nome file immesso nella colonna FileName del record della tabella file deve essere nel formato di file breve. \|Impossibile utilizzare la sintassi LFN di SFN.

</dd> <dt>

<span id="File_Setup"></span><span id="file_setup"></span><span id="FILE_SETUP"></span>\_Installazione file
</dt> <dd>

Il file DLL di installazione del driver se è diverso dal driver. La \_ colonna file è una chiave esterna nella [tabella file](file-table.md). Il nome file immesso nella colonna FileName del record della tabella file deve essere nel formato di file breve. \|Impossibile utilizzare la sintassi LFN di SFN.

</dd> </dl>

## <a name="remarks"></a>Commenti

Le azioni [InstallODBC](installodbc-action.md) e [RemoveODBC](removeodbc-action.md) nelle [*tabelle di sequenza*](s-gly.md) elaborano le informazioni contenute in questa tabella. Per informazioni sull'utilizzo di *tabelle di sequenza*, vedere [utilizzo di una tabella di sequenza](using-a-sequence-table.md).

## <a name="validation"></a>Convalida

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
</dl>

 

 



