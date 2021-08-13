---
description: La tabella SFPCatalog contiene i cataloghi usati da Windows Me.
ms.assetid: e9dc65a9-4ec9-4310-b03a-a2c38720ca8c
title: Tabella SFPCatalog
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 97498ff6437967a4a588be7b957aea130dad201699d55fad3abace6ff094b271
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118624892"
---
# <a name="sfpcatalog-table"></a>Tabella SFPCatalog

La tabella SFPCatalog contiene i cataloghi usati da Windows Me.

La tabella SFPCatalog include le colonne seguenti.



| Colonna     | Tipo                       | Chiave | Nullable |
|------------|----------------------------|-----|----------|
| SFPCatalog | [Filename](filename.md)   | S   | N        |
| Catalogo    | [Binario](binary.md)       | N   | N        |
| Dipendenza | [Formattato](formatted.md) | N   | S        |



 

## <a name="columns"></a>Colonne

<dl> <dt>

<span id="SFPCatalog"></span><span id="sfpcatalog"></span><span id="SFPCATALOG"></span>SFPCatalog
</dt> <dd>

Nome file breve per il catalogo. Poiché i cataloghi non hanno alcuna versione, il catalogo specificato in questa colonna può sovrascrivere un catalogo con lo stesso nome ed è già installato nel sistema locale. Vedere l'argomento relativo al controllo delle versioni dei [file Nessuno dei due file ha una versione](neither-file-has-a-version.md).

</dd> <dt>

<span id="Catalog"></span><span id="catalog"></span><span id="CATALOG"></span>Catalogo
</dt> <dd>

Dati binari per il catalogo.

</dd> <dt>

<span id="Dependency"></span><span id="dependency"></span><span id="DEPENDENCY"></span>Dipendenza
</dt> <dd>

Il catalogo specificato in questo campo è l'elemento padre del catalogo dipendente specificato nel campo SFPCatalog. Immettere il nome file breve del catalogo padre nel campo Dipendenza. Questo campo è una chiave nella colonna SFPCatalog. La corrispondenza delle dipendenze fa distinzione tra maiuscole e minuscole.

Se il campo Dipendenza fa riferimento a un altro record in questa tabella SFPCatalog, il catalogo padre viene installato prima del catalogo dipendente.

Se il campo Dipendenza fa riferimento a un catalogo padre non presente nel campo SFPCatalog di questa tabella e se il catalogo padre non è già installato, l'installazione non riesce.

</dd> </dl>

## <a name="remarks"></a>Commenti

[L'azione InstallSFPCatalogFile](installsfpcatalogfile-action.md) esegue una query sulla tabella [Component](component-table.md), sulla tabella [File](file-table.md), sulla [tabella FileSFPCatalog](filesfpcatalog-table.md) e sulla tabella SFPCatalog.

## <a name="validation"></a>Convalida

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE29](ice29.md)  
[ICE32](ice32.md)  
[ICE46](ice46.md)  
[ICE66](ice66.md)  
</dl>

 

 



