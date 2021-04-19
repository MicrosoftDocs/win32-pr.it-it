---
description: In questa sezione vengono descritte le strutture di riconoscimento.
ms.assetid: 4c17391f-7af4-42ab-b77f-e3c39cadc0b6
title: Strutture di riconoscimento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: addaccf3e69f35b99379710d681fe8ac45559ea1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317911"
---
# <a name="recognizer-structures"></a>Strutture di riconoscimento

In questa sezione vengono descritte le strutture di riconoscimento.

## <a name="in-this-section"></a>Contenuto della sezione



| Struttura                                                    | Descrizione                                                                                                                                                   |
|--------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**intervallo di caratteri \_**](/windows/win32/api/rectypes/ns-rectypes-character_range)                  | Specifica un intervallo di punti Unicode (caratteri).<br/>                                                                                                  |
| [**metriche del reticolo \_**](/windows/win32/api/rectypes/ns-rectypes-lattice_metrics)                  | Descrive la linea di base e l'altezza del midline.<br/>                                                                                                     |
| [**segmento di linea \_**](/windows/win32/api/rectypes/ns-rectypes-line_segment)                        | Descrive i punti di inizio e di fine di un segmento di riconoscimento della riga, ad esempio Baseline o midline.<br/>                                                 |
| [**\_Descrizione pacchetto**](/windows/desktop/api/tpcshrd/ns-tpcshrd-packet_description)            | Descrive il contenuto del pacchetto per un particolare contesto di Tablet.<br/>                                                                               |
| [**\_Proprietà pacchetto**](/windows/desktop/api/tpcshrd/ns-tpcshrd-packet_property)                  | Descrive una proprietà del pacchetto segnalata dal driver del tablet.<br/>                                                                                 |
| [**metriche delle proprietà \_**](/windows/desktop/api/tpcshrd/ns-tpcshrd-property_metrics)                | Definisce l'intervallo e la risoluzione di una proprietà del pacchetto.<br/>                                                                                             |
| [**\_attrs unto**](/windows/win32/api/rectypes/ns-rectypes-reco_attrs)                            | Recupera gli attributi di un riconoscimento o specifica gli attributi da utilizzare per la ricerca di un riconoscimento installato.<br/>                         |
| [**Guida a unto \_**](/windows/win32/api/rectypes/ns-rectypes-reco_guide)                            | Definisce i limiti dell'input penna per il riconoscimento.<br/>                                                                                               |
| [**\_reticolo unto**](/windows/win32/api/rectypes/ns-rectypes-reco_lattice)                        | Funge da punto di ingresso in un reticolo.<br/>                                                                                                          |
| [**\_colonna reticolo \_ unto**](/windows/win32/api/rectypes/ns-rectypes-reco_lattice_column)         | Rappresenta una colonna nel reticolo.<br/>                                                                                                                |
| [**\_elemento del reticolo unto \_**](/windows/win32/api/rectypes/ns-rectypes-reco_lattice_element)       | Corrisponde a una parola o a un carattere asiatico orientale, in genere; Tuttavia, un elemento può corrispondere anche a un movimento, una forma o un altro codice.<br/> |
| [**\_proprietà del reticolo unto \_**](/windows/win32/api/rectypes/ns-rectypes-reco_lattice_properties) | Contiene una matrice di puntatori alle strutture di proprietà.<br/>                                                                                              |
| [**\_Proprietà reticolo \_ unto**](/windows/win32/api/rectypes/ns-rectypes-reco_lattice_property)     | Contiene una proprietà utilizzata nel reticolo.<br/>                                                                                                           |
| [**\_intervallo unto**](/windows/win32/api/rectypes/ns-rectypes-reco_range)                            | Identifica un intervallo di caratteri nella stringa di risultato.<br/>                                                                                             |
| [**\_intervallo tratto**](/windows/win32/api/tpcshrd/ns-tpcshrd-stroke_range)                        | Specifica un intervallo di tratti nell'oggetto [**InkDisp**](inkdisp-class.md) .<br/>                                                                       |



 

 

 




