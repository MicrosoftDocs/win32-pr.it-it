---
title: Barre di stato (nozioni di base sulla progettazione)
description: Una barra di stato è un'area nella parte inferiore di una finestra primaria che visualizza informazioni sullo stato della finestra corrente (ad esempio, il modo in cui viene visualizzato e come), le attività in background (ad esempio la stampa, l'analisi e la formattazione) o altre informazioni contestuali, ad esempio lo stato della selezione e della tastiera.
ms.assetid: 09dc03d9-d730-4f03-86a8-7b39d9a55369
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 8f65d104f59cd0aec0c242d623f83c410c22f48d
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/10/2021
ms.locfileid: "104234439"
---
# <a name="status-bars-design-basics"></a>Barre di stato (nozioni di base sulla progettazione)

> [!NOTE]
> Questa guida alla progettazione è stata creata per Windows 7 e non è stata aggiornata per le versioni più recenti di Windows. Gran parte delle linee guida si applica ancora in linea di principio, ma la presentazione e gli esempi non riflettono le [linee guida di progettazione correnti](/windows/uwp/design/).

Una barra di stato è un'area nella parte inferiore di una finestra primaria che visualizza informazioni sullo stato della finestra corrente (ad esempio, il modo in cui viene visualizzato e come), le attività in background (ad esempio la stampa, l'analisi e la formattazione) o altre informazioni contestuali, ad esempio lo stato della selezione e della tastiera.

Le barre di stato indicano in genere lo stato tramite testo e icone, ma possono anche avere indicatori di stato, nonché i menu per i comandi e le opzioni correlate allo stato.

![screenshot della barra di stato tipica ](images/ctrl-status-bars-image1.png)

Una barra di stato tipica.

> [!Note]  
> Le linee guida correlate all' [area di notifica](winenv-notification.md) sono presentate in un articolo separato.

 

## <a name="is-this-the-right-user-interface"></a>Si tratta dell'interfaccia utente corretta?

Per decidere, prendi in considerazione queste domande:

-   **Lo stato è pertinente quando gli utenti utilizzano attivamente altri programmi?** In tal caso, utilizzare le [Icone dell'area di notifica](winenv-notification.md).
-   **È necessario che l'elemento di stato visualizzi le notifiche?** In tal caso, è necessario utilizzare un'icona dell'area di notifica.
-   **La finestra è una finestra primaria?** In caso contrario, non usare una barra di stato. Le finestre di dialogo, le procedure guidate, i pannelli di controllo e le finestre delle proprietà non devono avere barre di stato.
-   **Le informazioni sono relative allo stato principale?** In caso contrario, non usare una barra di stato. Le barre di stato non devono essere usate come [barra dei menu](cmd-menus.md) secondaria o [barra degli strumenti](cmd-toolbars.md).
-   **Le informazioni spiegano come usare il controllo selezionato?** In caso affermativo, visualizzare le informazioni accanto al controllo associato usando invece una spiegazione supplementare o un'etichetta di istruzione.
-   **Lo stato è utile e pertinente? Ovvero, è probabile che gli utenti modifichino il proprio comportamento in seguito a queste informazioni?** In caso contrario, non visualizzare lo stato o inserirlo in un file di log.
-   **Lo stato è critico? È richiesta un'azione immediata?** In tal caso, visualizzare le informazioni in un modulo che richiede attenzione e che non possono essere facilmente ignorate, ad esempio una finestra di [dialogo](win-dialog-box.md) o all'interno della finestra principale.

    ![screenshot della barra di stato ' errore certificato ' rosso ](images/ctrl-status-bars-image2.png)

    Barra degli indirizzi rossa in Windows Internet Explorer.

-   **Il programma è destinato principalmente agli utenti principianti?** Gli utenti inesperti non sono in genere a conoscenza delle barre di stato, quindi riconsiderare l'uso delle barre di stato in questo caso.

## <a name="design-concepts"></a>Concetti relativi alla progettazione

Le barre di stato sono un ottimo modo per fornire informazioni sullo stato senza interrompere gli utenti o suddividere il flusso. Tuttavia, le barre di stato sono facili da ignorare. Quindi, in realtà, molti utenti non notano alcuna barra di stato.

La soluzione a questo problema non è richiedere l'attenzione dell'utente usando icone vistosi, animazioni o lampeggianti, ma per progettare questa limitazione. A questo scopo:

-   **Verificare che le informazioni sullo stato siano utili e pertinenti.** In caso contrario, non specificare una barra di stato.
-   **Le barre di stato non vengono utilizzate per informazioni cruciali.** Gli utenti non devono mai sapere cosa si trova nella barra di stato. Se gli utenti devono visualizzarlo, non inserirlo in una barra di stato.

**Se si esegue una sola operazione...**

Verificare che le informazioni sulla barra di stato siano utili e pertinenti ma non cruciali.

## <a name="usage-patterns"></a>Modelli di utilizzo

Le barre di stato hanno diversi modelli di utilizzo:



|                                                                                                                                    |                                                                                                                                                                                                                                 |
|------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Stato corrente della finestra**<br/> Mostra l'origine degli elementi visualizzati insieme alle modalità di visualizzazione <br/>              | ![screenshot della barra di stato ' location ' ](images/ctrl-status-bars-image3.png)<br/> In questo esempio, la barra di stato Visualizza il percorso del documento.<br/>                                                         |
| **Progress**<br/> Mostra lo stato di avanzamento delle attività in background, con un indicatore di stato determinato o un'animazione. <br/> | ![screenshot della barra di stato con indicatore di stato ](images/ctrl-status-bars-image4.png)<br/> In questo esempio, la barra di stato include un indicatore di stato per visualizzare il caricamento della pagina Web in una finestra di Internet Explorer.<br/> |
| **Informazioni contestuali**<br/> Mostra informazioni contestuali sulle operazioni attualmente svolte dall'utente. <br/>              | ![screenshot della barra di stato che mostra il numero di pixel ](images/ctrl-status-bars-image5.png)<br/> In questo esempio Microsoft Paint Mostra le dimensioni della selezione in pixel.<br/>                                           |



 

## <a name="guidelines"></a>Indicazioni

### <a name="general"></a>Generale

-   Si consiglia di fornire un comando della barra di stato di visualizzazione se solo alcuni utenti necessitano delle informazioni sulla barra di stato. Per impostazione predefinita, nascondere la barra di stato se la maggior parte degli utenti non è necessaria.
-   Non utilizzare la barra di stato per spiegare gli elementi della barra dei menu. Questo modello di guida non è individuabile.

### <a name="presentation"></a>Presentazione

-   Disabilitare lo stato modale che non si applica. Lo stato modale include gli Stati della tastiera e del documento.
-   Rimuovere lo stato non modale che non si applica.
-   Presentare le informazioni sullo stato nell'ordine seguente: stato della finestra corrente; corso e informazioni contestuali.

### <a name="icons"></a>Icone

-   Scegliere la progettazione delle icone di stato facilmente riconoscibili. Preferisce icone con strutture univoche su icone quadrate o rettangolari.
-   Usare le vaste delle sole rosse, gialle e verdi solo per comunicare informazioni sullo stato. In caso contrario, tali icone sono confuse.

    **Corretto:**

    ![screenshot della barra di stato con icone blu ](images/ctrl-status-bars-image6.png)

    **Non corretto:**

    ![screenshot della barra di stato con un'icona rossa ](images/ctrl-status-bars-image7.png)

    Nell'esempio errato, l'icona rossa suggerisce inavvertitamente un errore, creando confusione.

-   Usare le variazioni delle icone o le sovrapposizioni per indicare le modifiche dello stato o dello stato. Usare le variazioni delle icone per visualizzare le modifiche apportate a quantità o punti di forza. Per altri tipi di stato, usare le sovrimpressioni standard seguenti: 

    |                                                                                               |                                  |
    |-----------------------------------------------------------------------------------------------|----------------------------------|
    | **Sovrapposizione**<br/>                                                                        | **Status**<br/>            |
    | ![screenshot dell'icona di avviso ](images/ctrl-status-bars-image8.png)<br/>                | Avviso<br/>               |
    | ![screenshot dell'icona di errore ](images/ctrl-status-bars-image9.png)<br/>                  | Errore<br/>                 |
    | ![screenshot dell'icona disabilitata/disconnessa ](images/ctrl-status-bars-image10.png)<br/> | Disabilitato/disconnesso<br/> |
    | ![screenshot dell'icona bloccata/offline ](images/ctrl-status-bars-image11.png)<br/>       | Bloccato/offline<br/>       |

    

     

-   Non modificare lo stato troppo spesso. Le icone della barra di stato non devono essere rumorose, instabili o richiedere attenzione. L'occhio è sensibile alle modifiche apportate al campo periferico della visione, quindi le modifiche di stato devono essere minime.
-   Per le icone che forniscono informazioni importanti sullo stato, preferire le etichette sul posto.
-   Le icone della barra di stato senza etichetta devono contenere descrizioni comandi.

Per altre informazioni, vedere [Icone](vis-icons.md).

### <a name="interaction"></a>Interazione

-   Rendere interattiva un'area della barra di stato per consentire agli utenti di accedere direttamente a comandi e opzioni correlati.
    -   Usare un controllo che sembra e si comporta come un [pulsante di menu](ctrl-command-buttons.md) o un pulsante di menu combinato. Queste aree della barra di stato devono disporre di una freccia a discesa per indicare che sono selezionabili.
    -   Visualizzare il menu facendo clic con il pulsante destro del mouse sulla freccia giù, non sul mouse.
    -   Non supporta il pulsante destro del mouse o il doppio clic. Gli utenti non si aspettano tali interazioni in una barra di stato, quindi non è probabile che ne vengano tentate.
-   Visualizza le descrizioni comandi al passaggio del mouse.

## <a name="text"></a>Testo

-   In genere, usare etichette concise. Taglia il testo che può essere eliminato.
-   Preferisce i frammenti di frase, senza la punteggiatura finale. Usare le frasi complete (con la punteggiatura finale) solo quando i frammenti di frase non sono significativamente più brevi.
-   Per le etichette di stato facoltative, indicare il comportamento dell'operazione con un'etichetta che inizia con un verbo (form gerundio) e termina con i puntini di sospensione. Ad esempio: "copia...". Questa etichetta può variare in modo dinamico se l'operazione ha più passaggi o sta elaborando più oggetti.
-   Non usare colore, grassetto o corsivo per enfatizzare il testo della barra di stato.
-   Per le linee guida per la formulazione della descrizione comando, vedere [Tooltips and infotip](ctrl-tooltips-and-infotips.md).

## <a name="documentation"></a>Documentazione

Vedere barre di stato come barre di stato, non righe di stato o altre varianti. Esempio: "il numero di pagina corrente è visualizzato sulla barra di stato."

 

