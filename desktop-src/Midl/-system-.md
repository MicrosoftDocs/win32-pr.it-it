---
title: /opzione di sistema
description: Il parametro/System indica al compilatore MIDL di generare una libreria dei tipi per il sistema specificato. Il valore predefinito è il sistema operativo corrente.
ms.assetid: 0fb69ffc-5ab4-49f3-b34d-859da776ce9e
keywords:
- /opzione di sistema MIDL
topic_type:
- apiref
api_name:
- / system
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0e09f2cf97f8edb86ad831cff35420fad9a07d76
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "104334167"
---
# <a name="system-switch"></a>/<system> commutatore

L' **/<system>** opzione indica al compilatore MIDL di generare una libreria dei tipi per il sistema specificato. Il valore predefinito è il sistema operativo corrente.

``` syntax
midl /{win32 | ia64 | amd64}
```

## <a name="switch-options"></a>Opzioni switch

<dl> <dt>

 
</dt> <dd>

<dt>

<span id="win32"></span><span id="WIN32"></span>

<span id="win32"></span><span id="WIN32"></span>Win32 * * * *


</dt> <dd>

Windows 2000, Windows XP, Windows Vista, Windows 7

</dd> <dt>

<span id="ia64"></span><span id="IA64"></span>

<span id="ia64"></span><span id="IA64"></span>ia64 * * * *


</dt> <dd>

Un ambiente Windows basato su Intel a 64 bit, ad esempio Windows 2000, Windows Server 2003, Windows XP Professional x64 Edition, Windows Vista o Windows 7.

</dd> <dt>

<span id="amd64"></span><span id="AMD64"></span>

<span id="amd64"></span><span id="AMD64"></span>amd64 * * * *


</dt> <dd>

Un ambiente Windows a 64 bit basato sui dispositivi statunitensi, ad esempio Windows 2000, Windows Server 2003, Windows XP Professional x64 Edition, Windows Vista o Windows 7.

</dd> </dl> </dd> </dl>

## <a name="remarks"></a>Commenti

Lo **/<system>** Switch è funzionalmente uguale all'opzione MIDL [**/ENV**](-env.md) e viene riconosciuto dal compilatore MIDL esclusivamente per la compatibilità con le versioni precedenti di mktyplib. Se si sta generando un nuovo Makefile, usare l'opzione **/ENV** .

## <a name="examples"></a>Esempio

**MIDL/Win32 nomefile. idl**

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Sintassi della riga di comando MIDL generale](general-midl-command-line-syntax.md)
</dt> <dt>

[**/ENV**](-env.md)
</dt> </dl>

 

 




