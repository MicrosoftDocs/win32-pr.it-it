---
title: Informazioni su IMFTransform
description: Informazioni su IMFTransform
ms.assetid: 889f2d82-148a-4a7e-b78c-37ec86b37e0b
keywords:
- Plug-in di Windows Media Player, interfacce
- plug-in, interfacce
- plug-in di elaborazione dei segnali digitali, interfacce
- Plug-in DSP, interfacce
- interfacce, plug-in DSP
- Plug-in di Windows Media Player, interfaccia IMFTransform
- plug-in, interfaccia IMFTransform
- plug-in per l'elaborazione di segnali digitali, interfaccia IMFTransform
- Plug-in DSP, interfaccia IMFTransform
- Interfaccia IMFTransform
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5eb58ab84070a8cb9390e4525b9b642f15a29f14
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106297797"
---
# <a name="about-imftransform"></a>Informazioni su IMFTransform

L'interfaccia **IMFTransform** è una delle interfacce che devono essere implementate da un plug-in DSP a doppia modalità. Windows Media Player chiama i metodi dell'interfaccia **IMFTransform** per fornire i dati al plug-in e recuperare i dati elaborati dal plug-in. Per la documentazione completa dell'interfaccia **IMFTransform** , vedere la sezione Media Foundation della Windows SDK.

I metodi di **IMFTransform** possono essere categorizzati come indicato di seguito.

## <a name="methods-that-handle-format-negotiation"></a>Metodi che gestiscono la negoziazione del formato

Windows Media Player chiama i metodi seguenti per ottenere informazioni sui formati di dati supportati dal plug-in.

-   **GetStreamCount**
-   **GetStreamLimits**
-   **GetInputStreamInfo**
-   **GetOutputStreamInfo**
-   **GetInputAvailableType**
-   **GetOutputAvailableType**
-   **SetInputType**
-   **SetOutputType**
-   **GetAttributes**
-   **GetInputStreamAttributes**
-   **GetOutputStreamAttributes**
-   **GetStreamIDs**

## <a name="methods-that-specify-or-retrieve-state-information"></a>Metodi che specificano o recuperano informazioni sullo stato

Windows Media Player chiama i metodi seguenti per ottenere o impostare i valori correlati allo stato corrente del plug-in.

-   **SetInputType**
-   **SetOutputType**
-   **GetInputCurrentType**
-   **GetOutputCurrentType**
-   **GetInputStatus**
-   **AddInputStreams**
-   **DeleteInputStreams**
-   **GetOutputStatus**
-   **SetOutputBounds**

> [!Note]  
> **SetInputType** e **SetOutputType** vengono usati sia per la negoziazione del formato sia per la specifica e il recupero delle informazioni sullo stato.

 

## <a name="methods-that-handle-buffering-and-processing-data"></a>Metodi che gestiscono il buffering e l'elaborazione dei dati

Windows Media Player chiama i metodi seguenti per avviare i vari processi eseguiti dal plug-in per eseguire l'elaborazione del segnale digitale.

-   **ProcessInput**
-   **ProcessOutput**
-   **ProcessMessage**
-   **ProcessEvent**

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Interfacce obbligatorie**](required-interfaces.md)
</dt> </dl>

 

 




