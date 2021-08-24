---
description: L'azione UnregisterFonts rimuove dal sistema le informazioni di registrazione sui tipi di carattere installati.
ms.assetid: 97cbbcbe-eb1c-45f0-91d2-4b17984498ae
title: Azione UnregisterFonts
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03ec15a7a431a03d678fb2fd8c39460ea40ebbcadf3efd0c24814c84e6042fb1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119787001"
---
# <a name="unregisterfonts-action"></a>Azione UnregisterFonts

L'azione UnregisterFonts rimuove dal sistema le informazioni di registrazione sui tipi di carattere installati.

## <a name="sequence-restrictions"></a>Restrizioni di sequenza

[L'azione RemoveFiles](removefiles-action.md) deve essere chiamata dopo UnregisterFonts.

## <a name="actiondata-messages"></a>Messaggi ActionData



| Campo | Descrizione dei dati dell'azione |
|-------|----------------------------|
| \[1\] | File del tipo di carattere.                 |



 

## <a name="remarks"></a>Commenti

L'azione UnregisterFonts viene eseguita se il file specificato nella colonna File della tabella \_ [Font](font-table.md) appartiene a un componente disinstallato.

 

 



