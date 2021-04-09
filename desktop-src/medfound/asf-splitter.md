---
description: Barra di divisione ASF
ms.assetid: 383b1cc6-4a77-4e0e-a766-6213c64b025c
title: Barra di divisione ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1f61bcd17a81197106d2f7c43fa1fdc25d9da2d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128003"
---
# <a name="asf-splitter"></a>Barra di divisione ASF

L'oggetto *splitter* ASF è un componente di livello WMContainer che analizza l'oggetto dati ASF di un file di formato Advanced Systems (ASF). È possibile utilizzare la barra di divisione per leggere i pacchetti di dati nell'oggetto dati e generare esempi di flusso. Per informazioni sulla struttura di un file ASF, vedere la pagina relativa alla [struttura dei file ASF](asf-file-structure.md).

La barra di divisione espone l'interfaccia [**IMFASFSplitter**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfsplitter) . La barra di divisione analizza i pacchetti di dati ASF per i flussi selezionati e li riassembla in singoli oggetti di esempio che espongono l'interfaccia [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) . La barra di divisione è uno dei componenti a livello di piattaforma di Media Foundation. Per analizzare i file ASF, l'origine dei supporti ASF usa internamente la barra di divisione.

Il diagramma seguente illustra la generazione di esempi per un file ASF tramite la barra di divisione.

![diagramma che illustra la generazione di esempio di un file ASF](images/1eb9789c-c586-4f44-b907-b086cf288cc1.gif)

Questa sezione contiene i seguenti argomenti:



| Argomento                                                                                                                        | Descrizione                                                             |
|------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| [Creazione dell'oggetto Splitter ASF](creating-the-asf-splitter-object.md)                                                     | Come creare e inizializzare la barra di divisione.                              |
| [Configurazione dell'oggetto Splitter ASF](configuring-the-asf-splitter-object.md)                                               | Impostazioni di configurazione per la barra di divisione.                                |
| [Generazione di esempi di flusso da un oggetto dati ASF esistente](generating-stream-samples-from-an-existing-asf-data-object.md) | Come analizzare l'oggetto dati ASF e generare esempi di vapore in pacchetto. |



 

Nella tabella seguente vengono illustrati gli attributi dell'oggetto dati rilevanti.



| Attributo                                                                                                    | Descrizione                                                                                          |
|--------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [**\_ \_ \_ pacchetti FileProperties ASF MF \_ PD**](mf-pd-asf-fileproperties-packets-attribute.md)                   | Numero di pacchetti di dati nell'oggetto dati ASF.                                                       |
| [**\_ \_ \_ \_ dimensioni minime del \_ pacchetto \_ per le proprietà ASF del valore MF PD ASF**](mf-pd-asf-fileproperties-min-packet-size-attribute.md) | Dimensioni minime dei pacchetti di dati nel file, in byte.                                              |
| [**\_dimensioni del \_ \_ \_ pacchetto max PD ASF FileProperties \_ \_**](mf-pd-asf-fileproperties-max-packet-size-attribute.md) | Dimensioni massime dei pacchetti di dati nel file, in byte                                               |
| [**\_ \_ \_ lunghezza dei dati MF PD ASF \_**](mf-pd-asf-data-length-attribute.md)                                         | Dimensioni dell'oggetto dati ASF, in byte.                                                               |
| [**\_ \_ \_ \_ offset avvio dati ASF MF PD \_**](mf-pd-asf-data-start-offset-attribute.md)                            | Offset, in byte, per il primo pacchetto di dati nell'oggetto dati ASF relativo all'inizio del file. |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Componenti ASF WMContainer](wmcontainer-asf-components.md)
</dt> <dt>

[Esercitazione: lettura di un file ASF](tutorial--reading-an-asf-file.md)
</dt> <dt>

[Supporto ASF in Media Foundation](asf-support-in-media-foundation.md)
</dt> </dl>

 

 



