---
title: Per impostare i valori di Impostazioni
description: Per impostare i valori di Impostazioni
ms.assetid: 288801a7-793f-43bd-9c5a-f9e1bd86ecc3
keywords:
- Advanced Systems Format (ASF), impostazioni di input
- ASF (Advanced Systems Format), impostazioni di input
- profili,impostazioni di input
- codec, impostazioni di input
- flussi, impostazioni di input
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5df5b10ea6bd15ad083b26a61af037527f00576eaa6b7e1fa795ea1591417ac3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119447021"
---
# <a name="to-set-input-settings"></a>Per impostare i valori di Impostazioni

Le proprietà di base dei supporti di input e dei supporti di flusso sono definite dalla [**struttura WM \_ MEDIA \_ TYPE.**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) Per i formati di input, le informazioni sul tipo di supporto vengono impostate dall'applicazione. Per i formati di flusso, le informazioni sul tipo di supporto vengono impostate nel profilo assegnato al writer. Alcune proprietà sono indipendenti dal tipo di supporto e devono essere impostate per un input prima dell'inizio della scrittura. Queste proprietà sono funzionalità di codec e writer indipendenti dal tipo di flusso e devono essere impostate dopo l'assegnazione del profilo nel writer, ma prima dell'inizio della scrittura.

L'impostazione di un'impostazione di input richiede una chiamata a [**IWMWriterAdvanced2::SetInputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced2-setinputsetting). È anche possibile controllare il valore corrente di un'impostazione con una chiamata a [**IWMWriterAdvanced2::GetInputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced2-getinputsetting).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Per utilizzare profili con il writer**](to-use-profiles-with-the-writer.md)
</dt> <dt>

[**Scrittura di file ASF**](writing-asf-files.md)
</dt> <dt>

[**Scrittura di immagini Flussi**](writing-image-streams.md)
</dt> </dl>

 

 




