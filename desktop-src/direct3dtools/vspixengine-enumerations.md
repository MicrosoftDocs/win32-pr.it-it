---
description: Le enumerazioni seguenti sono dichiarate in vspixengine.h.
MS-HAID: vspixengine.vspixengine\_enumerations
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Enumerazioni dell'interfaccia di acquisizione diagnostica Direct3D
ms.topic: article
ms.date: 05/31/2018
ms.assetid: A67402DE-8CBF-470A-97B4-3CF531731F24
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 94b5e656a1012f8b48cd4fbc34f34d94a145872d
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2021
ms.locfileid: "122626167"
---
# <a name="span-idvspixenginevspixengine_enumerationsspandirect3d-diagnostics-capture-interface-enumerations"></a><span id="vspixengine.vspixengine_enumerations"></span>Enumerazioni dell'interfaccia di acquisizione diagnostica Direct3D

Le enumerazioni seguenti sono dichiarate in vspixengine.h.

## <a name="span-idin_this_sectionspanin-this-section"></a><span id="in_this_section"></span>In questa sezione

<table><colgroup><col  /><col  /></colgroup><thead><tr class="header"><th>Argomento</th><th>Descrizione</th></tr></thead><tbody><tr class="odd"><td><p><a href="/windows/desktop/direct3dtools/xml-resource-ids"><strong>Xml_Resource_Ids</strong></a></p></td><td><p>ID stringa di risorsa impostati dal chiamante da restituire nei dati XML per la visualizzazione di oggetti</p></td></tr><tr class="even"><td><p><a href="/windows/desktop/direct3dtools/resource-id"><strong>Resource_Id</strong></a></p></td><td><p>Definisce gli ID risorsa per le risorse di stringa condivise. Questi vengono passati al motore di acquisizione dall'host. Vengono usate per visualizzare le stringhe nella sovrimpressione HUD dell'app acquisita o per passare i valori del Registro di sistema dalle opzioni Visual Studio all'engi di acquisizione</p></td></tr><tr class="odd"><td><p><a href="/windows/desktop/direct3dtools/hresult"><strong>Hresult</strong></a></p></td><td><p>Valori HRESULT personalizzati per l'interfaccia di acquisizione della diagnostica grafica.</p></td></tr><tr class="even"><td><p><a href="/windows/desktop/direct3dtools/remotecommandtype"><strong>RemoteCommandType</strong></a></p></td><td><p>Enumerazione utilizzata per comunicare tra il motore di acquisizione e un host,ad esempio Visual Studio Diagnostica della grafica.</p></td></tr><tr class="odd"><td><p><a href="/windows/desktop/direct3dtools/callbackcommandtype"><strong>CallbackCommandType</strong></a></p></td><td><p>Enumerazione utilizzata per comunicare tra il motore di acquisizione e un host,ad esempio Visual Studio Diagnostica della grafica.</p></td></tr><tr class="even"><td><p><a href="/windows/desktop/direct3dtools/pixpiperesponse"><strong>PixPipeResponse</strong></a></p></td><td><p>Enumerazione utilizzata per inviare risposte dal motore di acquisizione Diagnostica della grafica.</p></td></tr><tr class="odd"><td><p><a href="/windows/desktop/direct3dtools/remotingversion"><strong>REMOTINGVERSION</strong></a></p></td><td><p>Enumerazione utilizzata per indicare la versione del protocolo di comunicazione remota in uso.</p></td></tr><tr class="even"><td><p><a href="/windows/desktop/direct3dtools/pixelkillreason"><strong>PIXELKILLREASON</strong></a></p></td><td><p>Enumerazione utilizzata per indicare il motivo per cui un pixel è stato rifiutato.</p></td></tr><tr class="odd"><td><p><a href="/windows/desktop/direct3dtools/pixelhistoryflags"><strong>PIXELHISTORYFLAGS</strong></a></p></td><td><p>Enumerazione contenente i flag utilizzati per descrivere un risultato della cronologia dei pixel. Vedere PixelHistoryOperation.</p></td></tr><tr class="even"><td><p><a href="/windows/desktop/direct3dtools/eventcolumnid"><strong>EVENTCOLUMNID</strong></a></p></td><td><p>Enumerazione utilizzata per indicare ID di colonna noti. si tratta di ID colonna che tutte le implementazioni devono supportare.</p></td></tr><tr class="odd"><td><p><a href="/windows/desktop/direct3dtools/objectstatetype"><strong>OBJECTSTATETYPE</strong></a></p></td><td><p>Interno</p></td></tr><tr class="even"><td><p><a href="/windows/desktop/direct3dtools/objecttablecolumnid"><strong>OBJECTTABLECOLUMNID</strong></a></p></td><td><p>Enumerazione utilizzata per indicare le proprietà dei dati restituiti da una richiesta di tabella di oggetti. Per altre informazioni, vedere IObjectTableRequest.</p></td></tr><tr class="odd"><td><p><a href="/windows/desktop/direct3dtools/pipelinestages"><strong>PIPELINESTAGES</strong></a></p></td><td><p>Enumerazione utilizzata per indicare una fase della pipeline grafica.</p></td></tr><tr class="even"><td><p><a href="/windows/desktop/direct3dtools/checksumalgorithm"><strong>CHECKSUMALGORITHM</strong></a></p></td><td><p>Enumerazione utilizzata per indicare l'algoritmo di checksum da utilizzare.</p></td></tr><tr class="odd"><td><p><a href="/windows/desktop/direct3dtools/eventtype"><strong>EVENTTYPE</strong></a></p></td><td><p>Enumerazione utilizzata per indicare il tipo di un evento.</p></td></tr><tr class="even"><td><p><a href="/windows/desktop/direct3dtools/descriptor-heap-header-columns"><strong>DESCRIPTOR_HEAP_HEADER_COLUMNS</strong></a></p></td><td><p>Enumerazione utilizzata per indicare un'intestazione coumn nel visualizzatore heap del descrittore</p></td></tr><tr class="odd"><td><p><a href="/windows/desktop/direct3dtools/descriptor-heap-columns"><strong>DESCRIPTOR_HEAP_COLUMNS</strong></a></p></td><td><p>Enumerazione utilizzata per indicare una colonna nel visualizzatore heap del descrittore.</p></td></tr><tr class="even"><td><p><a href="/windows/desktop/direct3dtools/experimenttype"><strong>EXPERIMENTTYPE</strong></a></p></td></tr><tr class="odd"><td><p><a href="/windows/desktop/direct3dtools/dumpertype"><strong>DUMPERTYPE</strong></a></p></td><td><p>Enumerazione utilizzata per indicare il tipo di buffer restituito da IGenericBufferDataRequest.</p></td></tr><tr class="even"><td><p><a href="/windows/desktop/direct3dtools/experimenttriggertype"><strong>EXPERIMENTTRIGGERTYPE</strong></a></p></td></tr><tr class="odd"><td><p><a href="/windows/desktop/direct3dtools/register-format"><strong>REGISTER_FORMAT</strong></a></p></td><td><p>Interno</p></td></tr><tr class="even"><td><p><a href="/windows/desktop/direct3dtools/primitive-topology"><strong>PRIMITIVE_TOPOLOGY</strong></a></p></td><td><p>Enumerazione utilizzata per indicare la topologia di una mesh. Vedere MeshDataVertCallback.</p></td></tr><tr class="odd"><td><p><a href="/windows/desktop/direct3dtools/offlineanalysisstage"><strong>OFFLINEANALYSISSTAGE</strong></a></p></td><td><p>Enumerazione utilizzata per indicare le fasi di avanzamento nell'analisi dei frame.</p></td></tr><tr class="even"><td><p><a href="/windows/desktop/direct3dtools/offlineanalysissource"><strong>OFFLINEANALYSISSOURCE</strong></a></p></td><td><p>Enumerazione utilizzata per indicare l'origine delle informazioni grafiche per l'analisi dei frame.</p></td></tr></tbody></table>

 

## <a name="span-idrelated_topicsspanrelated-topics"></a><span id="related_topics"></span>Argomenti correlati

[Informazioni di riferimento su Direct3D Diagnostics Capture Interface](vspixengine-reference.md)

 

 
