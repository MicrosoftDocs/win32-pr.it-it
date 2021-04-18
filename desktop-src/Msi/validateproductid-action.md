---
description: L'azione ValidateProductID imposta la proprietà ProductID sull'identificatore completo del prodotto.
ms.assetid: 31b2f9d2-98d5-4cf3-af02-f12de2740bb8
title: Azione ValidateProductID
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f4d0f9f58641e8e24d73a1acae0b79cc0b875aba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308171"
---
# <a name="validateproductid-action"></a>Azione ValidateProductID

L'azione ValidateProductID imposta la proprietà [**ProductID**](productid.md) sull'identificatore completo del prodotto.

## <a name="sequence-restrictions"></a>Restrizioni sequenza

Questa azione deve essere sequenziata prima della creazione guidata interfaccia utente nella [tabella InstallUISequence](installuisequence-table.md) e prima dell' [azione RegisterUser](registeruser-action.md) nella [tabella InstallExecuteSequence](installexecutesequence-table.md).

## <a name="actiondata-messages"></a>Messaggi ActionData

Nessun messaggio ActionData.

## <a name="remarks"></a>Commenti

Il programma di installazione verifica se un prodotto è stato convalidato correttamente controllando la proprietà [**ProductID**](productid.md) . Il programma di installazione imposta la proprietà **ProductID** sull'identificatore completo del prodotto dopo una convalida corretta. L'azione ValidateProductID non esegue alcuna operazione se la proprietà **ProductID** è già stata impostata da una convalida corretta o da un altro metodo.

L'azione ValidateProductID restituisce sempre un esito positivo, indipendentemente dal fatto che l'identificatore del prodotto sia valido, in modo che l'identificatore del prodotto possa essere immesso nella riga di comando la prima volta che il prodotto viene eseguito.

L'identificatore del prodotto può essere convalidato senza che l'utente debba nuovamente immettere queste informazioni impostando la proprietà [**codice PIDKEY**](pidkey.md) nella riga di comando o utilizzando una trasformazione. La visualizzazione della finestra di dialogo in cui viene richiesto all'utente di immettere l'identificatore del prodotto può quindi essere resa condizionale alla presenza della proprietà [**ProductID**](productid.md) , che viene impostata quando la proprietà **codice PIDKEY** viene convalidata.

 

 



