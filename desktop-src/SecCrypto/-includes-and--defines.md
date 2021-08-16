---
description: Si presuppone che tutti gli esempi nella documentazione di Cryptography SDK includano e definino le direttive \# \# del compilatore seguenti.
ms.assetid: 98f85e7d-e557-4dde-b510-891b37daec87
title: '#include e #defines'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6dbab2a3c33b510df99c9d2e0fa292af53c96fcc471dfe8180d9d4be06b3a5b6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117774276"
---
# <a name="includes-and-defines"></a>\#include e \# definisce

Si presuppone che tutti gli esempi nella documentazione **\#** di Cryptography SDK includano e **\# definino le** direttive del compilatore seguenti.


```C++
#include <stdio.h>
#include <windows.h>
#include <Wincrypt.h>
#define MY_ENCODING_TYPE  (PKCS_7_ASN_ENCODING | X509_ASN_ENCODING)
```



Inoltre, la **\_ costante WIN32 \_ WINNT** deve essere definita in modo appropriato. Per altre informazioni su **\_ WIN32 \_ WINNT,** vedere [Using the Windows Headers](../winprog/using-the-windows-headers.md).

 

 
