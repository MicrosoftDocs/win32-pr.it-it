---
description: Viene illustrato come modificare l'aspetto del controllo di input matematico.
ms.assetid: 922562be-4d5b-45b6-ad0b-49176f893c8e
title: Personalizzazione del controllo di input matematico
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c3cab7c6efe003738c46a89d07866fcc9302ec5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104555584"
---
# <a name="customizing-the-math-input-control"></a><span data-ttu-id="00d00-103">Personalizzazione del controllo di input matematico</span><span class="sxs-lookup"><span data-stu-id="00d00-103">Customizing the Math Input Control</span></span>

<span data-ttu-id="00d00-104">È possibile modificare l'aspetto del controllo di input matematico in modo che sia più adatto per l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="00d00-104">It is possible to change the look and feel of the math input control so that it is better suited to your application.</span></span> <span data-ttu-id="00d00-105">In questo argomento vengono illustrati i vari modi in cui gli sviluppatori possono personalizzare il controllo di input matematico.</span><span class="sxs-lookup"><span data-stu-id="00d00-105">This topic explains the various ways that developers can customize the math input control.</span></span>

<span data-ttu-id="00d00-106">Sono possibili le seguenti personalizzazioni:</span><span class="sxs-lookup"><span data-stu-id="00d00-106">The following customizations are possible:</span></span>

-   [<span data-ttu-id="00d00-107">Modifica dei pulsanti visualizzati</span><span class="sxs-lookup"><span data-stu-id="00d00-107">Changing the Displayed Buttons</span></span>](#changing-the-displayed-buttons)
-   [<span data-ttu-id="00d00-108">Modifica della didascalia del controllo</span><span class="sxs-lookup"><span data-stu-id="00d00-108">Changing the Control Caption</span></span>](#changing-the-control-caption)
-   [<span data-ttu-id="00d00-109">Modifica delle dimensioni dell'area di anteprima del controllo</span><span class="sxs-lookup"><span data-stu-id="00d00-109">Changing the Control's Preview Area Size</span></span>](#changing-the-controls-preview-area-size)

## <a name="changing-the-displayed-buttons"></a><span data-ttu-id="00d00-110">Modifica dei pulsanti visualizzati</span><span class="sxs-lookup"><span data-stu-id="00d00-110">Changing the Displayed Buttons</span></span>

<span data-ttu-id="00d00-111">È possibile modificare i pulsanti visualizzati nel controllo di input matematico in modo che il controllo abbia funzionalità estese o venga visualizzato più piccolo sullo schermo.</span><span class="sxs-lookup"><span data-stu-id="00d00-111">You can change the buttons that are displayed on the math input control so that the control has extended functionality or appears smaller on the screen.</span></span> <span data-ttu-id="00d00-112">Se si Abilita il set di pulsanti estesi, vengono visualizzati i pulsanti **Ripeti** e **Annulla** .</span><span class="sxs-lookup"><span data-stu-id="00d00-112">Enabling the extended button set will show the **Redo** and **Undo** buttons.</span></span> <span data-ttu-id="00d00-113">Nel codice seguente viene illustrato come abilitare il set di pulsanti esteso.</span><span class="sxs-lookup"><span data-stu-id="00d00-113">The following code shows how to enable the extended button set.</span></span>


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



<span data-ttu-id="00d00-114">La figura seguente mostra il controllo con il set esteso di pulsanti.</span><span class="sxs-lookup"><span data-stu-id="00d00-114">The following image shows the control with the extended set of buttons.</span></span>

![controllo di input matematico con un set esteso di pulsanti](images/mic.png)

<span data-ttu-id="00d00-116">La figura seguente mostra il controllo senza il set esteso di pulsanti.</span><span class="sxs-lookup"><span data-stu-id="00d00-116">The following image shows the control without the extended set of buttons.</span></span>

![controllo di input matematico senza un set esteso di pulsanti](images/mic-no-extended.png)

## <a name="changing-the-control-caption"></a><span data-ttu-id="00d00-118">Modifica della didascalia del controllo</span><span class="sxs-lookup"><span data-stu-id="00d00-118">Changing the Control Caption</span></span>

<span data-ttu-id="00d00-119">È possibile modificare la didascalia del controllo per il controllo di input matematico per impostare la didascalia nella finestra del controllo di input matematico.</span><span class="sxs-lookup"><span data-stu-id="00d00-119">You can change the control caption for the math input control in order to set the caption on the math input control's window.</span></span> <span data-ttu-id="00d00-120">Il codice seguente illustra come impostare la didascalia.</span><span class="sxs-lookup"><span data-stu-id="00d00-120">The following code shows how to set the caption.</span></span>


```
  void CMath_Input_Control_testDlg::OnBnClickedSetCaption()
  {     
    g_spMIC->Hide();
    CComBSTR cap1(L"Some Caption Text");    
    g_spMIC->SetCaptionText((BSTR)cap1);
    g_spMIC->Show();
  }  
  
```



<span data-ttu-id="00d00-121">La figura seguente mostra il controllo dopo l'impostazione della didascalia.</span><span class="sxs-lookup"><span data-stu-id="00d00-121">The following image shows the control after the caption has been set.</span></span>

![controllo di input matematico con un set di didascalie](images/mic-caption.png)

## <a name="changing-the-controls-preview-area-size"></a><span data-ttu-id="00d00-123">Modifica delle dimensioni dell'area di anteprima del controllo</span><span class="sxs-lookup"><span data-stu-id="00d00-123">Changing the Control's Preview Area Size</span></span>

<span data-ttu-id="00d00-124">È possibile personalizzare il controllo di input matematico in modo che il controllo imposti in modo esplicito le dimensioni dell'area di anteprima.</span><span class="sxs-lookup"><span data-stu-id="00d00-124">You can customize the math input control so that the control explicitly sets its preview-area size.</span></span> <span data-ttu-id="00d00-125">In questo modo viene creata un'area più grande in cui vengono visualizzate le formule matematiche.</span><span class="sxs-lookup"><span data-stu-id="00d00-125">This creates a larger area in which the math formulas are displayed.</span></span> <span data-ttu-id="00d00-126">Nel codice seguente viene illustrato come impostare le dimensioni dell'area di anteprima.</span><span class="sxs-lookup"><span data-stu-id="00d00-126">The following code shows how to set the preview area size.</span></span>


```
  void CMath_Input_Control_testDlg::OnBnClickedSetPreviewAreaSize()
  {
    LONG height = 200;
    HRESULT hr = S_OK;
    hr = g_spMIC->SetPreviewHeight(height);
  }  
  
```



<span data-ttu-id="00d00-127">Le immagini seguenti mostrano un controllo con aree di anteprima di dimensioni diverse.</span><span class="sxs-lookup"><span data-stu-id="00d00-127">The following images show a control with differently sized preview areas.</span></span>

![controllo di input matematico con le dimensioni dell'area di anteprima predefinite](images/mic.png)![controllo di input matematico con un'area di anteprima più ampia](images/mic-big-preview.png)

 

 



