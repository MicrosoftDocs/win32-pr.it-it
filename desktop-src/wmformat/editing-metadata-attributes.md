---
title: Modifica degli attributi dei metadati
description: Modifica degli attributi dei metadati
ms.assetid: 96c979e2-c616-45e3-9c60-a24f03e29dc4
keywords:
- Windows Media Format SDK, modifica degli attributi dei metadati
- ASF (Advanced Systems Format), modifica degli attributi dei metadati
- ASF (Advanced Systems Format), modifica degli attributi dei metadati
- metadati, modifica degli attributi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a52990e5366da178e9ed5021af93a9f6403b80c4
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "104398625"
---
# <a name="editing-metadata-attributes"></a>Modifica degli attributi dei metadati

La modifica degli attributi dei metadati è molto simile all'impostazione di nuove. Anziché utilizzare [**IWMHeaderInfo3:: AddAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-addattribute), utilizzare [**IWMHeaderInfo3:: ModifyAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-modifyattribute). **ModifyAttribute** è identico a **AddAttribute** con la differenza che non si specifica un nome di attributo e il numero di indice è un parametro di input anziché un output.

È possibile utilizzare il numero di flusso 0xFFFF per specificare un attributo da modificare utilizzando il relativo indice globale.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Utilizzo dei metadati**](working-with-metadata.md)
</dt> </dl>

 

 




