---
title: valore booleano (WMI)
description: '\_Parametro bool di VT che accetta il valore di Variant \_ TRUE (&\# 8211; 1) o Variant \_ false (0).'
ms.assetid: 3928ff39-ed17-4a61-bb72-a3c9be16ae45
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 569f7ce633bfb70fdba5e7055a80ad73ebd0fb6c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316574"
---
# <a name="boolean-wmi"></a>valore booleano (WMI)

Il tipo di dati Boolean è un \_ parametro di VT bool che accetta il valore di Variant \_ true (-1) o Variant \_ false (0). Nella tabella seguente sono elencate le differenze tra le rappresentazioni a livello di codice di Logical **true** in C/C++ e il tipo di automazione.

| Linguaggio   | Valore         | Valore numerico |
|------------|---------------|-----------------|
| C/C++      | **TRUE**      | 1               |
| Automazione | VARIANT \_ true | –1              |

Entrambi i tipi sono diversi da zero e pertanto non sono **false**, ma hanno rappresentazioni diverse per **true**.
