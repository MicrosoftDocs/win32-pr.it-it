---
title: Modifica degli attributi dei metadati
description: Modifica degli attributi dei metadati
ms.assetid: 96c979e2-c616-45e3-9c60-a24f03e29dc4
keywords:
- Windows Media Format SDK, modifica degli attributi dei metadati
- Advanced Systems Format (ASF), modifica degli attributi dei metadati
- ASF (Advanced Systems Format), modifica degli attributi dei metadati
- metadati, modifica di attributi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b973b787b37bbf9333a0adb218ab5db0e6f677521f1bfc9a0cdc1d5c37200e83
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119586061"
---
# <a name="editing-metadata-attributes"></a>Modifica degli attributi dei metadati

La modifica degli attributi dei metadati è molto simile all'impostazione di nuovi attributi. Invece di usare [**IWMHeaderInfo3::AddAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-addattribute), usare [**IWMHeaderInfo3::ModifyAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-modifyattribute). **ModifyAttribute** è identico ad **AddAttribute,** ad eccezione del fatto che non si specifica un nome di attributo e il numero di indice è un parametro di input anziché un output.

È possibile usare il numero di 0xFFFF per specificare un attributo da modificare usando il relativo indice globale.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Uso dei metadati**](working-with-metadata.md)
</dt> </dl>

 

 




