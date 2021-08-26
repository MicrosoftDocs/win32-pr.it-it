---
description: Gli analizzatori di coerenza interna, detti anche ICO, sono azioni personalizzate scritte in VBScript, JScript o come DLL o EXE.
ms.assetid: 0789103d-ae34-46be-a9fb-093e066d6d4b
title: Analizzatori di coerenza interna - ICE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 744915d7f484128095e308f390caae75323775b684b38a0184592dc99a2700f4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120043381"
---
# <a name="internal-consistency-evaluators---ices"></a>Analizzatori di coerenza interna - ICE

Gli analizzatori di coerenza interna, detti anche ICO, sono azioni personalizzate scritte in VBScript, JScript o come DLL o EXE. Quando vengono eseguite queste azioni personalizzate, analizzano il database alla ricerca di voci nei record del database che sono valide quando vengono esaminate singolarmente, ma che possono causare un comportamento non corretto nel contesto dell'intero database. Si noti che questa operazione è diversa dalla convalida eseguita sui singoli record [**usando MsiViewModify.**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify)

Ad esempio, la [tabella Component può](component-table.md) elencare diversi componenti che sono tutti validi quando vengono testati singolarmente con [**MsiViewModify.**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify) **MsiViewModify, tuttavia,** non rileva l'errore quando due componenti usano lo stesso [GUID](guid.md) del codice del componente. L'azione [personalizzata ICE08](ice08.md) è progettata per verificare che la tabella Component non contenga GUID di codice componente duplicati.

Le azioni personalizzate ICE restituiscono quattro tipi di messaggi:

-   [**Errori**](merge-errors.md) I messaggi di errore segnalano la creazione di database che causano un comportamento non corretto. Ad esempio, i GUID dei componenti duplicati causano la registrazione non corretta dei componenti da parte del programma di installazione.
-   **Avvisi** I messaggi di avviso segnalano la creazione di database che causa un comportamento non corretto in alcuni casi. Gli avvisi possono anche segnalare effetti collaterali imprevisti della creazione di database. Ad esempio, immettendo lo stesso nome di proprietà in due condizioni che differiscono solo per la combinazione di maiuscole e minuscole nel nome. Poiché il programma di installazione fa distinzione tra maiuscole e minuscole, il programma di installazione li considera come proprietà diverse.
-   **Errori** I messaggi di errore segnalano l'errore dell'azione personalizzata ICE. L'errore è in genere causato da un database con problemi così gravi che l'ice non può essere eseguito.
-   **Informativo** I messaggi informativi forniscono informazioni dal ice e non indicano un problema con il database. Spesso si tratta di informazioni sul ice stesso, ad esempio una breve descrizione. Possono anche fornire informazioni sullo stato di avanzamento durante l'esecuzione del ice.

Per altre informazioni, vedere [Uso degli analizzatori di coerenza interna.](using-internal-consistency-evaluators.md)

 

 



