---
description: L'azione RegisterFonts registra i tipi di carattere installati con il sistema. Questa azione esegue il mapping del nome del tipo di carattere nella colonna FontTitle della tabella dei tipi di carattere al percorso del file del tipo di carattere installato.
ms.assetid: 3c6d3ec9-b36f-46f4-8b32-c97a75b9e238
title: Azione RegisterFonts
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98532be2744e89fff79f6e3d8becd2e6cc9259a1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311709"
---
# <a name="registerfonts-action"></a>Azione RegisterFonts

L'azione RegisterFonts registra i tipi di carattere installati con il sistema. Questa azione esegue il mapping del nome del tipo di carattere nella colonna FontTitle della [tabella dei tipi di carattere](font-table.md) al percorso del file del tipo di carattere installato.

## <a name="sequence-restrictions"></a>Restrizioni sequenza

Prima di chiamare l'azione RegisterFonts, è necessario chiamare l'azione [InstallFiles](installfiles-action.md) .

## <a name="actiondata-messages"></a>Messaggi ActionData



| Campo | Descrizione dei dati dell'azione |
|-------|----------------------------|
| \[1\] | File del tipo di carattere.                 |



 

## <a name="remarks"></a>Commenti

L'azione RegisterFonts viene eseguita se il file specificato nella colonna file \_ della tabella dei [tipi di carattere](font-table.md) appartiene a un componente in fase di installazione.

 

 



