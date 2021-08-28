---
description: Questa tabella temporanea abilita l'opzione custom action patch uninstall per le azioni personalizzate aggiunte o aggiornate da una patch.
ms.assetid: 2d4a934f-e245-4d0a-b8bf-52457107ac08
title: MsiTransformView
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e1b6c46ebfcfb82ee23ce6acec998490f53fe67
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/26/2021
ms.locfileid: "122882239"
---
# <a name="msitransformview"></a>MsiTransformView

Questa tabella temporanea abilita [l'opzione custom action patch uninstall per](custom-action-patch-uninstall-option.md) le azioni personalizzate aggiunte o aggiornate da una patch.

Se una patch aggiunge o aggiorna un'azione personalizzata con l'attributo **msidbCustomActionTypePatchUninstall,** il programma di installazione di Windows esegue l'azione personalizzata nuova o aggiornata quando la patch viene disinstallata. Windows Il programma di installazione rende disponibili gli aggiornamenti all'interno della patch disinstallata per l'azione personalizzata di disinstallazione della patch. La patch deve includere una tabella *&lt; PatchGUID &gt;* MsiTransformView per fornire queste informazioni Windows Installer. Le informazioni in questa tabella sono disponibili per qualsiasi azione personalizzata immediata e non sono disponibili per le azioni personalizzate posticipate.

**[Windows Installer 4.0 e versioni precedenti:](not-supported-in-windows-installer-4-0.md)** Non supportato. [L'opzione custom action patch uninstall è](custom-action-patch-uninstall-option.md) disponibile a partire da Windows Installer 4.5.

Questa tabella deve essere denominata MsiTransformView *&lt; PatchGUID &gt;* Table, dove *&lt; PatchGUID &gt;* è il GUID che identifica in modo univoco la patch. La tabella *&lt; PatchGUID &gt;* MsiTransformView include le colonne seguenti.



| Colonna  | Tipo                         | Chiave | Nullable |
|---------|------------------------------|-----|----------|
| Tabella   | [Identificatore](identifier.md) | S   | N        |
| Colonna  | [Text](text.md)             | S   | N        |
| Riga     | [Text](text.md)             | S   | S        |
| Dati    | [Text](text.md)             | N   | S        |
| Corrente | [Text](text.md)             | N   | S        |



 

## <a name="column"></a>Colonna

<dl> <dt>

<span id="Table"></span><span id="table"></span><span id="TABLE"></span>Tavolo
</dt> <dd>

Nome di una tabella di database modificata.

</dd> <dt>

<span id="Column"></span><span id="column"></span><span id="COLUMN"></span>Colonna
</dt> <dd>

Nome di una colonna di tabella modificata o INSERT, DELETE, CREATE o DROP.

</dd> <dt>

<span id="Row"></span><span id="row"></span><span id="ROW"></span>Riga
</dt> <dd>

Elenco dei valori di chiave primaria separati da tabulazioni. I valori di chiave primaria Null sono rappresentati da un singolo spazio. Un valore Null in questa colonna indica una modifica dello schema.

</dd> <dt>

<span id="Data"></span><span id="data"></span><span id="DATA"></span>Dati
</dt> <dd>

Dati, nome di un flusso di dati o definizione di colonna.

</dd> <dt>

<span id="Current"></span><span id="current"></span><span id="CURRENT"></span>Corrente
</dt> <dd>

Valore corrente del database di riferimento o colonna di un numero.

</dd> </dl>

## <a name="remarks"></a>Commenti

Le azioni personalizzate di disinstallazione della patch vengono eseguite quando la patch viene disinstallata. Non vengono eseguiti quando il prodotto viene disinstallato. Usare [l'opzione custom action patch uninstall e](custom-action-patch-uninstall-option.md) questa tabella per eseguire un'operazione personalizzata solo quando la patch viene disinstallata.

Una patch può aggiornare un'azione personalizzata fornita nel pacchetto originale (.msi file. Per eseguire la versione aggiornata dell'azione personalizzata quando la patch viene disinstallata, contrassegnare l'azione personalizzata con l'attributo **msidbCustomActionTypePatchUninstall** nel pacchetto originale.

 

 



