---
title: Coerenza del trasferimento di file
description: BITS garantisce che la versione del file che trasferisce sia coerente in base alle dimensioni del file e al timestamp, non al contenuto (BITS non protegge dagli attacchi man-in-the-middle).
ms.assetid: ba82f172-a3ac-49d6-bccd-7d0b68ba66de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 608566f6e9927fdcb39133c30720a46ead869f36d3084c950b9ed86379c4b749
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118959500"
---
# <a name="file-transfer-consistency"></a>Coerenza del trasferimento di file

BITS garantisce che la versione del file che trasferisce sia coerente in base alle dimensioni del file e al timestamp, non al contenuto (BITS non protegge dagli attacchi man-in-the-middle). Per verificare manualmente il contenuto, è possibile usare il metodo [**IBackgroundCopyFile3::GetTemporaryName**](/windows/desktop/api/Bits3_0/nf-bits3_0-ibackgroundcopyfile3-gettemporaryname) per ottenere il nome del file che contiene il contenuto scaricato, verificare il contenuto usando il proprio meccanismo e quindi chiamare il metodo [**IBackgroundCopyFile3::SetValidationState**](/windows/desktop/api/Bits3_0/nf-bits3_0-ibackgroundcopyfile3-setvalidationstate) per indicare a BITS se il contenuto del file è valido. Se si imposta lo stato di convalida su **FALSE** e il contenuto deriva dal server di origine, il processo passa allo stato di errore. Se il contenuto è di un peer, BITS scarica il file dal server di origine.

Per i download, se le dimensioni del file o il timestamp cambiano durante il trasferimento del file, BITS riavvia solo il trasferimento di tale file. Ad esempio, se il processo di download contiene due file e i file vengono aggiornati nel server mentre BITS trasferisce il secondo file, BITS riavvia solo il trasferimento del secondo file. Il primo file, che è già stato trasferito correttamente, non viene aggiornato per riflettere le nuove modifiche.

Si noti che se si è proprietari del file scaricato dal server, è necessario creare un nuovo URL per ogni nuova versione del file. Se si usa lo stesso URL per le nuove versioni del file, alcuni server proxy potrebbero gestire dati non obsoleti dalla cache perché non verificano con il server originale se il file non è obsoleto.

Per i caricamenti, se le dimensioni del file o il timestamp cambiano durante il trasferimento del file, BITS genera un errore e il processo viene inserito nello stato BG \_ JOB \_ STATE \_ ERROR.

BITS non sincronizza le richieste di trasferimento quando uno o più utenti richiedono il trasferimento dello stesso file nello stesso percorso. BITS trasferisce il file per ogni richiesta separatamente.

 

 




