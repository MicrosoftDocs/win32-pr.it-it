---
title: Coerenza del trasferimento di file
description: BITS garantisce che la versione del file da trasferire sia coerente in base alla dimensione del file e al timestamp, non al contenuto (i bit non proteggono dagli attacchi man-in-the-Middle).
ms.assetid: ba82f172-a3ac-49d6-bccd-7d0b68ba66de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 533bc0c0db9708528d4ae919572d6e4c1d251ac8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855477"
---
# <a name="file-transfer-consistency"></a>Coerenza del trasferimento di file

BITS garantisce che la versione del file da trasferire sia coerente in base alla dimensione del file e al timestamp, non al contenuto (i bit non proteggono dagli attacchi man-in-the-Middle). Per verificare il contenuto, è possibile usare il metodo [**IBackgroundCopyFile3:: Gettemporaryname**](/windows/desktop/api/Bits3_0/nf-bits3_0-ibackgroundcopyfile3-gettemporaryname) per ottenere il nome del file che contiene il contenuto scaricato, verificare il contenuto usando un meccanismo personalizzato, quindi chiamare il metodo [**IBackgroundCopyFile3:: SetValidationState**](/windows/desktop/api/Bits3_0/nf-bits3_0-ibackgroundcopyfile3-setvalidationstate) per indicare a BITS se il contenuto del file è valido. Se si imposta lo stato di convalida su **false** e il contenuto proviene dal server di origine, il processo passa allo stato di errore. Se il contenuto proviene da un peer, BITS scarica il file dal server di origine.

Per i download, se le dimensioni del file o l'indicatore di data e ora cambiano mentre BITS sta trasferendo il file, BITS riavvia solo il trasferimento del file. Se, ad esempio, il processo di download contiene due file e i file vengono aggiornati nel server mentre BITS trasferisce il secondo file, BITS riavvia il trasferimento solo del secondo file. Il primo file, che è già stato trasferito correttamente, non viene aggiornato in modo da riflettere le nuove modifiche.

Si noti che se il file viene scaricato dal server, è necessario creare un nuovo URL per ogni nuova versione del file. Se si utilizza lo stesso URL per le nuove versioni del file, alcuni server proxy possono fornire dati non aggiornati dalla propria cache perché non vengono verificati con il server originale se il file non è aggiornato.

Per i caricamenti, se le dimensioni del file o l'indicatore di data e ora cambiano durante il trasferimento di file, BITS genera un errore e il processo viene inserito nello \_ \_ stato di errore dello stato del processo BG \_ .

BITS non sincronizza le richieste di trasferimento quando uno o più utenti richiedono che lo stesso file venga trasferito nello stesso percorso. BITS trasferisce il file per ogni richiesta separatamente.

 

 




