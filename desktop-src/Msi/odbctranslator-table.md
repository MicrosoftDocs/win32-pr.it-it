---
description: Nella tabella ODBCTranslator sono elencati i convertitori ODBC appartenenti all'installazione.
ms.assetid: fecb7454-29bb-4ddf-b4d5-2e56c20ff2dc
title: Tabella ODBCTranslator
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd59c535963b3c42e94c8c904d448540072913b56bedb58c3e0bddc72dd6c6c9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118942892"
---
# <a name="odbctranslator-table"></a>Tabella ODBCTranslator

Nella tabella ODBCTranslator sono elencati i convertitori ODBC appartenenti all'installazione.

La tabella ODBCTranslator include le colonne seguenti.



| Colonna      | Tipo                         | Chiave | Nullable |
|-------------|------------------------------|-----|----------|
| Traduttore  | [Identificatore](identifier.md) | S   | N        |
| Componente\_ | [Identificatore](identifier.md) | N   | N        |
| Descrizione | [Text](text.md)             | N   | N        |
| file\_      | [Identificatore](identifier.md) | N   | N        |
| Installazione \_ file | [Identificatore](identifier.md) | N   | S        |



 

## <a name="columns"></a>Colonne

<dl> <dt>

<span id="Translator"></span><span id="translator"></span><span id="TRANSLATOR"></span>Translator
</dt> <dd>

Nome del token interno per translator. Chiave primaria per la tabella.

</dd> <dt>

<span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Componente\_
</dt> <dd>

Chiave esterna nella tabella Component.

</dd> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Descrizione
</dt> <dd>

Descrizione registrata per questo convertitore di driver ODBC. Questo valore non può essere localizzato.

</dd> <dt>

<span id="File_"></span><span id="file_"></span><span id="FILE_"></span>File\_
</dt> <dd>

File DLL per il trasferimento elencato nella colonna Translator. La colonna File \_ è una chiave esterna nella tabella [File](file-table.md). Il nome file immesso nella colonna Nome file del record della tabella File deve essere nel formato nome file breve. Non è possibile \| usare la sintassi LFN SFN.

</dd> <dt>

<span id="File_Setup"></span><span id="file_setup"></span><span id="FILE_SETUP"></span>Installazione \_ file
</dt> <dd>

Il file DLL di installazione per il traduttore se è diverso dalla Translator colonna. La colonna File \_ è una chiave esterna nella tabella [File](file-table.md). Il nome file immesso nella colonna Nome file del record della tabella File deve essere nel formato nome file breve. Non è possibile \| usare la sintassi LFN SFN.

</dd> </dl>

## <a name="remarks"></a>Commenti

Le [azioni InstallODBC](installodbc-action.md) [e RemoveODBC](removeodbc-action.md) nelle tabelle [*di sequenza*](s-gly.md) elaborano le informazioni contenute in questa tabella. Per informazioni sull'uso *delle tabelle di sequenza,* vedere [Using a Sequence Table](using-a-sequence-table.md).

## <a name="validation"></a>Convalida

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
</dl>

 

 



