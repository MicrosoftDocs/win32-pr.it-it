---
description: Quando vengono aggiunti, eliminati e modificati file, directory e altri oggetti di file system NTFS, il file system NTFS immette i record del journal delle modifiche nei flussi, uno per ogni volume del computer.
ms.assetid: c41aa3a8-c8d8-4bf2-9bbb-d6a6a556c5e4
title: Modificare i record del Journal
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56580a28c01ca164af4598cb290a37c8e36828f5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317804"
---
# <a name="change-journal-records"></a>Modificare i record del Journal

Quando vengono aggiunti, eliminati e modificati file, directory e altri oggetti di file system NTFS, il file system NTFS immette i record del journal delle modifiche nei flussi, uno per ogni volume del computer. In ogni record sono indicati il tipo di modifica e l'oggetto modificato. L'offset dall'inizio del flusso per un record specifico viene chiamato numero di sequenza di aggiornamento (USN) per il record specifico. I nuovi record vengono aggiunti alla fine del flusso.

Il file system NTFS potrebbe eliminare i record obsoleti per conservare spazio. Se sono stati eliminati record necessari, il servizio di indicizzazione esegue nuovamente l'indicizzazione del volume, come avviene quando non esiste alcun Journal delle modifiche.

Nel journal delle modifiche viene registrato solo il fatto di una modifica a un file e il motivo della modifica, ad esempio operazioni di scrittura, troncamento, allungamento, eliminazione e così via. Non registra informazioni sufficienti per consentire l'inversione della modifica.

Inoltre, più modifiche allo stesso file possono causare l'aggiunta di un solo flag Reason al record corrente. Se lo stesso tipo di modifica si verifica più di una volta, il file system NTFS non scrive un nuovo record per le modifiche dopo la prima. Ad esempio, diverse operazioni di scrittura senza operazioni di chiusura e riapertura che interessano il risultato di un solo record delle modifiche con il motivo per cui la \_ \_ sovrascrittura dei dati è impostata sul motivo del flag USN \_ .

Per illustrare il funzionamento del journal delle modifiche, si supponga che un utente acceda a un file nell'ordine seguente:

1.  Scrive nel file.
2.  Imposta il timestamp per il file.
3.  Scrive nel file.
4.  Tronca il file.
5.  Scrive nel file.
6.  Chiude il file.

In questo caso, il file system NTFS esegue le azioni seguenti nel journal delle modifiche (dove \| indica un'operazione OR bit per bit).



| Evento                                 | Azione file system NTFS                                                                                                                                                                                                                                                    |
|---------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Operazione di scrittura iniziale<br/>    | Il file system NTFS scrive un nuovo record USN con il flag motivo di \_ \_ sovrascrittura dei dati del motivo USN \_ impostato. Per ulteriori informazioni sui flag di motivo possibili, vedere la struttura dei [**\_ record USN**](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_record_v2) .<br/>                                                     |
| Impostazione dell'indicatore di data e ora del file<br/> | Il file system NTFS scrive un nuovo record USN con il flag impostazione \_ motivo USN \_ \_ Sovrascrivi \| \_ motivo USN \_ motivo \_ modifica informazioni di base \_ .<br/>                                                                                                                            |
| Seconda operazione di scrittura<br/>     | Il file system NTFS non scrive un nuovo record USN. Poiché la \_ \_ sovrascrittura dei dati del motivo USN \_ è già impostata per il record esistente, non viene apportata alcuna modifica al record.<br/>                                                                                           |
| Troncamento file<br/>            | Il file system NTFS scrive un nuovo record USN con il flag impostazione \_ motivo USN \_ \_ Sovrascrivi motivo \| USN \_ motivo informazioni di \_ base \_ \_ modifica \| USN \_ motivo \_ dati \_ troncamento.<br/>                                                                                           |
| Terza operazione di scrittura<br/>      | Il file system NTFS non scrive un nuovo record USN. Poiché la \_ \_ sovrascrittura dei dati del motivo USN \_ è già impostata per il record esistente, non viene apportata alcuna modifica al record.<br/>                                                                                           |
| Chiudi operazione<br/>            | Se l'utente che sta apportando modifiche è l'unico utente del file, il file system NTFS scrive un nuovo record USN con l'impostazione del flag seguente: USN \_ motivo per la \_ \_ sovrascrittura del \| \_ motivo per le \_ informazioni di base \_ \_ modifica USN motivo per il \| \_ \_ \_ troncamento dei dati \| USN \_ motivo \_ chiusura.<br/> |



 

Il Journal delle modifiche accumula una serie di record tra la prima apertura e l'ultima chiusura di un file. Per ogni record è stato impostato un nuovo flag Reason, che indica che si è verificato un nuovo tipo di modifica. La sequenza di record fornisce una cronologia parziale del file. Il record finale, creato quando il file viene chiuso, aggiunge il \_ flag di chiusura del motivo USN \_ . Questo record rappresenta un riepilogo delle modifiche apportate al file ma, a differenza dei record precedenti, non indica l'ordine delle modifiche.

L'utente successivo per accedere e modificare il file genera un nuovo record USN con un solo flag motivo.

 

 




