---
description: Attributi del nodo della topologia
ms.assetid: 584c0670-9051-4d03-9635-c8fadc8798c3
title: Attributi del nodo della topologia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 904213752c0a3444bc4c9ea2b5cf2d5c21c8bd83
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103967121"
---
# <a name="topology-node-attributes"></a>Attributi del nodo della topologia

Gli attributi seguenti si applicano ai nodi della topologia.

## <a name="general-topology-node-attributes"></a>Attributi generali del nodo della topologia



| Attributo                                                                       | Descrizione                                                                                                                                              |
|---------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_Metodo MF TOPONODE \_ Connect \_**](mf-toponode-connect-method-attribute.md)   | Specifica il modo in cui il caricatore della topologia connette il nodo della topologia e se il nodo è facoltativo.                                                        |
| [**\_decodificatore MF TOPONODE \_**](mf-toponode-decoder-attribute.md)                  | Specifica se l'oggetto di un nodo della topologia è un decodificatore.                                                                                                  |
| [**\_Decryptor MF TOPONODE \_**](mf-toponode-decryptor-attribute.md)              | Specifica se l'oggetto sottostante di un nodo della topologia è un decrittografia.                                                                                     |
| [**MF \_ TOPONODE \_ scartabile**](mf-toponode-discardable-attribute.md)          | Specifica se la pipeline può eliminare campioni da un nodo di topologia.                                                                                    |
| [**\_MAJORTYPE di \_ errore MF TOPONODE \_**](mf-toponode-error-majortype-attribute.md) | Contiene il tipo di supporto principale per un nodo di topologia. Questo attributo viene impostato quando la topologia non viene caricata perché non è stato possibile trovare il decodificatore corretto. |
| [**sottotipo di \_ errore MF TOPONODE \_ \_**](mf-toponode-error-subtype-attribute.md)     | Contiene il sottotipo di supporto per un nodo di topologia. Questo attributo viene impostato quando la topologia non viene caricata perché non è stato possibile trovare il decodificatore corretto.    |
| [**\_ErrorCode MF TOPONODE \_**](mf-toponode-errorcode-attribute.md)              | Contiene il codice di errore dell'ultimo errore di connessione per questo nodo di topologia.                                                                  |
| [**MF \_ TOPONODE \_ bloccato**](mf-toponode-locked-attribute.md)                    | Specifica se i tipi di supporto possono essere modificati in questo nodo di topologia.                                                                                  |
| [**MF \_ TOPONODE \_ Markin \_ qui**](mf-toponode-markin-here-attribute.md)         | Specifica se la pipeline applica Mark-in a questo nodo.                                                                                             |
| [**TOPONODE di MF \_ \_ \_**](mf-toponode-markout-here-attribute.md)       | Specifica se la pipeline applica Mark-out a questo nodo.                                                                                            |



 

## <a name="source-node-attributes"></a>Attributi del nodo di origine



| Attributo                                                                                       | Descrizione                                                                                                       |
|-------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| [**MF \_ TOPONODE \_ MEDIASTART**](mf-toponode-mediastart-attribute.md)                            | Specifica l'ora di inizio di una presentazione, relativa all'avvio del file di origine del supporto, in unità 100-nanosecondi. |
| [**MF \_ TOPONODE \_ MEDIASTOP**](mf-toponode-mediastop-attribute.md)                              | Specifica l'ora di arresto di una presentazione, relativa all'avvio del file di origine del supporto, in unità 100-nanosecondi.  |
| [**descrittore di presentazione MF \_ TOPONODE \_ \_**](mf-toponode-presentation-descriptor-attribute.md) | Contiene un puntatore al descrittore di presentazione per l'origine multimediale.                                           |
| [**\_ \_ ElementID sequenza MF \_ TOPONODE**](mf-toponode-sequence-elementid-attribute.md)           | Specifica l'elemento che contiene un nodo di origine.                                                                |
| [**\_origine MF TOPONODE \_**](mf-toponode-source-attribute.md)                                    | Contiene un puntatore all'origine multimediale associata a un nodo di topologia.                                           |
| [**\_ \_ descrittore flusso MF TOPONODE \_**](mf-toponode-stream-descriptor-attribute.md)             | Contiene un puntatore al descrittore di flusso per l'origine multimediale.                                                 |
| [**\_ \_ ID WORKQUEUE MF \_ TOPONODE**](mf-toponode-workqueue-id-attribute.md)                       | Specifica una coda di lavoro per un nodo di topologia.                                                                       |
| [**Classe MMCSS di MF \_ TOPONODE \_ WORKQUEUE \_ \_**](mf-toponode-workqueue-mmcss-class-attribute.md)    | Specifica un'attività MMCSS (Multimedia Class Scheduler Service) per un nodo di topologia.                                  |
| [**MF \_ TOPONODE \_ WORKQUEUE \_ MMCSS \_ taskId**](mf-toponode-workqueue-mmcss-taskid-attribute.md)  | Specifica un identificatore di attività MMCSS per un nodo di topologia.                                                            |



 

## <a name="transform-node-attributes"></a>Trasforma attributi nodo



| Attributo                                                                             | Descrizione                                                                                                |
|---------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [**MF \_ TOPONODE \_ D3DAWARE**](mf-toponode-d3daware-attribute.md)                      | Specifica se la trasformazione associata a un nodo della topologia supporta l'accelerazione video DirectX (DXVA) |
| [**\_ \_ scaricamento MF TOPONODE**](mf-toponode-drain-attribute.md)                            | Specifica quando una trasformazione viene svuotata.                                                                     |
| [**\_ \_ scaricamento MF TOPONODE**](mf-toponode-flush-attribute.md)                            | Specifica quando una trasformazione viene scaricata.                                                                     |
| [**\_ \_ ObjectID trasformazione MF \_ TOPONODE**](mf-toponode-transform-objectid-attribute.md) | Identificatore di classe (CLSID) della trasformazione associata a questo nodo della topologia.                          |



 

## <a name="output-node-attributes"></a>Attributi del nodo di output



| Attributo                                                                                  | Descrizione                                                                                                      |
|--------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------|
| [**MF \_ TOPONODE \_ Disabilita \_ preroll**](mf-toponode-disable-preroll-attribute.md)            | Specifica se la sessione multimediale usa il preroll sul sink multimediale rappresentato da questo nodo di topologia.            |
| [**MF \_ TOPONODE \_ noshutdown \_ al \_ rimozione**](mf-toponode-noshutdown-on-remove-attribute.md) | Specifica se la sessione multimediale arresta il sink multimediale quando il nodo di output viene rimosso dalla topologia. |
| [**MF \_ TOPONODE \_ senza frequenza**](mf-toponode-rateless-attribute.md)                           | Specifica se il sink multimediale associato a questo nodo della topologia è senza frequenza.                                 |
| [**MF \_ TOPONODE \_ STREAMID**](mf-toponode-streamid-attribute.md)                           | Identificatore di flusso del sink di flusso associato a questo nodo della topologia.                                     |



 

## <a name="tee-node-attributes"></a>Attributi del nodo Tee



| Attributo                                                                  | Descrizione                                                 |
|----------------------------------------------------------------------------|-------------------------------------------------------------|
| [**MF \_ TOPONODE \_ PrimaryOutput poiché provocherebbe**](mf-toponode-primaryoutput-attribute.md) | Indica quale output è l'output primario in un nodo tee. |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**IMFTopologyNode**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[Attributi di Media Foundation](media-foundation-attributes.md)
</dt> <dt>

[Attributi della topologia](topology-attributes.md)
</dt> </dl>

 

 



