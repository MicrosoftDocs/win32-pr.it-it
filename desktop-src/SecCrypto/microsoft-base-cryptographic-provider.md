---
description: Il provider del servizio di crittografia di base Microsoft è il provider del provider del servizio di crittografia (CSP) iniziale ed è distribuito con le versioni CryptoAPI 1,0 e 2,0. Si tratta di un provider di uso generico che supporta le firme digitali e la crittografia dei dati.
ms.assetid: c36025c5-a407-4a05-8780-23f8107730df
title: Provider di crittografia di base Microsoft
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dfc48060305337dd878dedcadca8cfed52bd2f34
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307677"
---
# <a name="microsoft-base-cryptographic-provider"></a>Provider di crittografia di base Microsoft

Il provider del servizio di crittografia di base Microsoft è il provider del [*provider del servizio di crittografia*](../secgloss/c-gly.md) (CSP) iniziale ed è distribuito con le versioni [*CryptoAPI*](../secgloss/c-gly.md) 1,0 e 2,0. Si tratta di un provider di uso generico che supporta le [*firme digitali*](../secgloss/d-gly.md) e la crittografia dei dati.

L'algoritmo di chiave pubblica RSA viene utilizzato per tutte le operazioni con chiave pubblica.

Per mantenere la compatibilità con le versioni precedenti, la nuova versione del provider mantiene la designazione della versione 1,0 del nome in WinCrypt. h. Tuttavia, la versione 2,0 di questo provider è attualmente in fase di spedizione. Per determinare la versione effettiva del provider in uso, chiamare [**CryptGetProvParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetprovparam) con l'argomento *DwParam* impostato su **PP \_ Version**. Se 0x0200 viene restituito in *pbData*, si avrà la versione 2,0.

|                |                     |
|----------------|---------------------|
| Tipo di provider: | **PROV \_ RSA \_ completo** |
| Nome provider: | **MS \_ def \_ prova**   |



 

 

 
