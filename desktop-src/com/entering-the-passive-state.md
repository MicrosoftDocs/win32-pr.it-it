---
title: Immissione dello stato passivo
description: Immissione dello stato passivo
ms.assetid: 544760e6-1706-4384-8e17-8971f0e0c5f1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a0a3a93b0ff0bd1c16701c82f271847ee435375112a8e7a03120155928fe1ec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117736855"
---
# <a name="entering-the-passive-state"></a>Immissione dello stato passivo

La chiusura dell'oggetto forza un oggetto incorporato o collegato nello stato passivo. Viene in genere avviata dall'interfaccia utente dell'applicazione server OLE, ad esempio quando l'utente seleziona il comando Chiudi file. In questo caso, l'applicazione server OLE invia una notifica al contenitore, che rilascia il conteggio dei riferimenti sull'oggetto. Quando tutti i riferimenti all'oggetto sono stati rilasciati, l'oggetto può essere liberato. Quando tutti gli oggetti sono stati liberati, l'applicazione server OLE può terminare in modo sicuro.

Un'applicazione contenitore può anche avviare la chiusura dell'oggetto. Per chiudere un oggetto, il contenitore rilascia il conteggio dei riferimenti dopo aver completato un'operazione di salvataggio facoltativa. È possibile progettare contenitori per rilasciare gli oggetti quando vengono disattivati dopo una sessione di attivazione sul posto, consentendo all'utente di fare clic all'esterno dell'oggetto senza perdere la sessione di modifica attiva.

 

 




