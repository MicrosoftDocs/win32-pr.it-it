---
description: L'architettura della DLL del parser deve fornire le funzionalità illustrate nella figura seguente.
ms.assetid: 2da5d4bc-a219-47b5-8522-1237f7bcac16
title: Architettura DLL parser
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7852029a892d8b74c954cbc2d7341fcaf29032fb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104485853"
---
# <a name="parser-dll-architecture"></a>Architettura DLL parser

L'architettura della DLL del parser deve fornire le funzionalità illustrate nella figura seguente. Tenere presente che alcune funzionalità richiedono l'implementazione di un solo punto di ingresso. Tuttavia, se la DLL del parser supporta più protocolli, la funzionalità richiede l'implementazione di più punti di ingresso.

![funzionalità dll del parser](images/parserarchitecture1.png)



| Per informazioni su                                                  | Vedere                                                                    |
|------------------------------------------------------------------------|------------------------------------------------------------------------|
| Come implementare le funzioni di esportazione della DLL del parser.                          | [Scrittura di un parser di protocollo](writing-a-protocol-parser.md)             |
| Funzioni e strutture specifiche utilizzate dai parser, ovvero argomenti di riferimento. | [Funzioni e strutture del parser](parser-functions-and-structures.md) |



 

 

 



