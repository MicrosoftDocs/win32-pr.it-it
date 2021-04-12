---
description: Una sequenza di finestra di dialogo FirstRun raccoglie il nome utente, il nome della società e le informazioni sull'ID prodotto. Il programma di installazione verifica l'ID prodotto durante la finestra di dialogo.
ms.assetid: bb77296f-705a-4409-b2ca-a76bbaf7ea57
title: Finestra di dialogo FirstRun
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b2024683d7a10395340a18ddd2015b94e1207bf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226618"
---
# <a name="firstrun-dialog"></a>Finestra di dialogo FirstRun

Una sequenza di finestra di dialogo FirstRun raccoglie il nome utente, il nome della società e le informazioni sull'ID prodotto. Il programma di installazione verifica l'ID prodotto durante la finestra di dialogo.

Una sequenza della finestra di dialogo FirstRun non fa in genere parte della sequenza di azione e viene invece chiamata dalla funzione [**MsiCollectUserInfo**](/windows/desktop/api/Msi/nf-msi-msicollectuserinfoa) alla prima esecuzione del prodotto.

Un autore di un pacchetto del programma di installazione può utilizzare la sequenza della finestra di dialogo modello o creare una sequenza diversa. La sequenza della finestra di dialogo richiede tuttavia che l'utente abbia impostato le proprietà seguenti:

-   [**Username**](username.md) (proprietà)
-   [**CompanyName**](companyname.md) (proprietà)
-   Proprietà [**codice PIDKEY**](pidkey.md)

L'ID prodotto verrà convalidato durante la finestra di dialogo mediante l' [azione ValidateProductID](validateproductid-action.md) o [ValidateProductID ControlEvent](validateproductid-controlevent.md).

Se l'ID prodotto è impostato come proprietà nella riga di comando o da una trasformazione, è necessario che l'utente immetta nuovamente l'ID prodotto durante la finestra di dialogo di prima esecuzione possa essere eluso controllando la visualizzazione utilizzando la proprietà [**ProductID**](productid.md) . Dopo la corretta convalida dell'ID prodotto, la proprietà **ProductID** è impostata sull'ID prodotto completo e valido.

 

 



