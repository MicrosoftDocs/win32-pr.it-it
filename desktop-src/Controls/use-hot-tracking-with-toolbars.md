---
title: Come usare Hot-Tracking con le barre degli strumenti
description: Quando un puntatore del mouse viene posizionato su un elemento, l'elemento diventa attivo. Se è abilitata la funzionalità di rilevamento a caldo, l'elemento critico viene evidenziato. Per impostazione predefinita, una barra degli strumenti creata con lo \_ stile TBSTYLE flat o un oggetto che utilizza stili visivi supporta il rilevamento a caldo.
ms.assetid: E77B15D7-F0C9-41F7-8BE9-30260FA4BB0C
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a486407b8dafade1e3bba083c5a56f3a9be2adcf
ms.sourcegitcommit: f0ca63c18dc52c357d3398af7be766d2bdd40be7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/17/2020
ms.locfileid: "104046462"
---
# <a name="how-to-use-hot-tracking-with-toolbars"></a>Come usare Hot-Tracking con le barre degli strumenti

Quando un puntatore del mouse viene posizionato su un elemento, l'elemento diventa attivo. Se è abilitata la funzionalità di rilevamento a caldo, l'elemento critico viene evidenziato. Per impostazione predefinita, una barra degli strumenti creata con lo stile [**TBSTYLE \_ Flat**](toolbar-control-and-button-styles.md) o un oggetto che utilizza [stili visivi](themes-overview.md)supporta il rilevamento a caldo.

Per il rilevamento a caldo è necessario creare elenchi di immagini; non è quindi possibile usare il messaggio [**TB \_ ADDBITMAP**](tb-addbitmap.md) o la funzione [**CreateToolbarEx**](/windows/desktop/api/Commctrl/nf-commctrl-createtoolbarex) per creare la barra degli strumenti.

Quando il mouse viene spostato su un pulsante della barra degli strumenti, il pulsante viene indicato per evidenziarlo. Nell'illustrazione seguente viene mostrata una barra degli strumenti con rilevamento a caldo abilitato; il puntatore del mouse è stato spostato sul pulsante Salva quando è stata eseguita la cattura dello schermo.

![Screenshot di una finestra di dialogo con una barra degli strumenti di tre elementi; l'icona selezionata è delineata](images/tb-withstyles.png)

Se si vuole modificare la bitmap di un pulsante della barra degli strumenti quando lo stato del controllo cambia, archiviare le diverse immagini negli [elenchi di immagini](image-lists.md). Alcune applicazioni, ad esempio, dispongono di pulsanti della barra degli strumenti neri e bianchi che diventano colorate quando vengono selezionate. Le due diverse immagini vengono archiviate in elenchi di immagini. Le barre degli strumenti supportano l'utilizzo di un massimo di tre elenchi di immagini. In genere, un'applicazione dispone di un elenco di immagini predefinito, disabilitato e con rilevamento attivo. Per impostare e recuperare elenchi di immagini per i pulsanti della barra degli strumenti caldi, usare i messaggi [**TB \_ SETHOTIMAGELIST**](tb-sethotimagelist.md) e [**TB \_ GETHOTIMAGELIST**](tb-gethotimagelist.md) .

## <a name="what-you-need-to-know"></a>Informazioni importanti

### <a name="technologies"></a>Tecnologie

-   [Controlli Windows](window-controls.md)

### <a name="prerequisites"></a>Prerequisiti

-   C/C++
-   Programmazione dell'interfaccia utente di Windows

## <a name="instructions"></a>Istruzioni

### <a name="use-hot-tracking-with-a-toolbar"></a>Usare Hot-Tracking con una barra degli strumenti

Nell'esempio di codice seguente viene creato, compilato e assegnato un elenco di immagini per i pulsanti di scelta rapida.


```C++
// Create the image list, himlHot.
g_himlHot = ImageList_Create(MYICON_CX,MYICON_CY,ILC_COLOR8,0,4);

// Load a bitmap from a resource file, and add the images to the image list.
// Note that the bitmap contains four images.

hBitmapHot = LoadBitmap(g_hinst, MAKEINTRESOURCE(IDB_HOT));

ImageList_Add(g_himlHot, hBitmapHot, NULL);
   
// Set the image list. 
SendMessage(hwndTB, TB_SETHOTIMAGELIST, 0, (LPARAM)g_himlHot);
   
// Loop to fill the array of TBBUTTON structures.  
for(i=0;i<MAX_BUTTONS;i++)
{
    tbArray[i].iBitmap   = i;                   // Bitmap from image list.
    tbArray[i].idCommand = IDM_BUTTONSTART + i;
    tbArray[i].fsState   = TBSTATE_ENABLED;
    tbArray[i].fsStyle   = BTNS_DROPDOWN;
    tbArray[i].dwData    = 0;
    tbArray[i].iString   = i;
}

DeleteObject(hBitmapHot);    // Delete the loaded bitmap.
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Utilizzo di controlli Toolbar](using-toolbar-controls.md)
</dt> <dt>

[Demo sui controlli comuni di Windows (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 




