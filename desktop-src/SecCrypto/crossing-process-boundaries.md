---
description: Il motore del protocollo Schannel esegue l'handshaking e l'autenticazione in un processo sicuro e la crittografia/messaggio bulk che passa nel processo dell'applicazione.
ms.assetid: bcd49aaf-b0e3-4c31-be95-986b8ad843a8
title: Attraversamento dei limiti del processo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0f8ba4c2d7a0a80ad97e62487421b5b4a0a6f8deda9d8edb550c2d8fcddab15
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117768876"
---
# <a name="crossing-process-boundaries"></a>Attraversamento dei limiti del processo

Il [*motore del protocollo Schannel*](../secgloss/s-gly.md) esegue l'handshaking e l'autenticazione in un processo sicuro e la crittografia/messaggio bulk che passa il processo dell'applicazione. [](../secgloss/p-gly.md) Ciò significa che le chiavi [*di crittografia bulk e*](../secgloss/b-gly.md) le chiavi [*MAC*](../secgloss/m-gly.md) devono essere copiate da un processo a un altro. Per copiare le chiavi da un processo a un altro, usare le funzioni [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey) e [**CryptImportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptimportkey) come indicato di seguito:

1.  Il processo protetto esporta ogni chiave in [*un oggetto OPAQUEKEYBLOB*](../secgloss/o-gly.md) usando [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey), quindi elimina la chiave [**usando CryptDestroyKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdestroykey). Si noti che se la chiave è archiviata nell'hardware, il provider di servizi di configurazione deve riconoscerlo e non deve tentare di eliminare la chiave.
2.  Il processo protetto passa gli OPAQUEKEYBLOB al processo dell'applicazione in modo che esepersi dall'ambito di questo documento.
3.  Il processo dell'applicazione importa ogni OPAQUEKEYBLOB nel provider di servizi di crittografia [**usando CryptImportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptimportkey). A questo punto, la chiave deve essere esattamente [*nello*](../secgloss/s-gly.md) stesso stato di quando è stata esportata.

 

 
