---
title: Stringhe di ricerca iniziali, mediali e finali
description: Sono disponibili tre tipi di ricerche con caratteri jolly a cui viene fatto riferimento in tutta la documentazione relativa alle query sulle stringhe di ricerca per la costruzione. Queste ricerche con caratteri jolly sono stringhe iniziali, mediali e di ricerca finale. In questo argomento vengono descritte queste ricerche.
ms.assetid: 23cc4771-2dd6-478c-9c7a-43052594cb71
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76f502753a87afc81856524c7ae5565db3af678d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106297719"
---
# <a name="initial-medial-and-final-search-strings"></a>Stringhe di ricerca iniziali, mediali e finali

Sono disponibili tre tipi di ricerche con caratteri jolly a cui viene fatto riferimento in tutta la documentazione relativa alle query sulle stringhe di ricerca per la costruzione. Queste ricerche con caratteri jolly sono: stringhe iniziali, mediali e di ricerca finale. In questo argomento vengono descritte queste ricerche.

## <a name="initial-search-strings"></a>Stringhe di ricerca iniziali

Le stringhe di ricerca iniziali corrispondono a un set di caratteri specificato all'inizio di una stringa, seguito da un carattere jolly. Ad esempio, la stringa di ricerca iniziale `Act*` corrisponderà a "Active Directory".

## <a name="medial-search-strings"></a>Stringhe di Medial-Search

Le stringhe di ricerca mediale corrispondono a un determinato set di caratteri all'interno di una stringa, preceduto da e/o seguito da un carattere jolly. Le stringhe di ricerca mediale `*Dir*` , `*ive*Dir*` e `*ve*Dir*tor*` corrisponderanno a "Active Directory".

## <a name="final-search-strings"></a>Ultime-stringhe di ricerca

Le stringhe di ricerca finale corrispondono a un set di caratteri specificato alla fine di una stringa, preceduta da un carattere jolly. Ad esempio, la stringa di ricerca finale `*ory` corrisponderà a "Active Directory".

 

 




