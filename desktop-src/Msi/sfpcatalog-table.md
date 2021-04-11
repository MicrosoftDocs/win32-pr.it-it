---
description: La tabella SFPCatalog contiene i cataloghi usati da Windows me.
ms.assetid: e9dc65a9-4ec9-4310-b03a-a2c38720ca8c
title: Tabella SFPCatalog
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08fe887644faf6cf0a5cda626bbf757e9f448ef1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226352"
---
# <a name="sfpcatalog-table"></a>Tabella SFPCatalog

La tabella SFPCatalog contiene i cataloghi usati da Windows me.

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

Nome di file breve per il catalogo. Poiché i cataloghi non hanno versione, il catalogo specificato in questa colonna può sovrascrivere un catalogo con lo stesso nome ed è già installato nel sistema locale. Vedere l'argomento relativo al controllo delle versioni dei file. [Nessun file ha una versione](neither-file-has-a-version.md).

</dd> <dt>

<span id="Catalog"></span><span id="catalog"></span><span id="CATALOG"></span>Catalogo
</dt> <dd>

Dati binari per il catalogo.

</dd> <dt>

<span id="Dependency"></span><span id="dependency"></span><span id="DEPENDENCY"></span>Dipendenza
</dt> <dd>

Il catalogo specificato in questo campo è l'elemento padre del catalogo dipendente specificato nel campo SFPCatalog. Immettere il nome file breve del catalogo padre nel campo dipendenza. Questo campo è una chiave di nuovo nella colonna SFPCatalog. La corrispondenza tra maiuscole e minuscole.

Se il campo di dipendenza fa riferimento a un altro record nella tabella SFPCatalog, il catalogo padre viene installato prima del catalogo dipendente.

Se il campo di dipendenza fa riferimento a un catalogo padre non presente nel campo SFPCatalog della tabella e se il catalogo padre non è già installato, l'installazione non riesce.

</dd> </dl>

## <a name="remarks"></a>Commenti

L' [azione InstallSFPCatalogFile](installsfpcatalogfile-action.md) esegue una query sulla tabella dei [componenti](component-table.md), sulla tabella [file](file-table.md), sulla tabella [FileSFPCatalog](filesfpcatalog-table.md) e sulla tabella SFPCatalog.

## <a name="validation"></a>Convalida

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE29](ice29.md)  
[ICE32](ice32.md)  
[ICE46](ice46.md)  
[ICE66](ice66.md)  
</dl>

 

 



