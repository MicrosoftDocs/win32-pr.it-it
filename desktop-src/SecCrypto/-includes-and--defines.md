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
# <a name="includes-and-defines"></a>\#include e \# definisce

Per tutti gli esempi della documentazione di Cryptography SDK si presuppone che siano incluse le direttive del compilatore seguenti **\# :** e **\# define** .


```C++
#include <stdio.h>
#include <windows.h>
#include <Wincrypt.h>
#define MY_ENCODING_TYPE  (PKCS_7_ASN_ENCODING | X509_ASN_ENCODING)
```



Inoltre, la costante **\_ \_ WinNT Win32** deve essere definita in modo appropriato. Per ulteriori informazioni su **\_ Win32 \_ WinNT**, vedere [utilizzo delle intestazioni di Windows](../winprog/using-the-windows-headers.md).

 

 
