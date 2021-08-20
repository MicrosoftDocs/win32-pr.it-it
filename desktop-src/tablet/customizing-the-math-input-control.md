---
description: Viene illustrato come modificare l'aspetto del controllo di input matematico.
ms.assetid: 922562be-4d5b-45b6-ad0b-49176f893c8e
title: Personalizzazione del Controllo input penna espressioni matematiche
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8adedc4ab5b655f4f753a1b83cabe28e322adaad3c73bcf9f25ea1dea6d0bc08
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118045640"
---
# <a name="customizing-the-math-input-control"></a>Personalizzazione del Controllo input penna espressioni matematiche

È possibile modificare l'aspetto del controllo di input matematico in modo che sia più adatto all'applicazione. Questo argomento illustra i vari modi in cui gli sviluppatori possono personalizzare il controllo di input matematico.

Sono possibili le personalizzazioni seguenti:

-   [Modifica dei pulsanti visualizzati](#changing-the-displayed-buttons)
-   [Modifica della didascalia del controllo](#changing-the-control-caption)
-   [Modifica delle dimensioni dell'area di anteprima del controllo](#changing-the-controls-preview-area-size)

## <a name="changing-the-displayed-buttons"></a>Modifica dei pulsanti visualizzati

È possibile modificare i pulsanti visualizzati nel controllo di input matematico in modo che il controllo abbia funzionalità estese o sia più piccolo sullo schermo. Se si abilita il set di pulsanti estesi, verranno visualizzati **i pulsanti Ripristina** e **Annulla.** Il codice seguente illustra come abilitare il set di pulsanti estesi.


```
  void CMath_Input_Control_testDlg::OnBnClickedToggleBtns()
  {
    static bool enabled = true;
    HRESULT hr = S_OK;

    hr = g_spMIC->Hide();    
    if(!enabled){
      if (SUCCEEDED(hr)){
        hr = g_spMIC->EnableExtendedButtons(VARIANT_TRUE);
        enabled = true;
      }
    }else{
      if (SUCCEEDED(hr)){
        hr = g_spMIC->EnableExtendedButtons(VARIANT_FALSE);
        enabled = false;
      }
    }
    if (SUCCEEDED(hr)){
      hr = g_spMIC->Show();
    }
  }
  
```



L'immagine seguente mostra il controllo con il set esteso di pulsanti.

![Controllo input matematico con un set esteso di pulsanti](images/mic.png)

L'immagine seguente mostra il controllo senza il set esteso di pulsanti.

![Controllo di input matematico senza un set esteso di pulsanti](images/mic-no-extended.png)

## <a name="changing-the-control-caption"></a>Modifica della didascalia del controllo

È possibile modificare la didascalia del controllo per il controllo di input matematico per impostare la didascalia nella finestra del controllo di input matematico. Il codice seguente illustra come impostare la didascalia.


```
  void CMath_Input_Control_testDlg::OnBnClickedSetCaption()
  {     
    g_spMIC->Hide();
    CComBSTR cap1(L"Some Caption Text");    
    g_spMIC->SetCaptionText((BSTR)cap1);
    g_spMIC->Show();
  }  
  
```



L'immagine seguente mostra il controllo dopo l'impostazione della didascalia.

![Controllo di input matematico con un set di didascalie](images/mic-caption.png)

## <a name="changing-the-controls-preview-area-size"></a>Modifica delle dimensioni dell'area di anteprima del controllo

È possibile personalizzare il controllo di input matematico in modo che il controllo ne imposta in modo esplicito le dimensioni dell'area di anteprima. Verrà creata un'area più ampia in cui vengono visualizzate le formule matematiche. Il codice seguente illustra come impostare le dimensioni dell'area di anteprima.


```
  void CMath_Input_Control_testDlg::OnBnClickedSetPreviewAreaSize()
  {
    LONG height = 200;
    HRESULT hr = S_OK;
    hr = g_spMIC->SetPreviewHeight(height);
  }  
  
```



Le immagini seguenti mostrano un controllo con aree di anteprima di dimensioni diverse.

![Controllo input matematico con le dimensioni predefinite dell'area di anteprima](images/mic.png)![Controllo input matematico con un'area di anteprima più grande](images/mic-big-preview.png)

 

 



