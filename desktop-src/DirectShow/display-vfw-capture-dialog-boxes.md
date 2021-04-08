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
# <a name="display-vfw-capture-dialog-boxes"></a><span data-ttu-id="75b8a-103">Visualizzare le finestre di dialogo di acquisizione VFW</span><span class="sxs-lookup"><span data-stu-id="75b8a-103">Display VFW Capture Dialog Boxes</span></span>

<span data-ttu-id="75b8a-104">Un dispositivo di acquisizione che usa ancora un driver video for Windows (VFW) può supportare una delle tre finestre di dialogo seguenti, che vengono usate per configurare il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="75b8a-104">A capture device that still uses a Video for Windows (VFW) driver can support any of the following three dialog boxes, which are used to configure the device.</span></span>



| <span data-ttu-id="75b8a-105">Finestra di dialogo</span><span class="sxs-lookup"><span data-stu-id="75b8a-105">Dialog box</span></span>    | <span data-ttu-id="75b8a-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="75b8a-106">Description</span></span>                                                                                           |
|---------------|-------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="75b8a-107">Origine video</span><span class="sxs-lookup"><span data-stu-id="75b8a-107">Video Source</span></span>  | <span data-ttu-id="75b8a-108">Usato per selezionare l'input del video e per modificare le impostazioni del dispositivo, ad esempio la luminosità o il contrasto dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="75b8a-108">Used to select the video input and to adjust device settings, such as picture brightness or contrast.</span></span> |
| <span data-ttu-id="75b8a-109">Formato video</span><span class="sxs-lookup"><span data-stu-id="75b8a-109">Video Format</span></span>  | <span data-ttu-id="75b8a-110">Consente di selezionare le dimensioni dell'immagine e la profondità dei bit.</span><span class="sxs-lookup"><span data-stu-id="75b8a-110">Used to select the image dimensions and bit depth.</span></span>                                                    |
| <span data-ttu-id="75b8a-111">Visualizzazione video</span><span class="sxs-lookup"><span data-stu-id="75b8a-111">Video Display</span></span> | <span data-ttu-id="75b8a-112">Usato per controllare l'aspetto del video di cui è stato eseguito il rendering.</span><span class="sxs-lookup"><span data-stu-id="75b8a-112">Used to control the appearance of the rendered video.</span></span>                                                 |



 

<span data-ttu-id="75b8a-113">Per visualizzare una di queste finestre di dialogo, procedere come segue:</span><span class="sxs-lookup"><span data-stu-id="75b8a-113">To show one of these dialog boxes, do the following:</span></span>

1.  <span data-ttu-id="75b8a-114">Arrestare il grafico del filtro.</span><span class="sxs-lookup"><span data-stu-id="75b8a-114">Stop the filter graph.</span></span>
2.  <span data-ttu-id="75b8a-115">Eseguire una query sul filtro di acquisizione per l'interfaccia [**IAMVfwCaptureDialogs**](/windows/desktop/api/Strmif/nn-strmif-iamvfwcapturedialogs) .</span><span class="sxs-lookup"><span data-stu-id="75b8a-115">Query the capture filter for the [**IAMVfwCaptureDialogs**](/windows/desktop/api/Strmif/nn-strmif-iamvfwcapturedialogs) interface.</span></span> <span data-ttu-id="75b8a-116">Se **QueryInterface** riesce, significa che il dispositivo di acquisizione è un dispositivo VFW.</span><span class="sxs-lookup"><span data-stu-id="75b8a-116">If **QueryInterface** succeeds, it means the capture device is a VFW device.</span></span>
3.  <span data-ttu-id="75b8a-117">Chiamare [**IAMVfwCaptureDialogs:: HasDialog**](/windows/desktop/api/Strmif/nf-strmif-iamvfwcapturedialogs-hasdialog) per verificare se il driver supporta la finestra di dialogo che si desidera visualizzare.</span><span class="sxs-lookup"><span data-stu-id="75b8a-117">Call [**IAMVfwCaptureDialogs::HasDialog**](/windows/desktop/api/Strmif/nf-strmif-iamvfwcapturedialogs-hasdialog) to check if the driver supports the dialog box that you wish to display.</span></span> <span data-ttu-id="75b8a-118">L'enumerazione [**VfwCaptureDialogs**](/windows/desktop/api/strmif/ne-strmif-vfwcapturedialogs) definisce i flag per ogni finestra di dialogo VFW.</span><span class="sxs-lookup"><span data-stu-id="75b8a-118">The [**VfwCaptureDialogs**](/windows/desktop/api/strmif/ne-strmif-vfwcapturedialogs) enumeration defines flags for each of the VFW dialog boxes.</span></span> <span data-ttu-id="75b8a-119">**HasDialog** restituisce \_ OK se la finestra di dialogo è supportata.</span><span class="sxs-lookup"><span data-stu-id="75b8a-119">**HasDialog** returns S\_OK if the dialog box is supported.</span></span> <span data-ttu-id="75b8a-120">\_In caso contrario, restituisce false, quindi controllare direttamente il valore s \_ OK, anziché usare la macro **succeeded** .</span><span class="sxs-lookup"><span data-stu-id="75b8a-120">It returns S\_FALSE otherwise, so check for the value S\_OK directly, rather than using the **SUCCEEDED** macro.</span></span>
4.  <span data-ttu-id="75b8a-121">Se la finestra di dialogo è supportata, chiamare [**IAMVfwCaptureDialogs:: ShowDialog**](/windows/desktop/api/Strmif/nf-strmif-iamvfwcapturedialogs-showdialog) per visualizzare la finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="75b8a-121">If the dialog box is supported, call [**IAMVfwCaptureDialogs::ShowDialog**](/windows/desktop/api/Strmif/nf-strmif-iamvfwcapturedialogs-showdialog) to display the dialog box.</span></span>
5.  <span data-ttu-id="75b8a-122">Riavviare il grafo.</span><span class="sxs-lookup"><span data-stu-id="75b8a-122">Restart the graph.</span></span>

<span data-ttu-id="75b8a-123">Il codice seguente illustra questi passaggi per la finestra di dialogo origine video:</span><span class="sxs-lookup"><span data-stu-id="75b8a-123">The following code shows these steps for the Video Source dialog box:</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="75b8a-124">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="75b8a-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="75b8a-125">Configurazione di un dispositivo di acquisizione video</span><span class="sxs-lookup"><span data-stu-id="75b8a-125">Configuring a Video Capture Device</span></span>](configuring-a-video-capture-device.md)
</dt> </dl>

 

 



