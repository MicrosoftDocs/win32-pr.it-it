---
description: Il motore di protocollo Schannel esegue l'handshake e l'autenticazione in un processo sicuro e la crittografia/messaggi in blocco al passaggio del processo dell'applicazione.
ms.assetid: bcd49aaf-b0e3-4c31-be95-986b8ad843a8
title: Superamento dei limiti del processo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 046bc6f53d609ec22ed37edd08d6967cc4ae73e6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306464"
---
# <a name="crossing-process-boundaries"></a>Superamento dei limiti del processo

Il motore di protocollo [*Schannel*](../secgloss/s-gly.md) esegue l'handshake e l'autenticazione in un [*processo*](../secgloss/p-gly.md) sicuro e la crittografia/messaggi in blocco al passaggio del processo dell'applicazione. Ciò significa che le [*chiavi di crittografia bulk*](../secgloss/b-gly.md) e le chiavi [*Mac*](../secgloss/m-gly.md) devono essere copiate da un processo a un altro. Per copiare le chiavi da un processo a un altro, usare le funzioni [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey) e [**CryptImportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptimportkey) come indicato di seguito:

1.  Il processo sicuro esporta ogni chiave in un [*OPAQUEKEYBLOB*](../secgloss/o-gly.md) usando [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey), quindi Elimina la chiave usando [**CryptDestroyKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdestroykey). Si noti che se la chiave viene archiviata in hardware, il CSP deve riconoscere questo e non deve tentare di eliminare definitivamente la chiave.
2.  Il processo protetto passa il OPAQUEKEYBLOBs al processo dell'applicazione in un modo che esula dall'ambito di questo documento.
3.  Il processo dell'applicazione importa ogni OPAQUEKEYBLOB di backup nel CSP usando [**CryptImportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptimportkey). A questo punto, la chiave deve trovarsi esattamente nello stesso [*stato*](../secgloss/s-gly.md) in cui è stata esportata.

 

 
