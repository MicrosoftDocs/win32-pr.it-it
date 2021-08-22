---
description: Il codice seguente scarica un modulo di simboli a cui fa riferimento l'indirizzo del modulo BaseOfDll usando SymUnloadModule64.
ms.assetid: f185ae64-1de9-4139-acd5-7c3a108e1eba
title: Scaricamento di un modulo simboli
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0da437fe0ce188e3559280d2bc347f3b976aba52adbf8e4a0306e4e469747435
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119929281"
---
# <a name="unloading-a-symbol-module"></a>Scaricamento di un modulo simboli

Il codice seguente scarica un modulo di simboli a cui fa riferimento l'indirizzo del modulo BaseOfDll [**usando SymUnloadModule64.**](/windows/desktop/api/Dbghelp/nf-dbghelp-symunloadmodule)


```C++
if (SymUnloadModule64(hProcess, BaseOfDll))
{
    // SymUnloadModule64 returned success
}
else
{
    // SymUnloadModule64 failed
    DWORD error = GetLastError();
    printf("SymUnloadModule64 returned error : %d\n", error);
}
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Caricamento di un modulo di simboli](loading-a-symbol-module.md)
</dt> </dl>

 

 



