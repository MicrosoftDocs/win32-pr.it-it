---
description: Crypt32.dll è il modulo che implementa molte delle funzioni CryptoAPI.
ms.assetid: b6063c92-5831-4b78-b2cd-812e55194bc9
title: Crypt32.dll versioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88fed9fb7e31af86673c4d24a9dd828c8d690441986725026f982c0720753c7e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119876471"
---
# <a name="crypt32dll-versions"></a>Crypt32.dll versioni

Crypt32.dll è il modulo che implementa molte delle funzioni di certificato e di messaggistica crittografica in CryptoAPI, ad [**esempio CryptSignMessage.**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsignmessage) Crypt32.dll è un modulo fornito con i sistemi operativi Windows e Windows Server, ma versioni diverse di questa DLL offrono funzionalità diverse. Non è disponibile alcuna API per determinare la versione di CryptoAPI in uso, ma è possibile determinare la versione di Crypt32.dll attualmente in uso usando le funzioni [**GetFileVersionInfo**](/windows/win32/api/winver/nf-winver-getfileversioninfoa) e [**VerQueryValue.**](/windows/win32/api/winver/nf-winver-verqueryvaluea)

In generale, gli intervalli di Crypt32.dll mapping alle versioni del sistema operativo, come illustrato nella tabella seguente. Tuttavia, questa tabella deve essere usata come linea guida solo perché è possibile, tramite altri percorsi di aggiornamento, che la versione di Crypt32.dll sia diversa da quella indicata nella tabella.

| Crypt32.dll versione                               | Sistema operativo                                                                                                                                                                |
|---------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *versione* >= 5.131.3790.0                      | Windows Server 2003                                                                                                                                                             |
| *versione* >= 5.131.2600.1243                   | Windows XP con Service Pack 2 (SP2)Windows XP con Service Pack 1 (SP1) con hotfix [Q329433](https://support.microsoft.com/kb/329433)<br/> Windows XP<br/> |
| 5.131.2600.0 <*=* versione < 5.131.2600.1243 | Windows XP con SP1Windows XP<br/>                                                                                                                                        |



 

 

 
