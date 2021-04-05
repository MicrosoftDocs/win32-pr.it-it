---
description: Crypt32.dll è il modulo che implementa molte delle funzioni CryptoAPI.
ms.assetid: b6063c92-5831-4b78-b2cd-812e55194bc9
title: Versioni Crypt32.dll
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d71b55d78b3ff3654e4bf3e5956917dd8de20eec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750922"
---
# <a name="crypt32dll-versions"></a>Versioni Crypt32.dll

Crypt32.dll è il modulo che implementa molte delle funzioni di messaggistica crittografica e di certificato in CryptoAPI, ad esempio [**CryptSignMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsignmessage). Crypt32.dll è un modulo fornito con i sistemi operativi Windows e Windows Server, ma versioni diverse di questa DLL offrono funzionalità diverse. Non è disponibile alcuna API per determinare la versione di CryptoAPI in uso, ma è possibile determinare la versione di Crypt32.dll attualmente in uso usando le funzioni [**GetFileVersionInfo**](/windows/win32/api/winver/nf-winver-getfileversioninfoa) e [**VerQueryValue**](/windows/win32/api/winver/nf-winver-verqueryvaluea) .

In generale, gli intervalli di versione di Crypt32.dll mappato alle versioni del sistema operativo, come illustrato nella tabella seguente. Questa tabella, tuttavia, deve essere utilizzata come riferimento solo perché è possibile, attraverso altre vie di aggiornamento, che la versione del Crypt32.dll sia diversa da quella indicata nella tabella.

| Versione Crypt32.dll                               | Sistema operativo                                                                                                                                                                |
|---------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *versione* >= 5.131.3790.0                      | Windows Server 2003                                                                                                                                                             |
| *versione* >= 5.131.2600.1243                   | Windows XP con Service Pack 2 (SP2) Windows XP con Service Pack 1 (SP1) con hotfix [Q329433](https://support.microsoft.com/kb/329433)<br/> Windows XP<br/> |
| 5.131.2600.0 <= *versione* < 5.131.2600.1243 | Windows XP con SP1Windows XP<br/>                                                                                                                                        |



 

 

 
