---
description: L smart card interfaccia utente è una singola finestra di dialogo comune che consente all'utente di specificare o cercare un smart card da aprire, ovvero connettersi e usare in un'applicazione.
ms.assetid: a64a617a-b2ae-471f-a88f-a73f0fc3a791
title: Smart Card Interfaccia utente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3b94a82889d196b01f8a1d1ca6af7b4788398d9508accc2d5ca245f7929d9d0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118917331"
---
# <a name="smart-card-user-interface"></a>Smart Card Interfaccia utente

L smart card [](../secgloss/u-gly.md) interfaccia utente è una [](../secgloss/s-gly.md) singola finestra di dialogo comune che consente all'utente di specificare o cercare un smart card da aprire, ovvero connettersi e usare in un'applicazione.

Di seguito sono riportati due modi in cui è possibile usare la finestra di dialogo comune. Entrambi presuppongono che verrà visualizzata l'interfaccia utente della finestra di dialogo. Per altre informazioni, vedere [**OPENCARDNAME**](/windows/desktop/api/Winscard/ns-winscard-opencardnamea).

**Per selezionare un smart card da aprire**

1.  Dichiarare una variabile di tipo **OPENCARDNAME**.
2.  Specificare informazioni sufficienti nella finestra di dialogo comune per restringere la ricerca di un smart card che l'applicazione chiamante sta cercando. Ciò include la specifica **di lpstrGroupNames,** **lpstrCardNames** e **rgguidInterfaces**. Ciò include anche la specifica di una modalità di condivisione e di un protocollo preferiti da usare quando la finestra di dialogo comune si connette alla scheda usando i membri **dwShareMode** e **dwPreferredProtocols** della struttura [**OPENCARDNAME.**](/windows/desktop/api/Winscard/ns-winscard-opencardnamea)
3.  Chiamare la [**funzione GetOpenCardName**](/windows/desktop/api/Winscard/nf-winscard-getopencardnamea) per visualizzare la finestra di dialogo comune all'utente. Verrà visualizzata una semplice riga di informazioni della Guida e, se viene trovata una delle schede richieste, la scheda verrà evidenziata. Per le ricerche di più nomi di scheda, verrà evidenziato il primo lettore che contiene una delle schede preferite.
4.  L'utente seleziona quindi una scheda, fa clic su **OK** e si connette al smart card.

**Per cercare una scheda specifica**

1.  Dichiarare una variabile di tipo **OPENCARDNAME**.
2.  Specificare informazioni sufficienti nella finestra di dialogo comune per restringere la ricerca di un smart card che l'applicazione chiamante sta cercando. Ciò include la specifica **di lpstrGroupNames,** **lpstrCardNames** e **rgguidInterfaces**.
3.  Creare le **Connessione** di callback , **Check** e **Disconnect** e impostare i membri dati **lpfnConnect**, **lpfnCheck** e **lpfnDisconnect** in modo appropriato.
    > [!Note]  
    > Tutte e tre le funzioni e i membri devono essere disponibili quando si usa la finestra di dialogo comune in questo modo.

     

4.  Chiamare la funzione della finestra di dialogo comune [**GetOpenCardName.**](/windows/desktop/api/Winscard/nf-winscard-getopencardnamea)
5.  La finestra di dialogo comune cerca quindi le schede richieste. Se viene trovato un nome di scheda corrispondente o una stringa [*ATR,*](../secgloss/a-gly.md) le funzioni di callback **Connessione**, **Check** e **Disconnect** verranno chiamate in sequenza. Se una scheda passa la routine **Check** (ovvero il callback **Check** restituisce **TRUE),** questa scheda viene evidenziata nella visualizzazione all'utente.
    > [!Note]  
    > Se vengono specificati più nomi di scheda, il primo lettore che contiene una delle schede richieste e passa la routine **Check** sarà la scheda selezionata.

     

6.  Se non viene trovata alcuna corrispondenza, verrà visualizzata una finestra di dialogo comune.

 

 
