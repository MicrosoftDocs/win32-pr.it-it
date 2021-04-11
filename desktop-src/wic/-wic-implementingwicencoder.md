---
description: Implementazione di un codificatore di WIC-Enabled
ms.assetid: 9c1a4fa4-30b9-445f-8aee-46711355ace7
title: Implementazione di un codificatore di WIC-Enabled
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6e65f969ba7c65e6860009b2fc998024d358301
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232472"
---
# <a name="implementing-a-wic-enabled-encoder"></a>Implementazione di un codificatore di WIC-Enabled

## <a name="introduction"></a>Introduzione

L'implementazione di un codificatore Windows Imaging Component (WIC) richiede la scrittura di due classi, come accade anche per l'implementazione di un decodificatore WIC. Le interfacce di queste classi corrispondono direttamente alle responsabilità del codificatore descritte nella sezione relativa alla [codifica](-wic-howwicworks.md) del funzionamento del componente Windows Imaging.

Una delle classi fornisce servizi a livello di contenitore e gestisce la serializzazione dei singoli frame di immagine all'interno del contenitore. Questa classe implementa l'interfaccia [**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) . Se il formato dell'immagine supporta i metadati a livello di contenitore, è necessario implementare anche l'interfaccia [**IWICMetadataBlockWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter) in questa classe.

L'altra classe fornisce servizi a livello di frame ed esegue la codifica effettiva dei bit dell'immagine per ogni fotogramma nel contenitore. Scorre inoltre i blocchi di metadati per ogni frame e richiede ai writer di metadati appropriati di serializzare i blocchi. Questa classe implementa l'interfaccia **IWICBitmapFrameEncode** e l'interfaccia [**IWICMetadataBlockWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter) . Questa classe deve avere un membro IStream che la classe a livello di contenitore Inizializza durante la creazione dell'istanza, in cui il metodo **commit** serializza i dati del frame.

In alcuni casi, ad esempio formati non elaborati, è possibile che l'autore del codec non desideri che le applicazioni siano in grado di codificare o ricodificare nel formato non elaborato, perché lo scopo di un file non elaborato è quello di contenere i dati del sensore esattamente come provengono dalla fotocamera. Nei casi in cui l'autore del codec non vuole abilitare la codifica, è comunque necessario implementare un codificatore rudimentale solo per consentire l'aggiunta di metadati. In tal caso, il codificatore deve supportare solo questi metodi necessari per la scrittura dei metadati e può copiare i bit dell'immagine non modificati dal decodificatore.

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

[Come scrivere un CODEC WIC-Enabled](-wic-howtowriteacodec.md)
</dt> <dt>

[Panoramica del componente imaging Windows](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 



