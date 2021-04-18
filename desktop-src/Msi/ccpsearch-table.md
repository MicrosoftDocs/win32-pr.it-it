---
description: La tabella CCPSearch contiene l'elenco delle firme di file utilizzate per il programma di verifica della conformità (CCP). È necessario che almeno uno di questi file sia presente nel computer di un utente affinché l'utente sia conforme al programma.
ms.assetid: 98d21e24-1633-44b7-bfdb-5a40bab8d319
title: Tabella CCPSearch
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 368c0452fea011aca1080ca17020467ba6e0dc4f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310997"
---
# <a name="ccpsearch-table"></a>Tabella CCPSearch

La tabella CCPSearch contiene l'elenco delle firme di file utilizzate per il programma di verifica della conformità (CCP). È necessario che almeno uno di questi file sia presente nel computer di un utente affinché l'utente sia conforme al programma.

La tabella CCPSearch include la colonna seguente.



| Colonna      | Tipo                         | Chiave | Nullable |
|-------------|------------------------------|-----|----------|
| Firma\_ | [Identificatore](identifier.md) | S   | N        |



 

## <a name="column"></a>Colonna

<dl> <dt>

<span id="Signature_"></span><span id="signature_"></span><span id="SIGNATURE_"></span>Firma\_
</dt> <dd>

La firma \_ rappresenta una firma del file univoca ed è anche la chiave esterna nelle tabelle [Signature](signature-table.md), [RegLocator](reglocator-table.md), [IniLocator](inilocator-table.md), [CompLocator](complocator-table.md)e [DrLocator](drlocator-table.md) .

</dd> </dl>

## <a name="remarks"></a>Commenti

Questa tabella viene definita quando viene eseguita l'azione [CCPSearch](ccpsearch-action.md) o [RMCCPSearch](rmccpsearch-action.md) .

## <a name="validation"></a>Convalida

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
</dl>

 

 



