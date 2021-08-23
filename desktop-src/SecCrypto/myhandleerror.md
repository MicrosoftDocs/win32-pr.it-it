---
description: La funzione MyHandleError è un esempio di funzione dello strumento usata per stampare un messaggio di errore e uscire dal programma chiamante.
ms.assetid: 7b28509f-a77f-4b60-90d4-18edaa6d1a2d
title: MyHandleError
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47a3c3ad412b6719b59402e820411377c08d2c6b9a17f44771a7156e0b52567a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119739661"
---
# <a name="myhandleerror"></a>MyHandleError

La **funzione MyHandleError** è un esempio di funzione dello strumento usata per stampare un messaggio di errore e uscire dal programma chiamante. Gli esempi per diverse funzioni CryptoAPI in [Riferimento alla](cryptography-reference.md) crittografia e gli esempi più estesi in [Uso della](using-cryptography.md) crittografia implementano questa funzione. Le applicazioni reali possono richiedere funzionalità di gestione degli errori più complesse.


```C++
#include <stdio.h>
#include <tchar.h>
#include <windows.h>

void MyHandleError(LPTSTR psz)
{
    _ftprintf(stderr, TEXT("An error occurred in the program. \n"));
    _ftprintf(stderr, TEXT("%s\n"), psz);
    _ftprintf(stderr, TEXT("Error number %x.\n"), GetLastError());
    _ftprintf(stderr, TEXT("Program terminating. \n"));
    exit(1);
} // End of MyHandleError

```



 

 



