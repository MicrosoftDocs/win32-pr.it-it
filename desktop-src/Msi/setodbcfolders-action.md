---
description: L'azione SetODBCFolders verifica la presenza di driver ODBC esistenti nel sistema e imposta la directory di destinazione di ogni nuovo driver sul percorso di un driver esistente.
ms.assetid: d1739b37-d89b-400e-a4ac-b417e0fb9918
title: Azione SetODBCFolders
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ceaefc2e9722b82ab0753c46b9e1e85a0ab3628a83b9f3abe66cf183c543fbe5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119628641"
---
# <a name="setodbcfolders-action"></a>Azione SetODBCFolders

L'azione SetODBCFolders verifica la presenza di driver ODBC esistenti nel sistema e imposta la directory di destinazione di ogni nuovo driver sul percorso di un driver esistente.

## <a name="sequence-restrictions"></a>Restrizioni relative alle sequenze

L'azione SetODBCFolders deve essere eseguita dopo [l'azione CostFinalize](costfinalize-action.md) e prima [dell'azione InstallValidate](installvalidate-action.md).

## <a name="actiondata-messages"></a>Messaggi ActionData



| Campo | Descrizione dei dati dell'azione                                                          |
|-------|-------------------------------------------------------------------------------------|
| \[1\] | Descrizione del driver. Tasto del driver ODBC.                                            |
| \[2\] | Percorso della cartella originale del nuovo driver.                                         |
| \[3\] | Nuovo percorso della cartella per il nuovo driver. Questo è il percorso di un driver esistente. |



 

## <a name="remarks"></a>Commenti

Questa azione inserisce un nuovo driver nella stessa directory del driver esistente da sostituire. L'azione SetODBCFolders usa la [tabella Directory](directory-table.md) per impostare i percorsi dei driver esistenti da sostituire.

 

 



