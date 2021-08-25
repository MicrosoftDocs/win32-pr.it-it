---
description: La tabella ActionText contiene testo da visualizzare in una finestra di dialogo di stato e scritto nel log per le azioni che possono richiedere molto tempo per l'esecuzione. Il testo visualizzato è costituito dalla descrizione dell'azione e, facoltativamente, dai dati formattati dall'azione.
ms.assetid: 88d18422-77d0-4929-9341-d078843cb2a9
title: Tabella ActionText
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f21923588676db4ad38482768a493428ce76caf32b32334e429fbe41335c2bf7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119927261"
---
# <a name="actiontext-table"></a>Tabella ActionText

La tabella ActionText contiene testo da visualizzare in una finestra di dialogo di stato e scritto nel log per le azioni che possono richiedere molto tempo per l'esecuzione. Il testo visualizzato è costituito dalla descrizione dell'azione e, facoltativamente, dai dati formattati dall'azione.

La tabella ActionText include le colonne seguenti.



| Colonna      | Tipo                         | Chiave | Nullable |
|-------------|------------------------------|-----|----------|
| Azione      | [Identificatore](identifier.md) | S   | N        |
| Descrizione | [Text](text.md)             | N   | S        |
| Modello    | [Modello](template.md)     | N   | S        |



 

## <a name="columns"></a>Colonne

<dl> <dt>

<span id="Action"></span><span id="action"></span><span id="ACTION"></span>Azione
</dt> <dd>

Nome dell'azione.

Chiave della tabella primaria.

</dd> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Descrizione
</dt> <dd>

Descrizione localizzata visualizzata nella finestra di dialogo di stato o scritta nel log durante l'esecuzione dell'azione.

</dd> <dt>

<span id="Template"></span><span id="template"></span><span id="TEMPLATE"></span>Modello
</dt> <dd>

Modello di formato localizzato utilizzato per formattare i record di dati delle azioni da visualizzare durante l'esecuzione dell'azione. Se non viene fornito un modello, i dati dell'azione non vengono visualizzati.

</dd> </dl>

## <a name="remarks"></a>Commenti

In genere, le voci nella tabella ActionText fanno riferimento alle azioni nelle tabelle di sequenza. Il programma di installazione esegue altre azioni che non sono elencate nella tabella delle sequenze, ma devono comunque essere specificate nella tabella. La tabella seguente identifica le voci di tabella necessarie in cui il nome dell'azione e il modello devono essere creati esattamente come illustrato, ma la descrizione può essere personalizzata.



| Azione          | Descrizione                             | Modello |
|-----------------|-----------------------------------------|----------|
| Rollback        | Annulla le azioni.                         | \[1\]    |
| RollbackCleanup | Rimuove i file vecchi.                      | \[1\]    |
| GenerateScript  | Genera operazioni di sistema per l'azione. | \[1\]    |



 

> [!Note]  
> Il testo dell'azione viene visualizzato solo per le azioni eseguite all'interno dello script di installazione. Di conseguenza, il testo dell'azione viene visualizzato solo per le azioni sequenziate tra le [azioni InstallInitialize](installinitialize-action.md) [e InstallFinalize.](installfinalize-action.md)

 

È possibile importare una tabella ActionText localizzata nel database usando Msidb.exe [**o MsiDatabaseImport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta). L'SDK include una tabella ActionText localizzata per ognuna delle lingue elencate nella sezione Localizzazione delle tabelle [Error e ActionText.](localizing-the-error-and-actiontext-tables.md) Se la tabella ActionText non viene popolata, il programma di installazione carica le stringhe localizzate per la lingua specificata dalla [**proprietà ProductLanguage.**](productlanguage.md)

## <a name="validation"></a>Convalida

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE46](ice46.md)  
</dl>

 

 



