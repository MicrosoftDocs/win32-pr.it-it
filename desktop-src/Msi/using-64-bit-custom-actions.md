---
description: Nei sistemi operativi a 64 bit, Windows installer può chiamare azioni personalizzate compilate per sistemi a 32 o 64 bit.
ms.assetid: e9ef684d-e22c-43b3-a5ea-75a4cce663c1
title: Uso di azioni personalizzate a 64 bit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70d94e5d6118c0f2f5dcf5a297718e135cce25a69bea0f48a2d4ea5df4cc0463
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119809111"
---
# <a name="using-64-bit-custom-actions"></a>Uso di azioni personalizzate a 64 bit

Nei sistemi operativi a 64 bit, Windows installer può chiamare azioni personalizzate compilate per sistemi a 32 o 64 bit. Un'azione personalizzata a 64 bit basata su Script deve essere contrassegnata in modo esplicito come azione personalizzata a 64 bit aggiungendo il bit **msidbCustomActionType64BitScript** al tipo numerico dell'azione personalizzata nella colonna Tipo della [tabella CustomAction](customaction-table.md). [](scripts.md) Le azioni [](executable-files.md) personalizzate basate su file eseguibili o librerie a [collegamento](dynamic-link-libraries.md) dinamico che vengono rispettate per i sistemi operativi a 64 bit non richiedono l'inclusione di questo bit aggiuntivo nella colonna Tipo della tabella CustomAction.

Per altre informazioni, vedere [Azioni personalizzate a 64 bit.](64-bit-custom-actions.md)

 

 



