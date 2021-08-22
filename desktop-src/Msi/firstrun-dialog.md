---
description: Una sequenza di finestre di dialogo FirstRun raccoglie il nome utente, il nome della società e le informazioni sull'ID prodotto. Il programma di installazione verifica l'ID prodotto durante questa finestra di dialogo.
ms.assetid: bb77296f-705a-4409-b2ca-a76bbaf7ea57
title: Finestra di dialogo FirstRun
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de44417014aefb84d2d381166d5a2fceb7f956c4212e9dba31556053c583fef6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119828891"
---
# <a name="firstrun-dialog"></a>Finestra di dialogo FirstRun

Una sequenza di finestre di dialogo FirstRun raccoglie il nome utente, il nome della società e le informazioni sull'ID prodotto. Il programma di installazione verifica l'ID prodotto durante questa finestra di dialogo.

Una sequenza di finestre di dialogo FirstRun in genere non fa parte della sequenza di azioni e viene invece chiamata dalla funzione [**MsiCollectUserInfo**](/windows/desktop/api/Msi/nf-msi-msicollectuserinfoa) alla prima esecuzione del prodotto.

Un autore di un pacchetto del programma di installazione può usare la sequenza del dialogo modello o creare una sequenza diversa. La sequenza di dialogo deve tuttavia fare in modo che l'utente abbia impostato le proprietà seguenti:

-   [**USERNAME**](username.md) - proprietà
-   [**CompanyNAME**](companyname.md) - proprietà
-   [**Proprietà PIDKEY**](pidkey.md)

L'ID prodotto verrà convalidato durante la finestra di dialogo usando l'azione [ValidateProductID](validateproductid-action.md) o [ValidateProductID ControlEvent](validateproductid-controlevent.md).

Se l'ID prodotto viene impostato come proprietà nella riga di comando o tramite una trasformazione, è possibile evitare che l'utente reimima l'ID prodotto durante la finestra di dialogo alla prima esecuzione controllando la visualizzazione usando la [**proprietà ProductID.**](productid.md) Dopo la convalida corretta dell'ID prodotto, la **proprietà ProductID** viene impostata sull'ID prodotto valido completo.

 

 



