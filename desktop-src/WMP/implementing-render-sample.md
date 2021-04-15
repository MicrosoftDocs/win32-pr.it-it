---
title: Esempio di implementazione di render
description: Esempio di implementazione di render
ms.assetid: 5791f6ea-ddad-49e6-8c6f-8093592895d4
keywords:
- Visualizzazioni, esempio Glow
- Visualizzazioni personalizzate, esempio Glow
- Guida per programmatori, visualizzazioni
- esempi, visualizzazione bagliore
- Esempio di visualizzazione bagliore
- Visualizzazioni, funzione render
- Visualizzazioni personalizzate, funzione render
- Funzione render, esempio Glow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dabc816283113a82c1d5d677dfc0ca8e8887d344
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "104517331"
---
# <a name="implementing-render-sample"></a>Esempio di implementazione di render

Il codice seguente viene usato per implementare la funzione **Render** :


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

Una variabile denominata *colori* viene utilizzata per il colore del bagliore ed è dichiarata con **COLORREF**. Tutti i colori devono usare il tipo di dati **COLORREF** .

Una variabile denominata " *livello* " viene usata per lo snapshot del livello di forma d'onda audio. Questo valore dipenderà dal livello di potenza effettivo al momento dello snapshot.

L'istruzione **Switch** viene impostata dal set di impostazioni scelto dall'utente in Windows Media Player. La scelta imposterà *colore* sul colore desiderato (rosso, verde o blu). Tuttavia, il colore esatto sarà determinato dal livello di alimentazione audio. Se, ad esempio, si sceglie il set di impostazioni rosso, il colore sarà un rosso tinta unita, ma sarà più chiaro o più scuro a seconda della forma d'onda audio al momento dello snapshot. Assicurarsi di usare la macro **RBG** per creare il colore.

Viene creato un pennello denominato *hNewBrush* che viene utilizzato per riempire il rettangolo *PRC* fornito da Windows Media Player. La superficie di disegno è il contesto di dispositivo *HDC* fornito da Windows Media Player.

Il pennello viene eliminato da **DeleteObject**. Assicurarsi sempre di eliminare le penne o i pennelli creati.

Al termine del codice di **rendering** , Windows Media Player visualizzerà la grafica *HDC* in una finestra determinata dall'interfaccia usata.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Esempio Glow**](the-glow-sample.md)
</dt> </dl>

 

 




