---
title: Stringhe di ricerca iniziali, mediali e finali
description: Esistono tre tipi di ricerche con caratteri jolly a cui viene fatto riferimento nella documentazione relativa alla costruzione di query di stringa di ricerca. Queste ricerche con caratteri jolly sono stringhe iniziali, mediali e finali. In questo argomento vengono descritte queste ricerche.
ms.assetid: 23cc4771-2dd6-478c-9c7a-43052594cb71
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39547116846cad4d75a1fd9ae1998e602a8084912965a3dd269803c86845cefc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119024969"
---
# <a name="initial-medial-and-final-search-strings"></a>Stringhe di ricerca iniziali, mediali e finali

Esistono tre tipi di ricerche con caratteri jolly a cui viene fatto riferimento nella documentazione relativa alla costruzione di query di stringa di ricerca. Queste ricerche con caratteri jolly sono: stringhe iniziali, mediali e finali. In questo argomento vengono descritte queste ricerche.

## <a name="initial-search-strings"></a>Stringhe di ricerca iniziali

Le stringhe di ricerca iniziale corrispondono a un determinato set di caratteri all'inizio di una stringa, seguita da un carattere jolly. Ad esempio, la stringa di ricerca iniziale `Act*` corrisponderebbe a "Active Directory".

## <a name="medial-search-strings"></a>Medial-Search stringhe

Le stringhe di ricerca mediale corrispondono a un determinato set di caratteri al centro di una stringa, preceduti da e/o seguiti da un carattere jolly. Le stringhe mediali di ricerca `*Dir*` `*ive*Dir*` , e `*ve*Dir*tor*` corrisponderebbero tutte a "Active Directory".

## <a name="final-search-strings"></a>Stringhe di ricerca finale

Le stringhe di ricerca finale corrispondono a un determinato set di caratteri alla fine di una stringa, precedute da un carattere jolly. Ad esempio, la stringa di ricerca finale `*ory` corrisponderebbe a "Active Directory".

 

 




