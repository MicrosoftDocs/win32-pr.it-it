---
description: L'azione BindImage associa ogni eseguibile o DLL che deve essere associato alle DLL importate da esso.
ms.assetid: bf90acc0-4e90-4180-9df7-268b63a66538
title: Azione BindImage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d621728de551c182d6678561b2ef5daf649fb8fae840f47a460d83a4d38f3635
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118638777"
---
# <a name="bindimage-action"></a>Azione BindImage

L'azione BindImage associa ogni eseguibile o DLL che deve essere associato alle DLL importate da esso. L'azione BindImage agisce su ogni file nella [tabella BindImage,](bindimage-table.md) ma solo su quelli che devono essere installati in locale. Il programma di installazione calcola l'indirizzo virtuale di ogni funzione importata da tutte le DLL, quindi salva l'indirizzo virtuale calcolato nella tabella degli indirizzi di importazione [](i-gly.md) (IAT) dell'immagine di importazione.

L'azione BindImage chiama internamente l'API **Windows BindImageEx.**

## <a name="sequence-restrictions"></a>Restrizioni di sequenza

L'azione BindImage deve essere eseguita dopo [l'azione InstallFiles.](installfiles-action.md)

## <a name="actiondata-messages"></a>Messaggi ActionData



| Campo | Descrizione dei dati dell'azione     |
|-------|--------------------------------|
| \[1\] | Identificatore di file dell'eseguibile. |



 

 

 



