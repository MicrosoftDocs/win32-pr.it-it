---
description: Override del percorso della piattaforma
ms.assetid: f430fd9a-f865-4cdb-b0ea-4e6d79913308
title: Override del percorso della piattaforma
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a9a6ae6795b444c44db91d90ecd93efd19ea9dc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319333"
---
# <a name="platform-path-override"></a>Override del percorso della piattaforma

La funzione [**SetupSetPlatformPathOverride**](/windows/desktop/api/Setupapi/nf-setupapi-setupsetplatformpathoverridea) viene utilizzata per impostare un override del percorso della piattaforma per un computer di destinazione quando si utilizzano file inf da un computer diverso. Di conseguenza, può fare riferimento a una piattaforma diversa da quella in cui è attualmente in esecuzione. Per la gestione delle origini multimediali, è possibile fare riferimento a piattaforme che non sono più supportate, ad esempio Alpha, MIPS e PPC. Viene rimossa l'override del percorso della piattaforma se non ne viene specificato alcuno.

Dopo che l'override di un percorso della piattaforma è stato impostato da una chiamata a [**SetupSetPlatformPathOverride**](/windows/desktop/api/Setupapi/nf-setupapi-setupsetplatformpathoverridea), qualsiasi funzione di installazione che accoda le operazioni di copia dei file analizzerà il componente finale del percorso di origine. Se il componente finale corrisponde al nome della piattaforma dell'utente, la funzione di installazione lo sostituirà con la stringa di sostituzione impostata da **SetupSetPlatformPathOverride**.

Ad esempio, quando si installano i driver della stampante in un server MIPS, potrebbe essere necessario installare i driver per tutte le piattaforme supportate. Accodamento dei file normalmente installerebbe i file specificati nelle sezioni dipendenti da MIPS del file INF, con percorsi di origine, ad esempio l' \\ \\ \\ origine radice \\ MIPS. Per installare i file per una seconda piattaforma, è necessario chiamare [**SetupSetPlatformPathOverride**](/windows/desktop/api/Setupapi/nf-setupapi-setupsetplatformpathoverridea) con *override* che indica la piattaforma sostitutiva. Se il percorso indicato da *override* contiene il valore di stringa "Alpha", le operazioni di copia di file inviate alla coda con un percorso di origine di \\ \\ \\ origine radice \\ MIPS avranno il percorso di origine modificato in \\ \\ \\ alfa origine radice \\ . Questo processo viene ripetuto per ogni piattaforma di interesse.

 

 



