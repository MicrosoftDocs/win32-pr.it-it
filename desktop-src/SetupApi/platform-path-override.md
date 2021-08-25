---
description: Override del percorso della piattaforma
ms.assetid: f430fd9a-f865-4cdb-b0ea-4e6d79913308
title: Override del percorso della piattaforma
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c63cc1e6ba4b1cb53c26e380eeab95a96091d5159e8356d8f7067529a6b589d6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119992621"
---
# <a name="platform-path-override"></a>Override del percorso della piattaforma

La [**funzione SetupSetPlatformPathOverride**](/windows/desktop/api/Setupapi/nf-setupapi-setupsetplatformpathoverridea) viene usata per impostare un override del percorso della piattaforma per un computer di destinazione quando si lavora con file INF da un computer diverso. Di conseguenza, può fare riferimento a una piattaforma diversa da quella in cui è attualmente in esecuzione. Per la gestione delle origini multimediali, può fare riferimento a piattaforme non più supportate, ad esempio Alpha, MIPS e PPC. Rimuove l'override del percorso della piattaforma se non ne viene specificato nessuno.

Dopo che un override del percorso della piattaforma è stato impostato da una chiamata a [**SetupSetPlatformPathOverride,**](/windows/desktop/api/Setupapi/nf-setupapi-setupsetplatformpathoverridea)qualsiasi funzione di installazione che accoda le operazioni di copia dei file esaminerà il componente finale del percorso di origine. Se il componente finale corrisponde al nome della piattaforma dell'utente, la funzione di installazione lo sostituirà con la stringa di override impostata da **SetupSetPlatformPathOverride.**

Ad esempio, quando si installano i driver della stampante in un server MIPS, è possibile installare i driver per tutte le piattaforme supportate. L'accodamento dei file normalmente installerebbe i file specificati nelle sezioni dipendenti da MIPS del file INF, con percorsi di origine, ad esempio \\ \\ \\ mips di \\ origine radice. Per installare i file per una seconda piattaforma, è necessario chiamare [**SetupSetPlatformPathOverride**](/windows/desktop/api/Setupapi/nf-setupapi-setupsetplatformpathoverridea) con *Override* che indica la piattaforma sostitutiva. Se il percorso indicato da *Override* contiene il valore stringa "alpha", le operazioni di copia dei file inviate alla coda con un percorso di origine mips di origine radice modificherebbero il percorso di origine in alpha di origine \\ \\ \\ \\ \\ \\ \\ \\ radice. È necessario ripetere questo processo per ogni piattaforma di interesse.

 

 



