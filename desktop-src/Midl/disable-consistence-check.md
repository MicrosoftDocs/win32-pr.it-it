---
title: Attributo disable_consistency_check
description: Indica a RPC di non applicare la verifica della coerenza di correlazione.
ms.assetid: 33ba331d-56e5-4965-a844-7780ea81623d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc55197b5eb680533745a09d4fca4f5827574a7c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104329047"
---
# <a name="disable_consistency_check-attribute"></a>disabilitare \_ l' \_ attributo di verifica coerenza

Indica a RPC di non applicare la verifica della coerenza di correlazione.

``` syntax
interface interface-name
{
  return-type function-name(
        [[attribute-list,] disable_consistency_check] param-type param-name
}
```

Per i parametri correlati, RPC imporrà che viene passato un buffer non null quando la variabile di conteggio delle correlazioni è non null.

## <a name="example"></a>Esempio

``` syntax
HRESULT PassString( [in] DWORD Length, [in, unique, string, 
    size_is( Length )]LPWSTR MyString );
```

Se la *stringa* è **null**, RPC rifiuterà la chiamata a meno che length non sia impostato su 0. Si noti che RPC consentirà la *lunghezza* pari a 0 mentre la *stringa* è non null e RPC tratterà la *stringa* come un'allocazione di buffer di lunghezza 0.

## <a name="remarks"></a>Commenti

Per disabilitare questo controllo, l'IDL può contenere l' \[ \_ attributo disable \_ Verifica coerenza \] su un parametro, un typedef o un tipo di puntatore. In questo modo, RPC non impone la coerenza tra il puntatore del buffer e la variabile di correlazione per il buffer a cui punta il parametro o il puntatore.

Per disabilitare la verifica della coerenza per un'intera compilazione MIDL (e disabilitare l'imposizione del controllo in tutti i casi), è possibile usare l'opzione della riga di comando MIDL [/Backward \_ compat MAYBENULL \_ sizeis](-backward-compat.md) . A tale scopo, è necessario che la destinazione della compilazione MIDL sia almeno â € "NT60 di destinazione.

 

 




