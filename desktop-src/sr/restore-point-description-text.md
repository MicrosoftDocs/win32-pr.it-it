---
title: Testo Descrizione punto di ripristino
description: Quando un'applicazione chiama la funzione SRSetRestorePoint, può fornire qualsiasi testo come descrizione per il punto di ripristino; Tuttavia, nella tabella seguente viene illustrato il testo della descrizione consigliata.
ms.assetid: e6e1974b-c162-4019-9349-936f3786cb9b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59e90fd1b7d5776c8c3798a68946382cc702b3bd
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104221532"
---
# <a name="restore-point-description-text"></a>Testo Descrizione punto di ripristino

Quando un'applicazione chiama la funzione [**SRSetRestorePoint**](/windows/desktop/api/SRRestorePtAPI/nf-srrestoreptapi-srsetrestorepointa) , può fornire qualsiasi testo come descrizione per il punto di ripristino; Tuttavia, nella tabella seguente viene illustrato il testo della descrizione consigliata.



| Modifica del sistema                            | Tipo di punto di ripristino      | Descrizione            |
|------------------------------------------------|-------------------------|------------------------|
| Installazione delle applicazioni                       | \_installazione applicazione    | *Appname* installato    |
| Modifica dell'applicazione (aggiunta/rimozione di funzionalità) | MODIFICARE \_ le impostazioni        | *Appname* configurato   |
| Rimozione di applicazioni                            | disinstallazione dell'applicazione \_  | *Appname* rimosso      |
| Installazione del driver di dispositivo                     | \_installazione del driver di dispositivo \_ | *Drivername* installato |



 

I programmi di installazione, ad esempio Windows Installer e InstallShield, usano le convenzioni seguenti per il testo della descrizione:

-   Il nome del prodotto segue il verbo. ad esempio, è installato *appname*.
-   Il nome del prodotto può essere usato da solo (*appname*) o il nome del prodotto e il nome della società può essere usato (*MyCompany AppName*).

 

 




