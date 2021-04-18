---
description: Nella tabella ODBCTranslator sono elencati i convertitori ODBC che appartengono all'installazione.
ms.assetid: fecb7454-29bb-4ddf-b4d5-2e56c20ff2dc
title: Tabella ODBCTranslator
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9fdf85f73b649e18c0980508e234bf7599e69c5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319002"
---
# <a name="odbctranslator-table"></a>Tabella ODBCTranslator

Nella tabella ODBCTranslator sono elencati i convertitori ODBC che appartengono all'installazione.

La tabella ODBCTranslator include le colonne seguenti.



| Colonna      | Tipo                         | Chiave | Nullable |
|-------------|------------------------------|-----|----------|
| Traduttore  | [Identificatore](identifier.md) | S   | N        |
| Componente\_ | [Identificatore](identifier.md) | N   | N        |
| Descrizione | [Text](text.md)             | N   | N        |
| file\_      | [Identificatore](identifier.md) | N   | N        |
| \_Installazione file | [Identificatore](identifier.md) | N   | S        |



 

## <a name="columns"></a>Colonne

<dl> <dt>

<span id="Translator"></span><span id="translator"></span><span id="TRANSLATOR"></span>Translator
</dt> <dd>

Nome del token interno per Translator. Chiave primaria per la tabella.

</dd> <dt>

<span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Componente\_
</dt> <dd>

Chiave esterna nella tabella dei componenti.

</dd> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Descrizione
</dt> <dd>

Descrizione registrata per questo convertitore di driver ODBC. Questo valore non può essere localizzato.

</dd> <dt>

<span id="File_"></span><span id="file_"></span><span id="FILE_"></span>File\_
</dt> <dd>

File DLL per il trasferimento elencato nella colonna Translator. La \_ colonna file è una chiave esterna nella [tabella file](file-table.md). Il nome file immesso nella colonna FileName del record della tabella file deve essere nel formato di file breve. \|Impossibile utilizzare la sintassi LFN di SFN.

</dd> <dt>

<span id="File_Setup"></span><span id="file_setup"></span><span id="FILE_SETUP"></span>\_Installazione file
</dt> <dd>

Il file DLL di installazione per il traduttore se è diverso dalla colonna Translator. La \_ colonna file è una chiave esterna nella [tabella file](file-table.md). Il nome file immesso nella colonna FileName del record della tabella file deve essere nel formato di file breve. \|Impossibile utilizzare la sintassi LFN di SFN.

</dd> </dl>

## <a name="remarks"></a>Commenti

Le azioni [InstallODBC](installodbc-action.md) e [RemoveODBC](removeodbc-action.md) nelle [*tabelle di sequenza*](s-gly.md) elaborano le informazioni contenute in questa tabella. Per informazioni sull'utilizzo di *tabelle di sequenza*, vedere [utilizzo di una tabella di sequenza](using-a-sequence-table.md).

## <a name="validation"></a>Convalida

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
</dl>

 

 



