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
# <a name="myhandleerror"></a><span data-ttu-id="b8bb5-103">MyHandleError</span><span class="sxs-lookup"><span data-stu-id="b8bb5-103">MyHandleError</span></span>

<span data-ttu-id="b8bb5-104">La funzione **MyHandleError** è un esempio di una funzione strumento utilizzata per stampare un messaggio di errore e uscire dal programma chiamante.</span><span class="sxs-lookup"><span data-stu-id="b8bb5-104">The **MyHandleError** function is an example of a tool function used to print an error message and exit the calling program.</span></span> <span data-ttu-id="b8bb5-105">Gli esempi per diverse funzioni CryptoAPI in [riferimento alla crittografia](cryptography-reference.md) e gli esempi più estesi nell' [uso della crittografia](using-cryptography.md) implementano questa funzione.</span><span class="sxs-lookup"><span data-stu-id="b8bb5-105">The examples for several CryptoAPI functions in [Cryptography Reference](cryptography-reference.md) and the more extended examples in [Using Cryptography](using-cryptography.md) implement this function.</span></span> <span data-ttu-id="b8bb5-106">Le applicazioni reali possono richiedere una funzionalità di gestione degli errori più complessa.</span><span class="sxs-lookup"><span data-stu-id="b8bb5-106">Real applications may require more complex error handling capability.</span></span>


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



 

 



