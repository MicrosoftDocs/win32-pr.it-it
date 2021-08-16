---
description: L'azione ValidateProductID imposta la proprietà ProductID sull'identificatore completo del prodotto.
ms.assetid: 31b2f9d2-98d5-4cf3-af02-f12de2740bb8
title: Azione ValidateProductID
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be241bddbafb8f963aea1e73a2750c9d45766eb06767b0b30142883fa1bcebac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118942231"
---
# <a name="validateproductid-action"></a>Azione ValidateProductID

L'azione ValidateProductID imposta la [**proprietà ProductID**](productid.md) sull'identificatore completo del prodotto.

## <a name="sequence-restrictions"></a>Restrizioni relative alle sequenze

Questa azione deve essere sequenziata prima della procedura guidata dell'interfaccia utente nella tabella [InstallUISequence](installuisequence-table.md) e prima dell'azione [RegisterUser](registeruser-action.md) nella [tabella InstallExecuteSequence](installexecutesequence-table.md).

## <a name="actiondata-messages"></a>Messaggi ActionData

Non sono presenti messaggi ActionData.

## <a name="remarks"></a>Commenti

Il programma di installazione controlla se un prodotto è stato convalidato correttamente controllando la [**proprietà ProductID.**](productid.md) Il programma di installazione imposta la **proprietà ProductID** sull'identificatore completo del prodotto dopo una convalida riuscita. L'azione ValidateProductID non esegue alcuna operazione se la **proprietà ProductID** è già stata impostata da una convalida riuscita o da un altro metodo.

L'azione ValidateProductID restituisce sempre un esito positivo, indipendentemente dal fatto che l'identificatore del prodotto sia valido, in modo che l'identificatore del prodotto possa essere immesso nella riga di comando la prima volta che viene eseguito il prodotto.

L'identificatore del prodotto può essere convalidato senza che l'utente reimima queste informazioni impostando la [**proprietà PIDKEY**](pidkey.md) nella riga di comando o usando una trasformazione. La visualizzazione della finestra di dialogo che richiede all'utente di immettere l'identificatore del prodotto può quindi essere resa condizionale in base alla presenza della proprietà [**ProductID,**](productid.md) che viene impostata quando viene convalidata la **proprietà PIDKEY.**

 

 



