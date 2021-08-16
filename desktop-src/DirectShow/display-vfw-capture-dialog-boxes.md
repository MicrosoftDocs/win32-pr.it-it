---
description: Visualizzare le finestre di dialogo di acquisizione di VFW
ms.assetid: 708212ca-d148-4079-8052-3bf6696a33ab
title: Visualizzare le finestre di dialogo di acquisizione di VFW
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2713cc4d2eba52626c66974eed23f2c1752a1268fea78a30ca2bc9d7babc3a27
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117821139"
---
# <a name="display-vfw-capture-dialog-boxes"></a>Visualizzare le finestre di dialogo di acquisizione di VFW

Un dispositivo di acquisizione che usa ancora un driver Video for Windows (VFW) può supportare una delle tre finestre di dialogo seguenti, usate per configurare il dispositivo.



| Finestra di dialogo    | Descrizione                                                                                           |
|---------------|-------------------------------------------------------------------------------------------------------|
| Origine video  | Consente di selezionare l'input video e di modificare le impostazioni del dispositivo, ad esempio la luminosità o il contrasto dell'immagine. |
| Formato video  | Consente di selezionare le dimensioni dell'immagine e la profondità in bit.                                                    |
| Visualizzazione video | Usato per controllare l'aspetto del video di cui è stato eseguito il rendering.                                                 |



 

Per visualizzare una di queste finestre di dialogo, eseguire le operazioni seguenti:

1.  Arrestare il grafico dei filtri.
2.  Eseguire una query sul filtro di acquisizione [**per l'interfaccia IAMVfwCaptureDialogs.**](/windows/desktop/api/Strmif/nn-strmif-iamvfwcapturedialogs) Se **QueryInterface** ha esito positivo, significa che il dispositivo di acquisizione è un dispositivo VFW.
3.  Chiamare [**IAMVfwCaptureDialogs::HasDialog**](/windows/desktop/api/Strmif/nf-strmif-iamvfwcapturedialogs-hasdialog) per verificare se il driver supporta la finestra di dialogo che si vuole visualizzare. [**L'enumerazione VfwCaptureDialogs**](/windows/desktop/api/strmif/ne-strmif-vfwcapturedialogs) definisce i flag per ogni finestra di dialogo di VFW. **HasDialog restituisce** S \_ OK se la finestra di dialogo è supportata. In caso contrario, restituisce S FALSE, quindi cercare direttamente il valore \_ S \_ OK, anziché usare la macro **SUCCEEDED.**
4.  Se la finestra di dialogo è supportata, chiamare [**IAMVfwCaptureDialogs::ShowDialog**](/windows/desktop/api/Strmif/nf-strmif-iamvfwcapturedialogs-showdialog) per visualizzare la finestra di dialogo.
5.  Riavviare il grafico.

Il codice seguente illustra questi passaggi per la finestra di dialogo Origine video:


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

 

 



