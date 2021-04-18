---
description: L'interfaccia utente della smart card è una singola finestra di dialogo comune che consente all'utente di specificare o cercare una smart card da aprire, ovvero connettersi e utilizzare in un'applicazione.
ms.assetid: a64a617a-b2ae-471f-a88f-a73f0fc3a791
title: Interfaccia utente della smart card
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc558446516149529e9a98d28aa9fe94f80b2777
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316221"
---
# <a name="smart-card-user-interface"></a>Interfaccia utente della smart card

L' [*interfaccia utente*](../secgloss/u-gly.md) della smart card è una singola finestra di [*dialogo comune*](../secgloss/s-gly.md) che consente all'utente di specificare o cercare una smart card da aprire, ovvero connettersi e utilizzare in un'applicazione.

Di seguito sono illustrati due modi per utilizzare la finestra di dialogo comune. Entrambi presuppongono che venga visualizzata l'interfaccia utente della finestra di dialogo. Per ulteriori informazioni, vedere [**OPENCARDNAME**](/windows/desktop/api/Winscard/ns-winscard-opencardnamea).

**Per selezionare una smart card da aprire**

1.  Dichiarare una variabile di tipo **OPENCARDNAME**.
2.  Fornire informazioni sufficienti nella finestra di dialogo comune per limitare la ricerca di una smart card che l'applicazione chiamante sta cercando. Ciò include la specifica di **lpstrGroupNames**, **lpstrCardNames** e **rgguidInterfaces**. Questo include anche la definizione di una modalità di condivisione preferita e di un protocollo da usare quando la finestra di dialogo comune si connette alla scheda usando i membri **dwShareMode** e **DwPreferredProtocols** della struttura [**OPENCARDNAME**](/windows/desktop/api/Winscard/ns-winscard-opencardnamea) .
3.  Chiamare la funzione [**GetOpenCardName**](/windows/desktop/api/Winscard/nf-winscard-getopencardnamea) per visualizzare la finestra di dialogo comune all'utente. Verrà visualizzata una semplice riga di informazioni della guida e, se viene trovata una delle schede richieste, la scheda verrà evidenziata nella visualizzazione. Per le ricerche con più nomi di carta, verrà evidenziato il primo lettore che contiene una delle schede preferite.
4.  L'utente seleziona quindi una scheda, fa clic su **OK** e si connette alla smart card.

**Per cercare una scheda specifica**

1.  Dichiarare una variabile di tipo **OPENCARDNAME**.
2.  Fornire informazioni sufficienti nella finestra di dialogo comune per limitare la ricerca di una smart card che l'applicazione chiamante sta cercando. Ciò include la specifica di **lpstrGroupNames**, **lpstrCardNames** e **rgguidInterfaces**.
3.  Creare le funzioni di callback **Connect**, **Check** e **Disconnect** e impostare i membri dati **lpfnConnect**, **lpfnCheck** e **lpfnDisconnect** in modo appropriato.
    > [!Note]  
    > Tutte e tre le funzioni e i membri devono essere disponibili quando si utilizza la finestra di dialogo comune in questo modo.

     

4.  Chiamare la funzione della finestra di dialogo comune [**GetOpenCardName**](/windows/desktop/api/Winscard/nf-winscard-getopencardnamea) .
5.  Nella finestra di dialogo comune sarà quindi possibile cercare le schede richieste. Se viene trovato un nome di scheda o una [*stringa ATR*](../secgloss/a-gly.md) corrispondente, le funzioni di callback **Connect**, **Check** e **Disconnect** verranno chiamate in sequenza. Se una scheda supera la routine di **controllo** , ovvero il callback di **controllo** restituisce **true**, questa scheda viene evidenziata nella visualizzazione dell'utente.
    > [!Note]  
    > Se vengono specificati più nomi di schede, il primo lettore che contiene una delle schede richieste e passa la routine di **controllo** sarà la scheda selezionata.

     

6.  Se non viene trovata alcuna corrispondenza, viene visualizzata una finestra di dialogo comune.

 

 
