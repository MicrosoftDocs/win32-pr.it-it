---
description: L'architettura della DLL del parser deve fornire le funzionalità illustrate nella figura seguente.
ms.assetid: 2da5d4bc-a219-47b5-8522-1237f7bcac16
title: Architettura della DLL del parser
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb8b2c3ead77d5172bc57fa3bc1c8b6001b9c690cd254dc436ac93f504ddb732
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119962866"
---
# <a name="parser-dll-architecture"></a>Architettura della DLL del parser

L'architettura della DLL del parser deve fornire le funzionalità illustrate nella figura seguente. Tenere presente che alcune funzionalità richiedono l'implementazione di un solo punto di ingresso. Tuttavia, se la DLL del parser supporta più protocolli, la funzionalità richiede l'implementazione di più punti di ingresso.

![funzionalità dll del parser](images/parserarchitecture1.png)



| Per informazioni su                                                  | Vedere                                                                    |
|------------------------------------------------------------------------|------------------------------------------------------------------------|
| Come implementare le funzioni di esportazione dll del parser.                          | [Scrittura di un parser di protocollo](writing-a-protocol-parser.md)             |
| Funzioni e strutture specifiche usate dal parser, ovvero argomenti di riferimento. | [Funzioni e strutture del parser](parser-functions-and-structures.md) |



 

 

 



