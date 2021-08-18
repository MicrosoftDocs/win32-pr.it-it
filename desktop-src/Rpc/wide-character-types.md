---
title: Wide-Character tipi
description: Microsoft RPC supporta il tipo di carattere wide wchar \_ t.
ms.assetid: 1a601461-df34-456d-93e8-4cf0b655cf2c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4eff57cf22e4836032acb59e1585da15285f55718b6c5b91733b1955ea85072a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119010399"
---
# <a name="wide-character-types"></a>Wide-Character tipi

Microsoft RPC supporta il tipo di carattere wide [**wchar \_ t**](/windows/desktop/Midl/wchar-t). Il tipo di carattere wide usa 2 byte per ogni carattere. La definizione del linguaggio C ANSI consente di inizializzare caratteri lunghi e stringhe lunghe come:

``` syntax
wchar_t wcInitial = L'a';
wchar_t * pwszString = L"Hello, world";
```

 

 