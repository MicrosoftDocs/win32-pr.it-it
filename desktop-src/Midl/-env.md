---
title: opzione/env
description: L'opzione/env consente di selezionare l'ambiente in cui viene eseguita l'applicazione.
ms.assetid: 70a548c8-fdc3-48f3-a865-14ba9b29fb02
keywords:
- /ENV switch MIDL
topic_type:
- apiref
api_name:
- /env
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 59da7185900d4b75781916bd6b4a9d70bf39dc85
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104398893"
---
# <a name="env-switch"></a>opzione/env

L'opzione **/ENV** consente di selezionare l'ambiente in cui viene eseguita l'applicazione.

``` syntax
midl /env { win32 | ia64 | amd64 | win64 }
```

## <a name="switch-options"></a>Opzioni switch

<dl> <dt>

 
</dt> <dd>

<dt>

<span id="win32"></span><span id="WIN32"></span>

<span id="win32"></span><span id="WIN32"></span>Win32 * * * *


</dt> <dd>

Indica al compilatore MIDL di generare file stub o un file di libreria dei tipi per un ambiente a 32 bit.

</dd> <dt>

<span id="ia64"></span><span id="IA64"></span>

<span id="ia64"></span><span id="IA64"></span>ia64 * * * *


</dt> <dd>

Indica al compilatore MIDL di generare file stub o un file di libreria dei tipi per un ambiente Intel Architecture 64-bit (IA64).

</dd> <dt>

<span id="amd64"></span><span id="AMD64"></span>

<span id="amd64"></span><span id="AMD64"></span>amd64 * * * *


</dt> <dd>

Indica al compilatore MIDL di generare file stub o un file di libreria dei tipi per un ambiente di Micro Devices a 64 bit (AMD64) avanzato.

</dd> <dt>

<span id="win64"></span><span id="WIN64"></span>

<span id="win64"></span><span id="WIN64"></span>Win64 * * * *


</dt> <dd>

Stesso comportamento di *ia64*.

</dd> </dl> </dd> </dl>

## <a name="remarks"></a>Commenti

L'opzione **/ENV** influiscono principalmente sul livello di compressione usato per le strutture in tale ambiente. Assicurarsi di specificare la stessa impostazione a livello di compressione sia per il compilatore MIDL sia per il compilatore C.

L'opzione **/ENV** determina il livello di compressione e altre impostazioni come indicato di seguito:

-   Quando si specifica **Win32**, gli stub generati usano il livello di compressione del compilatore C 8 per tutti i tipi utilizzati nelle operazioni remote. I tipi di dati [**int**](int.md) sono entrambi 32 bit. I puntatori sono di 32 bit.
-   Quando si specifica **ia64** o **amd64**, il compilatore MIDL viene eseguito in modalità compilatore incrociato per la piattaforma 64 bit indicata (Intel o AMD). Gli stub generati usano il livello di compressione del compilatore C 8 per tutti i tipi utilizzati nelle operazioni remote. I tipi di dati [**Long**](long.md) e [**int**](int.md) sono di 32 bit. I puntatori sono di 64 bit.

Le opzioni [**/align**](-align.md), [**/Pack**](-pack.md)e [**/ZP**](-zp.md) hanno la precedenza sulle impostazioni di **/ENV** .

Per ulteriori informazioni sul supporto di 64 bit per MIDL e RPC, vedere [progettazione di interfacce compatibili con 64 bit](/windows/desktop/WinProg64/designing-64-bit-compatible-interfaces).

## <a name="examples"></a>Esempio

**nome file Win32 MIDL/ENV. idl**

**MIDL/env ia64 nomefile. idl**

**MIDL/ENV amd64 nomefile. idl**

**MIDL/ENV Win64 nomefile. idl**

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Sintassi della riga di comando MIDL generale](general-midl-command-line-syntax.md)
</dt> <dt>

[**/Pack**](-pack.md)
</dt> <dt>

[**/ZP**](-zp.md)
</dt> </dl>

 

 