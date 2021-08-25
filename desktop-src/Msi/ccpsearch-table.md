---
description: La tabella CCPSearch contiene l'elenco delle firme di file usate per il programma di controllo della conformità (CCP). Almeno uno di questi file deve essere presente nel computer di un utente perché l'utente sia conforme al programma.
ms.assetid: 98d21e24-1633-44b7-bfdb-5a40bab8d319
title: Tabella CCPSearch
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62d20894960dce7f346601bd2ed459140caa305323ca02d14d54416f32737216
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119821841"
---
# <a name="ccpsearch-table"></a>Tabella CCPSearch

La tabella CCPSearch contiene l'elenco delle firme di file usate per il programma di controllo della conformità (CCP). Almeno uno di questi file deve essere presente nel computer di un utente perché l'utente sia conforme al programma.

La tabella CCPSearch include la colonna seguente.



| Colonna      | Tipo                         | Chiave | Nullable |
|-------------|------------------------------|-----|----------|
| Firma\_ | [Identificatore](identifier.md) | S   | N        |



 

## <a name="column"></a>Colonna

<dl> <dt>

<span id="Signature_"></span><span id="signature_"></span><span id="SIGNATURE_"></span>Firma\_
</dt> <dd>

La firma rappresenta una firma di file univoca ed è anche la chiave esterna nelle tabelle \_ [Signature](signature-table.md), [RegLocator](reglocator-table.md), [IniLocator](inilocator-table.md), [CompLocator](complocator-table.md) [e DrLocator.](drlocator-table.md)

</dd> </dl>

## <a name="remarks"></a>Commenti

Questa tabella viene indicata quando viene eseguita [l'azione CCPSearch](ccpsearch-action.md) o [L'azione RMCCPSearch.](rmccpsearch-action.md)

## <a name="validation"></a>Convalida

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
</dl>

 

 



