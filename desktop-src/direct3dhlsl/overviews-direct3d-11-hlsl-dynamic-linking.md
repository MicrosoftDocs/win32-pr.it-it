---
title: Collegamento dinamico
description: Gli sviluppatori di grafica talvolta creano shader di grandi dimensioni e per utilizzo generico che possono essere usati da un'ampia gamma di elementi della scena.
ms.assetid: 2f5f7852-0f0a-4fad-a412-9a0d634c73b6
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: d5cd10bab8e2b4a28458cad1050847e0184ce43b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103710861"
---
# <a name="dynamic-linking"></a>Collegamento dinamico

Gli sviluppatori di grafica talvolta creano shader di grandi dimensioni e per utilizzo generico che possono essere usati da un'ampia gamma di elementi della scena. In fase di esecuzione, lo shader esegue in modo condizionale il codice appropriato per la situazione specificata. Sfortunatamente, questi shader di uso generale di grandi dimensioni usano i registri di utilizzo generico (GPRs) in modo non efficiente e possono essere molto più lenti rispetto agli shader più piccoli e più mirati.

Il modello di shader 5 risolve questo problema di prestazioni introducendo il collegamento dinamico dello shader. Il collegamento dinamico separa i frammenti di codice dello shader usando le interfacce e le funzioni virtuali e consente all'applicazione di selezionare il frammento da usare in fase di estrazione. Ciò consente di migliorare le prestazioni associando solo il codice dello shader necessario e non l'intero shader di utilizzo generico.

## <a name="in-this-section"></a>Contenuto della sezione



| Elemento                                                                                                                                                                                                                                                                                                                         | Descrizione                                                                                                    |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span id="Storing_Variables_and_Types_for_Shaders_to_Share"></span><span id="storing_variables_and_types_for_shaders_to_share"></span><span id="STORING_VARIABLES_AND_TYPES_FOR_SHADERS_TO_SHARE"></span>[Archiviazione di variabili e tipi per gli shader da condividere](storing-variables-and-types-for-shaders-to-share.md)<br/> | Descrive l'oggetto collegamento di classe per l'archiviazione di variabili e tipi che possono essere condivisi da più shader.<br/> |
| <span id="Interfaces_and_Classes"></span><span id="interfaces_and_classes"></span><span id="INTERFACES_AND_CLASSES"></span>[Interfacce e classi](overviews-direct3d-11-hlsl-dynamic-linking-class.md)<br/>                                                                                                         | Viene descritto l'utilizzo di interfacce e classi HLSL per implementare il collegamento dinamico.<br/>                           |
| <span id="Interface_Usage_Restrictions"></span><span id="interface_usage_restrictions"></span><span id="INTERFACE_USAGE_RESTRICTIONS"></span>[Limitazioni di utilizzo dell'interfaccia](overviews-direct3d-11-hlsl-dynamic-linking-expression.md)<br/>                                                                            | Descrive le restrizioni relative all'uso delle interfacce nel codice dello shader.<br/>                                     |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[HLSL](overviews-direct3d-11-hlsl.md)
</dt> </dl>

 

 





