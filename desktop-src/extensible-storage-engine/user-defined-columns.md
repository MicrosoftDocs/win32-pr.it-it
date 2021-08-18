---
description: "Altre informazioni su: Colonne definite dall'utente"
title: Colonne definite dall'utente
TOCTitle: User Defined Columns
ms:assetid: cccfc97c-acde-4328-a87f-ee7dcc54203c
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294091(v=EXCHG.10)
ms:contentKeyID: 32765706
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: 57212f49fe97f276677a2ca4396a23d672e175a86eb067f1d276b9c20a46b891
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117890072"
---
# <a name="user-defined-columns"></a>Colonne definite dall'utente


_**Si applica a:** Windows | Windows Server_

## <a name="user-defined-columns"></a>Colonne definite dall'utente

Le colonne definite dall'utente sono colonne i cui valori predefiniti vengono forniti da una funzione di callback. Queste colonne vengono sempre contrassegnate e impostate sul valore calcolato dalla funzione di callback. Questo valore deve essere stabile per ogni riga della tabella. La funzione di callback viene usata solo quando l'applicazione o il motore di database stesso deve leggere il valore della colonna per una determinata riga. L'applicazione può eseguire l'override del valore predefinito e impostare un valore specifico nella colonna . Quando il valore predefinito viene sostituito nelle colonne, usa lo spazio nella riga, in caso contrario le colonne predefinite definite dall'utente non usano spazio nel record.

L'opzione Defaults definita dall'utente è impostata nel membro **grbit** della struttura JET_COLUMNDEF [nella](./jet-columndef-structure.md) chiamata a [JetAddColumn](./jetaddcolumn-function.md). Il *parametro pvDefault* della funzione [JetAddColumn](./jetaddcolumn-function.md) punta a una struttura [JET_USERDEFINEDDEFAULT,](./jet-userdefineddefault-structure.md) che contiene il nome della funzione di callback nel membro **szCallback** e i dati passati al callback nel membro **pbUserData.**
