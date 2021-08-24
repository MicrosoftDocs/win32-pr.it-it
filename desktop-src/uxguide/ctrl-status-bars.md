---
title: Barre di stato (nozioni di base sulla progettazione)
description: Una barra di stato è un'area nella parte inferiore di una finestra primaria che visualizza informazioni sullo stato della finestra corrente (ad esempio cosa viene visualizzato e come), attività in background (ad esempio stampa, analisi e formattazione) o altre informazioni contestuali (ad esempio la selezione e lo stato della tastiera).
ms.assetid: 09dc03d9-d730-4f03-86a8-7b39d9a55369
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: fa76563adbd3810b48339cc49014441512e3d76a0ac7484ff632f64f635b4cf6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119934235"
---
# <a name="status-bars-design-basics"></a>Barre di stato (nozioni di base sulla progettazione)

> [!NOTE]
> Questa guida di progettazione è stata creata per Windows 7 e non è stata aggiornata per le versioni più recenti di Windows. Gran parte delle linee guida si applica ancora in linea di principio, ma la presentazione e gli esempi non riflettono le [linee guida di progettazione correnti.](/windows/uwp/design/)

Una barra di stato è un'area nella parte inferiore di una finestra primaria che visualizza informazioni sullo stato della finestra corrente (ad esempio cosa viene visualizzato e come), attività in background (ad esempio stampa, analisi e formattazione) o altre informazioni contestuali (ad esempio la selezione e lo stato della tastiera).

Le barre di stato indicano in genere lo stato tramite testo e icone, ma possono anche avere indicatori di stato, nonché menu per comandi e opzioni correlati allo stato.

![Screenshot della barra di stato tipica ](images/ctrl-status-bars-image1.png)

Una barra di stato tipica.

> [!Note]  
> Le linee guida relative [all'area di](winenv-notification.md) notifica sono presentate in un articolo separato.

 

## <a name="is-this-the-right-user-interface"></a>Si tratta dell'interfaccia utente giusta?

Per decidere, prendi in considerazione queste domande:

-   **Lo stato è rilevante quando gli utenti usano attivamente altri programmi?** In tal caso, usare le [icone dell'area di notifica](winenv-notification.md).
-   **L'elemento di stato deve visualizzare le notifiche?** In tal caso, è necessario usare un'icona dell'area di notifica.
-   **La finestra è una finestra primaria?** In caso contrario, non usare una barra di stato. Le finestre di dialogo, le procedure guidate, i pannelli di controllo e le finestre delle proprietà non devono avere barre di stato.
-   **Le informazioni sono principalmente relative allo stato?** In caso contrario, non usare una barra di stato. Le barre di stato non devono essere usate come barra dei menu o barra [degli strumenti](cmd-menus.md) [secondaria.](cmd-toolbars.md)
-   **Le informazioni spiegano come usare il controllo selezionato?** In tal caso, visualizzare le informazioni accanto al controllo associato usando invece una spiegazione supplementare o un'etichetta di istruzione.
-   **Lo stato è utile e pertinente? Ciò significa che è probabile che gli utenti cambino il proprio comportamento in seguito a queste informazioni?** In caso contrario, non visualizzare lo stato o inserirlo in un file di log.
-   **Lo stato è critico? È necessaria un'azione immediata?** In tal caso, visualizzare le informazioni in un modulo che [](win-dialog-box.md) richiede attenzione e non può essere facilmente ignorato, ad esempio una finestra di dialogo o all'interno della finestra primaria stessa.

    ![Screenshot della barra di stato "Errore certificato" rossa ](images/ctrl-status-bars-image2.png)

    Barra degli indirizzi rossa in Windows Internet Explorer.

-   **Il programma è destinato principalmente a utenti non esperti?** Gli utenti meno esperti in genere non sono a conoscenza delle barre di stato, quindi in questo caso è necessario riconsiderare l'uso delle barre di stato.

## <a name="design-concepts"></a>Concetti relativi alla progettazione

Le barre di stato sono un ottimo modo per fornire informazioni sullo stato senza interrompere gli utenti o interrompere il flusso. Tuttavia, le barre di stato sono facili da tralasciare. È così semplice, infatti, che molti utenti non notano affatto le barre di stato.

La soluzione a questo problema non è richiedere l'attenzione dell'utente usando icone, animazioni o flashing, ma progettare per questa limitazione. A questo scopo:

-   **Assicurarsi che le informazioni sullo stato siano utili e rilevanti.** In caso contrario, non specificare affatto una barra di stato.
-   **Non usare le barre di stato per informazioni cruciali.** Gli utenti non devono mai sapere cosa c'è nella barra di stato. Se gli utenti devono visualizzarlo, non inserire il valore in una barra di stato.

**Se si fa una sola cosa...**

Assicurarsi che le informazioni sulla barra di stato siano utili e rilevanti, ma non cruciali.

## <a name="usage-patterns"></a>Modelli di utilizzo

Le barre di stato hanno diversi modelli di utilizzo:



|   Utilizzo                                                                                                                                 |    Esempio                                                                                                                                                                                                                             |
|------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Stato della finestra corrente**<br/> Visualizzare l'origine di ciò che viene visualizzato insieme a tutte le modalità di visualizzazione <br/>              | ![Screenshot di una barra di stato "location" ](images/ctrl-status-bars-image3.png)<br/> In questo esempio la barra di stato visualizza il percorso del documento.<br/>                                                         |
| **Progress**<br/> Mostra lo stato di avanzamento delle attività in background, con un indicatore di stato determinato o un'animazione. <br/> | ![Screenshot della barra di stato con l'indicatore di stato ](images/ctrl-status-bars-image4.png)<br/> In questo esempio la barra di stato include un indicatore di stato per visualizzare il caricamento della pagina Web in una Internet Explorer finestra.<br/> |
| **Informazioni contestuali**<br/> Mostra le informazioni contestuali sull'operazione attualmente in corso da parte dell'utente. <br/>              | ![Screenshot della barra di stato che mostra il numero di pixel ](images/ctrl-status-bars-image5.png)<br/> In questo esempio, Microsoft Paint mostra le dimensioni della selezione in pixel.<br/>                                           |



 

## <a name="guidelines"></a>Indicazioni

### <a name="general"></a>Generale

-   È consigliabile specificare un comando Visualizza barra di stato se solo alcuni utenti necessitano delle informazioni sulla barra di stato. Nascondere la barra di stato per impostazione predefinita se la maggior parte degli utenti non ne ha bisogno.
-   Non usare la barra di stato per spiegare le voci della barra dei menu. Questo modello di guida non è individuabile.

### <a name="presentation"></a>Presentazione

-   Disabilitare lo stato modale che non è applicabile. Lo stato modale include gli stati della tastiera e del documento.
-   Rimuovere lo stato non modale che non è applicabile.
-   Presentare le informazioni sullo stato nell'ordine seguente: stato della finestra corrente; stato di avanzamento; e informazioni contestuali.

### <a name="icons"></a>Icone

-   Scegliere progettazioni di icone di stato facilmente riconoscibili. Preferisce icone con contorni univoci rispetto a icone a forma quadrata o rettangolare.
-   Usare swath di colore rosso puro, giallo e verde solo per comunicare le informazioni sullo stato. In caso contrario, tali icone confondono.

    **Corretto:**

    ![Screenshot della barra di stato con icone blu ](images/ctrl-status-bars-image6.png)

    **Non corretto:**

    ![Screenshot della barra di stato con un'icona rossa ](images/ctrl-status-bars-image7.png)

    Nell'esempio errato, l'icona rossa suggerisce involontariamente un errore, creando confusione.

-   Usare varianti di icona o sovrimpressione per indicare lo stato o le modifiche dello stato. Usare le varianti delle icone per visualizzare le modifiche nelle quantità o nei punti di forza. Per altri tipi di stato, usare le sovrimpressione standard seguenti: 

    | Sovrapposizione (Overlay)                 | Stato            |
    |-----------------------------------------------------------------------------------------------|----------------------------------|
    | ![Screenshot dell'icona di avviso ](images/ctrl-status-bars-image8.png)<br/>                | Avviso<br/>               |
    | ![Screenshot dell'icona di errore ](images/ctrl-status-bars-image9.png)<br/>                  | Errore<br/>                 |
    | ![Screenshot dell'icona disabilitata/disconnessa ](images/ctrl-status-bars-image10.png)<br/> | Disabilitato/Disconnesso<br/> |
    | ![Screenshot dell'icona bloccato/offline ](images/ctrl-status-bars-image11.png)<br/>       | Bloccato/Offline<br/>       |

    

     

-   Non modificare lo stato troppo frequentemente. Le icone della barra di stato non dovrebbero apparire rumorose, instabili o richiedere attenzione. L'occhio è sensibile ai cambiamenti nel campo periferico della vista, quindi le modifiche dello stato devono essere meno sensibili.
-   Per le icone che forniscono informazioni importanti sullo stato, preferire le etichette sul posto.
-   Le icone della barra di stato senza etichetta devono contenere descrizioni comando.

Per altre informazioni, vedere [Icone](vis-icons.md).

### <a name="interaction"></a>Interazione

-   Rendere interattiva un'area della barra di stato per consentire agli utenti l'accesso diretto ai comandi e alle opzioni correlati.
    -   Usare un controllo che ha un aspetto e si comporta come un [pulsante di menu](ctrl-command-buttons.md) o un pulsante di divisione. Queste aree della barra di stato devono avere una freccia a discesa per indicare che è possibile fare clic su di esse.
    -   Visualizzare il menu al clic con il pulsante sinistro del mouse verso il basso, non verso l'alto.
    -   Non supporta il clic con il pulsante destro del mouse o il doppio clic. Gli utenti non si aspettano interazioni di questo tipo in una barra di stato, quindi è probabile che non le tentino.
-   Visualizzare le descrizioni comando al passaggio del mouse.

## <a name="text"></a>Testo

-   In genere, usare etichette concise. Tagliare qualsiasi testo che può essere eliminato.
-   Preferisce i frammenti di frase, senza terminare la punteggiatura. Usare frasi complete (con punteggiatura finale) solo quando i frammenti di frase non sono significativamente più brevi.
-   Per le etichette di stato facoltative, indicare l'operazione eseguita con un'etichetta che inizia con un verbo (forma gerund) e termina con i puntini di sospensione. Ad esempio: "Copia...". Questa etichetta può cambiare dinamicamente se l'operazione ha più passaggi o sta elaborando più oggetti.
-   Non usare il colore, il grassetto o il corsivo per evidenziare il testo della barra di stato.
-   Per le linee guida per la formulazione delle descrizioni comando, vedere [Descrizioni comando e suggerimenti.](ctrl-tooltips-and-infotips.md)

## <a name="documentation"></a>Documentazione

Fare riferimento alle barre di stato come barre di stato, non come righe di stato o altre variazioni. Esempio: "Il numero di pagina corrente viene visualizzato sulla barra di stato".

 

