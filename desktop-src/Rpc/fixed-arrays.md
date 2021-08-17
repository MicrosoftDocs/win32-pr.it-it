---
title: Matrici fisse
description: Se l'interfaccia specifica una matrice con un numero specifico di elementi come parametro, viene utilizzata una matrice fissa. Quando si usa MIDL, le matrici fisse vengono definite nello stesso modo in cui vengono definite in C. Specificare il tipo, il nome e le dimensioni della matrice.
ms.assetid: b9a2fa0b-1386-43e1-ab55-0a57cd8d1f18
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1040e417cc896b9f4bd2271dc69e23033332354357b2aad32053724d94b79035
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118929980"
---
# <a name="fixed-arrays"></a>Matrici fisse

Se l'interfaccia specifica una matrice con un numero specifico di elementi come parametro, viene utilizzata una matrice fissa. Quando si usa MIDL, le matrici fisse vengono definite nello stesso modo in cui vengono definite in C. Specificare il tipo, il nome e le dimensioni della matrice.

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

Quando un programma client passa una matrice fissa a un programma server, lo stub client invia l'intera matrice al server stub. Lo stub del server alloca memoria per la matrice e archivia i dati della matrice ricevuti in rete nella memoria allocata. Passa quindi la matrice alla procedura remota nel server. Il server può modificare i dati nella matrice.

Al termine della procedura remota, lo stub del server invia nuovamente il contenuto della matrice al client. Lo stub client copia i dati ricevuti dallo stub del server nella matrice originale. Il programma client può quindi usare i dati come se ricevesse i dati da una chiamata di procedura locale.

 

 




