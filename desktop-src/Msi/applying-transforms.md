---
description: La proprietà TRANSFORMS contiene l'elenco delle trasformazioni per un pacchetto di installazione. Il programma di installazione applica tutte le trasformazioni nell'elenco delle trasformazioni a ogni installazione, annuncio, installazione su richiesta o installazione di manutenzione del pacchetto.
ms.assetid: dde2ef55-7794-4eb1-984a-ed13e990c97f
title: Applicazione di trasformazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: daf6c1bd60a084b745df14d89772008867b618f3b21116ca20c5313747950b5c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119264251"
---
# <a name="applying-transforms"></a>Applicazione di trasformazioni

La [**proprietà TRANSFORMS**](transforms.md) contiene l'elenco delle trasformazioni per un pacchetto di installazione. Il programma di installazione applica tutte le trasformazioni nell'elenco delle trasformazioni a ogni installazione, annuncio, installazione su richiesta o installazione di manutenzione del pacchetto.

La [**proprietà TRANSFORMS**](transforms.md) viene impostata specificando l'elenco di trasformazioni nella riga di comando. Tuttavia, quando si usa l'opzione della riga di comando /jm o [/ju](command-line-options.md), l'elenco delle trasformazioni deve essere specificato usando l'opzione /t .

Si noti che l'elenco delle trasformazioni non può essere modificato dopo l'installazione e può essere rimosso solo disinstallando l'applicazione.

> [!Note]  
> Un Windows installer può applicare non più di 255 trasformazioni durante l'installazione di un'applicazione o di un aggiornamento. Quando sono necessarie molte trasformazioni, devono essere combinate e le trasformazioni obsolete precedenti devono essere eliminate.

 

Nella tabella seguente vengono forniti esempi di varie stringhe di trasformazioni che possono essere aggiunte all'elenco delle trasformazioni.



| Trasforma una stringa                                                                                                              | Descrizione                                                                                                                                                                                                                                                                                                                                                                             |
|--------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| transform1.mst;:transform2.mst;:transform3.mst                                                                                 | Transform2.mst e transform3.mst sono [trasformazioni incorporate](embedded-transforms.md). transform1.mst è [](secure-at-source-transforms.md) una trasformazione sicura all'origine solo se è impostata la proprietà [**TRANSFORMSSECURE**](transformssecure.md) o il criterio [TransformsSecure.](transformssecure-policy.md) In caso contrario, transform1 è una trasformazione [non protetta.](unsecured-transforms.md) |
| \\\\percorso \\ condivisione \\ server \\ transform1.mst;:transform2.mst                                                                        | Transform2.mst è una [trasformazione incorporata.](embedded-transforms.md) transform1.mst è una trasformazione [secure-full-path](secure-full-path-transforms.md) solo se è impostata la proprietà [**TRANSFORMSSECURE**](transformssecure.md) o il criterio [TransformsSecure.](transformssecure-policy.md) In caso contrario, transform1 è una trasformazione [non protetta.](unsecured-transforms.md)                   |
| @:transform2.mst;transform1.mst @transform1.mst ;:transform2.mst<br/>                                                     | Transform2.mst è una trasformazione incorporata. transform1.mst è una trasformazione autonoma [sicura all'origine.](secure-at-source-transforms.md)                                                                                                                                                                                                                                                |
| \|\\\\percorso \\ condivisione \\ server \\ transform1.mst;:transform2.mst \| :transform2.mst; \\ \\ percorso \\ condivisione \\ server \\ transform1.mst<br/> | Transform2.mst è una trasformazione incorporata. transform1.mst è un'istanza autonoma [di trasformazioni secure-full-path.](secure-full-path-transforms.md)                                                                                                                                                                                                                                                 |



 

 

 




