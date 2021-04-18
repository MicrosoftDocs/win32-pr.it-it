---
description: L'azione SetODBCFolders controlla i driver ODBC esistenti nel sistema e imposta la directory di destinazione di ogni nuovo driver sul percorso di un driver esistente.
ms.assetid: d1739b37-d89b-400e-a4ac-b417e0fb9918
title: Azione SetODBCFolders
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7477b229d127e976ddb37096c5f3a21605ba8d05
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305962"
---
# <a name="setodbcfolders-action"></a>Azione SetODBCFolders

L'azione SetODBCFolders controlla i driver ODBC esistenti nel sistema e imposta la directory di destinazione di ogni nuovo driver sul percorso di un driver esistente.

## <a name="sequence-restrictions"></a>Restrizioni sequenza

L'azione SetODBCFolders deve essere successiva all'azione [CostFinalize secondo](costfinalize-action.md) e prima dell' [azione InstallValidate](installvalidate-action.md).

## <a name="actiondata-messages"></a>Messaggi ActionData



| Campo | Descrizione dei dati dell'azione                                                          |
|-------|-------------------------------------------------------------------------------------|
| \[1\] | Descrizione del driver. Chiave del driver ODBC.                                            |
| \[2\] | Percorso della cartella originale del nuovo driver.                                         |
| \[3\] | Nuovo percorso della cartella per il nuovo driver. Si tratta del percorso di un driver esistente. |



 

## <a name="remarks"></a>Commenti

Questa azione inserisce un nuovo driver nella stessa directory del driver esistente da sostituire. L'azione SetODBCFolders utilizza la [tabella directory](directory-table.md) per impostare i percorsi dei driver esistenti che devono essere sostituiti.

 

 



