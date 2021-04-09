---
title: Per impostare le impostazioni di input
description: Per impostare le impostazioni di input
ms.assetid: 288801a7-793f-43bd-9c5a-f9e1bd86ecc3
keywords:
- ASF (Advanced Systems Format), impostazioni di input
- ASF (formato avanzato dei sistemi), impostazioni di input
- profili, impostazioni di input
- codec, impostazioni di input
- flussi, impostazioni di input
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e7b2db64a7346cc8b9d46c48f0add79dafcac95
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "103956199"
---
# <a name="to-set-input-settings"></a>Per impostare le impostazioni di input

Le proprietà di base dei supporti di input e del flusso sono definite dalla struttura del [**\_ \_ tipo di supporto WM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) . Per i formati di input, le informazioni sul tipo di supporto sono impostate dall'applicazione. Per i formati di flusso, le informazioni sul tipo di supporto sono impostate nel profilo assegnato al writer. Alcune proprietà sono indipendenti dal tipo di supporto e devono essere impostate per un input prima che inizi la scrittura. Queste proprietà sono funzionalità di codec e writer indipendenti dal tipo di flusso e devono essere impostate dopo l'assegnazione del profilo nel writer, ma prima dell'inizio della scrittura.

Per l'impostazione di un'impostazione di input è richiesta una chiamata a [**IWMWriterAdvanced2:: SetInputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced2-setinputsetting). È anche possibile controllare il valore corrente di un'impostazione con una chiamata a [**IWMWriterAdvanced2:: GetInputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced2-getinputsetting).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Per utilizzare profili con il writer**](to-use-profiles-with-the-writer.md)
</dt> <dt>

[**Scrittura di file ASF**](writing-asf-files.md)
</dt> <dt>

[**Scrittura di flussi di immagini**](writing-image-streams.md)
</dt> </dl>

 

 




