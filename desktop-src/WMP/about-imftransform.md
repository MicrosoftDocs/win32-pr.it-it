---
title: Informazioni su IMFTransform
description: Informazioni su IMFTransform
ms.assetid: 889f2d82-148a-4a7e-b78c-37ec86b37e0b
keywords:
- Windows Media Player plug-in, interfacce
- plug-in, interfacce
- plug-in per l'elaborazione di segnali digitali, interfacce
- plug-in DSP, interfacce
- interfacce, plug-in DSP
- Windows Media Player plug-in, interfaccia IMFTransform
- plug-in, interfaccia IMFTransform
- plug-in di elaborazione del segnale digitale,interfaccia IMFTransform
- Plug-in DSP, interfaccia IMFTransform
- Interfaccia IMFTransform
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c3b410702d63657261faa2fc8e7db123e05dcdc12c3096a49f8c0e2e36a41ff4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119903581"
---
# <a name="about-imftransform"></a>Informazioni su IMFTransform

**L'interfaccia IMFTransform** è una delle interfacce che devono essere implementate da un plug-in DSP in modalità doppia. Windows Media Player chiama i metodi **dell'interfaccia IMFTransform** per fornire dati al plug-in e recuperare i dati elaborati dal plug-in. Per la documentazione completa **dell'interfaccia IMFTransform,** vedere la Media Foundation di Windows SDK.

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

Windows Media Player chiama i metodi seguenti per ottenere o impostare valori correlati allo stato corrente del plug-in.

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
> **SetInputType e** **SetOutputType** vengono usati sia per la negoziazione del formato che per specificare e recuperare informazioni sullo stato.

 

## <a name="methods-that-handle-buffering-and-processing-data"></a>Metodi che gestiscono il buffering e l'elaborazione dei dati

Windows Media Player chiama i metodi seguenti per avviare i vari processi eseguono il plug-in per eseguire l'elaborazione del segnale digitale.

-   **ProcessInput**
-   **ProcessOutput**
-   **ProcessMessage**
-   **ProcessEvent**

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Interfacce necessarie**](required-interfaces.md)
</dt> </dl>

 

 




