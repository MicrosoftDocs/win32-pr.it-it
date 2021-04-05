---
description: Funzioni transazionali NTFS (TxF).
ms.assetid: fb6be33c-9d6c-48b2-a4da-31c60af8d972
title: Funzioni TxF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b59fa3c9a1323ce77c97ee36390190ea6301d71d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103758831"
---
# <a name="txf-functions"></a>Funzioni TxF

Transactional NTFS (TxF) fornisce le funzioni seguenti.

## <a name="in-this-section"></a>Contenuto della sezione



| Funzione                                                                      | Descrizione                                                                                                                  |
|-------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| [**TxfLogCreateFileReadContext**](/windows/desktop/api/TxfW32/nf-txfw32-txflogcreatefilereadcontext)<br/> | Crea un contesto da utilizzare per leggere i record di replica.<br/>                                                         |
| [**TxfLogDestroyReadContext**](/windows/desktop/api/TxfW32/nf-txfw32-txflogdestroyreadcontext)<br/>       | Chiude un contesto di lettura creato dalla funzione [**TxfLogCreateFileReadContext**](/windows/desktop/api/TxfW32/nf-txfw32-txflogcreatefilereadcontext) .<br/> |
| [**TxfLogReadRecords**](/windows/desktop/api/TxfW32/nf-txfw32-txflogreadrecords)<br/>                     | Legge i record di rollforward dal log.<br/>                                                                              |



 

 

 




