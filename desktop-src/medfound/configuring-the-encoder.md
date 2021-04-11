---
description: Proprietà di codifica
ms.assetid: 6845c3fb-38a8-4b0d-aea2-e10f7e518653
title: Proprietà di codifica
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 093b72dc37501ca88882c6e3b530cda0eed1baa2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127955"
---
# <a name="encoding-properties"></a>Proprietà di codifica

I codificatori Windows Media Audio e Windows Media Video supportano un'ampia gamma di modalità di codifica. Queste modalità vengono in genere configurate impostando le proprietà del codificatore [Media Foundation trasformazione](media-foundation-transforms.md) (MFT). Per eseguire la codifica dei file, sia che si utilizzino componenti a livello di WMContainer che compilando una topologia parziale, è necessario configurare il codificatore in modo appropriato, impostando le proprietà in base alla modalità di codifica e al tipo di supporto del flusso. Per scrivere il file ASF è necessario impostare lo stesso set di proprietà sia nel codificatore che nell'oggetto (sink di file ASF o nel multiplexer ASF) utilizzato.

Le proprietà del codificatore sono definite in wmcodecdsp. h. Le proprietà specifiche utilizzate per configurare il codificatore vengono impostate utilizzando i metodi dell'interfaccia [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) .

-   [Proprietà del flusso audio](#audio-stream-properties)
-   [Proprietà del flusso video](#video-stream-properties)
-   [Configurazione dell'archivio di proprietà del codificatore](#configuring-the-encoders-property-store)

### <a name="audio-stream-properties"></a>Proprietà del flusso audio

La tabella seguente illustra le configurazioni del codificatore per un flusso audio.



| Tipo di codifica                                                                                        | Nome proprietà-valore                                                                                                                                                                               |
|------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Codifica della velocità in bit costante](constant-bit-rate-encoding.md)                                         | MFPKEY \_ VBRENABLED- **false** (facoltativo) per impostazione predefinita, MFPKEY \_ VBRENABLED è impostato su **false**.<br/>                                                                                             |
| [Codifica della velocità in bit della variabile basata sulla qualità](quality-based-variable-bit-rate--vbr--encoding.md)       | MFPKEY \_ VBRENABLED- **true**<br/> MFPKEY \_ PASSESUSED-1 (facoltativo)<br/> Per impostazione predefinita, MFPKEY \_ PASSESUSED è impostato su 1.<br/> MFPKEY \_ desired \_ VBRQUALITY-da 0 a 100<br/> |
| [Codifica della velocità in bit variabile non vincolata](unconstrained-variable-bit-rate--vbr--encoding.md)       | MFPKEY \_ VBRENABLED- **true**<br/> MFPKEY \_ PASSESUSED-2<br/>                                                                                                                          |
| [Codifica della velocità in bit a variabili con vincoli di picco](peak-constrained-variable-bit-rate--vbr--encoding.md) | MFPKEY \_ VBRENABLED- **true**<br/> MFPKEY \_ PASSESUSED-2<br/> MFPKEY \_ Rmax-velocità in bit massima<br/> MFPKEY \_ BMAX-finestra buffer massima<br/>                               |



 

### <a name="video-stream-properties"></a>Proprietà del flusso video

La tabella seguente illustra le configurazioni del codificatore per un flusso video.



| Tipo di codifica                                                                                        | Nome proprietà                                                                                                                                                                                       |
|------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Codifica della velocità in bit costante](constant-bit-rate-encoding.md)                                         | MFPKEY \_ VBRENABLED- **false** (facoltativo)<br/> Per impostazione predefinita, MFPKEY \_ VBRENABLED è impostato su **false**.<br/> MFPKEY \_ VIDEOWINDOW-finestra buffer<br/>                                  |
| [Codifica della velocità in bit della variabile basata sulla qualità](quality-based-variable-bit-rate--vbr--encoding.md)       | MFPKEY \_ VBRENABLED- **true**<br/> MFPKEY \_ PASSESUSED-1 (facoltativo)<br/> Per impostazione predefinita, MFPKEY \_ PASSESUSED è impostato su 1.<br/> MFPKEY \_ desired \_ VBRQUALITY-da 0 a 100<br/> |
| [Codifica della velocità in bit variabile non vincolata](unconstrained-variable-bit-rate--vbr--encoding.md)       | MFPKEY \_ VBRENABLED- **true**<br/> MFPKEY \_ PASSESUSED-2<br/>                                                                                                                          |
| [Codifica della velocità in bit a variabili con vincoli di picco](peak-constrained-variable-bit-rate--vbr--encoding.md) | MFPKEY \_ VBRENABLED- **true**<br/> MFPKEY \_ PASSESUSED-2<br/> MFPKEY \_ Rmax-velocità in bit massima<br/> MFPKEY \_ BMAX-finestra buffer massima<br/>                               |



 

### <a name="configuring-the-encoders-property-store"></a>Configurazione dell'archivio di proprietà del codificatore

È necessario configurare un codificatore specificando il tipo di codifica e le varie impostazioni specifiche del flusso prima della sessione di codifica. È inoltre necessario impostare le proprietà del codificatore nell'archivio delle proprietà di un oggetto di una configurazione [ASF](asf-contentinfo-object.md) che rappresenta l'oggetto intestazione ASF del file di output.

Se si usa un codificatore MFT:

1.  Ottenere un riferimento all'interfaccia [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) di MFT del codificatore, come descritto in [uso dell'interfaccia IMFTransform di un codificatore](using-an-encoder-s-imftransform--interface.md).
2.  Esecuzione di query sul codificatore MFT per l'interfaccia **IPropertyStore** .
3.  Impostazione delle proprietà obbligatorie chiamando **IPropertyStore:: SetValue**.

Se si usano gli oggetti di attivazione del codificatore incorporati ed è già stato creato un sink di file ASF configurato, è possibile passare l'archivio delle proprietà del sink multimediale ASF a [**MFCreateWMAEncoderActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreatewmaencoderactivate) o [**MFCreateWMVEncoderActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreatewmvencoderactivate). Il codificatore viene configurato automaticamente in base alle impostazioni specificate dall'applicazione. Per ulteriori informazioni, vedere la procedura descritta in [utilizzo di oggetti di attivazione di un codificatore](using-an-encoder-s-activation-objects.md).

Per ulteriori informazioni sulla creazione di oggetti Media Foundation tramite oggetti Activation, vedere [oggetti Activation](activation-objects.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Creazione di un'istanza di un codificatore MFT](instantiating-the-encoder-mft.md)
</dt> <dt>

[Codificatori Windows Media](windows-media-encoders.md)
</dt> </dl>

 

 
