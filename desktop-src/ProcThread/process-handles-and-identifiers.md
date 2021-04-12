---
description: Quando un nuovo processo viene creato dalla funzione CreateProcess, vengono restituiti gli handle del nuovo processo e del relativo thread primario.
ms.assetid: cf6b80de-de02-4222-a414-e940ffaed8fe
title: Handle di processo e identificatori
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39a1ec0acb6535f8f64b9f4bd0815392d61fccbc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104345446"
---
# <a name="process-handles-and-identifiers"></a>Handle di processo e identificatori

Quando un nuovo processo viene creato dalla funzione [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) , vengono restituiti gli handle del nuovo processo e del relativo thread primario. Questi handle vengono creati con diritti di accesso completi e, in base al controllo di accesso di sicurezza, possono essere usati in qualsiasi funzione che accetti handle di thread o di processo. Questi handle possono essere ereditati dai processi figlio, a seconda del flag di ereditarietà specificato quando vengono creati. Gli handle sono validi fino alla chiusura, anche dopo la terminazione del processo o del thread che rappresentano.

La funzione [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) restituisce inoltre un identificatore che identifica in modo univoco il processo nell'intero sistema. Un processo può usare la funzione [**GetCurrentProcessId**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentprocessid) per ottenere un identificatore di processo (noto anche come ID processo o PID). L'identificatore è valido dal momento in cui il processo viene creato fino a quando il processo non è stato terminato. Un processo può utilizzare la funzione [**Process32First**](/windows/win32/api/tlhelp32/nf-tlhelp32-process32first) per ottenere l'identificatore del processo padre.

Se si dispone di un identificatore di processo, è possibile ottenere l'handle di processo chiamando la funzione [**OpenProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openprocess) . **OpenProcess** consente di specificare i diritti di accesso dell'handle e se può essere ereditato.

Un processo può utilizzare la funzione [**GetCurrentProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentprocess) per recuperare uno pseudo-handle per il proprio oggetto Process. Questo pseudo handle è valido solo per il processo chiamante. non può essere ereditato o duplicato per l'uso da altri processi. Per ottenere l'handle reale per il processo, chiamare la funzione [**DuplicateHandle**](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle) .

 

 
