---
title: Tipi di Wide-Character
description: Microsoft RPC supporta il tipo di carattere "wide" WCHAR \_ t.
ms.assetid: 1a601461-df34-456d-93e8-4cf0b655cf2c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 821d69999a0ec7e175409120f223721defd6cd10
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104118139"
---
# <a name="wide-character-types"></a>Tipi di Wide-Character

Microsoft RPC supporta il tipo di carattere "wide" [**WCHAR \_ t**](/windows/desktop/Midl/wchar-t). Il tipo di carattere wide USA 2 byte per ogni carattere. La definizione del linguaggio C ANSI consente di inizializzare caratteri Long e stringhe lunghe come:

``` syntax
wchar_t wcInitial = L'a';
wchar_t * pwszString = L"Hello, world";
```

 

 