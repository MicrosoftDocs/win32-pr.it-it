---
description: ICE58 verifica che la tabella multimediale non includa più di 80 righe.
ms.assetid: 693b195e-1e69-4895-87dd-59714646cff9
title: ICE58
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 152e3a528506861107bfc3c2d64c48935ea7320e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968099"
---
# <a name="ice58"></a>ICE58

ICE58 verifica che la [tabella multimediale](media-table.md) non includa più di 80 righe.

## <a name="result"></a>Risultato

Gli avvisi segnalati da ICE58 determinano l'esito negativo dell'installazione, a meno che il pacchetto non sia installato con Windows Installer 2,0 o versione successiva. A partire da Windows Installer 2,0, viene rimossa la restrizione a più di 80 voci della tabella multimediale. Se la proprietà di riepilogo dei conteggi delle [**pagine**](page-count-summary.md) del pacchetto è maggiore o uguale a 150, non viene generato alcun avviso. I pacchetti dello schema 200 o versioni successive possono essere installati solo da Windows Installer 2,0 o versioni successive.

## <a name="example"></a>Esempio

ICE58 segnala gli errori e gli avvisi seguenti per l'esempio illustrato.

``` syntax
This package has 81 media entries. Packages are limited to 80 entries in the media table.
```

Per correggere l'errore, eliminare le voci della tabella multimediale inutilizzata, consolidare le voci della tabella multimediale che fanno riferimento allo stesso supporto e riassemblare l'applicazione per ridurre i supporti necessari.

[Tabella media](media-table.md) (parziale)



| DiskId | LastSequence\_ |
|--------|----------------|
| 1      | 10             |
| 2      | 20             |
| ...    | ...            |
| 81     | 810            |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Riferimento ghiaccio](ice-reference.md)
</dt> </dl>

 

 



