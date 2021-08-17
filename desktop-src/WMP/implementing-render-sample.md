---
title: Implementazione dell'esempio di rendering
description: Implementazione dell'esempio di rendering
ms.assetid: 5791f6ea-ddad-49e6-8c6f-8093592895d4
keywords:
- visualizzazioni,Esempio di alone
- visualizzazioni personalizzate,Esempio di alone
- guida alla programmazione, visualizzazioni
- esempi, visualizzazione Alone
- Esempio di visualizzazione alone
- visualizzazioni, funzione Render
- visualizzazioni personalizzate, funzione Render
- Funzione di rendering, esempio di alone
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c00b57f15655468e5bd0000ccc3b5120e19c2af58d5a1ad6b5493b535c7253f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119135574"
---
# <a name="implementing-render-sample"></a>Implementazione dell'esempio di rendering

Il codice seguente viene usato per implementare la **funzione Render:**


```C++
STDMETHODIMP CGlow::Render(TimedLevel *pLevels, HDC hdc, RECT *prc)
{
    COLORREF mycolor;
    int mylevel = pLevels->waveform[0][0];
    
    switch (m_nPreset)
    {
    case PRESET_RED:
        {
        mycolor = RGB( mylevel, 0, 0);    
        }
        break;
    case PRESET_GREEN:
        {
        mycolor = RGB( 0, mylevel, 0);        
        }
        break;
    case PRESET_BLUE:
        {
        mycolor = RGB( 0, 0, mylevel);        
        }
        break;
    }

     HBRUSH hNewBrush = ::CreateSolidBrush( mycolor );
    ::FillRect( hdc, prc, hNewBrush );

    if (hNewBrush)
    {
        ::DeleteObject( hNewBrush );
    }

    return S_OK;
}

```



Ecco una spiegazione del codice:

Una variabile denominata *mycolor* viene usata per il colore dell'alone ed è dichiarata con **COLORREF**. Tutti i colori devono usare il **tipo di dati COLORREF.**

Una variabile denominata *mylevel* viene usata per lo snapshot del livello della forma d'onda audio. Questo valore dipenderà dal livello di potenza effettivo al momento dello snapshot.

**L'istruzione switch** viene impostata dal set di impostazioni scelto dall'utente Windows Media Player. La scelta imposta *mycolor* sul colore desiderato (rosso, verde o blu). Tuttavia, il colore esatto verrà determinato dal livello di potenza audio. Ad esempio, se si sceglie il set di impostazioni rosso, il colore sarà rosso a tinta unita, ma sarà più chiaro o scuro a seconda della forma d'onda audio al momento dello snapshot. Assicurarsi di usare la macro **RBG** per creare il colore.

Viene creato un pennello denominato *hNewBrush* e viene usato per riempire il *rettangolo prc* fornito da Windows Media Player. L'area di disegno è il contesto di dispositivo *hdc* fornito da Windows Media Player.

Il pennello viene eliminato da **DeleteObject.** Assicurarsi sempre di eliminare eventuali penne o pennelli creati.

Al termine **del** codice di rendering, Windows Media Player la grafica *hdc* in una finestra determinata dall'interfaccia usata.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Esempio di alone**](the-glow-sample.md)
</dt> </dl>

 

 




