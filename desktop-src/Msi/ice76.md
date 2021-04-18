---
description: ICE76 verifica l'utilizzo del catalogo SFP (WFP) all'interno di Windows Installer pacchetti per Windows me. Questo ghiaccio verifica anche che nessun file nella tabella azione BindImage sul faccia riferimento a cataloghi SFP.
ms.assetid: e8b60b11-19ac-4ec4-aa36-a1f7a3ccd6f6
title: ICE76
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5beb0157053e9bd3e4bf0d896f52af04a511ac24
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308191"
---
# <a name="ice76"></a>ICE76

ICE76 verifica l'utilizzo del catalogo SFP (WFP) all'interno di Windows Installer pacchetti per Windows me. Questo ghiaccio verifica anche che nessun file nella [tabella](bindimage-table.md) azione BindImage sul faccia riferimento a cataloghi SFP.

La protezione dei file di Windows richiede una corrispondenza esatta tra il file e la firma incorporata nel file di catalogo. I file che fanno riferimento a un catalogo SFP non devono essere elencati nella tabella azione BindImage sul perché l'effetto dell' [azione azione BindImage sul](bindimage-action.md) su questi file è diverso tra i computer. I file a cui fanno riferimento i cataloghi SFP devono trovarsi in componenti permanenti o installati localmente.

## <a name="result"></a>Risultato

ICE76 Invia un errore per ogni file nella [tabella azione BindImage sul](bindimage-table.md) presente anche nella [tabella FileSFPCatalog](filesfpcatalog-table.md).

ICE76 genera un errore se un file nella tabella FileSFPCatalog appartiene a un componente con una delle seguenti condizioni:

-   **msidbComponentAttributesPermanent** non è impostato nella colonna Attributes della [tabella Component](component-table.md).
-   **msidbComponentAttributesSourceOnly** viene impostato nella colonna Attributes della tabella Component.
-   **msidbAttributesOptional** viene impostato nella colonna Attributes della tabella Component.

## <a name="example"></a>Esempio

ICE76 segnala l'errore seguente per l'esempio:

``` syntax
File 'File1' references a SFP catalog. Therefore it cannot be in the BindImage table.
```

[Tabella FileSFPCatalog](filesfpcatalog-table.md) (parziale)



| file\_ | SFPCatalog\_ |
|--------|--------------|
| File1  | Catalog1.Cat |



 

[Tabella azione BindImage sul](bindimage-table.md) (parziale)



| file\_ |
|--------|
| File1  |



 

Per risolvere questo problema, non immettere file che fanno riferimento a cataloghi SFP nella tabella azione BindImage sul.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Tabella azione BindImage sul](bindimage-table.md)
</dt> <dt>

[Tabella componenti](component-table.md)
</dt> <dt>

[Tabella FileSFPCatalog](filesfpcatalog-table.md)
</dt> <dt>

[Riferimento ghiaccio](ice-reference.md)
</dt> </dl>

 

 



