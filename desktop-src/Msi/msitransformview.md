---
description: Questa tabella temporanea Abilita l'opzione di disinstallazione patch azione personalizzata per le azioni personalizzate aggiunte o aggiornate da una patch.
ms.assetid: 2d4a934f-e245-4d0a-b8bf-52457107ac08
title: MsiTransformView
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7eb50c397c10ede3a21b40600952d50e55a5ba1a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316256"
---
# <a name="msitransformview"></a>MsiTransformView

Questa tabella temporanea Abilita l' [opzione di disinstallazione patch azione personalizzata](custom-action-patch-uninstall-option.md) per le azioni personalizzate aggiunte o aggiornate da una patch.

Se una patch aggiunge o aggiorna un'azione personalizzata con l'attributo **msidbCustomActionTypePatchUninstall** , Windows Installer esegue l'azione personalizzata nuova o aggiornata quando la patch viene disinstallata. Windows Installer rende gli aggiornamenti all'interno della patch disinstallati disponibili per l'azione personalizzata di disinstallazione della patch. La patch deve includere una *<PatchGUID>* tabella MsiTransformView per fornire queste informazioni Windows Installer. Le informazioni contenute in questa tabella sono disponibili per qualsiasi azione personalizzata immediata e non sono disponibili per le azioni personalizzate posticipate.

**[Windows Installer 4,0 e versioni precedenti](not-supported-in-windows-installer-4-0.md):** Non supportato. L' [opzione di disinstallazione patch azione personalizzata](custom-action-patch-uninstall-option.md) è disponibile a partire da Windows Installer 4,5.

Questa tabella deve essere denominata MsiTransformView *<PatchGUID>* Table, dove *<PatchGUID>* è il GUID che identifica in modo univoco la patch. La *<PatchGUID>* tabella MsiTransformView include le colonne seguenti.



| Colonna  | Tipo                         | Chiave | Nullable |
|---------|------------------------------|-----|----------|
| Tabella   | [Identificatore](identifier.md) | S   | N        |
| Colonna  | [Text](text.md)             | S   | N        |
| Riga     | [Text](text.md)             | S   | S        |
| Data    | [Text](text.md)             | N   | S        |
| Corrente | [Text](text.md)             | N   | S        |



 

## <a name="column"></a>Colonna

<dl> <dt>

<span id="Table"></span><span id="table"></span><span id="TABLE"></span>tavolo
</dt> <dd>

Nome di una tabella di database modificata.

</dd> <dt>

<span id="Column"></span><span id="column"></span><span id="COLUMN"></span>Colonna
</dt> <dd>

Nome di una colonna di tabella modificata o di inserimento, eliminazione, creazione o eliminazione.

</dd> <dt>

<span id="Row"></span><span id="row"></span><span id="ROW"></span>Riga
</dt> <dd>

Elenco dei valori di chiave primaria separati da tabulazioni. I valori di chiave primaria null sono rappresentati da un singolo carattere di spazio. Un valore null in questa colonna indica una modifica dello schema.

</dd> <dt>

<span id="Data"></span><span id="data"></span><span id="DATA"></span>Dati
</dt> <dd>

Dati, nome di un flusso di dati o definizione di colonna.

</dd> <dt>

<span id="Current"></span><span id="current"></span><span id="CURRENT"></span>Corrente
</dt> <dd>

Valore corrente dal database di riferimento o da un numero di colonna.

</dd> </dl>

## <a name="remarks"></a>Commenti

Patch disinstallare le azioni personalizzate vengono eseguite quando la patch viene disinstallata. Non vengono eseguite quando il prodotto viene disinstallato. Usare l' [opzione di disinstallazione patch di azione personalizzata](custom-action-patch-uninstall-option.md) e questa tabella per eseguire un'operazione personalizzata solo quando la patch viene disinstallata.

Una patch può aggiornare un'azione personalizzata fornita nel pacchetto originale (file con estensione msi). Per eseguire la versione aggiornata dell'azione personalizzata quando la patch viene disinstallata, contrassegnare l'azione personalizzata con l'attributo **msidbCustomActionTypePatchUninstall** nel pacchetto originale.

 

 



