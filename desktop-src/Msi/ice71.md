---
description: ICE71 verifica che la tabella media includa una voce con DiskID uguale a 1.
ms.assetid: b48c2f3f-24ef-48a8-849f-7abed69c0fc9
title: ICE71
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c6e136362caa13da2b6305e3d8c3ca9c3a5c7bd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968234"
---
# <a name="ice71"></a>ICE71

ICE71 verifica che la [tabella media](media-table.md) includa una voce con DiskID uguale a 1. (Windows Installer presuppone che il pacchetto MSI si trovi sul disco 1.)

## <a name="result"></a>Risultato

ICE71 restituisce un errore se la tabella media non contiene una voce con DiskID uguale a 1.

## <a name="example"></a>Esempio

ICE71 segnala l'errore seguente per l'esempio illustrato.

``` syntax
The Media table requires an entry with DiskId=1. First DiskId is '2'.
```

T0 correggere l'errore, modificare il DiskID della voce in cui il pacchetto viene archiviato in 1.

[Tabella media](media-table.md) (parziale)



| DiskId |
|--------|
| 2      |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Riferimento ghiaccio](ice-reference.md)
</dt> </dl>

 

 



