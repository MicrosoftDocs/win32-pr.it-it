---
description: ICE58 verifica che la tabella Media non abbia più di 80 righe.
ms.assetid: 693b195e-1e69-4895-87dd-59714646cff9
title: ICE58
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0be8cec8fda3a3ddc1efce397dfbd17a95a2baf37ab0392eb8e5ffd08c7df4a6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119528231"
---
# <a name="ice58"></a>ICE58

ICE58 verifica che la [tabella Media](media-table.md) non abbia più di 80 righe.

## <a name="result"></a>Risultato

Gli avvisi segnalati da ICE58 causano l'esito negativo dell'installazione, a meno che il pacchetto non sia installato con Windows Installer 2.0 o versione successiva. A partire Windows Installer 2.0, la restrizione per più di 80 voci della tabella dei supporti viene rimossa. Non viene generato alcun avviso se la proprietà [**Riepilogo**](page-count-summary.md) conteggio pagine del pacchetto è maggiore o uguale a 150. I pacchetti dello schema 200 o versione successiva possono essere installati solo da Windows Installer 2.0 o versione successiva.

## <a name="example"></a>Esempio

ICE58 segnala gli errori e gli avvisi seguenti per l'esempio illustrato.

``` syntax
This package has 81 media entries. Packages are limited to 80 entries in the media table.
```

Per correggere l'errore, eliminare eventuali voci della tabella multimediale inutilizzata, consolidare le voci della tabella multimediale che fanno riferimento allo stesso supporto e creare un nuovo pacchetto dell'applicazione per ridurre i supporti necessari.

[Media Table](media-table.md) (partial)



| DiskId | LastSequence\_ |
|--------|----------------|
| 1      | 10             |
| 2      | 20             |
| ...    | ...            |
| 81     | 810            |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni di riferimento su ICE](ice-reference.md)
</dt> </dl>

 

 



