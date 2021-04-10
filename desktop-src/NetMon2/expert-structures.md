---
description: Le funzioni di supporto di esperti fornite da Network Monitor e funzioni helper comuni utilizzano le strutture descritte nella tabella seguente.
ms.assetid: 3c49dd0a-836f-43f1-b383-357e8ba6545f
title: Strutture di esperti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34b9da00a71c3cdb9defe4396f4339f750cca359
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966481"
---
# <a name="expert-structures"></a>Strutture di esperti

Le funzioni di supporto di esperti fornite da Network Monitor e funzioni helper comuni utilizzano le strutture descritte nella tabella seguente.



| Struttura                                              | Descrizione                                                                                            |
|--------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [**CONFIGUREDEXPERT**](configuredexpert.md)           | Associa una DLL di esperti alla relativa configurazione.                                                       |
| [**EXPERTCONFIG**](expertconfig.md)                   | Fornisce dati di configurazione non elaborati.                                                                       |
| [**EXPERTENUMINFO**](expertenuminfo.md)               | Fornisce informazioni sulla DLL degli esperti. Network Monitor utilizza le informazioni.                       |
| [**EXPERTFRAMEDESCRIPTOR**](expertframedescriptor.md) | Fornisce informazioni su un frame.                                                                    |
| [**EXPERTSTARTUPINFO**](expertstartupinfo.md)         | Fornisce informazioni di avvio sull'esperto.                                                         |
| [**EXPERTSTATUS**](expertstatus.md)                   | Fornisce lo stato corrente di un esperto in esecuzione.                                                       |
| [**FILTEROBJECT**](filterobject.md)                   | Definisce le caratteristiche del filtro di visualizzazione per un esperto.                                              |
| [**NMEVENTDATA**](nmeventdata.md)                     | Fornisce informazioni su una riga visualizzata nel Visualizzatore esperti.                                      |
| [**NMCOLUMNINFO**](nmcolumninfo.md)                   | Fornisce informazioni che definiscono una colonna nell'Visualizzatore eventi.                                        |
| [**NMCOLUMNVARIANT**](nmcolumnvariant.md)             | Fornisce un contenitore per tutti i dati possibili inseriti in una colonna in una riga del Visualizzatore eventi.     |
| [**NMCOLUMNTYPE**](nmcolumntype.md)                   | Il punto di ingresso nella variante che indica l'elemento dell'Unione da usare e come formattarlo. |



 

Network Monitor fornisce anche funzioni di esportazione (funzioni helper che l'esperto può chiamare) ed enumerazioni.



| Per informazioni su                                          | Vedere                                                                          |
|----------------------------------------------------------------|------------------------------------------------------------------------------|
| Funzioni di esportazione che forniscono punti di ingresso alla DLL di esperti. | [Funzioni di esportazione DLL di esperti](expert-dll-export-functions.md)               |
| Funzioni helper che possono essere chiamate da esperti e parser.    | [Funzioni comuni di esperti e parser](expert-and-parser-common-functions.md) |
| Funzioni di supporto chiamate solo da esperti.              | [Funzioni di esperti](expert-functions.md)                                     |
| Enumerazioni utilizzate da funzioni e strutture di esperti.          | [Enumerazioni di esperti](expert-enumerations.md)                               |



 

 

 



