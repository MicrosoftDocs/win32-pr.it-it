---
description: ICE71 verifica che la tabella Media contenga una voce con DiskId uguale a 1.
ms.assetid: b48c2f3f-24ef-48a8-849f-7abed69c0fc9
title: ICE71
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb1090eb8b1a36ed361ef763bfda3875a8fde052ed8643dceeb660c88ae954a3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118142515"
---
# <a name="ice71"></a>ICE71

ICE71 verifica che la tabella [Media](media-table.md) contenga una voce con DiskId uguale a 1. (Windows programma di installazione presuppone che .msi pacchetto sia sul disco 1.

## <a name="result"></a>Risultato

ICE71 restituisce un errore se la tabella Media non contiene una voce con DiskId uguale a 1.

## <a name="example"></a>Esempio

ICE71 segnala l'errore seguente per l'esempio illustrato.

``` syntax
The Media table requires an entry with DiskId=1. First DiskId is '2'.
```

T0 corregge questo errore, modifica diskId della voce in cui è archiviato il pacchetto su 1.

[Media Table](media-table.md) (partial)



| DiskId |
|--------|
| 2      |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni di riferimento su ICE](ice-reference.md)
</dt> </dl>

 

 



