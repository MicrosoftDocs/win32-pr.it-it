---
description: Questa sezione descrive le strutture che è possibile usare per sviluppare parser. Queste strutture vengono usate dalle funzioni che è possibile usare per sviluppare parser e funzioni che è possibile usare per sviluppare parser o esperti.
ms.assetid: ce45a8ef-4355-46fd-909e-3ab4d63a3bf1
title: Strutture del parser
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c0d54e02e26e9874f27f49312a84b4b643cc4b3bfdb0c6056f274e4febecf0ec
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120082531"
---
# <a name="parser-structures"></a>Strutture del parser

Questa sezione descrive le strutture che è possibile usare per sviluppare parser. Queste strutture vengono usate dalle funzioni che è possibile usare per sviluppare parser e funzioni che è possibile usare per sviluppare parser o esperti.



| Struttura                                 | Descrizione                                                                                                                     |
|-------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| [MACFRAME](macframe.md)                  | Definisce i protocolli iniziali più comunemente usati.                                                                               |
| [PUNTI DI INGRESSO](entrypoints.md)            | Specifica i puntatori ai punti di ingresso per la DLL del parser.                                                                      |
| [PF \_ FOLLOWENTRY](pf-followentry.md)     | Specifica il protocollo che segue il protocollo corrente.                                                                       |
| [PF \_ FOLLOWSET](pf-followset.md)         | Specifica il set di protocolli che segue il protocollo corrente.                                                               |
| [PF \_ HANDOFFENTRY](pf-handoffentry.md)   | Specifica il protocollo che si lasser al protocollo corrente o il protocollo a cui il protocollo corrente si lase.    |
| [PF \_ HANDOFFSET](pf-handoffset.md)       | Specifica il set di protocolli che traslano il protocollo corrente o il set di protocolli a cui il protocollo corrente si consegna. |
| [PF \_ PARSERDLLINFO](pf-parserdllinfo.md) | Specifica il numero di parser nella DLL del parser e le informazioni su ogni parser.                                            |
| [PF \_ PARSERINFO](pf-parserinfo.md)       | Specifica informazioni su un parser specifico.                                                                                  |
| [BIT CON \_ ETICHETTA](labeled-bit.md)           | Specifica handle, campi BIT o flag.                                                                                        |
| [BYTE CON \_ ETICHETTA](labeled-byte.md)         | Specifica una coppia **di etichette BYTE.**                                                                                                |
| [DWORD \_ CON ETICHETTA](labeled-dword.md)       | Specifica una coppia **di etichette DWORD.**                                                                                               |
| [PAROLA CON \_ ETICHETTA](labeled-word.md)         | Specifica una coppia **di etichette WORD.**                                                                                                |
| [Propertyinfo](propertyinfo.md)          | Specifica le proprietà necessarie al parser del protocollo per descrivere i frame.                                                  |
| [PROPERTYINST](propertyinst.md)          | Specifica un'istanza di una proprietà in un frame.                                                                                 |
| [PROPERTYINSTEX](propertyinstex.md)      | Specifica un'istanza di proprietà estesa in formato libero.                                                                              |
| [PROTOCOLINFO](protocolinfo.md)          | Specifica un protocollo.                                                                                                           |
| [Gamma](range.md)                        | Specifica un intervallo per un numero.                                                                                                 |
| [SET](set.md)                            | Specifica una tabella di valori per una proprietà.                                                                                     |



 

Per informazioni sulle funzioni usate per sviluppare DLL del parser, vedere gli argomenti seguenti.



| Per informazioni su                                         | Vedere                                                                          |
|---------------------------------------------------------------|------------------------------------------------------------------------------|
| Funzioni esportate nelle DLL del parser.                        | [Funzioni di esportazione dll del parser](parser-dll-export-functions.md)               |
| Funzioni che è possibile usare per sviluppare DLL del parser.            | [Funzioni del parser](parser-functions.md)                                     |
| Funzioni che è possibile usare per sviluppare DLL di parser ed esperti. | [Funzioni comuni di Expert e Parser](expert-and-parser-common-functions.md) |



 

 

 



