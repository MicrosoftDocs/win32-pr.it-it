---
description: Attributi del nodo della topologia
ms.assetid: 584c0670-9051-4d03-9635-c8fadc8798c3
title: Attributi del nodo della topologia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2ffd366c03607c4fc6646a09dae8571e6e4847a45b985f4996d28c15a828937
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119034669"
---
# <a name="topology-node-attributes"></a>Attributi del nodo della topologia

Gli attributi seguenti si applicano ai nodi della topologia.

## <a name="general-topology-node-attributes"></a>Attributi generali del nodo della topologia



| Attributo                                                                       | Descrizione                                                                                                                                              |
|---------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**METODO MF \_ TOPONODE \_ \_ CONNECT**](mf-toponode-connect-method-attribute.md)   | Specifica il modo in cui il caricatore della topologia connette questo nodo della topologia e se questo nodo è facoltativo.                                                        |
| [**DECODIFICATORE \_ TOPONODE MF \_**](mf-toponode-decoder-attribute.md)                  | Specifica se l'oggetto di un nodo toplogic è un decodificatore.                                                                                                  |
| [**MF \_ TOPONODE \_ DECRYPTOR**](mf-toponode-decryptor-attribute.md)              | Specifica se l'oggetto sottostante di un nodo toplogic è un decrittografo.                                                                                     |
| [**MF \_ TOPONODE \_ DISCARDABLE**](mf-toponode-discardable-attribute.md)          | Specifica se la pipeline può eliminare campioni da un nodo della topologia.                                                                                    |
| [**MF \_ TOPONODE \_ ERROR \_ MAJORTYPE**](mf-toponode-error-majortype-attribute.md) | Contiene il tipo di supporto principale per un nodo della topologia. Questo attributo viene impostato quando il caricamento della topologia non riesce perché non è stato trovato il decodificatore corretto. |
| [**SOTTOTIPO DI \_ ERRORE TOPONODE \_ \_ MF**](mf-toponode-error-subtype-attribute.md)     | Contiene il sottotipo di supporto per un nodo della topologia. Questo attributo viene impostato quando il caricamento della topologia non riesce perché non è stato trovato il decodificatore corretto.    |
| [**MF \_ TOPONODE \_ ERRORCODE**](mf-toponode-errorcode-attribute.md)              | Contiene il codice di errore dell'errore di connessione più recente per questo nodo della topologia.                                                                  |
| [**MF \_ TOPONODE \_ BLOCCATO**](mf-toponode-locked-attribute.md)                    | Specifica se i tipi di supporti possono essere modificati in questo nodo della topologia.                                                                                  |
| [**MF \_ TOPONODE \_ MARKIN \_ QUI**](mf-toponode-markin-here-attribute.md)         | Specifica se la pipeline applica il mark-in in questo nodo.                                                                                             |
| [**MF \_ TOPONODE \_ MARKOUT \_ QUI**](mf-toponode-markout-here-attribute.md)       | Specifica se la pipeline applica il mark-out in questo nodo.                                                                                            |



 

## <a name="source-node-attributes"></a>Attributi del nodo di origine



| Attributo                                                                                       | Descrizione                                                                                                       |
|-------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| [**MF \_ TOPONODE \_ MEDIASTART**](mf-toponode-mediastart-attribute.md)                            | Specifica l'ora di inizio di una presentazione, relativa all'inizio del file di origine multimediale, in unità da 100 nanosecondi. |
| [**MF \_ TOPONODE \_ MEDIASTOP**](mf-toponode-mediastop-attribute.md)                              | Specifica l'ora di arresto di una presentazione, relativa all'avvio del file di origine multimediale, in unità da 100 nanosecondi.  |
| [**DESCRITTORE DI \_ PRESENTAZIONE TOPONODE MF \_ \_**](mf-toponode-presentation-descriptor-attribute.md) | Contiene un puntatore al descrittore di presentazione per l'origine multimediale.                                           |
| [**ELEMENTI DELLA \_ SEQUENZA TOPONODE MF \_ \_**](mf-toponode-sequence-elementid-attribute.md)           | Specifica l'elemento che contiene un nodo di origine.                                                                |
| [**ORIGINE \_ TOPONODE MF \_**](mf-toponode-source-attribute.md)                                    | Contiene un puntatore all'origine multimediale associata a un nodo della topologia.                                           |
| [**DESCRITTORE DEL \_ FLUSSO TOPONODE MF \_ \_**](mf-toponode-stream-descriptor-attribute.md)             | Contiene un puntatore al descrittore di flusso per l'origine multimediale.                                                 |
| [**ID DELLA CODA DI \_ \_ LAVORO TOPONODE MF \_**](mf-toponode-workqueue-id-attribute.md)                       | Specifica una coda di lavoro per un nodo della topologia.                                                                       |
| [**CLASSE \_ MMCSS MF TOPONODE \_ WORKQUEUE \_ \_**](mf-toponode-workqueue-mmcss-class-attribute.md)    | Specifica un'attività del servizio Utilità di pianificazione classi multimediali (MMCSS) per un nodo della topologia.                                  |
| [**MF \_ TOPONODE \_ WORKQUEUE \_ MMCSS \_ TASKID**](mf-toponode-workqueue-mmcss-taskid-attribute.md)  | Specifica un identificatore di attività MMCSS per un nodo della topologia.                                                            |



 

## <a name="transform-node-attributes"></a>Attributi dei nodi di trasformazione



| Attributo                                                                             | Descrizione                                                                                                |
|---------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [**MF \_ TOPONODE \_ D3DAWARE**](mf-toponode-d3daware-attribute.md)                      | Specifica se la trasformazione associata a un nodo della topologia supporta DirectX Video Acceleration (DXVA) |
| [**MF \_ TOPONODE \_ DRAIN**](mf-toponode-drain-attribute.md)                            | Specifica quando viene svuotata una trasformazione.                                                                     |
| [**MF \_ TOPONODE \_ FLUSH**](mf-toponode-flush-attribute.md)                            | Specifica quando viene scaricata una trasformazione.                                                                     |
| [**MF \_ TOPONODE \_ TRANSFORM \_ OBJECTID**](mf-toponode-transform-objectid-attribute.md) | Identificatore di classe (CLSID) della trasformazione associata a questo nodo della topologia.                          |



 

## <a name="output-node-attributes"></a>Attributi del nodo di output



| Attributo                                                                                  | Descrizione                                                                                                      |
|--------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------|
| [**MF \_ TOPONODE \_ DISABLE \_ PREROLL**](mf-toponode-disable-preroll-attribute.md)            | Specifica se la sessione multimediale usa la pre-registrazione nel sink multimediale rappresentato da questo nodo della topologia.            |
| [**MF \_ TOPONODE \_ NOSHUTDOWN \_ ON \_ REMOVE**](mf-toponode-noshutdown-on-remove-attribute.md) | Specifica se la sessione multimediale arresta il sink multimediale quando il nodo di output viene rimosso dalla topologia. |
| [**MF \_ TOPONODE \_ RATELESS**](mf-toponode-rateless-attribute.md)                           | Specifica se il sink multimediale associato a questo nodo della topologia è senza frequenza.                                 |
| [**MF \_ TOPONODE \_ STREAMID**](mf-toponode-streamid-attribute.md)                           | Identificatore di flusso del sink di flusso associato a questo nodo della topologia.                                     |



 

## <a name="tee-node-attributes"></a>Attributi del nodo tee



| Attributo                                                                  | Descrizione                                                 |
|----------------------------------------------------------------------------|-------------------------------------------------------------|
| [**MF \_ TOPONODE \_ PRIMARYOUTPUT**](mf-toponode-primaryoutput-attribute.md) | Indica quale output è l'output primario in un nodo tee. |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**IMFTopologyNode**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[Media Foundation attributi](media-foundation-attributes.md)
</dt> <dt>

[Attributi della topologia](topology-attributes.md)
</dt> </dl>

 

 



