---
description: Le funzioni elencate nella tabella seguente sono punti di ingresso per le DLL del parser. Le funzioni sono i punti di ingresso per le chiamate dal sistema operativo e Network Monitor.
ms.assetid: 67811ddb-1961-4306-a62f-b9fd2d2d2b55
title: Funzioni di esportazione dll del parser
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 94c04eb57cf5d5f76b60bca43fc5ed47ae641182efc74b21c8b41fa5d909af6b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120037031"
---
# <a name="parser-dll-export-functions"></a>Funzioni di esportazione dll del parser

Le funzioni elencate nella tabella seguente sono punti di ingresso per le DLL del parser. Le funzioni sono i punti di ingresso per le chiamate dal sistema operativo e Network Monitor.



| Funzione                                           | Descrizione                                                                                                                                                    |
|----------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [DllMain Parser](dllmain-parser.md)               | Indica alla DLL del parser che viene caricata o scaricata. Il sistema operativo chiama la **funzione DllMain Parser** quando un processo carica o scarica la DLL. |
| [AttachProperties](attachproperties.md)           | Notifica al parser di associare le proprietà presenti in un frame.                                                                                            |
| [Annullamento registrazione](deregister.md)                       | Notifica al parser di eseguire la pulizia.                                                                                                                               |
| [Proprietà FormatProperties](formatproperties.md)           | Notifica al parser di prendere tutte le istanze della proprietà in e di compilare il membro **szPropertyText** di ogni **struttura PROPERTYINST.**                       |
| [RecognizeFrame](recognizeframe.md)               | Determina se il parser può interpretare i dati del frame non elaborato con il protocollo specificato.                                                            |
| [Registrare il parser](register-parser.md)             | Determina le informazioni di base sul parser all'interno della DLL. Network Monitor chiama la **funzione Register Parser.**                                          |
| [ParserAutoInstallInfo](parserautoinstallinfo.md) | Installa automaticamente un parser.                                                                                                                               |



 

Network Monitor fornisce strutture e funzioni helper che il parser può chiamare.



| Per altre informazioni su                          | Vedere                                                                          |
|-----------------------------------------------------|------------------------------------------------------------------------------|
| Funzioni helper che possono essere chiamate da esperti e parser. | [Funzioni comuni di Esperti e Parser](expert-and-parser-common-functions.md) |
| Funzioni helper che solo i parser possono chiamare.        | [Funzioni del parser](parser-functions.md)                                     |
| Strutture usate da funzioni del parser.               | [Strutture del parser](parser-structures.md)                                   |



 

 

 



