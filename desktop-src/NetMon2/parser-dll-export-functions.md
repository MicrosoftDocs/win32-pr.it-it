---
description: Le funzioni, elencate nella tabella seguente, sono punti di ingresso per le dll del parser. Le funzioni sono i punti di ingresso per le chiamate dal sistema operativo e Network Monitor.
ms.assetid: 67811ddb-1961-4306-a62f-b9fd2d2d2b55
title: Funzioni di esportazione DLL del parser
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 929541a1eda60740fe219352fee285a5a34a89df
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104401602"
---
# <a name="parser-dll-export-functions"></a>Funzioni di esportazione DLL del parser

Le funzioni, elencate nella tabella seguente, sono punti di ingresso per le dll del parser. Le funzioni sono i punti di ingresso per le chiamate dal sistema operativo e Network Monitor.



| Funzione                                           | Descrizione                                                                                                                                                    |
|----------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Parser DllMain](dllmain-parser.md)               | Indica alla DLL del parser che è caricata o scaricata. Il sistema operativo chiama la funzione del **parser DllMain** quando un processo carica o Scarica la dll. |
| [AttachProperties](attachproperties.md)           | Notifica al parser di alleghi eventuali proprietà presenti in un frame.                                                                                            |
| [Annullamento registrazione](deregister.md)                       | Notifica al parser di eseguire la pulizia.                                                                                                                               |
| [FormatProperties](formatproperties.md)           | Notifica al parser di prendere tutte le istanze di proprietà in e di compilare il membro **szPropertyText** di ogni struttura **PROPERTYINST** .                       |
| [RecognizeFrame](recognizeframe.md)               | Determina se il parser può interpretare i dati del frame non elaborati con il protocollo specificato.                                                            |
| [Registra parser](register-parser.md)             | Determina le informazioni di base sul parser all'interno della DLL. Network Monitor chiama la funzione **Register parser** .                                          |
| [ParserAutoInstallInfo](parserautoinstallinfo.md) | Installa un parser automaticamente.                                                                                                                               |



 

Network Monitor fornisce le funzioni di supporto e le strutture che possono essere chiamate dal parser.



| Per altre informazioni su                          | Vedere                                                                          |
|-----------------------------------------------------|------------------------------------------------------------------------------|
| Funzioni helper che possono essere chiamate da esperti e analizzatori. | [Funzioni comuni di esperti e parser](expert-and-parser-common-functions.md) |
| Funzioni helper che possono essere chiamate solo dai parser.        | [Funzioni del parser](parser-functions.md)                                     |
| Strutture utilizzate dalle funzioni del parser.               | [Strutture del parser](parser-structures.md)                                   |



 

 

 



