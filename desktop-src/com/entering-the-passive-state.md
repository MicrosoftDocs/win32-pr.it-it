---
title: Immissione dello stato passivo
description: Immissione dello stato passivo
ms.assetid: 544760e6-1706-4384-8e17-8971f0e0c5f1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9f98a30117174c5953c19cc9e1092ebf79403e0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856781"
---
# <a name="entering-the-passive-state"></a>Immissione dello stato passivo

La chiusura degli oggetti forza un oggetto incorporato o collegato nello stato passivo. Viene in genere avviato dall'interfaccia utente dell'applicazione server OLE, ad esempio quando l'utente seleziona il comando file Close. In questo caso, l'applicazione server OLE invia una notifica al contenitore, che rilascia il conteggio dei riferimenti nell'oggetto. Quando tutti i riferimenti all'oggetto sono stati rilasciati, l'oggetto può essere liberato. Quando tutti gli oggetti sono stati liberati, l'applicazione server OLE può terminare in modo sicuro.

Un'applicazione contenitore può anche avviare la chiusura degli oggetti. Per chiudere un oggetto, il contenitore rilascia il conteggio dei riferimenti dopo aver completato un'operazione di salvataggio facoltativa. È possibile progettare contenitori per rilasciare oggetti quando vengono disattivati dopo una sessione di attivazione sul posto, consentendo all'utente di fare clic all'esterno dell'oggetto senza perdere la sessione di modifica attiva.

 

 




