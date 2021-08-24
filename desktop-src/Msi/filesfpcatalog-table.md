---
description: La tabella FileSFPCatalog associa i file specificati ai file di catalogo usati dalla protezione dei file di sistema.
ms.assetid: 70c8b64a-cf15-411c-8388-4a7e3051f45c
title: Tabella FileSFPCatalog
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41bec6e31cba93730cc65b04ffdfb4a509f0cd817ba709cc029edfb47c4c4e60
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119581591"
---
# <a name="filesfpcatalog-table"></a>Tabella FileSFPCatalog

La tabella FileSFPCatalog associa i file specificati ai file di catalogo usati dalla protezione dei file di sistema.

**Windows Vista, Windows Server 2003 e Windows XP:** Non supportato.

La tabella FileSFPCatalog contiene le colonne seguenti.



| Colonna       | Tipo                         | Chiave | Nullable |
|--------------|------------------------------|-----|----------|
| file\_       | [Identificatore](identifier.md) | S   | N        |
| SFPCatalog\_ | [Filename](filename.md)     | S   | N        |



 

## <a name="columns"></a>Colonne

<dl> <dt>

<span id="File_"></span><span id="file_"></span><span id="FILE_"></span>File\_
</dt> <dd>

Chiave esterna per la [tabella File](file-table.md).

</dd> <dt>

<span id="SFPCatalog_"></span><span id="sfpcatalog_"></span><span id="SFPCATALOG_"></span>SFPCatalog\_
</dt> <dd>

Chiave esterna per la [tabella SFPCatalog](sfpcatalog-table.md).

</dd> </dl>

## <a name="remarks"></a>Commenti

[L'azione InstallSFPCatalogFile](installsfpcatalogfile-action.md) esegue una query sulla tabella [Component](component-table.md), la tabella [File](file-table.md), la tabella FileSFPCatalog e la [tabella SFPCatalog](sfpcatalog-table.md).

## <a name="validation"></a>Convalida

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
[ICE66](ice66.md)  
[ICE76](ice76.md)  
</dl>

 

 



