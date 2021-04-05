---
title: Istruzione VERSION
description: Definisce le informazioni sulla versione di una risorsa che possono essere usate da strumenti che leggono e scrivono file di risorse.
ms.assetid: 3a33cff3-b8b3-43f4-b43a-ff1d1728cdc1
keywords:
- Menu di istruzioni della versione e altre risorse
topic_type:
- apiref
api_name:
- VERSION
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 302ffcee38b287afff2697b9c5a5241fa406b55c
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "103718511"
---
# <a name="version-statement"></a>Istruzione VERSION

Definisce le informazioni sulla versione di una risorsa che possono essere usate da strumenti che leggono e scrivono file di risorse. Il valore *DWORD* specificato viene visualizzato con la risorsa nell'oggetto compilato. File RES. Tuttavia, il valore non viene archiviato nel file eseguibile e non ha significato per il sistema.

L'istruzione **Version** viene visualizzata prima dell'inizio del corpo di una definizione di risorsa [**Accelerators**](accelerators-resource.md), [**DIALOGEX**](dialogex-resource.md), [**menu**](menu-resource.md), [**RCDATA**](rcdata-resource.md)o [**un'STRINGTABLE**](stringtable-resource.md) . Il valore specificato si applica solo a tale risorsa.

``` syntax
VERSION dword
```

<dl> <dt>

<span id="dword"></span><span id="DWORD"></span>*DWORD*
</dt> <dd>

Valore **DWORD** definito dall'utente.

</dd> </dl>

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ACCELERATORI**](accelerators-resource.md)
</dt> <dt>

[**CARATTERISTICHE**](characteristics-statement.md)
</dt> <dt>

[**LINGUAGGIO**](language-statement.md)
</dt> <dt>

[**MENU**](menu-resource.md)
</dt> <dt>

[**RCDATA**](rcdata-resource.md)
</dt> <dt>

[**UN'STRINGTABLE**](stringtable-resource.md)
</dt> </dl>

 

 




