---
title: /opzione di sistema
description: L'opzione /system indica al compilatore MIDL di generare una libreria dei tipi per il sistema specificato. Il valore predefinito è il sistema operativo corrente.
ms.assetid: 0fb69ffc-5ab4-49f3-b34d-859da776ce9e
keywords:
- /system switch MIDL
topic_type:
- apiref
api_name:
- / system
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 31def6297a1a91f6ed28943290a66b544dc368d5a00a91932035a338af50bac5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118643779"
---
# <a name="system-switch"></a>/<system> Interruttore

**/<system>** L'opzione indica al compilatore MIDL di generare una libreria dei tipi per il sistema specificato. Il valore predefinito è il sistema operativo corrente.

``` syntax
midl /{win32 | ia64 | amd64}
```

## <a name="switch-options"></a>Opzioni di cambio

<dl> <dt>

 
</dt> <dd>

<dt>

<span id="win32"></span><span id="WIN32"></span>

<span id="win32"></span><span id="WIN32"></span>win32****


</dt> <dd>

Windows 2000, Windows XP, Windows Vista, Windows 7

</dd> <dt>

<span id="ia64"></span><span id="IA64"></span>

<span id="ia64"></span><span id="IA64"></span>ia64****


</dt> <dd>

Un ambiente Windows a 64 bit basato su Intel, ad esempio Windows 2000, Windows Server 2003, Windows XP Professional x64 Edition, Windows Vista o Windows 7.

</dd> <dt>

<span id="amd64"></span><span id="AMD64"></span>

<span id="amd64"></span><span id="AMD64"></span>amd64****


</dt> <dd>

Un ambiente Windows a 64 bit basato su micro dispositivi statunitensi, ad esempio Windows 2000, Windows Server 2003, Windows XP Professional x64 Edition, Windows Vista o Windows 7.

</dd> </dl> </dd> </dl>

## <a name="remarks"></a>Commenti

L'opzione è funzionalmente uguale all'opzione MIDL /env ed è riconosciuta dal compilatore MIDL esclusivamente per la compatibilità con le versioni precedenti **/<system>** con MkTypLib. [](-env.md) Se si genera un nuovo makefile, usare **l'opzione /env.**

## <a name="examples"></a>Esempio

**midl /win32 filename.idl**

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Sintassi della riga di comando MIDL generale](general-midl-command-line-syntax.md)
</dt> <dt>

[**/env**](-env.md)
</dt> </dl>

 

 




