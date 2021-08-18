---
description: Le funzioni helper esperte Network Monitor e funzioni helper comuni usano le strutture descritte nella tabella seguente.
ms.assetid: 3c49dd0a-836f-43f1-b383-357e8ba6545f
title: Strutture esperte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16accf769b0983b782a6e6dbd723dd08df27415220bda1d59122b951439bac65
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118939018"
---
# <a name="expert-structures"></a>Strutture esperte

Le funzioni helper esperte Network Monitor e funzioni helper comuni usano le strutture descritte nella tabella seguente.



| Struttura                                              | Descrizione                                                                                            |
|--------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [**CONFIGUREDEXPERT**](configuredexpert.md)           | Associa una DLL esperta alla relativa configurazione.                                                       |
| [**EXPERTCONFIG**](expertconfig.md)                   | Fornisce dati di configurazione non elaborati.                                                                       |
| [**EXPERTENUMINFO**](expertenuminfo.md)               | Fornisce informazioni sulla DLL esperta. Network Monitor usa le informazioni.                       |
| [**EXPERTFRAMEDESCRIPTOR**](expertframedescriptor.md) | Fornisce informazioni su un frame.                                                                    |
| [**EXPERTSTARTUPINFO**](expertstartupinfo.md)         | Fornisce informazioni di avvio sull'esperto.                                                         |
| [**EXPERTSTATUS**](expertstatus.md)                   | Fornisce lo stato corrente di un esperto in esecuzione.                                                       |
| [**FILTEROBJECT**](filterobject.md)                   | Definisce le caratteristiche del filtro di visualizzazione per un esperto.                                              |
| [**NMEVENTDATA**](nmeventdata.md)                     | Fornisce informazioni su una riga visualizzata nel visualizzatore esperti.                                      |
| [**NMCOLUMNINFO**](nmcolumninfo.md)                   | Fornisce informazioni che definiscono una colonna nel Visualizzatore eventi.                                        |
| [**NMCOLUMNVARIANT**](nmcolumnvariant.md)             | Fornisce un contenitore per tutti i dati possibili inseriti in una colonna in una riga nel Visualizzatore eventi.     |
| [**NMCOLUMNTYPE**](nmcolumntype.md)                   | Punto di ingresso nella variante che indica quale elemento dell'unione usare e come formattarlo. |



 

Network Monitor fornisce anche funzioni di esportazione (funzioni helper che l'esperto può chiamare) ed enumerazioni.



| Per informazioni su                                          | Vedere                                                                          |
|----------------------------------------------------------------|------------------------------------------------------------------------------|
| Esportare funzioni che forniscono punti di ingresso alla DLL esperta. | [Funzioni di esportazione di DLL expert](expert-dll-export-functions.md)               |
| Funzioni helper che possono essere chiamate da esperti e parser.    | [Funzioni comuni di esperti e parser](expert-and-parser-common-functions.md) |
| Funzioni helper chiamate solo da esperti.              | [Funzioni esperte](expert-functions.md)                                     |
| Enumerazioni utilizzate da strutture e funzioni esperte.          | [Enumerazioni di esperti](expert-enumerations.md)                               |



 

 

 



