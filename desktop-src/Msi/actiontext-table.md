---
description: La tabella ActionText contiene testo da visualizzare in una finestra di dialogo di avanzamento e scritta nel log per le azioni che importano molto tempo per l'esecuzione. Il testo visualizzato è costituito dalla descrizione dell'azione e, facoltativamente, dal formato dati dell'azione.
ms.assetid: 88d18422-77d0-4929-9341-d078843cb2a9
title: Tabella ActionText
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8071a8542571a3364e151522a7fc4c0b11362045
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311087"
---
# <a name="actiontext-table"></a>Tabella ActionText

La tabella ActionText contiene testo da visualizzare in una finestra di dialogo di avanzamento e scritta nel log per le azioni che importano molto tempo per l'esecuzione. Il testo visualizzato è costituito dalla descrizione dell'azione e, facoltativamente, dal formato dati dell'azione.

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

Descrizione localizzata visualizzata nella finestra di dialogo dello stato di avanzamento o scritta nel log durante l'esecuzione dell'azione.

</dd> <dt>

<span id="Template"></span><span id="template"></span><span id="TEMPLATE"></span>Modello
</dt> <dd>

Modello di formato localizzato utilizzato per formattare i record di dati dell'azione da visualizzare durante l'esecuzione dell'azione. Se non viene fornito un modello, i dati dell'azione non vengono visualizzati.

</dd> </dl>

## <a name="remarks"></a>Commenti

Le voci nella tabella ActionText, in genere, fanno riferimento a azioni nelle tabelle di sequenza. Sono presenti altre azioni eseguite dal programma di installazione che non sono elencate nella tabella di sequenza, ma che è comunque necessario specificare nella tabella. Nella tabella seguente vengono identificate le voci di tabella richieste in cui il nome e il modello dell'azione devono essere creati esattamente come illustrato, ma la descrizione può essere personalizzata.



| Azione          | Descrizione                             | Modello |
|-----------------|-----------------------------------------|----------|
| Rollback        | Annulla le azioni.                         | \[1\]    |
| RollbackCleanup | Rimuove i file obsoleti.                      | \[1\]    |
| GenerateScript  | Genera operazioni di sistema per l'azione. | \[1\]    |



 

> [!Note]  
> Il testo dell'azione viene visualizzato solo per le azioni eseguite all'interno dello script di installazione. Il testo dell'azione viene pertanto visualizzato solo per le azioni sequenziate tra le azioni [InstallInitialize](installinitialize-action.md) e [InstallFinalize](installfinalize-action.md) .

 

È possibile importare una tabella ActionText localizzata nel database usando Msidb.exe o [**MsiDatabaseImport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta). L'SDK include una tabella ActionText localizzata per ogni lingua elencata nella sezione [localizzazione delle tabelle Error e ActionText](localizing-the-error-and-actiontext-tables.md) . Se la tabella ActionText non è popolata, il programma di installazione carica le stringhe localizzate per la lingua specificata dalla proprietà [**ProductLanguage**](productlanguage.md) .

## <a name="validation"></a>Convalida

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE46](ice46.md)  
</dl>

 

 



