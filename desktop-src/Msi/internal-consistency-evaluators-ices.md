---
description: Gli analizzatori di coerenza interni, detti anche CIEM, sono azioni personalizzate scritte in VBScript, JScript o come DLL o EXE.
ms.assetid: 0789103d-ae34-46be-a9fb-093e066d6d4b
title: Analizzatori di coerenza interni-CIEM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77be6e2bf33bbe348acab45191782a211ea4663a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318286"
---
# <a name="internal-consistency-evaluators---ices"></a>Analizzatori di coerenza interni-CIEM

Gli analizzatori di coerenza interni, detti anche CIEM, sono azioni personalizzate scritte in VBScript, JScript o come DLL o EXE. Quando vengono eseguite, le azioni personalizzate analizzano il database per verificare la presenza di voci nei record del database valide quando vengono esaminate singolarmente, ma che possono causare comportamenti non corretti nel contesto dell'intero database. Si noti che questa operazione è diversa rispetto alla convalida eseguita sui singoli record con [**MsiViewModify**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify).

La [tabella Component](component-table.md) , ad esempio, può elencare diversi componenti che sono tutti validi se testati singolarmente con [**MsiViewModify**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify). Tuttavia, **MsiViewModify** non rileva l'errore quando due componenti utilizzano lo stesso [GUID](guid.md) del codice componente. L'azione personalizzata [ICE08](ice08.md) è progettata per verificare che la tabella dei componenti non contenga GUID duplicati del codice componente.

Le azioni personalizzate ICE restituiscono quattro tipi di messaggi:

-   [**Errori**](merge-errors.md) di I messaggi di errore segnalano la creazione del database che provoca un comportamento non corretto. I GUID di componenti duplicati, ad esempio, fanno sì che il programma di installazione registri erroneamente i componenti.
-   **Avvisi** di I messaggi di avviso segnalano la creazione del database che causa un comportamento errato in alcuni casi. Gli avvisi possono anche segnalare effetti collaterali imprevisti della creazione di database. Ad esempio, immettendo lo stesso nome di proprietà in due condizioni che differiscono solo per la combinazione di maiuscole e minuscole nel nome. Poiché il programma di installazione fa distinzione tra maiuscole e minuscole, il programma di installazione li considera come proprietà diverse.
-   **Errori** I messaggi di errore segnalano l'errore dell'azione personalizzata ICE. L'errore è in genere causato da un database con problemi gravi che il ghiaccio non può neanche essere eseguito.
-   **Informazioni** I messaggi informativi forniscono informazioni dal ghiaccio e non indicano un problema con il database. Spesso si tratta di informazioni sul ghiaccio stesso, ad esempio una breve descrizione. Possono inoltre fornire informazioni sullo stato di avanzamento durante l'esecuzione del ghiaccio.

Per ulteriori informazioni, vedere [utilizzo degli analizzatori di coerenza interni](using-internal-consistency-evaluators.md).

 

 



