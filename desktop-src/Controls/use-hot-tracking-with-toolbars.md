---
title: Come usare le Hot-Tracking con le barre degli strumenti
description: Quando un puntatore del mouse passa su un elemento, l'elemento diventa hot. Se il rilevamento a caldo è abilitato, l'elemento attivo viene evidenziato. Una barra degli strumenti creata con lo stile TBSTYLE FLAT o una che usa gli stili di visualizzazione supporta il rilevamento a caldo \_ per impostazione predefinita.
ms.assetid: E77B15D7-F0C9-41F7-8BE9-30260FA4BB0C
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6dd735828675ca360cfa91aceefb2d76d34252a96aa7b5edb776e3d48a1fcdc5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117829087"
---
# <a name="how-to-use-hot-tracking-with-toolbars"></a>Come usare le Hot-Tracking con le barre degli strumenti

Quando un puntatore del mouse passa su un elemento, l'elemento diventa hot. Se il rilevamento a caldo è abilitato, l'elemento attivo viene evidenziato. Una barra degli strumenti creata con lo stile [**TBSTYLE \_ FLAT**](toolbar-control-and-button-styles.md) o una che usa gli stili di visualizzazione [supporta](themes-overview.md)il rilevamento a caldo per impostazione predefinita.

Il rilevamento a caldo richiede la creazione di elenchi di immagini. Pertanto, non è possibile usare il [**messaggio \_ TB ADDBITMAP**](tb-addbitmap.md) o la [**funzione CreateToolbarEx**](/windows/desktop/api/Commctrl/nf-commctrl-createtoolbarex) per creare la barra degli strumenti.

Quando il puntatore del mouse viene posizionato su un pulsante della barra degli strumenti, il pulsante viene delineato per evidenziarlo. La figura seguente mostra una barra degli strumenti con il rilevamento a caldo abilitato. il puntatore del mouse era posizionato sul pulsante Salva quando è stata ripresa la schermata.

![screenshot di una finestra di dialogo con una barra degli strumenti a tre elementi; l'icona selezionata è delineata](images/tb-withstyles.png)

Se si desidera che una bitmap del pulsante della barra degli strumenti cambi quando lo stato del controllo cambia, archiviare le diverse immagini negli [elenchi di immagini](image-lists.md). Ad esempio, alcune applicazioni hanno pulsanti della barra degli strumenti in bianco e nero che diventano colorati quando vengono selezionati. Le due immagini diverse vengono archiviate negli elenchi di immagini. Le barre degli strumenti supportano l'uso di un massimo di tre elenchi di immagini. In genere un'applicazione dispone di un elenco di immagini predefinito, disabilitato e di rilevamento a caldo. Per impostare e recuperare elenchi di immagini per i pulsanti della barra degli strumenti ad accesso rapido, usare i messaggi [**TB \_ SETHOTIMAGELIST**](tb-sethotimagelist.md) e [**TB \_ GETHOTIMAGELIST.**](tb-gethotimagelist.md)

## <a name="what-you-need-to-know"></a>Informazioni importanti

### <a name="technologies"></a>Tecnologie

-   [Windows Controlli](window-controls.md)

### <a name="prerequisites"></a>Prerequisiti

-   C/C++
-   Windows Interfaccia utente programmazione

## <a name="instructions"></a>Istruzioni

### <a name="use-hot-tracking-with-a-toolbar"></a>Usare Hot-Tracking con una barra degli strumenti

Nell'esempio di codice seguente viene creato, riempito e assegnato un elenco di immagini per i pulsanti di scelta rapida.


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

[Uso dei controlli barra degli strumenti](using-toolbar-controls.md)
</dt> <dt>

[Windows di controlli comuni (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 




