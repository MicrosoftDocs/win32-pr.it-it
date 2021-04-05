---
title: Esempio di codice di rendering
description: Esempio di codice di rendering
ms.assetid: 14978cf4-47fa-4b2e-ba51-799be873dc8a
keywords:
- Visualizzazioni, codice di esempio
- Visualizzazioni personalizzate, codice di esempio
- Visualizzazioni, funzione render
- Visualizzazioni personalizzate, funzione render
- Funzione render, codice di esempio
- esempi, funzione Render per le visualizzazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a1ee5d00bc1aed5bd8bd91880e43e2ac2d1f6bc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044956"
---
# <a name="sample-render-code"></a>Esempio di codice di rendering

Di seguito è riportato un codice di esempio che usa la funzione **Render** per disegnare una riga sullo schermo. L'altezza della linea è definita dal valore della forma d'onda.


```C++
STDMETHODIMP CStock::Render(TimedLevel *pLevels, HDC hdc, RECT *prc)
{
    // Create new brushes and pens.
    HBRUSH hNewBrush = ::CreateSolidBrush( 0 );
    // Create a new solid pen the color of the foreground.
    HPEN hNewPen = ::CreatePen( PS_SOLID, 0, m_clrForeground );


    // Add the pen to the device context.
    HPEN hOldPen= static_cast<HPEN>(::SelectObject( hdc, hNewPen ));

    // Fill the background with the black brush.
    ::FillRect( hdc, prc, hNewBrush );

    // Get the y value from the waveform.
    int y = pLevels->waveform[0][0];

    // Draw the line from left to right.
    ::MoveToEx( hdc, prc->left, y, NULL);  
    ::LineTo(hdc, prc->right, y); 

    // Delete your brush.
    if (hNewBrush)
    {
        ::DeleteObject( hNewBrush );
    }
    // Delete your pen.
    if (hNewPen)
    {
        ::SelectObject( hdc, hOldPen );
        ::DeleteObject( hNewPen );
    }

    // You're done for this round.
    return S_OK;
}

```



La funzione **Render** è la posizione in cui viene eseguita l'attività principale del codice. Ogni volta che Windows Media Player acquisisce un'istantanea dell'audio, chiamerà questa funzione e il codice verrà eseguito.

Questo codice esegue le attività seguenti. Per informazioni dettagliate sulle funzioni specifiche, vedere Microsoft Windows Platform SDK per Windows a 32 bit.

## <a name="creating-objects"></a>Creazione di oggetti

In genere si useranno le funzioni di disegno disponibili con l'interfaccia di visualizzazione grafica (GDI) di Microsoft Windows. È necessario creare le penne per creare linee e pennelli per riempire le aree.

Viene creato un pennello nero a tinta unita per riempire lo sfondo.

Viene creata una penna a tinta unita per creare una linea. Il colore sarà il colore di primo piano definito dall'interfaccia che visualizzerà la visualizzazione.

## <a name="adding-the-object-to-the-dc"></a>Aggiunta dell'oggetto al controller di dominio

È necessario aggiungere la penna al contesto di dispositivo (DC). Il controller di dominio è la porzione di memoria in cui sono archiviati tutti i dati e gli oggetti del disegno. In sostanza, il controller di dominio è gestione traffico di Windows che tiene traccia di tutti gli elementi grafici.

È necessario *eseguire il cast* dell'oggetto Pen creato e archiviarlo come penna precedente. Usare questa tecnica di codifica per tutte le nuove penne. Questa tecnica è necessaria per la programmazione a 32 bit.

## <a name="filling-in-the-background"></a>Riempimento in background

A questo punto è possibile creare. La funzione **fillRect** riempirà il rettangolo della finestra, come definito dai parametri della funzione **Render** . Il rettangolo è riempito con un pennello nero.

## <a name="getting-audio-data"></a>Recupero di dati audio

Il codice ottiene quindi alcuni dati audio da Windows Media Player. Usando la matrice di forme d'onda, è possibile ottenere il valore corrente della potenza audio nel momento in cui è stato effettuato lo snapshot. In questo caso, si stanno prendendo i dati audio del canale sinistro. Il primo valore nella matrice è il primo 1024th dello snapshot di alimentazione audio.

Queste informazioni verranno usate per visualizzare una riga la cui altezza corrisponderà allo snapshot di Power audio.

## <a name="draw-the-line"></a>Creare la linea

La linea viene disegnata da sinistra a destra usando le funzioni GDI **MoveToEx** e **LineTo** .

Spostare prima di tutto la penna al punto di partenza. In questo caso, x e y vengono utilizzati per definire i valori da sinistra a destra e dall'alto verso il basso che verranno visualizzati dall'utente sullo schermo. X è definito dal rettangolo PRC e in particolare dal valore di PRC->Left. Y è definito come valore dei dati della forma d'onda in quel momento.

Viene quindi disegnato un oggetto line sull'altro lato della finestra. Il punto in cui si richiama la linea è di nuovo un valore x, y. X è definito dal rettangolo PRC, ma questa volta da PRC->right. Y è ancora definito dai dati della forma d'onda ed è uguale al punto da cui è stato avviato, perché si sta disegnando una linea retta da sinistra a destra.

## <a name="clean-up-everything"></a>Pulisci tutto

È necessario eliminare gli oggetti creati. In particolare, è necessario eliminare tutti i pennelli e le penne creati. È consigliabile eliminare penne e pennelli al termine dell'uso.

Se non vengono eliminati prima di terminare l'implementazione della funzione di **rendering** , la visualizzazione si arresterà in modo anomalo in un minuto o meno. È necessario contenere un conteggio delle penne e dei pennelli ed eliminare ogni singolo oggetto. Prestare particolare attenzione a non creare penne all'interno di un ciclo di codice.

Usare la tecnica di codifica fornita nell'esempio per eliminare le penne e i pennelli.

-   **Importante** Elimina le penne e i pennelli.

Al termine della pulizia, assicurarsi di restituire S OK, in \_ modo che Windows Media Player sappia che il disegno è terminato. Al termine, il disegno verrà trasferito alla finestra, verrà eseguito un altro snapshot, il **rendering** chiederà di nuovo al codice di disegnare e così via.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Implementazione di rendering**](implementing-render.md)
</dt> </dl>

 

 




