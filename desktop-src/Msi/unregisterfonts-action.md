---
description: L'azione UnregisterFonts rimuove le informazioni di registrazione sui tipi di carattere installati dal sistema.
ms.assetid: 97cbbcbe-eb1c-45f0-91d2-4b17984498ae
title: Azione UnregisterFonts
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9fcc847203b72b0e2d92fb5e9a4dc465bebb001b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319418"
---
# <a name="unregisterfonts-action"></a>Azione UnregisterFonts

L'azione UnregisterFonts rimuove le informazioni di registrazione sui tipi di carattere installati dal sistema.

## <a name="sequence-restrictions"></a>Restrizioni sequenza

L'azione [RemoveFiles](removefiles-action.md) deve essere chiamata dopo UnregisterFonts.

## <a name="actiondata-messages"></a>Messaggi ActionData



| Campo | Descrizione dei dati dell'azione |
|-------|----------------------------|
| \[1\] | File del tipo di carattere.                 |



 

## <a name="remarks"></a>Commenti

L'azione UnregisterFonts viene eseguita se il file specificato nella colonna file \_ della tabella dei [tipi di carattere](font-table.md) appartiene a un componente di cui è in corso la disinstallazione.

 

 



