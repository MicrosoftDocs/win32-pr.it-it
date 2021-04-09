---
description: Questa sezione descrive come usare l'API transcode per ricodificare i file multimediali. L'API transcode è stata introdotta in Windows 7.
ms.assetid: 24bf68a8-39bf-4302-b28c-71bb23b63469
title: API transcodifica
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9783c6f99a25ba6835171dcc7f7555a1f747c72b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103880586"
---
# <a name="transcode-api"></a>API transcodifica

Questa sezione descrive come usare l'API transcode per ricodificare i file multimediali. L'API transcode è stata introdotta in Windows 7.

La *transcodifica* è la conversione di un file multimediale digitale da un formato a un altro. L'API transcode è progettata per essere usata con la [sessione multimediale](media-session.md). Semplifica l'uso della sessione multimediale per determinati tipi di applicazioni di transcodifica:

-   Codifica della velocità in bit costante (CBR), in cui la velocità in bit della destinazione è nota in anticipo.
-   Al massimo un flusso audio e un flusso video.
-   Codifica da e in un file.

L'API transcode non supporta quanto segue:

-   Velocità in bit variabile (VBR) o codifica Multipass.
-   Più flussi audio o più flussi video.
-   Contenuto protetto da DRM diverso da file ASF protetti con WMDRM.
-   Streaming Live, ad esempio streaming live-to-file o streaming live-to-Live.

Se l'applicazione di codifica rientra in questi vincoli, l'API transcode è un modello di programmazione più semplice rispetto all'uso della sessione multimediale da solo.

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                                                          | Descrizione                                                                                                                                                                                                                 |
|------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Informazioni sull'API transcodifica](about-the-transcode-api.md)<br/>                              | Viene fornita una panoramica generale dell'API transcodifica.<br/>                                                                                                                                                                |
| [Uso dell'API transcode](fast-transcode-objects.md)<br/>                               | Viene descritto il modo in cui un'applicazione utilizza l'API transcode.<br/>                                                                                                                                                             |
| [Esercitazione: codifica di un file MP4](tutorial--encoding-an-mp4-file-.md)<br/>               | Esercitazione dettagliata che illustra come usare l'API transcode per codificare un file MP4.<br/>                                                                                                                           |
| [Esercitazione: codifica di un file WMA](tutorial--converting-an-mp3-file-to-a-wma-file.md)<br/> | Viene illustrato come utilizzare l'API transcode per codificare un file WMA. Questa esercitazione modifica il codice illustrato in [esercitazione: codifica di un file MP4](tutorial--encoding-an-mp4-file-.md), quindi è consigliabile leggere prima l'esercitazione.<br/> |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Codifica e creazione di file](encoding-and-file-authoring.md)
</dt> <dt>

[Media Foundation: concetti essenziali](media-foundation-programming--essential-concepts.md)
</dt> <dt>

[Cenni preliminari sulla codifica in Media Foundation](overview-of-encoding-in-media-foundation.md)
</dt> </dl>

 

 




