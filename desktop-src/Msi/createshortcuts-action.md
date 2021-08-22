---
description: L'azione CreateShortcuts gestisce la creazione di collegamenti.
ms.assetid: 2e8a30ec-e8e7-4855-addb-2501bf85ab54
title: Azione CreateShortcuts
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 209dbd38d64abb2ddedb267512dd3872991d58071769d25606ed364a15c6d958
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119649741"
---
# <a name="createshortcuts-action"></a>Azione CreateShortcuts

L'azione CreateShortcuts gestisce la creazione di collegamenti.

## <a name="sequence-restrictions"></a>Restrizioni di sequenza

L'azione CreateShortcuts deve essere eseguita dopo [l'azione InstallFiles](installfiles-action.md) e [l'azione RemoveShortcuts.](removeshortcuts-action.md)

## <a name="actiondata-messages"></a>Messaggi ActionData



| Campo | Descrizione dei dati dell'azione      |
|-------|---------------------------------|
| \[1\] | Identificatore del collegamento creato. |



 

## <a name="remarks"></a>Commenti

L'azione CreateShortcuts crea collegamenti ai file chiave dei componenti delle funzionalità selezionati per l'installazione o l'annuncio.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Tabella dei collegamenti](shortcut-table.md)
</dt> <dt>

[Tabella MsiShortcutProperty](msishortcutproperty-table.md)
</dt> </dl>

 

 



