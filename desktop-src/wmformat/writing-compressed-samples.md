---
title: Scrittura di esempi compressi
description: Scrittura di esempi compressi
ms.assetid: f85ca719-1b9d-404f-b2b1-c9e3524e4bc6
keywords:
- Formato di sistemi avanzati (ASF), scrittura di esempi compressi
- ASF (Advanced Systems Format), scrittura di esempi compressi
- ASF (Advanced Systems Format), passaggio di esempi compressi
- ASF (Advanced Systems Format), passaggio di esempi compressi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c0c43fed30aa89e83c157479257e78fbab4acd98
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "104472251"
---
# <a name="writing-compressed-samples"></a>Scrittura di esempi compressi

Per alcuni flussi audio o video, potrebbe essere necessario passare esempi già compressi anziché passare dati non elaborati. Questa funzionalità viene usata per copiare un flusso esistente o per scrivere esempi compressi con un codec di terze parti. Il processo di scrittura di un campione compresso è identico alla scrittura di un campione non compresso, con la differenza che si usa [**IWMWriterAdvanced:: WriteStreamSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-writestreamsample) anziché [**IWMWriter:: WriteSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-writesample). Per ulteriori informazioni sulla scrittura di esempi non compressi, vedere [per scrivere esempi](to-write-samples.md).

Quando si scrivono esempi compressi, per i profili CBR, il writer eliminerà alcuni esempi, se necessario, per preservare il contenuto entro i valori specificati per la velocità in bit e la finestra del buffer. Per VBR, il writer non eliminerà gli esempi, ma non esiste alcun modo per assicurarsi che i valori della velocità in bit e della finestra del buffer siano corretti.

Se si copia un flusso da un file a un altro, è necessario copiare sempre l'oggetto di configurazione del flusso dal profilo del file originale nel profilo del nuovo file. Ciò garantisce che siano disponibili le informazioni corrette sulla velocità in bit e sulla finestra del buffer. Se si copia un flusso compresso in un flusso con una finestra buffer inferiore impostata, gli esempi verranno eliminati durante la scrittura di file.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Scrittura di file ASF**](writing-asf-files.md)
</dt> </dl>

 

 




