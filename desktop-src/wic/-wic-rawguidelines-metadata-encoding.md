---
description: Codifica
ms.assetid: 501e63bf-26ef-42fb-b181-f1a8b26c122c
title: Codifica (componente Windows Imaging)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d6d15b983b7455d0fe0c406cbad64dbbb77588b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315943"
---
# <a name="encoding-windows-imaging-component"></a>Codifica (componente Windows Imaging)

L'autore del codificatore deve eseguire le operazioni seguenti:

-   Implementare le interfacce [**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) e [**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) .
-   Implementare [**IWICMetadataBlockWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter) nel codificatore di frame. Se il codec supporta i metadati a livello di contenitore, questa interfaccia deve essere implementata nel codificatore a livello di contenitore e nel codificatore di frame.
-   Se il formato del contenitore contiene implicitamente eventuali blocchi di metadati obbligatori, creare un'istanza di un writer di metadati per ogni blocco di questo tipo. Il formato TIFF, ad esempio, richiede un dispositivo di interfaccia (IFD) per ogni fotogramma, quindi il writer IFD deve sempre essere esposto.
-   Implementare il supporto per la gestione della raccolta di writer di metadati. Il writer del blocco gestisce tutti i requisiti dell'ordine o le restrizioni del contenitore sui tipi di blocchi di metadati che possono essere codificati. Il writer del blocco deve verificare che tutti i nuovi writer di metadati possano essere incorporati nel formato del contenitore.
-   Quando si codifica il flusso di immagini, chiamare [**WICSerializeMetadataContent**](/windows/desktop/api/wincodecsdk/nf-wincodecsdk-wicserializemetadatacontent) per serializzare il contenuto di ogni writer di metadati nel flusso. Se il blocco di metadati contiene metadati "critici", il codificatore deve impostare gli elementi di metadati critici prima di chiedere al writer dei metadati di serializzare il contenuto.
-   Verificare la presenza di gestori di metadati sconosciuti per assicurarsi che i blocchi di metadati ridondanti non siano presenti. Questo è importante perché, mantenendo i metadati in uno scenario di decodifica o codifica, i blocchi sconosciuti potrebbero essere un duplicato di blocchi di metadati obbligatori.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Informazioni concettuali**
</dt> <dt>

[Panoramica del componente imaging Windows](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[Linee guida per WIC per i formati di immagine RAW della fotocamera](-wic-rawguidelines.md)
</dt> <dt>

[Come scrivere un CODEC WIC-Enabled](-wic-howtowriteacodec.md)
</dt> </dl>

 

 



