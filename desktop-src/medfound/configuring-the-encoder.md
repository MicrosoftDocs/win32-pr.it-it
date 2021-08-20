---
description: Proprietà di codifica
ms.assetid: 6845c3fb-38a8-4b0d-aea2-e10f7e518653
title: Proprietà di codifica
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bc7a1528e68153c742ece8c8d7fcb34bfb9b7bbc08f86567f51b54754bb6da3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118743493"
---
# <a name="encoding-properties"></a>Proprietà di codifica

I Windows Media Audio e Windows Media Video supportano un'ampia gamma di modalità di codifica. Queste modalità vengono in genere configurate impostando proprietà sul [codificatore Media Foundation transform](media-foundation-transforms.md) (MFT). Per eseguire la codifica dei file, sia che si utilizzino componenti a livello di WMContainer che compilando una topologia parziale, è necessario configurare il codificatore in modo appropriato impostando le proprietà in base alla modalità di codifica e al tipo di supporto del flusso. Lo stesso set di proprietà deve essere impostato sia nel codificatore che nell'oggetto (sink di file ASF o multiplexer ASF) in uso per scrivere il file ASF.

Le proprietà del codificatore sono definite in wmcodecdsp.h. Le proprietà specifiche usate per configurare il codificatore vengono impostate usando i metodi [**dell'interfaccia IPropertyStore.**](/windows/win32/api/propsys/nn-propsys-ipropertystore)

-   [Proprietà del flusso audio](#audio-stream-properties)
-   [Proprietà del flusso video](#video-stream-properties)
-   [Configurazione delle impostazioni del codificatore Archivio proprietà](#configuring-the-encoders-property-store)

### <a name="audio-stream-properties"></a>Proprietà del flusso audio

La tabella seguente illustra le configurazioni del codificatore per un flusso audio.



| Tipo di codifica                                                                                        | Nome proprietà - Valore                                                                                                                                                                               |
|------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Codifica a velocità in bit costante](constant-bit-rate-encoding.md)                                         | MFPKEY \_ VBRENABLED - **FALSE** (facoltativo)Per impostazione predefinita, MFPKEY \_ VBRENABLED è impostato su **FALSE.**<br/>                                                                                             |
| [Codifica della velocità in bit variabile basata sulla qualità](quality-based-variable-bit-rate--vbr--encoding.md)       | MFPKEY \_ VBRENABLED - **TRUE**<br/> MFPKEY \_ PASSESUSED - 1 (facoltativo)<br/> Per impostazione predefinita, MFPKEY \_ PASSESUSED è impostato su 1.<br/> MFPKEY \_ DESIRED \_ VBRQUALITY : da 0 a 100<br/> |
| [Codifica a velocità in bit variabile non vincolata](unconstrained-variable-bit-rate--vbr--encoding.md)       | MFPKEY \_ VBRENABLED - **TRUE**<br/> MFPKEY \_ PASSESUSED - 2<br/>                                                                                                                          |
| [Codifica della velocità in bit delle variabili con vincoli di picco](peak-constrained-variable-bit-rate--vbr--encoding.md) | MFPKEY \_ VBRENABLED - **TRUE**<br/> MFPKEY \_ PASSESUSED - 2<br/> MFPKEY \_ RMAX - Velocità in bit massima<br/> MFPKEY \_ BMAX - Finestra buffer massima<br/>                               |



 

### <a name="video-stream-properties"></a>Proprietà del flusso video

La tabella seguente illustra le configurazioni del codificatore per un flusso video.



| Tipo di codifica                                                                                        | Nome proprietà                                                                                                                                                                                       |
|------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Codifica a velocità in bit costante](constant-bit-rate-encoding.md)                                         | MFPKEY \_ VBRENABLED - **FALSE** (facoltativo)<br/> Per impostazione predefinita, MFPKEY \_ VBRENABLED è impostato su **FALSE.**<br/> MFPKEY \_ VIDEOWINDOW - Finestra Buffer<br/>                                  |
| [Codifica della velocità in bit variabile basata sulla qualità](quality-based-variable-bit-rate--vbr--encoding.md)       | MFPKEY \_ VBRENABLED - **TRUE**<br/> MFPKEY \_ PASSESUSED - 1 (facoltativo)<br/> Per impostazione predefinita, MFPKEY \_ PASSESUSED è impostato su 1.<br/> MFPKEY \_ DESIRED \_ VBRQUALITY : da 0 a 100<br/> |
| [Codifica a velocità in bit variabile non vincolata](unconstrained-variable-bit-rate--vbr--encoding.md)       | MFPKEY \_ VBRENABLED - **TRUE**<br/> MFPKEY \_ PASSESUSED - 2<br/>                                                                                                                          |
| [Codifica della velocità in bit delle variabili con vincoli di picco](peak-constrained-variable-bit-rate--vbr--encoding.md) | MFPKEY \_ VBRENABLED - **TRUE**<br/> MFPKEY \_ PASSESUSED - 2<br/> MFPKEY \_ RMAX - Velocità in bit massima<br/> MFPKEY \_ BMAX - Finestra buffer massima<br/>                               |



 

### <a name="configuring-the-encoders-property-store"></a>Configurazione delle impostazioni del codificatore Archivio proprietà

È necessario configurare un codificatore specificando il tipo di codifica e le varie impostazioni specifiche del flusso prima della sessione di codifica. È inoltre necessario impostare le proprietà del codificatore nell'archivio delle proprietà di un oggetto [ContentInfo di ASF](asf-contentinfo-object.md) che rappresenta l'oggetto intestazione ASF del file di output.

Se si usa un codificatore MFT:

1.  Ottenere un riferimento all'interfaccia [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) del codificatore MFT come descritto in [Uso dell'interfaccia IMFTransform di un codificatore.](using-an-encoder-s-imftransform--interface.md)
2.  Esecuzione di query sul codificatore MFT per **l'interfaccia IPropertyStore.**
3.  Impostare le proprietà necessarie chiamando **IPropertyStore::SetValue**.

Se si usano gli oggetti di attivazione del codificatore predefiniti ed è già stato creato un sink di file ASF configurato, è possibile passare l'archivio delle proprietà del sink multimediale asf a [**MFCreateWMAEncoderActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreatewmaencoderactivate) o [**MFCreateWMVEncoderActivate.**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreatewmvencoderactivate) Il codificatore viene configurato automaticamente in base alle impostazioni specificate dall'applicazione. Per altre informazioni, vedere la procedura descritta in [Uso degli oggetti di attivazione di un codificatore.](using-an-encoder-s-activation-objects.md)

Per altre informazioni sulla creazione di Media Foundation di attivazione tramite oggetti di attivazione, vedere [Oggetti di attivazione.](activation-objects.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Creazione di un'istanza di un codificatore MFT](instantiating-the-encoder-mft.md)
</dt> <dt>

[Windows Codificatori multimediali](windows-media-encoders.md)
</dt> </dl>

 

 
