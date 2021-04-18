---
description: La tabella FileSFPCatalog associa i file specificati ai file di catalogo utilizzati dalla protezione dei file di sistema.
ms.assetid: 70c8b64a-cf15-411c-8388-4a7e3051f45c
title: Tabella FileSFPCatalog
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2300b73cc1639d8a54e206ea609043cf657c91f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315470"
---
# <a name="filesfpcatalog-table"></a>Tabella FileSFPCatalog

La tabella FileSFPCatalog associa i file specificati ai file di catalogo utilizzati dalla protezione dei file di sistema.

**Windows Vista, Windows Server 2003 e Windows XP:** Non supportato.

La tabella FileSFPCatalog include le colonne seguenti.



| Colonna       | Tipo                         | Chiave | Nullable |
|--------------|------------------------------|-----|----------|
| file\_       | [Identificatore](identifier.md) | S   | N        |
| SFPCatalog\_ | [Filename](filename.md)     | S   | N        |



 

## <a name="columns"></a>Colonne

<dl> <dt>

<span id="File_"></span><span id="file_"></span><span id="FILE_"></span>File\_
</dt> <dd>

Chiave esterna per la [tabella dei file](file-table.md).

</dd> <dt>

<span id="SFPCatalog_"></span><span id="sfpcatalog_"></span><span id="SFPCATALOG_"></span>SFPCatalog\_
</dt> <dd>

Chiave esterna per la [tabella SFPCatalog](sfpcatalog-table.md).

</dd> </dl>

## <a name="remarks"></a>Commenti

L' [azione InstallSFPCatalogFile](installsfpcatalogfile-action.md) esegue una query sulla tabella dei [componenti](component-table.md), sulla tabella [file](file-table.md), sulla tabella FileSFPCatalog e sulla [tabella SFPCatalog](sfpcatalog-table.md).

## <a name="validation"></a>Convalida

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
[ICE66](ice66.md)  
[ICE76](ice76.md)  
</dl>

 

 



