---
description: I BLOB opachi, noti anche come OPAQUEKEYBLOBs, vengono usati per archiviare le chiavi di sessione in un formato specifico del fornitore, ad esempio Schannel.
ms.assetid: a0756c03-0c27-41ff-9b74-8af462e09675
title: Tipo di BLOB opaco
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e45cf8899d5cc63fb360a6b5e4177733de3880f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104401783"
---
# <a name="opaque-blob-type"></a>Tipo di BLOB opaco

I [*BLOB opachi*](../secgloss/o-gly.md), noti anche come OPAQUEKEYBLOBs, vengono usati per archiviare le [*chiavi di sessione*](../secgloss/s-gly.md) in un formato specifico del fornitore, ad esempio [*Schannel*](../secgloss/s-gly.md). Contengono il materiale della chiave di base e tutte le informazioni [*sullo stato*](../secgloss/s-gly.md) corrente. Sono incluse informazioni quali il [*valore salt*](../secgloss/s-gly.md), il [*vettore di inizializzazione*](../secgloss/i-gly.md)e la tabella delle chiavi. Il formato dei BLOB opachi non è pubblicato. Ogni fornitore CSP determina il proprio formato BLOB.

Poiché una chiave viene esportata in un BLOB opaco nel formato specifico di CSP, può essere importata solo nel CSP da cui è stata originariamente esportata.

Quando sono interessati due processi, ogni [*processo*](../secgloss/p-gly.md) chiama [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) in modo indipendente. Ogni processo ottiene un handle per un contenitore di chiavi. È possibile che entrambi i processi dispongano di handle per lo stesso contenitore di chiavi. Un processo crea le chiavi e le esporta in BLOB opachi, quindi passa i BLOB al secondo processo. Il secondo processo importa le chiavi dal BLOB nel relativo [*contenitore di chiavi*](../secgloss/k-gly.md).

Se un CSP hardware non supporta l'esportazione di chiavi, il BLOB potrebbe contenere solo l'indice di un registro della chiave o qualcosa di simile. In questo caso, il resto della procedura viene ignorato.

``` syntax
<secure process>
cbBlob = sizeof(rgbBlob);
CryptExportKey(
          hKey, 
          0, 
          OPAQUEKEYBLOB, 
          0, 
          rgbBlob, 
          &cbBlob);
hKey = 0;

<BLOB is transferred to other process>

<user process>
CryptImportKey(
            hProv, 
            pbBlob, 
            cbBlob, 
            0, 
            0, 
            &hKey);
```

 

 
