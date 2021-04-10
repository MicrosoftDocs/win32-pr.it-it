---
description: Esempio EVRPresenter
ms.assetid: 791a9816-4c40-4683-8b32-22f73d7fe84d
title: Esempio EVRPresenter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2bde85de152c41f348b1aae74a8c0d67ca746cab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127890"
---
# <a name="evrpresenter-sample"></a>Esempio EVRPresenter

Viene illustrato come implementare un presentatore personalizzato per il [renderer video avanzato](enhanced-video-renderer.md) (EVR). Il Presenter personalizzato può essere usato con il filtro EVR DirectShow o con il sink EVR Microsoft Media Foundation.

## <a name="apis-demonstrated"></a>API illustrate

In questo esempio vengono illustrate le interfacce Media Foundation seguenti:

-   [**IMFClockStateSink**](/windows/desktop/api/mfidl/nn-mfidl-imfclockstatesink)
-   [**IMFRateSupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport)
-   [**IMFTopologyServiceLookupClient**](/windows/desktop/api/evr/nn-evr-imftopologyservicelookupclient)
-   [**IMFVideoDeviceID**](/windows/desktop/api/evr/nn-evr-imfvideodeviceid)
-   [**IMFVideoDisplayControl**](/windows/desktop/api/evr/nn-evr-imfvideodisplaycontrol)
-   [**IMFVideoPresenter**](/windows/desktop/api/evr/nn-evr-imfvideopresenter)

## <a name="usage"></a>Utilizzo

L'esempio EVRPresenter compila una DLL che è un server COM per il relatore. Prima di utilizzare il Presenter personalizzato, è necessario registrare la DLL.

Per usare questo esempio in Media Foundation:

1.  Compilare l'esempio.
2.  Regsvr32 EvrPresenter.dll.
3.  Compilare ed eseguire l' [esempio MFPlayer](/previous-versions//bb970516(v=vs.85)).
4.  Scegliere **Apri** file dal menu **file** .
5.  Nella finestra di dialogo **Apri file** selezionare **Custom EVR Presenter.**
6.  Selezionare un file per la riproduzione.

Per usare questo esempio in DirectShow:

1.  Compilare l'esempio.
2.  Registra EvrPresenter.dll.
3.  Compilare ed eseguire l'esempio EVRPlayer. Questo esempio è incluso negli esempi di DirectShow nell'Windows SDK.
4.  Scegliere **EVR Presenter** dal menu **file** .
5.  Selezionare un file per la riproduzione.

## <a name="requirements"></a>Requisiti



| Prodotto                                                        | Versione   |
|----------------------------------------------------------------|-----------|
| [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | Windows 7 |



 

## <a name="downloading-the-sample"></a>Download dell'esempio

Questo esempio è disponibile nel [repository GitHub degli esempi classici di Windows](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/AudioClip).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Renderer video migliorato](enhanced-video-renderer.md)
</dt> <dt>

[Come scrivere un presentatore EVR](how-to-write-an-evr-presenter.md)
</dt> <dt>

[Esempi di Media Foundation SDK](media-foundation-sdk-samples.md)
</dt> </dl>

 

 
