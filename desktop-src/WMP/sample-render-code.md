---
title: Codice di rendering di esempio
description: Codice di rendering di esempio
ms.assetid: 14978cf4-47fa-4b2e-ba51-799be873dc8a
keywords:
- visualizzazioni, codice di esempio
- visualizzazioni personalizzate, codice di esempio
- visualizzazioni,funzione Render
- visualizzazioni personalizzate,funzione Render
- Funzione di rendering, codice di esempio
- esempi,funzione di rendering per le visualizzazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 51265191ba7fd8b5eb9e4b1140990a7713eba08356d01c58097c727ec2fe533e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118569787"
---
# <a name="sample-render-code"></a>Codice di rendering di esempio

Ecco un codice di esempio che usa la **funzione Render** per disegnare una linea sullo schermo. L'altezza della linea è definita dal valore della forma d'onda.


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



La **funzione** Render è la posizione in cui viene eseguito il lavoro principale del codice. Ogni volta Windows Media Player snapshot dell'audio, chiamerà questa funzione e il codice verrà eseguito.

Questo codice esegue le attività seguenti. Per altre informazioni su funzioni specifiche, fare riferimento a Microsoft Windows Platform SDK per Windows a 32 bit.

## <a name="creating-objects"></a>Creazione di oggetti

In genere si usano le funzioni di disegno disponibili con Microsoft Windows Graphical Display Interface (GDI). È necessario creare penne per disegnare linee e pennelli per riempire le aree.

Viene creato un pennello nero a tinta unita per riempire lo sfondo.

Viene creata una penna a tinta unita per disegnare una linea. Il colore sarà il colore di primo piano definito dall'interfaccia che visualizza la visualizzazione.

## <a name="adding-the-object-to-the-dc"></a>Aggiunta dell'oggetto al controller di dominio

È necessario aggiungere la penna al contesto di dispositivo. Il controller di dominio è la parte di memoria in cui vengono archiviati tutti i dati e gli oggetti di disegno. Essenzialmente, il controller di dominio è il gestore del traffico finestra che tiene traccia di tutti gli elementi grafici.

È necessario eseguire *il cast* dell'oggetto penna creato e archiviarlo come penna precedente. Usare questa tecnica di codifica per tutte le nuove penna. Questa tecnica è necessaria per la programmazione a 32 bit.

## <a name="filling-in-the-background"></a>Riempimento dello sfondo

A questo punto è possibile disegnare. La **funzione FillRect** riempirà il rettangolo della finestra, come definito dai parametri della **funzione Render.** Il rettangolo viene riempito con un pennello nero.

## <a name="getting-audio-data"></a>Recupero di dati audio

Successivamente, il codice ottiene alcuni dati audio da Windows Media Player. Usando la matrice della forma d'onda, è possibile ottenere il valore corrente della potenza audio nel momento in cui è stato creato lo snapshot. In questo caso, si prendono i dati audio del canale sinistro. Il primo valore nella matrice è il primo 1024 dello snapshot di alimentazione audio.

Queste informazioni verranno usate per visualizzare una linea la cui altezza corrisponderà all'istantanea di alimentazione audio.

## <a name="draw-the-line"></a>Porre un limite

La linea viene disegnata da sinistra a destra usando le **funzioni GDI MoveToEx** e **LineTo.**

Per prima cosa, spostare la penna nel punto iniziale. In questo caso, x e y vengono usati per definire i valori da sinistra a destra e dall'alto verso il basso che l'utente vedrà sullo schermo. X è definito dal rettangolo prc e in particolare dal valore di prc->sinistra. Y è definito come valore dei dati della forma d'onda in quel momento.

Si disegna quindi una linea sull'altro lato della finestra. Il punto in cui si disegna la linea è di nuovo un valore x, y. X è definito dal rettangolo prc, ma questa volta da prc->destra. Y è ancora definito dai dati della forma d'onda ed è lo stesso del punto da cui si è iniziato, perché si disegna una linea retta da sinistra a destra.

## <a name="clean-up-everything"></a>Pulisci tutto

È necessario eliminare gli oggetti creati. In particolare, è necessario eliminare tutti i pennelli e i pennarelli creati. È buona norma eliminare penna e pennelli al termine dell'uso.

Se non vengono eliminati prima di completare l'implementazione della funzione **Render,** la visualizzazione si arresterà in modo anomalo in un minuto o meno. È necessario mantenere un conteggio delle penne e dei pennelli ed eliminare ogni singolo oggetto. Prestare particolare attenzione a non creare penna all'interno di un ciclo di codice.

Usare la tecnica di codifica illustrata nell'esempio per eliminare le penna e i pennelli.

-   **Importante** Distruggere le penna e i pennelli.

Al termine della pulizia, assicurarsi di restituire S OK in modo che Windows Media Player che il disegno \_ sia terminato. Al termine, il disegno verrà trasferito alla finestra, verrà creato un altro snapshot, **Render** chiederà al codice di disegnare di nuovo e così via.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Implementazione del rendering**](implementing-render.md)
</dt> </dl>

 

 




