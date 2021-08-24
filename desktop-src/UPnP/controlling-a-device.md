---
title: Controllo di un dispositivo
description: Dopo aver individuato i dispositivi, è possibile controllarli.
ms.assetid: 6d0efb80-d6f5-4b36-a184-19f06afeb2a7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be79d6e6993794a4af972af8538b9b1cd56902c34596197836990028b2761ffa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119656076"
---
# <a name="controlling-a-device"></a>Controllo di un dispositivo

Dopo aver individuato i dispositivi, è possibile controllarli.

**Per visualizzare le proprietà del dispositivo**

1.  Selezionare un dispositivo **dall'elenco Dispositivi** trovati.
2.  Fare clic **su Proprietà dispositivo**. Verrà **visualizzata la finestra** Proprietà dispositivo con le informazioni richieste.

> [!Note]  
> La **funzionalità Visualizza** presentazione non è disponibile nel codice di esempio C++.

 

**Per visualizzare la pagina di presentazione di un dispositivo**

1.  Selezionare un dispositivo **dall'elenco Dispositivi** trovati.
2.  Fare clic **su Visualizza presentazione**. Viene Internet Explorer finestra con la pagina di presentazione richiesta.

> [!Note]  
> **L'oggetto View Service Desc.** La funzionalità non è disponibile nel codice di esempio C++.

 

**Per visualizzare una descrizione del servizio**

1.  È possibile immettere l'URL della descrizione del servizio in **Service Desc. Campo URL.**

    ![URL della descrizione del servizio](images/ucp-url.png)

2.  Fare **clic su Visualizza desc servizio.** Verrà **visualizzata la finestra Visualizzatore** descrizione servizio. È quindi possibile esplorare la descrizione del servizio usando la visualizzazione albero. Questa funzionalità non è disponibile nel codice di esempio C++.

    ![finestra del visualizzatore della descrizione del servizio](images/ucp-serv.png)

    Nella finestra Visualizzatore descrizione servizio è possibile usare cinque comandi.



| Button                 | Azione eseguita                                                                                                                                                                      |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Go                     | Carica il file visualizzato in **Service Desc. Campo URL.**                                                                                                                              |
| Imposta azione             | Selezionare un nome di azione nell'albero della descrizione del servizio e fare clic **su Imposta azione**. Il nome dell'azione viene immesso nel campo Richiama azione della finestra principale del punto di controllo **dell'utilità** **generico.**       |
| Impostare una variabile           | Selezionare un nome di variabile nell'albero della descrizione del servizio e fare clic **su Imposta variabile**. Il nome della variabile viene immesso nel campo **Variabile di query** della finestra principale del punto di controllo dell'utilità generico.  |
| Popolare l'elenco delle variabili | Carica tutti i nomi delle variabili del servizio nell'elenco **Variabile di query** della finestra principale del punto di controllo dell'utilità generico.                                                                            |
| Popolamento dell'elenco di azioni   | Carica tutti i nomi delle azioni del servizio nell'elenco **Richiama** azione della finestra principale del punto di controllo dell'utilità **generico.**                                                                              |



 

**Per controllare un dispositivo**

1.  **Nell'elenco Dispositivi** trovati selezionare il dispositivo da controllare.
2.  **Nell'elenco Scegli servizio** selezionare il servizio che si vuole richiamare o la variabile di stato su cui eseguire la query.

    ![finestra di controllo dei dispositivi](images/ucp-contr.png)

    > [!Note]  
    > Il contenuto **dell'elenco dei servizi** si basa sul dispositivo selezionato nell'elenco **Dispositivi** trovati.

     

3.  Se si vuole trovare il valore di una variabile di stato per il servizio selezionato, immettere il nome della variabile nel campo **Variabile di** query per il servizio. Fare clic su **Query**. I risultati vengono visualizzati nel campo **Query State Value/Action Out Arguments** (Valore stato query/Argomenti uscita azione).
4.  Se si vuole richiamare un'azione per un servizio, immettere il nome dell'azione nel campo **Richiama** azione ed eventuali argomenti nel **campo Argomenti** azione. Fare clic **su Richiama**. I risultati vengono visualizzati nel campo **Valore stato query/Argomenti** azione in uscita, se presenti.

    Il valore restituito, se presente, è contenuto nel primo argomento out.

    > [!Note]  
    > Se sono presenti più argomenti per un'azione, separarli con spazi.

     

5.  Consente di visualizzare le informazioni sugli eventi **nel campo** Eventi per il servizio selezionato.

 

 




