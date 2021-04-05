---
title: Matrici fisse
description: Se l'interfaccia specifica una matrice con un numero specifico di elementi come parametro, viene utilizzata una matrice fissa. Quando si usa MIDL, si definiscono matrici fisse nello stesso modo in cui vengono definite in C. Specificare il tipo, il nome e la dimensione della matrice.
ms.assetid: b9a2fa0b-1386-43e1-ab55-0a57cd8d1f18
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2bb3a620e86bff47e04afb5078dff50faee9fef0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103711431"
---
# <a name="fixed-arrays"></a>Matrici fisse

Se l'interfaccia specifica una matrice con un numero specifico di elementi come parametro, viene utilizzata una matrice fissa. Quando si usa MIDL, si definiscono matrici fisse nello stesso modo in cui vengono definite in C. Specificare il tipo, il nome e la dimensione della matrice.

Nell'esempio seguente viene illustrato come definire una matrice fissa.

``` syntax
[
    /*Attributes are defined here. */
]
interface MyInterface
{
    const long ARRAY_SIZE = 1000;

    MyRemoteProc(char achArray[ARRAY_SIZE]);

    /* Other interface procedures are defined here. */
}
```

Quando un programma client passa un array fisso a un programma server, lo stub del client invia l'intera matrice allo stub del server. Lo stub del server alloca memoria per la matrice e archivia i dati della matrice ricevuti attraverso la rete nella memoria allocata. Passa quindi la matrice alla procedura remota sul server. Il server può modificare i dati nella matrice.

Al termine della procedura remota, lo stub del server invia nuovamente il contenuto della matrice al client. Lo stub client copia i dati ricevuti dallo stub del server nella matrice originale. Il programma client può quindi utilizzare i dati come se ricevesse i dati da una chiamata di procedura locale.

 

 




