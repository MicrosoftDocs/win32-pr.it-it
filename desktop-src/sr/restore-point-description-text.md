---
title: Testo della descrizione del punto di ripristino
description: Quando un'applicazione chiama la funzione SRSetRestorePoint, può fornire qualsiasi testo come descrizione per il punto di ripristino. Tuttavia, la tabella seguente mostra il testo di descrizione consigliato.
ms.assetid: e6e1974b-c162-4019-9349-936f3786cb9b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd785d143d3eed243e5d80ec261f121817db6187013f70b6f6cc6be0b1c2b790
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120111250"
---
# <a name="restore-point-description-text"></a>Testo della descrizione del punto di ripristino

Quando un'applicazione chiama [**la funzione SRSetRestorePoint,**](/windows/desktop/api/SRRestorePtAPI/nf-srrestoreptapi-srsetrestorepointa) può fornire qualsiasi testo come descrizione per il punto di ripristino. Tuttavia, la tabella seguente mostra il testo di descrizione consigliato.



| Modifica del sistema                            | Tipo di punto di ripristino      | Descrizione            |
|------------------------------------------------|-------------------------|------------------------|
| Installazione delle applicazioni                       | INSTALLAZIONE \_ DELL'APPLICAZIONE    | AppName *installato*    |
| Modifica dell'applicazione (aggiunta/rimozione di funzionalità) | MODIFICARE \_ LE IMPOSTAZIONI        | AppName *configurato*   |
| Rimozione dell'applicazione                            | DISINSTALLAZIONE \_ DELL'APPLICAZIONE  | Rimozione *di AppName*      |
| Installazione del driver di dispositivo                     | INSTALLAZIONE \_ DEL DRIVER DI \_ DISPOSITIVO | DriverName *installato* |



 

I programmi di installazione, ad esempio Windows Installer e InstallShield, usano queste convenzioni per il testo della descrizione:

-   Il nome del prodotto segue il verbo; ad esempio *AppName installato.*
-   Il nome del prodotto può essere usato da solo (*AppName*) o dal nome del prodotto e dal nome della società (*MyCompany AppName*).

 

 




