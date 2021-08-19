---
description: Nella tabella ODBCDriver sono elencati i driver ODBC che appartengono all'installazione.
ms.assetid: 3518b370-0652-4b54-8057-9871365d5e8c
title: Tabella ODBCDriver
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a1eb0da3217d7466fc0beef90933c8a6af32e3d0551ecc6975a31ac55ed2730
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118943122"
---
# <a name="odbcdriver-table"></a>Tabella ODBCDriver

Nella tabella ODBCDriver sono elencati i driver ODBC che appartengono all'installazione.

La tabella ODBCDriver include le colonne seguenti.



| Colonna      | Tipo                         | Chiave | Nullable |
|-------------|------------------------------|-----|----------|
| Driver      | [Identificatore](identifier.md) | S   | N        |
| Componente\_ | [Identificatore](identifier.md) | N   | N        |
| Descrizione | [Text](text.md)             | N   | N        |
| file\_      | [Identificatore](identifier.md) | N   | N        |
| Configurazione \_ file | [Identificatore](identifier.md) | N   | S        |



 

## <a name="columns"></a>Colonne

<dl> <dt>

<span id="Driver"></span><span id="driver"></span><span id="DRIVER"></span>autista
</dt> <dd>

Nome del token interno per il driver. Chiave primaria per la tabella

</dd> <dt>

<span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Componente\_
</dt> <dd>

Chiave esterna nella tabella Component.

</dd> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Descrizione
</dt> <dd>

Descrizione registrata per questo driver ODBC. Questo valore non può essere localizzato.

</dd> <dt>

<span id="File_"></span><span id="file_"></span><span id="FILE_"></span>File\_
</dt> <dd>

File DLL per i driver elencati nella colonna Driver. La colonna File \_ è una chiave esterna nella tabella [File](file-table.md). Il nome file immesso nella colonna Nome file del record della tabella File deve essere nel formato di nome file breve. Non è possibile usare la sintassi \| LFN SFN.

</dd> <dt>

<span id="File_Setup"></span><span id="file_setup"></span><span id="FILE_SETUP"></span>Configurazione \_ file
</dt> <dd>

File DLL di installazione per il driver se è diverso da Driver. La colonna File \_ è una chiave esterna nella tabella [File](file-table.md). Il nome file immesso nella colonna Nome file del record della tabella File deve essere nel formato di nome file breve. Non è possibile usare la sintassi \| LFN SFN.

</dd> </dl>

## <a name="remarks"></a>Commenti

Le [azioni InstallODBC](installodbc-action.md) [e RemoveODBC](removeodbc-action.md) nelle tabelle [*di sequenza*](s-gly.md) elaborano le informazioni in questa tabella. Per informazioni sull'uso *delle tabelle di sequenza,* vedere [Uso di una tabella di sequenza](using-a-sequence-table.md).

## <a name="validation"></a>Convalida

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
</dl>

 

 



