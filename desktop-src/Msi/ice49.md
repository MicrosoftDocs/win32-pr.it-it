---
description: ICE49 verifica la presenza di voci del registro di sistema predefinite che non sono di \_ tipo reg SZ.
ms.assetid: 53d976fe-07d2-4b68-ae21-1dbd00d76942
title: ICE49
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5edc5ba319380e92fe7d1b7410673c1c688eb337
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103883938"
---
# <a name="ice49"></a>ICE49

ICE49 verifica la presenza di voci del registro di sistema predefinite che non sono di tipo **reg \_ SZ** .

## <a name="result"></a>Risultato

ICE49 pubblica un avviso se è presente una voce del registro di sistema predefinita che non è un tipo **reg \_ SZ** .

## <a name="example"></a>Esempio

ICE49 segnala l'avviso seguente per l'esempio illustrato.

``` syntax
Reg Entry 'Reg1' is not of type REG_SZ. Default types must be REG_SZ 
    on Win95 Systems. Make sure the component is conditionalized 
    to never be installed on Win95 machines.
```

Il valore " \# 123" è un valore **DWORD** del registro di sistema.

[Tabella del registro di sistema](registry-table.md) (parziale)



| Registro | Nome | Valore |
|----------|------|-------|
| Reg1     |      | \#123 |



 

Per correggere il problema, modificare il valore di tipo **reg \_ SZ**.

I componenti con non **reg \_ SZ** sono validi.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Sintassi dell'istruzione condizionale](conditional-statement-syntax.md)
</dt> <dt>

[Riferimento ghiaccio](ice-reference.md)
</dt> </dl>

 

 



