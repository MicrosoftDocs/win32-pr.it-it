---
description: 'Per tutti gli esempi della documentazione di Cryptography SDK si presuppone che siano \# incluse le direttive del compilatore seguenti: e \# define.'
ms.assetid: 98f85e7d-e557-4dde-b510-891b37daec87
title: '#include e #defines'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9834fd8103b9fd28a01e416bd1df8b03fb7ad680
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "106320627"
---
# <a name="includes-and-defines"></a><span data-ttu-id="c7d71-103">\#include e \# definisce</span><span class="sxs-lookup"><span data-stu-id="c7d71-103">\#includes and \#defines</span></span>

<span data-ttu-id="c7d71-104">Per tutti gli esempi della documentazione di Cryptography SDK si presuppone che siano incluse le direttive del compilatore seguenti **\# :** e **\# define** .</span><span class="sxs-lookup"><span data-stu-id="c7d71-104">All of the examples in the Cryptography SDK documentation are assumed to have the following **\#include** and **\#define** compiler directives.</span></span>


```C++
#include <stdio.h>
#include <windows.h>
#include <Wincrypt.h>
#define MY_ENCODING_TYPE  (PKCS_7_ASN_ENCODING | X509_ASN_ENCODING)
```



<span data-ttu-id="c7d71-105">Inoltre, la costante **\_ \_ WinNT Win32** deve essere definita in modo appropriato.</span><span class="sxs-lookup"><span data-stu-id="c7d71-105">Additionally, the **\_WIN32\_WINNT** constant must be appropriately defined.</span></span> <span data-ttu-id="c7d71-106">Per ulteriori informazioni su **\_ Win32 \_ WinNT**, vedere [utilizzo delle intestazioni di Windows](../winprog/using-the-windows-headers.md).</span><span class="sxs-lookup"><span data-stu-id="c7d71-106">For more information about **\_WIN32\_WINNT**, see [Using the Windows Headers](../winprog/using-the-windows-headers.md).</span></span>

 

 
