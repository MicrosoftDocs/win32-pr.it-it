---
title: Caratteristiche (istruzione)
description: Definisce le informazioni su una risorsa che può essere usata da strumenti che leggono e scrivono file di definizione delle risorse.
ms.assetid: 07834b02-a36e-40cc-8907-bff6631842f3
keywords:
- Menu di istruzioni caratteristiche e altre risorse
topic_type:
- apiref
api_name:
- CHARACTERISTICS
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de681785fa2ec815b1edbdda913dd8032f8feb8e
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "104045720"
---
# <a name="characteristics-statement"></a>Caratteristiche (istruzione)

Definisce le informazioni su una risorsa che può essere usata da strumenti che leggono e scrivono file di definizione delle risorse. Il valore **DWORD** specificato viene visualizzato con la risorsa nel file. res compilato. Tuttavia, il valore non viene archiviato nel file eseguibile e non ha significato per il sistema.

L'istruzione delle **caratteristiche** viene visualizzata prima dell'inizio del corpo di un [**acceleratore**](accelerators-resource.md), una [**finestra di dialogo**](dialog-resource.md), un [**menu**](menu-resource.md), una definizione di risorsa [**RCDATA**](rcdata-resource.md)o [**un'STRINGTABLE**](stringtable-resource.md) . Il valore specificato si applica solo a tale risorsa.

``` syntax
CHARACTERISTICS dword
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

[**DIALOGO**](dialog-resource.md)
</dt> <dt>

[**LINGUAGGIO**](language-statement.md)
</dt> <dt>

[**MENU**](menu-resource.md)
</dt> <dt>

[**RCDATA**](rcdata-resource.md)
</dt> <dt>

[**UN'STRINGTABLE**](stringtable-resource.md)
</dt> </dl>

 

 




