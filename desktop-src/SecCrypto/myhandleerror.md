---
description: La funzione MyHandleError è un esempio di una funzione strumento utilizzata per stampare un messaggio di errore e uscire dal programma chiamante.
ms.assetid: 7b28509f-a77f-4b60-90d4-18edaa6d1a2d
title: MyHandleError
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 047c9642a1b19c2af4a6e5ef2134ca305c472c09
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317712"
---
# <a name="myhandleerror"></a>MyHandleError

La funzione **MyHandleError** è un esempio di una funzione strumento utilizzata per stampare un messaggio di errore e uscire dal programma chiamante. Gli esempi per diverse funzioni CryptoAPI in [riferimento alla crittografia](cryptography-reference.md) e gli esempi più estesi nell' [uso della crittografia](using-cryptography.md) implementano questa funzione. Le applicazioni reali possono richiedere una funzionalità di gestione degli errori più complessa.


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



 

 



