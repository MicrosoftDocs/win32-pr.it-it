---
title: Attributi delle risorse comuni
description: Le istruzioni per la definizione delle risorse supportate in Windows a 16 bit includono un'opzione Load-MEM che specifica le caratteristiche di caricamento e memoria della risorsa.
ms.assetid: 53740997-854b-447c-9ab1-de8e17c0de1e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa15ae7207c80737e284151f0dfd3d7981935943
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298459"
---
# <a name="common-resource-attributes"></a>Attributi delle risorse comuni

Le istruzioni per la definizione delle risorse supportate in Windows a 16 bit includono un'opzione *Load-MEM* che specifica le caratteristiche di caricamento e memoria della risorsa. Questi attributi sono consentiti negli script di risorse per la compatibilità con le versioni precedenti, ma vengono ignorati. Le risorse di Windows vengono caricate quando viene caricato il modulo corrispondente e vengono liberate quando il modulo viene scaricato.

## <a name="load-attributes"></a>Carica attributi

Gli attributi Load specificano quando deve essere caricata la risorsa. Il parametro Load deve essere uno degli attributi seguenti.



| Attributo      | Descrizione                                                                  |
|----------------|------------------------------------------------------------------------------|
| **PRECARICARE**    | Ignorato. In Windows a 16 bit la risorsa viene caricata con il file eseguibile. |
| **LOADONCALL** | Ignorato. Nelle finestre a 16 bit la risorsa viene caricata quando viene chiamata.              |



 

## <a name="memory-attributes"></a>Attributi di memoria

Gli attributi di memoria specificano se la risorsa è fissa o spostata, se è annullabile e se è pura. Il parametro Memory può essere costituito da uno o più degli attributi seguenti.



| Attributo       | Descrizione                                                                                                                               |
|-----------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| **FIXED**       | Ignorato. Nelle finestre a 16 bit la risorsa rimane in una posizione di memoria fissa.                                                              |
| **SPOSTABILE**    | Ignorato. Nelle finestre a 16 bit è possibile spostare la risorsa se necessario per compattare la memoria.                                                     |
| **ANNULLABILE** | Ignorato. Nelle finestre a 16 bit la risorsa può essere eliminata se non è più necessaria.                                                            |
| **PURO**        | Ignorato. Accettato per la compatibilità con gli script di risorse esistenti.                                                                       |
| **IMPURO**      | Ignorato. Accettato per la compatibilità con gli script di risorse esistenti.                                                                       |
| **CONDIVISO**      | Ignorato. In Windows a 16 bit, SHARED viene ignorato per i moduli normali. Per una risorsa da un modulo Windows ROM, la memoria è condivisa.        |
| **NONSHARED**   | Ignorato. In Windows a 16 bit, non condiviso viene ignorato per i moduli normali. Per una risorsa da un modulo Windows ROM, la memoria non è condivisa. |



 

 

 




