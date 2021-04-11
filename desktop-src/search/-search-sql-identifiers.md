---
description: Gli identificatori specificano i nomi delle colonne (talvolta denominate proprietà), i cataloghi e gli alias.
ms.assetid: 799afe2c-9217-4006-a4a3-644e5393993c
title: Identificatori
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df79bd0d70564ea3e87ff4821a1cb59e3d0a5eb3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128539"
---
# <a name="identifiers"></a>Identificatori

Gli identificatori specificano i nomi delle colonne (talvolta denominate proprietà), i cataloghi e gli alias. Ad esempio, System. ItemName e System. DateCreated sono gli identificatori di due colonne di proprietà definite dal sistema. I valori letterali, al contrario, specificano valori stringa e numerici.


È possibile creare identificatori costituiti da un massimo di 128 caratteri e in uno dei due tipi distinti in base ai caratteri utilizzati nel nome dell'identificatore:

-   Gli **identificatori regolari** contengono solo i caratteri a-z, a-z, 0-9, il carattere di sottolineatura ( \_ ) e il punto (.) e iniziano con una lettera. Non è necessario racchiudere gli identificatori regolari racchiusi tra virgolette doppie ("").
-   Gli **identificatori delimitati** possono contenere qualsiasi carattere Unicode valido e devono essere racchiusi tra virgolette doppie.

> [!Note]  
> Nelle clausole FREETEXT e CONTAINs è possibile utilizzare l'asterisco ( \* ) come identificatore di colonna speciale quando si desidera specificare che Windows Search includa tutte le proprietà indicizzate nella query. Sebbene non sia un identificatore regolare, non richiede virgolette doppie.

 

 

 



