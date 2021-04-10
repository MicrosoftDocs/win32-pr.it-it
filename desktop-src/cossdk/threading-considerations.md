---
description: Considerazioni sul threading
ms.assetid: 4d27f0b3-3e30-4e88-b2b2-d57218da4ffa
title: Considerazioni sul threading
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8acde9a06802a867cb6a93e7c52be8066ad483c3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049278"
---
# <a name="threading-considerations"></a>Considerazioni sul threading

La registrazione dei componenti in coda COM+ è in grado di essere eseguita nell'Apartment a thread multipli (MTA) del processo o in un Apartment a thread singolo (STA). Quando il registratore viene eseguito in STA, COM+ richiede che ogni Apartment contenente oggetti disponga di una coda di [Accodamento messaggi](/previous-versions/windows/desktop/legacy/ms711472(v=vs.85)) per gestire le chiamate da altri processi e Apartment nello stesso processo. Ciò significa che la funzione lavoro del thread deve avere un ciclo di messaggi. Quando viene creata un'istanza di un componente in coda, il puntatore a interfaccia restituito è sempre un puntatore a interfaccia proxy invece di un puntatore a interfaccia diretta. Il puntatore è effettivamente un riferimento a un'istanza del registratore. Se questo riferimento all'interfaccia di registrazione viene passato a un altro thread, il thread originale deve ancora eseguire il ciclo di messaggi di Windows in modo che il thread di ricezione possa annullare il marshalling dell'interfaccia. In caso contrario, il thread ricevente si blocca in una chiamata a [**CoUnmarshalInterface**](/windows/desktop/api/combaseapi/nf-combaseapi-counmarshalinterface).

Se si usano primitive per sincronizzare i thread, è consigliabile usare [**MsgWaitForMultipleObjects**](/windows/desktop/api/winuser/nf-winuser-msgwaitformultipleobjects) anziché altre funzioni di sincronizzazione. In questo modo viene verificata la presenza di messaggi nella coda, nonché lo stato dell'oggetto di sincronizzazione.

 

 
