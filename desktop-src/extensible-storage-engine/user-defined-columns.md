---
description: "Altre informazioni su: colonne definite dall'utente"
title: Colonne definite dall'utente
TOCTitle: User Defined Columns
ms:assetid: cccfc97c-acde-4328-a87f-ee7dcc54203c
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294091(v=EXCHG.10)
ms:contentKeyID: 32765706
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: 624a916ee2048d9069c7695c79824e3357b511f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049741"
---
# <a name="user-defined-columns"></a>Colonne definite dall'utente


_**Si applica a:** Windows | Windows Server_

## <a name="user-defined-columns"></a>Colonne definite dall'utente

Le colonne definite dall'utente sono colonne i cui valori predefiniti sono forniti da una funzione di callback. Queste colonne vengono sempre contrassegnate e impostate sul valore calcolato dalla funzione di callback. Questo valore deve essere stabile per ogni riga della tabella. La funzione di callback viene utilizzata solo quando il motore di database o l'applicazione deve leggere il valore della colonna per una determinata riga. Nell'applicazione è possibile eseguire l'override del valore predefinito e impostare un valore specifico nella colonna. Quando si esegue l'override del valore predefinito nelle colonne, viene utilizzato lo spazio nella riga; in caso contrario, le colonne predefinite definite dall'utente non utilizzano lo spazio nel record.

L'opzione impostazioni predefinite definite dall'utente è impostata nel membro **grbit** della struttura [JET_COLUMNDEF](./jet-columndef-structure.md) nella chiamata a [JetAddColumn](./jetaddcolumn-function.md). Il parametro *pvDefault* della funzione [JetAddColumn](./jetaddcolumn-function.md) punta a una struttura di [JET_USERDEFINEDDEFAULT](./jet-userdefineddefault-structure.md) , che contiene il nome della funzione di callback nel membro **szCallback** e i dati passati al callback nel membro **pbUserData** .
