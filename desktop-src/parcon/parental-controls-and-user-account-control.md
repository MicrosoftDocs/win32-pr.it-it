---
description: Controlli padre e controllo dell'account utente
ms.assetid: dc7c322a-f534-4dda-8c62-aa628a7b91bc
title: Controlli padre e controllo dell'account utente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7798661a7cadc4d497791925c83cdfa684b252a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311835"
---
# <a name="parental-controls-and-user-account-control"></a>Controlli padre e controllo dell'account utente

Il controllo dell'account utente (UAC) determinerà la presenza di account utente standard e amministratore protetto. Un amministratore protetto viene eseguito con gli stessi diritti di un utente standard in base all'utilizzo normale. Per le operazioni con privilegi:

-   Verrà visualizzata la finestra di dialogo interfaccia utente credenziali che richiede l'immissione di un nome utente e di una password per un amministratore protetto o un amministratore predefinito.
-   Verrà visualizzata la finestra di dialogo interfaccia utente di consenso, che richiede la selezione di Consenti per continuare.

È importante notare che il controllo dell'account utente viene implementato in base al processo, quindi un processo viene eseguito con privilegi elevati. In genere, non è adatto da un punto di vista della sicurezza per eseguire applicazioni di grandi dimensioni come sempre con privilegi elevati. Per i controlli padre, il codice che deve modificare le impostazioni deve essere isolato da una delle due opzioni di implementazione:

1.  Creare un file eseguibile di piccole dimensioni per la gestione delle impostazioni contrassegnata nel manifesto come che richiede diritti amministrativi. La chiamata del file eseguibile provocherà la visualizzazione dell'interfaccia utente di consenso o credenziali prima di consentire l'esecuzione del processo.
2.  Fornire le interfacce COM in una DLL del prodotto che consenta la chiamata per la documentazione del controllo dell'account utente. In questo modo verrà visualizzata anche l'interfaccia utente di consenso o credenziali appropriata.

 

 



