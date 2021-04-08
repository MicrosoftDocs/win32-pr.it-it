---
title: Controllo di un dispositivo
description: Dopo aver individuato i dispositivi, è possibile controllarli.
ms.assetid: 6d0efb80-d6f5-4b36-a184-19f06afeb2a7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ff91339c67b67de5d3e90eda0ce64ebcc68b9e2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856785"
---
# <a name="controlling-a-device"></a>Controllo di un dispositivo

Dopo aver individuato i dispositivi, è possibile controllarli.

**Per visualizzare le proprietà del dispositivo**

1.  Selezionare un dispositivo nell'elenco **dispositivi trovati** .
2.  Fare clic su **Proprietà dispositivo**. Viene visualizzata la finestra **Proprietà dispositivo** con le informazioni richieste.

> [!Note]  
> La funzionalità di **presentazione della vista** non è disponibile nel codice di esempio C++.

 

**Per visualizzare la pagina di presentazione di un dispositivo**

1.  Selezionare un dispositivo nell'elenco **dispositivi trovati** .
2.  Fare clic su **Visualizza presentazione**. Verrà visualizzata una finestra di Internet Explorer con la pagina di presentazione richiesta.

> [!Note]  
> Il **servizio di visualizzazione desc.** funzionalità non è disponibile nel codice di esempio C++.

 

**Per visualizzare la descrizione di un servizio**

1.  È possibile immettere l'URL della descrizione del servizio nel **servizio desc. Campo URL** .

    ![URL Descrizione servizio](images/ucp-url.png)

2.  Fare clic su **View Service desc.** Viene visualizzata la finestra **Visualizzatore Descrizione servizio** . È quindi possibile esplorare la descrizione del servizio utilizzando la visualizzazione albero. Questa funzionalità non è disponibile nel codice di esempio C++.

    ![finestra Visualizzatore Descrizione servizio](images/ucp-serv.png)

    Nella finestra Visualizzatore Descrizione servizio è possibile utilizzare cinque comandi.



| Pulsante                 | Azione eseguita                                                                                                                                                                      |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Go                     | Carica il file visualizzato nella **Descrizione del servizio. Campo URL** .                                                                                                                              |
| Imposta azione             | Selezionare un nome di azione nell'albero Descrizione servizio e fare clic su **imposta azione**. Il nome dell'azione viene immesso nel campo **azione Invoke** della finestra principale del punto di controllo dell' **utilità generico** .       |
| Impostare una variabile           | Selezionare un nome di variabile nell'albero Descrizione servizio e fare clic su **Imposta variabile**. Il nome della variabile viene immesso nel campo **variabile query** della finestra principale del punto di controllo dell' **utilità generico** . |
| Popola elenco variabili | Carica tutti i nomi delle variabili del servizio nell'elenco delle **variabili di query** della finestra principale del punto di controllo dell' **utilità generica** .                                                                           |
| Popola elenco di azioni   | Carica tutti i nomi di azione del servizio nell'elenco di **azioni Invoke** della finestra principale del punto di controllo dell' **utilità** .                                                                              |



 

**Per controllare un dispositivo**

1.  Dall'elenco **dispositivi trovati** selezionare il dispositivo che si desidera controllare.
2.  Dall'elenco **Scegli servizio** selezionare il servizio da richiamare o la variabile di stato su cui si vuole eseguire la query.

    ![finestra dispositivi di controllo](images/ucp-contr.png)

    > [!Note]  
    > Il contenuto dell' **elenco dei servizi** è basato sul dispositivo selezionato nell'elenco **dispositivi trovati** .

     

3.  Se si desidera individuare il valore di una variabile di stato per il servizio selezionato, immettere il nome della variabile nel campo **variabile query** per servizio. Fare clic su **Query**. I risultati vengono visualizzati nel campo **valore stato query/argomenti di azione** .
4.  Se si desidera richiamare un'azione per un servizio, immettere il nome dell'azione nel campo **azione richiama** e gli eventuali argomenti nel campo **Argomenti azione** . Fare clic su **richiama**. I risultati vengono visualizzati nel campo **valore dello stato della query/argomenti di azione fuori** , se disponibile.

    Il valore restituito, se presente, è contenuto nel primo argomento out.

    > [!Note]  
    > Se sono presenti più argomenti per un'azione, è necessario separarli con spazi.

     

5.  Visualizzare le informazioni sugli eventi nel campo **eventi** per il servizio selezionato.

 

 




