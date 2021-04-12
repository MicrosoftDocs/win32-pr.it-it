---
description: La tabella MsiSFCBypass contiene un elenco di file che devono ignorare la protezione dei file di Windows quando i file vengono installati in Microsoft Windows me.
ms.assetid: 86de0dc1-ed8f-410c-a411-6c44c8e5c9fd
title: Tabella MsiSFCBypass
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 707294e9461aaf321add8a3959682a0db555cc2c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104347336"
---
# <a name="msisfcbypass-table"></a>Tabella MsiSFCBypass

La tabella MsiSFCBypass contiene un elenco di file che devono ignorare la protezione dei file di Windows quando i file vengono installati in Microsoft Windows me.

La tabella MsiSFCBypass include la colonna seguente.



| Colonna | Tipo                         | Chiave | Nullable |
|--------|------------------------------|-----|----------|
| file\_ | [Identificatore](identifier.md) | S   | N        |



 

## <a name="columns"></a>Colonne

<dl> <dt>

<span id="File_"></span><span id="file_"></span><span id="FILE_"></span>File\_
</dt> <dd>

Chiave esterna per la [tabella file](file-table.md) che specifica il file che deve ignorare la protezione dei file di Windows quando il file viene installato in Windows me.

</dd> </dl>

 

 



