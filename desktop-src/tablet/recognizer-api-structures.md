---
description: Questa sezione descrive le strutture del riconoscitore.
ms.assetid: 4c17391f-7af4-42ab-b77f-e3c39cadc0b6
title: Strutture di riconoscimento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37b04dbee480993a50c3ed3b8847e6595df76347f36a179d1205d8b49807c955
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119596591"
---
# <a name="recognizer-structures"></a>Strutture di riconoscimento

Questa sezione descrive le strutture del riconoscitore.

## <a name="in-this-section"></a>Contenuto della sezione



| Struttura                                                    | Descrizione                                                                                                                                                   |
|--------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**INTERVALLO \_ DI CARATTERI**](/windows/win32/api/rectypes/ns-rectypes-character_range)                  | Specifica un intervallo di punti Unicode (caratteri).<br/>                                                                                                  |
| [**METRICHE \_ LATTICE**](/windows/win32/api/rectypes/ns-rectypes-lattice_metrics)                  | Descrive la linea di base e l'altezza della linea media.<br/>                                                                                                     |
| [**SEGMENTO \_ DI LINEA**](/windows/win32/api/rectypes/ns-rectypes-line_segment)                        | Descrive i punti iniziale e finale di un segmento di riconoscimento linea, ad esempio la linea di base o la linea mediana.<br/>                                                 |
| [**DESCRIZIONE \_ DEL PACCHETTO**](/windows/desktop/api/tpcshrd/ns-tpcshrd-packet_description)            | Descrive il contenuto del pacchetto per un particolare contesto di tablet.<br/>                                                                               |
| [**PROPRIETÀ \_ PACKET**](/windows/desktop/api/tpcshrd/ns-tpcshrd-packet_property)                  | Descrive una proprietà del pacchetto segnalata dal driver tablet.<br/>                                                                                 |
| [**METRICHE DELLE \_ PROPRIETÀ**](/windows/desktop/api/tpcshrd/ns-tpcshrd-property_metrics)                | Definisce l'intervallo e la risoluzione di una proprietà del pacchetto.<br/>                                                                                             |
| [**RECO \_ ATTRS**](/windows/win32/api/rectypes/ns-rectypes-reco_attrs)                            | Recupera gli attributi di un riconoscitore o specifica quali attributi usare quando si cerca un sistema di riconoscimento installato.<br/>                         |
| [**RECO GUIDE (GUIDA AL \_ RECUPERO)**](/windows/win32/api/rectypes/ns-rectypes-reco_guide)                            | Definisce i limiti dell'input penna per il riconoscimento.<br/>                                                                                               |
| [**RECO \_ LATTICE**](/windows/win32/api/rectypes/ns-rectypes-reco_lattice)                        | Funge da punto di ingresso in un reticolo.<br/>                                                                                                          |
| [**RECO \_ LATTICE \_ COLUMN**](/windows/win32/api/rectypes/ns-rectypes-reco_lattice_column)         | Rappresenta una colonna nel reticolo.<br/>                                                                                                                |
| [**ELEMENTO \_ RECO \_ LATTICE**](/windows/win32/api/rectypes/ns-rectypes-reco_lattice_element)       | Corrisponde a una parola o a un carattere dell'Asia orientale, in genere; Tuttavia, un elemento può anche corrispondere a un movimento, a una forma o a un altro codice.<br/> |
| [**PROPRIETÀ \_ RECO \_ LATTICE**](/windows/win32/api/rectypes/ns-rectypes-reco_lattice_properties) | Contiene una matrice di puntatori alle strutture di proprietà.<br/>                                                                                              |
| [**RECO \_ \_ LATTICE - PROPRIETÀ**](/windows/win32/api/rectypes/ns-rectypes-reco_lattice_property)     | Contiene una proprietà utilizzata nel reticolo.<br/>                                                                                                           |
| [**RECO \_ RANGE**](/windows/win32/api/rectypes/ns-rectypes-reco_range)                            | Identifica un intervallo di caratteri nella stringa di risultato.<br/>                                                                                             |
| [**INTERVALLO \_ TRATTO**](/windows/win32/api/tpcshrd/ns-tpcshrd-stroke_range)                        | Specifica un intervallo di tratti [**nell'oggetto InkDisp.**](inkdisp-class.md)<br/>                                                                       |



 

 

 




