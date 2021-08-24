---
title: boolean (WMI)
description: Parametro VT BOOL che accetta il valore \_ VARIANT \_ TRUE (&\# 8211;1) o VARIANT \_ FALSE (0).
ms.assetid: 3928ff39-ed17-4a61-bb72-a3c9be16ae45
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50422990a45dd59c2bedc3ac90bddcf06f7796cd3308daf03a11db0dca38f0b5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119051059"
---
# <a name="boolean-wmi"></a>boolean (WMI)

Il tipo di dati booleano è un parametro VT BOOL che accetta il valore \_ VARIANT \_ TRUE (-1) o VARIANT \_ FALSE (0). La tabella seguente elenca la differenza tra le rappresentazioni a livello di codice di **TRUE** logico in C/C++ e il tipo di automazione.

| Linguaggio   | Valore         | Valore numerico |
|------------|---------------|-----------------|
| C/C++      | **TRUE**      | 1               |
| Automazione | VARIANT \_ TRUE | –1              |

Entrambi i tipi sono diversi da zero e pertanto non **FALSE,** ma hanno rappresentazioni diverse per **TRUE.**
