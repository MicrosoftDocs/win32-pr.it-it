---
description: Visualizzare le finestre di dialogo di acquisizione VFW
ms.assetid: 708212ca-d148-4079-8052-3bf6696a33ab
title: Visualizzare le finestre di dialogo di acquisizione VFW
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45b8b51b164630a8fa6e91b2e68ca8a9a3a875b6
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103745650"
---
# <a name="display-vfw-capture-dialog-boxes"></a>Visualizzare le finestre di dialogo di acquisizione VFW

Un dispositivo di acquisizione che usa ancora un driver video for Windows (VFW) può supportare una delle tre finestre di dialogo seguenti, che vengono usate per configurare il dispositivo.



| Finestra di dialogo    | Descrizione                                                                                           |
|---------------|-------------------------------------------------------------------------------------------------------|
| Origine video  | Usato per selezionare l'input del video e per modificare le impostazioni del dispositivo, ad esempio la luminosità o il contrasto dell'immagine. |
| Formato video  | Consente di selezionare le dimensioni dell'immagine e la profondità dei bit.                                                    |
| Visualizzazione video | Usato per controllare l'aspetto del video di cui è stato eseguito il rendering.                                                 |



 

Per visualizzare una di queste finestre di dialogo, procedere come segue:

1.  Arrestare il grafico del filtro.
2.  Eseguire una query sul filtro di acquisizione per l'interfaccia [**IAMVfwCaptureDialogs**](/windows/desktop/api/Strmif/nn-strmif-iamvfwcapturedialogs) . Se **QueryInterface** riesce, significa che il dispositivo di acquisizione è un dispositivo VFW.
3.  Chiamare [**IAMVfwCaptureDialogs:: HasDialog**](/windows/desktop/api/Strmif/nf-strmif-iamvfwcapturedialogs-hasdialog) per verificare se il driver supporta la finestra di dialogo che si desidera visualizzare. L'enumerazione [**VfwCaptureDialogs**](/windows/desktop/api/strmif/ne-strmif-vfwcapturedialogs) definisce i flag per ogni finestra di dialogo VFW. **HasDialog** restituisce \_ OK se la finestra di dialogo è supportata. \_In caso contrario, restituisce false, quindi controllare direttamente il valore s \_ OK, anziché usare la macro **succeeded** .
4.  Se la finestra di dialogo è supportata, chiamare [**IAMVfwCaptureDialogs:: ShowDialog**](/windows/desktop/api/Strmif/nf-strmif-iamvfwcapturedialogs-showdialog) per visualizzare la finestra di dialogo.
5.  Riavviare il grafo.

Il codice seguente illustra questi passaggi per la finestra di dialogo origine video:


```C++
pControl->Stop(); // Stop the graph.

// Query the capture filter for the IAMVfwCaptureDialogs interface.
IAMVfwCaptureDialogs *pVfw = 0;
hr = pCap->QueryInterface(IID_IAMVfwCaptureDialogs, (void**)&pVfw);
if (SUCCEEDED(hr))
{
    // Check if the device supports this dialog box.
    if (S_OK == pVfw->HasDialog(VfwCaptureDialog_Source))
    {
        // Show the dialog box.
        hr = pVfw->ShowDialog(VfwCaptureDialog_Source, hwndParent);
    }
}
pControl->Run();
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Configurazione di un dispositivo di acquisizione video](configuring-a-video-capture-device.md)
</dt> </dl>

 

 



