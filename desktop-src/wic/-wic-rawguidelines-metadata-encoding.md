---
description: Codifica
ms.assetid: 501e63bf-26ef-42fb-b181-f1a8b26c122c
title: Codifica (Windows Imaging Component)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0b3d6eef499379bbdc668e70d5d0ec4326b390372da910934a6e7c7f547d177
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118964650"
---
# <a name="encoding-windows-imaging-component"></a>Codifica (Windows Imaging Component)

L'autore del codificatore deve eseguire le operazioni seguenti:

-   Implementare [**le interfacce IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) [**e IWICBitmapFrameEncode.**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)
-   Implementare [**IWICMetadataBlockWriter nel**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter) codificatore di fotogrammi. Se il codec supporta i metadati a livello di contenitore, questa interfaccia deve essere implementata nel codificatore a livello di contenitore e nel codificatore di fotogrammi.
-   Se il formato del contenitore contiene implicitamente blocchi di metadati obbligatori, creare un'istanza di un writer di metadati per ogni blocco di questo tipo. Ad esempio, il formato TIFF richiede un dispositivo di interfaccia (IFD) per ogni frame, quindi il writer IFD deve essere sempre esposto.
-   Implementare il supporto per la gestione della raccolta di writer di metadati. Il block writer gestisce tutti i requisiti di ordine o le restrizioni dei contenitori sui tipi di blocchi di metadati che possono essere codificati. Il block writer deve verificare che i nuovi writer di metadati possano essere incorporati nel formato del contenitore.
-   Quando si codifica il flusso di immagini, chiamare [**WICSerializeMetadataContent**](/windows/desktop/api/wincodecsdk/nf-wincodecsdk-wicserializemetadatacontent) per serializzare il contenuto di ogni writer di metadati nel flusso. Se il blocco di metadati contiene metadati "critici", il codificatore deve impostare gli elementi di metadati critici prima di chiedere al writer di metadati di serializzare il contenuto.
-   Verificare la presenza di gestori di metadati sconosciuti per assicurarsi che non siano presenti blocchi di metadati ridondanti. Questo è importante perché, pur mantenendo i metadati in uno scenario di decodifica o codifica, i blocchi sconosciuti potrebbero essere un duplicato dei blocchi di metadati obbligatori.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Informazioni concettuali**
</dt> <dt>

[Windows Panoramica del componente di creazione dell'immagine](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[Linee guida WIC per i formati di immagine RAW della fotocamera](-wic-rawguidelines.md)
</dt> <dt>

[Come scrivere un codec WIC-Enabled](-wic-howtowriteacodec.md)
</dt> </dl>

 

 



