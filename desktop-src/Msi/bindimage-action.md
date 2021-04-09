---
description: L'azione azione BindImage sul associa ogni file eseguibile o DLL che deve essere associato alle DLL importate da tale file.
ms.assetid: bf90acc0-4e90-4180-9df7-268b63a66538
title: Azione azione BindImage sul
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa2ac4c5ca16b83a3f0f0796d9a755542ec108c3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103881082"
---
# <a name="bindimage-action"></a>Azione azione BindImage sul

L'azione azione BindImage sul associa ogni file eseguibile o DLL che deve essere associato alle DLL importate da tale file. L'azione azione BindImage sul agisce su ogni file nella tabella [azione BindImage sul](bindimage-table.md) , ma solo su quelli che devono essere installati localmente. Il programma di installazione calcola l'indirizzo virtuale di ogni funzione importata da tutte le dll, quindi Salva l'indirizzo virtuale calcolato nella [*tabella degli indirizzi di importazione*](i-gly.md) (IAT) dell'immagine di importazione.

L'azione azione BindImage sul chiama internamente l'API Windows **BindImageEx** .

## <a name="sequence-restrictions"></a>Restrizioni sequenza

L'azione azione BindImage sul deve essere successiva all'azione [InstallFiles](installfiles-action.md) .

## <a name="actiondata-messages"></a>Messaggi ActionData



| Campo | Descrizione dei dati dell'azione     |
|-------|--------------------------------|
| \[1\] | Identificatore di file eseguibile. |



 

 

 



