---
description: L'azione RegisterFonts registra i tipi di carattere installati nel sistema. Questa azione esegue il mapping del nome del tipo di carattere nella colonna FontTitle della tabella Font al percorso del file del tipo di carattere installato.
ms.assetid: 3c6d3ec9-b36f-46f4-8b32-c97a75b9e238
title: Azione RegisterFonts
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2588dc1e2fd332521d43a7cefc4aae0378a63747166154730e0b832a9bf3835b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119339711"
---
# <a name="registerfonts-action"></a>Azione RegisterFonts

L'azione RegisterFonts registra i tipi di carattere installati nel sistema. Questa azione esegue il mapping del nome del tipo di carattere nella colonna FontTitle della tabella [Font](font-table.md) al percorso del file del tipo di carattere installato.

## <a name="sequence-restrictions"></a>Restrizioni relative alle sequenze

[L'azione InstallFiles](installfiles-action.md) deve essere chiamata prima di chiamare l'azione RegisterFonts.

## <a name="actiondata-messages"></a>Messaggi ActionData



| Campo | Descrizione dei dati dell'azione |
|-------|----------------------------|
| \[1\] | File del tipo di carattere.                 |



 

## <a name="remarks"></a>Commenti

L'azione RegisterFonts viene eseguita se il file specificato nella colonna File della tabella Font appartiene \_ a un componente da installare. [](font-table.md)

 

 



