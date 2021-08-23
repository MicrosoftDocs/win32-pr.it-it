---
description: Quando file, directory e altri oggetti file system NTFS vengono aggiunti, eliminati e modificati, il file system NTFS immette i record del journal delle modifiche nei flussi, uno per ogni volume del computer.
ms.assetid: c41aa3a8-c8d8-4bf2-9bbb-d6a6a556c5e4
title: Record del journal delle modifiche
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2313dde6a71b36ed046a7086d39ce8e1a86b909cc7c815f295bb8a45c82ab92f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119765991"
---
# <a name="change-journal-records"></a>Record del journal delle modifiche

Quando file, directory e altri oggetti file system NTFS vengono aggiunti, eliminati e modificati, il file system NTFS immette i record del journal delle modifiche nei flussi, uno per ogni volume del computer. In ogni record sono indicati il tipo di modifica e l'oggetto modificato. L'offset dall'inizio del flusso per un determinato record è denominato numero di sequenza di aggiornamento (USN) per il record specifico. I nuovi record vengono aggiunti alla fine del flusso.

Il file system NTFS può eliminare i record precedenti per risparmiare spazio. Se i record necessari sono stati eliminati, il servizio di indicizzazione esegue il ripristino tramite la nuova indicizzazione del volume, come quando non esiste alcun journal delle modifiche.

Il journal delle modifiche registra solo il fatto di una modifica apportata a un file e il motivo della modifica, ad esempio operazioni di scrittura, troncamento, allungamento, eliminazione e così via. Non registra informazioni sufficienti per consentire l'inverso della modifica.

Inoltre, più modifiche allo stesso file possono comportare l'aggiunta di un solo flag motivo al record corrente. Se lo stesso tipo di modifica si verifica più di una volta, il file system NTFS non scrive un nuovo record per le modifiche dopo il primo. Ad esempio, diverse operazioni di scrittura senza operazioni di chiusura e riapertura che interviene comportano un solo record di modifica con il flag di motivo USN \_ REASON \_ DATA OVERWRITE \_ impostato.

Per illustrare il funzionamento del journal delle modifiche, si supponga che un utente accedono a un file nell'ordine seguente:

1.  Scrive nel file.
2.  Imposta il timestamp per il file.
3.  Scrive nel file.
4.  Tronca il file.
5.  Scrive nel file.
6.  Chiude il file.

In questo caso, il file system NTFS accetta le azioni seguenti nel journal delle modifiche (dove indica \| un'operazione OR bit per bit).



| Evento                                 | Azione file system NTFS                                                                                                                                                                                                                                                    |
|---------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Operazione di scrittura iniziale<br/>    | Il file system NTFS scrive un nuovo record USN con il flag motivo USN \_ REASON \_ DATA OVERWRITE \_ impostato. Per altre informazioni sui possibili flag motivo, vedere la [**struttura USN \_ RECORD.**](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_record_v2)<br/>                                                     |
| Impostazione del timestamp del file<br/> | Il file system NTFS scrive un nuovo record USN con l'impostazione del flag USN \_ REASON \_ DATA OVERWRITE \_ \| USN REASON BASIC \_ INFO \_ \_ \_ CHANGE.<br/>                                                                                                                            |
| Seconda operazione di scrittura<br/>     | Il file system NTFS non scrive un nuovo record USN. Poiché USN \_ REASON DATA OVERWRITE è già impostato per il record \_ \_ esistente, non viene apportata alcuna modifica al record.<br/>                                                                                           |
| Troncamento del file<br/>            | Il file system NTFS scrive un nuovo record USN con l'impostazione del flag USN \_ REASON \_ DATA OVERWRITE \_ \| USN REASON BASIC \_ INFO \_ CHANGE \_ \_ \| USN REASON DATA \_ \_ \_ TRUNCATION.<br/>                                                                                           |
| Terza operazione di scrittura<br/>      | Il file system NTFS non scrive un nuovo record USN. Poiché USN \_ REASON DATA OVERWRITE è già impostato per il record \_ \_ esistente, non viene apportata alcuna modifica al record.<br/>                                                                                           |
| Operazione di chiusura<br/>            | Se l'utente che apporta modifiche è l'unico utente del file, il file system NTFS scrive un nuovo record USN con l'impostazione del flag seguente: USN \_ REASON \_ DATA OVERWRITE \_ \| USN REASON BASIC INFO \_ \_ CHANGE \_ \_ \| USN REASON \_ \_ \_ USN REASON \| \_ \_ CLOSE.<br/> |



 

Il journal delle modifiche accumula una serie di record tra la prima apertura e l'ultima chiusura di un file. A ogni record è stato impostato un nuovo flag motivo, che indica che è stata apportata una nuova modifica. La sequenza di record fornisce una cronologia parziale del file. Il record finale, creato alla chiusura del file, aggiunge il flag USN \_ REASON \_ CLOSE. Questo record rappresenta un riepilogo delle modifiche apportate al file, ma a differenza dei record precedenti, non fornisce alcuna indicazione dell'ordine delle modifiche.

L'utente successivo che accede e modifica il file genera un nuovo record USN con un singolo flag motivo.

 

 




