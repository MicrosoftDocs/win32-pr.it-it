---
description: L'azione CreateShortcuts gestisce la creazione di tasti di scelta rapida.
ms.assetid: 2e8a30ec-e8e7-4855-addb-2501bf85ab54
title: Azione CreateShortcuts
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e59ae3cdcc9d35091690742322617f3c9d07628
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104058114"
---
# <a name="createshortcuts-action"></a>Azione CreateShortcuts

L'azione CreateShortcuts gestisce la creazione di tasti di scelta rapida.

## <a name="sequence-restrictions"></a>Restrizioni sequenza

L'azione CreateShortcuts deve essere successiva all'azione [InstallFiles](installfiles-action.md) e [RemoveShortcuts](removeshortcuts-action.md) .

## <a name="actiondata-messages"></a>Messaggi ActionData



| Campo | Descrizione dei dati dell'azione      |
|-------|---------------------------------|
| \[1\] | Identificatore del collegamento creato. |



 

## <a name="remarks"></a>Commenti

L'azione CreateShortcuts crea collegamenti ai file principali dei componenti delle funzionalità selezionate per l'installazione o l'annuncio.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Tabella di collegamento](shortcut-table.md)
</dt> <dt>

[Tabella MsiShortcutProperty](msishortcutproperty-table.md)
</dt> </dl>

 

 



