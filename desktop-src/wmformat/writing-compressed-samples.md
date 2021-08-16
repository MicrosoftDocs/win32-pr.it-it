---
title: Scrittura di esempi compressi
description: Scrittura di esempi compressi
ms.assetid: f85ca719-1b9d-404f-b2b1-c9e3524e4bc6
keywords:
- Advanced Systems Format (ASF), scrittura di esempi compressi
- ASF (Advanced Systems Format), scrittura di esempi compressi
- Advanced Systems Format (ASF), passaggio di esempi compressi
- ASF (Advanced Systems Format), passaggio di esempi compressi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0eaa6bf5298e465716fe7a60eb5de2459f09be405611ac7322b534804bbbc997
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117843655"
---
# <a name="writing-compressed-samples"></a>Scrittura di esempi compressi

Per alcuni flussi audio o video, è possibile passare esempi già compressi anziché passare dati non elaborati. Questa funzionalità viene usata per copiare un flusso esistente o per scrivere esempi compressi con un codec di terze parti. Il processo di scrittura di un esempio compresso è identico alla scrittura di un esempio non compresso, ad eccezione del fatto che si usa [**IWMWriterAdvanced::WriteStreamSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-writestreamsample) anziché [**IWMWriter::WriteSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-writesample). Per altre informazioni sulla scrittura di esempi non compressi, vedere [Per scrivere esempi](to-write-samples.md).

Quando si scrivono esempi compressi, per i profili CBR, il writer elimina alcuni esempi, se necessario, per mantenere il contenuto entro la velocità in bit e i valori della finestra del buffer specificati. Per VBR, il writer non elimina gli esempi, ma non è possibile assicurarsi che la velocità in bit e i valori della finestra del buffer siano corretti.

Se si copia un flusso da un file a un altro, è necessario copiare sempre l'oggetto di configurazione del flusso dal profilo del file originale al profilo del nuovo file. In questo modo si garantisce che siano disponibili le informazioni corrette sulla velocità in bit e sulla finestra del buffer. Se si copia un flusso compresso in un flusso con una finestra del buffer inferiore impostata, gli esempi verranno eliminati durante la scrittura del file.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Scrittura di file ASF**](writing-asf-files.md)
</dt> </dl>

 

 




