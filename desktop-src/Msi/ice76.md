---
description: ICE76 verifica l'uso del catalogo SFP (WFP) all'interno di Windows installer per Windows Me. Questo ICE verifica anche che nessun file nella tabella BindImage fa riferimento ai cataloghi SFP.
ms.assetid: e8b60b11-19ac-4ec4-aa36-a1f7a3ccd6f6
title: ICE76
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a0b6caf5e29d26ba68721daa156dd0fc78a1868b5aa1ba1b7ea165834dd5ac8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120129431"
---
# <a name="ice76"></a>ICE76

ICE76 verifica l'uso del catalogo SFP (WFP) all'interno di Windows installer per Windows Me. Questo ICE verifica anche che nessun file nella tabella [BindImage](bindimage-table.md) fa riferimento ai cataloghi SFP.

Windows Protezione file richiede una corrispondenza esatta tra il file e la firma incorporata nel file di catalogo. I file che fanno riferimento a un catalogo SFP non devono essere elencati nella tabella BindImage perché l'effetto dell'azione [BindImage](bindimage-action.md) su questi file è diverso tra i computer. I file a cui fanno riferimento i cataloghi SFP devono essere in componenti permanenti o installati in locale.

## <a name="result"></a>Risultato

ICE76 invia un errore per ogni file nella tabella [BindImage](bindimage-table.md) presente anche nella [tabella FileSFPCatalog](filesfpcatalog-table.md).

ICE76 genera un errore se un file nella tabella FileSFPCatalog appartiene a un componente con uno dei valori true seguenti:

-   **msidbComponentAttributesPermanent** non è impostato nella colonna Attributi della [tabella Component](component-table.md).
-   **msidbComponentAttributesSourceOnly** è impostato nella colonna Attributi della tabella Component.
-   **msidbAttributesOptional** è impostato nella colonna Attributi della tabella Component.

## <a name="example"></a>Esempio

ICE76 segnala l'errore seguente per l'esempio:

``` syntax
File 'File1' references a SFP catalog. Therefore it cannot be in the BindImage table.
```

[Tabella FileSFPCatalog](filesfpcatalog-table.md) (parziale)



| file\_ | SFPCatalog\_ |
|--------|--------------|
| File1  | Catalog1.Cat |



 

[Tabella BindImage](bindimage-table.md) (parziale)



| file\_ |
|--------|
| File1  |



 

Per risolvere questo problema, non immettere i file che fanno riferimento ai cataloghi SFP nella tabella BindImage.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Tabella BindImage](bindimage-table.md)
</dt> <dt>

[Tabella dei componenti](component-table.md)
</dt> <dt>

[Tabella FileSFPCatalog](filesfpcatalog-table.md)
</dt> <dt>

[Informazioni di riferimento su ICE](ice-reference.md)
</dt> </dl>

 

 



