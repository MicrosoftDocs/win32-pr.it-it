---
title: / opzione di sistema
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
ms.openlocfilehash: 01b6455807aedb99d7bd525c69fffc524dbe25d4
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/26/2021
ms.locfileid: "122882782"
---
# <a name="ltsystemgt-switch"></a>/&lt;commutatore &gt; di sistema

**/ &lt; L'opzione &gt;** di sistema indica al compilatore MIDL di generare una libreria dei tipi per il sistema specificato. Il valore predefinito è il sistema operativo corrente.

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

**/ &lt; L'opzione &gt;** di sistema è funzionalmente uguale all'opzione MIDL [**/env**](-env.md) ed è riconosciuta dal compilatore MIDL esclusivamente per la compatibilità con le versioni precedenti con MkTypLib. Se si genera un nuovo makefile, usare **l'opzione /env.**

## <a name="examples"></a>Esempio

**midl /win32 filename.idl**

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Sintassi della riga di comando MIDL generale](general-midl-command-line-syntax.md)
</dt> <dt>

[**/env**](-env.md)
</dt> </dl>

 

 




