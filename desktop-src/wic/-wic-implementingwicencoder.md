---
description: Implementazione di un WIC-Enabled codificatore
ms.assetid: 9c1a4fa4-30b9-445f-8aee-46711355ace7
title: Implementazione di un WIC-Enabled codificatore
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b7f0bf3c073b3658c6c6edda6cf0761e3d594965b83b1b54206a48b62c96727
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118710930"
---
# <a name="implementing-a-wic-enabled-encoder"></a>Implementazione di un WIC-Enabled codificatore

## <a name="introduction"></a>Introduzione

L'implementazione Windows codificatore WIC (Windows Imaging Component) richiede la scrittura di due classi, come anche per l'implementazione di un decodificatore WIC. Le interfacce su queste classi corrispondono direttamente alle responsabilità del codificatore descritte nella sezione [Codifica](-wic-howwicworks.md) di Funzionamento del Windows imaging.

Una delle classi fornisce servizi a livello di contenitore e gestisce la serializzazione dei singoli fotogrammi immagine all'interno del contenitore. Questa classe implementa [**l'interfaccia IWICBitmapEncoder.**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) Se il formato dell'immagine supporta i metadati a livello di contenitore, è necessario implementare anche [**l'interfaccia IWICMetadataBlockWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter) in questa classe.

L'altra classe fornisce servizi a livello di frame ed esegue la codifica effettiva dei bit dell'immagine per ogni frame nel contenitore. Scorre anche i blocchi di metadati per ogni frame e richiede ai writer di metadati appropriati di serializzare i blocchi. Questa classe implementa **l'interfaccia IWICBitmapFrameEncode** e [**l'interfaccia IWICMetadataBlockWriter.**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter) Questa classe deve avere un membro IStream inizializzato dalla classe a livello di contenitore durante la creazione di un'istanza, in cui il metodo **Commit** serializza i dati del frame.

In alcuni casi, ad esempio nei formati non elaborati, l'autore del codec potrebbe non volere che le applicazioni siano in grado di codificare o ricodificare il formato non elaborato, perché lo scopo di un file non elaborato è quello di contenere i dati del sensore esattamente come provenivano dalla fotocamera. Nei casi in cui l'autore del codec non vuole abilitare la codifica, è comunque necessario implementare un codificatore rudimentale solo per abilitare l'aggiunta di metadati. In tal caso, il codificatore deve supportare solo i metodi necessari per la scrittura dei metadati e può copiare i bit dell'immagine senza modifiche dal decodificatore.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Riferimento**
</dt> <dt>

[**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Implementazione di IWICDevelopRaw](-wic-imp-iwicdevelopraw.md)
</dt> <dt>

[Interfacce del codificatore](-wic-encoderinterfaces.md)
</dt> <dt>

[Come scrivere un codec WIC-Enabled](-wic-howtowriteacodec.md)
</dt> <dt>

[Windows Cenni preliminari sul componente di creazione dell'immagine](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 



