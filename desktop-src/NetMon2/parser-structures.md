---
description: In questa sezione vengono descritte le strutture che è possibile utilizzare per sviluppare parser. Queste strutture sono utilizzate da funzioni che è possibile utilizzare per sviluppare parser e funzioni che è possibile utilizzare per sviluppare parser o esperti.
ms.assetid: ce45a8ef-4355-46fd-909e-3ab4d63a3bf1
title: Strutture del parser
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59a9b767974214472f24ea9e1ec9359c97d26fc4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968753"
---
# <a name="parser-structures"></a>Strutture del parser

In questa sezione vengono descritte le strutture che è possibile utilizzare per sviluppare parser. Queste strutture sono utilizzate da funzioni che è possibile utilizzare per sviluppare parser e funzioni che è possibile utilizzare per sviluppare parser o esperti.



| Struttura                                 | Descrizione                                                                                                                     |
|-------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| [MACFRAME](macframe.md)                  | Definisce i protocolli iniziali usati più di frequente.                                                                               |
| [ENTRYPOINTS](entrypoints.md)            | Specifica i puntatori ai punti di ingresso per la DLL del parser.                                                                      |
| [PF \_ FOLLOWENTRY](pf-followentry.md)     | Specifica il protocollo che segue il protocollo corrente.                                                                       |
| [PF \_](pf-followset.md)         | Specifica il set di protocolli che segue il protocollo corrente.                                                               |
| [PF \_ HANDOFFENTRY](pf-handoffentry.md)   | Specifica il protocollo che passa al protocollo corrente o al protocollo che il protocollo corrente passa a.    |
| [PF \_ HANDOFFSET](pf-handoffset.md)       | Specifica il set di protocolli che passa al protocollo corrente o il set di protocolli a cui il protocollo corrente passa. |
| [PF \_ PARSERDLLINFO](pf-parserdllinfo.md) | Specifica il numero di parser nella DLL del parser e le informazioni su ogni parser.                                            |
| [PF \_ PARSERINFO](pf-parserinfo.md)       | Specifica le informazioni su un parser specifico.                                                                                  |
| [con etichetta \_ bit](labeled-bit.md)           | Specifica gli handle, i campi di BIT o i flag.                                                                                        |
| [BYTE con etichetta \_](labeled-byte.md)         | Specifica una coppia di etichette di **byte** .                                                                                                |
| [DWORD con etichetta \_](labeled-dword.md)       | Specifica una coppia di etichette **DWORD** .                                                                                               |
| [parola con etichetta \_](labeled-word.md)         | Specifica una coppia di etichette di **Word** .                                                                                                |
| [PROPERTYINFO](propertyinfo.md)          | Specifica le proprietà richieste dal parser di protocollo per descrivere i frame.                                                  |
| [PROPERTYINST](propertyinst.md)          | Specifica un'istanza di una proprietà in un frame.                                                                                 |
| [PROPERTYINSTEX](propertyinstex.md)      | Specifica un'istanza di proprietà estesa in formato libero.                                                                              |
| [PROTOCOLINFO](protocolinfo.md)          | Specifica un protocollo.                                                                                                           |
| [INTERVALLO](range.md)                        | Specifica un intervallo per un numero.                                                                                                 |
| [SET](set.md)                            | Specifica una tabella di valori per una proprietà.                                                                                     |



 

Per informazioni sulle funzioni usate per lo sviluppo di dll del parser, vedere gli argomenti seguenti.



| Per informazioni su                                         | Vedere                                                                          |
|---------------------------------------------------------------|------------------------------------------------------------------------------|
| Funzioni che vengono esportate dalle DLL del parser.                        | [Funzioni di esportazione DLL del parser](parser-dll-export-functions.md)               |
| Funzioni che è possibile usare per sviluppare dll del parser.            | [Funzioni del parser](parser-functions.md)                                     |
| Funzioni che è possibile usare per sviluppare dll di parser ed esperti. | [Funzioni comuni di esperti e parser](expert-and-parser-common-functions.md) |



 

 

 



