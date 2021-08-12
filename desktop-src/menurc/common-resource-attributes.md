---
title: Attributi comuni delle risorse
description: Le istruzioni di definizione delle risorse supportate nelle Windows a 16 bit includono un'opzione load-mem che specifica le caratteristiche di caricamento e memoria della risorsa.
ms.assetid: 53740997-854b-447c-9ab1-de8e17c0de1e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8b7bf01f95c700f12d130490673ef4f0df61cb84ae8077ca759655a2c4a1577
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118235578"
---
# <a name="common-resource-attributes"></a>Attributi comuni delle risorse

Le istruzioni di definizione delle risorse supportate nelle Windows a 16 bit includono un'opzione *load-mem* che specifica le caratteristiche di caricamento e memoria della risorsa. Questi attributi sono consentiti negli script delle risorse per compatibilità con le versioni precedenti, ma vengono ignorati. Windows le risorse vengono caricate quando viene caricato il modulo corrispondente e vengono liberate quando il modulo viene scaricato.

## <a name="load-attributes"></a>Caricare attributi

Gli attributi di caricamento specificano quando la risorsa deve essere caricata. Il parametro load deve essere uno degli attributi seguenti.



| Attributo      | Descrizione                                                                  |
|----------------|------------------------------------------------------------------------------|
| **Precarico**    | Ignorato. Nella versione a 16 bit Windows, la risorsa viene caricata con il file eseguibile. |
| **LOADONCALL** | Ignorato. In caso di Windows a 16 bit, la risorsa viene caricata quando viene chiamata.              |



 

## <a name="memory-attributes"></a>Attributi di memoria

Gli attributi di memoria specificano se la risorsa è fissa o mobile, se è eliminabile e se è pura. Il parametro memory può essere uno o più degli attributi seguenti.



| Attributo       | Descrizione                                                                                                                               |
|-----------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| **FIXED**       | Ignorato. Nelle risorse a 16 bit Windows, la risorsa rimane in una posizione di memoria fissa.                                                              |
| **Mobile**    | Ignorato. In un Windows a 16 bit, la risorsa può essere spostata se necessario per compattare la memoria.                                                     |
| **Scaricabile** | Ignorato. In un Windows a 16 bit, la risorsa può essere rimossa se non è più necessaria.                                                            |
| **Puro**        | Ignorato. Accettato per la compatibilità con gli script di risorse esistenti.                                                                       |
| **Impuro**      | Ignorato. Accettato per la compatibilità con gli script di risorse esistenti.                                                                       |
| **condiviso**      | Ignorato. Nelle applicazioni a 16 bit Windows SHARED viene ignorato per i moduli normali. Per una risorsa da un modulo di Windows ROM, la memoria è condivisa.        |
| **NON CONDIVISO**   | Ignorato. Nelle applicazioni a 16 bit Windows, NONSHARED viene ignorato per i moduli normali. Per una risorsa da un modulo Windows ROM, la memoria non è condivisa. |



 

 

 




