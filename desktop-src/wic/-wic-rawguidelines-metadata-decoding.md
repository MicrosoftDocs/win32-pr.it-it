---
description: Decodifica
ms.assetid: ff7e5e66-e1ea-49fc-909f-de361214afc3
title: Decodifica
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6700865d55ba7349447f5e41285d60446f0e4630
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103883962"
---
# <a name="decoding"></a>Decodifica

Per supportare correttamente i metadati, gli autori del decodificatore devono eseguire le operazioni seguenti:

-   Implementare le interfacce [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) e [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) .
-   Implementare [**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) nel decodificatore di frame. Se il codec supporta i metadati a livello di contenitore, questa interfaccia deve essere implementata nel decodificatore a livello di contenitore e nel decodificatore di frame.
-   Durante la decodifica del flusso di immagini, chiamare [**IWICComponentFactory**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwiccomponentfactory)::[**CreateMetadataReaderFromContainer**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwiccomponentfactory-createmetadatareaderfromcontainer) per creare un'istanza di un lettore di metadati per ogni blocco di metadati. (Tutti i nuovi lettori di metadati implementati dal codec devono essere registrati con WIC).

    Il decodificatore non deve creare i lettori di metadati in modo autonomo, bensì utilizzare WIC per crearli in base ai blocchi di metadati nel flusso. Il decodificatore deve eseguire questa operazione su tutti i blocchi che trova, anche se non sono noti in modo nativo a docoder, perché i lettori di metadati futuri potrebbero essere installati nel sistema in grado di gestire questi blocchi di metadati.

-   Se non è presente alcun gestore di metadati per un blocco, creare un'istanza del lettore di metadati sconosciuti usando le opzioni di creazione dei metadati.
-   Esporre la raccolta di Reader di metadati tramite l'interfaccia [**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) .

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

 

 



