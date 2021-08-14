---
title: Per eseguire la ricerca in base all'ora usando il lettore asincrono
description: Per eseguire la ricerca in base all'ora usando il lettore asincrono
ms.assetid: 731b0a6e-1472-45a7-998c-e395be86036f
keywords:
- Advanced Systems Format (ASF), ricerca in base all'ora
- ASF (Advanced Systems Format), ricerca in base all'ora
- Advanced Systems Format (ASF), lettori asincroni
- ASF (Advanced Systems Format),lettori asincroni
- lettori asincroni, ricerca in base all'ora
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 070d480cade395cdbead99b1aedde8928c6fb18b4af15bf6b72c1bcc0dcd6dc3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118196460"
---
# <a name="to-seek-by-time-using-the-asynchronous-reader"></a>Per eseguire la ricerca in base all'ora usando il lettore asincrono

Se si vuole cercare un'ora di presentazione specifica in un file ASF, il file deve essere configurato correttamente. È possibile eseguire la ricerca nei file solo audio per impostazione predefinita, ma i file video devono essere indicizzati prima della ricerca. Se non si è certi di come è stato creato un file, è possibile controllare l'attributo \_ g wszWMSeekable nell'intestazione del file chiamando [**IWMHeaderInfo::GetAttributeByName**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-getattributebyname).

Per cercare i dati in un file ASF in base all'ora di presentazione usando il lettore asincrono, chiamare [**IWMReader::Start**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-start), passando l'ora e la durata desiderate della parte del file che si vuole leggere rispettivamente come *cnsStart* e *cnsDuration.*

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Interfaccia IWMReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreader)
</dt> <dt>

[**Lettura di file con il lettore asincrono**](reading-files-with-the-asynchronous-reader.md)
</dt> <dt>

[**Lettura dei metadati in fase di riproduzione**](reading-metadata-at-playback.md)
</dt> <dt>

[**Operazioni con gli indici**](working-with-indexes.md)
</dt> </dl>

 

 




