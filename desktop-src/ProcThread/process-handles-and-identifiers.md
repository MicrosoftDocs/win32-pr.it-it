---
description: Quando un nuovo processo viene creato dalla funzione CreateProcess, vengono restituiti gli handle del nuovo processo e del relativo thread primario.
ms.assetid: cf6b80de-de02-4222-a414-e940ffaed8fe
title: Handle e identificatori del processo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4603b3d217db0870aeb890b05c7a416f46f2309ea9a0230b33d150387ebc5173
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120031771"
---
# <a name="process-handles-and-identifiers"></a>Handle e identificatori del processo

Quando un nuovo processo viene creato dalla [**funzione CreateProcess,**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) vengono restituiti gli handle del nuovo processo e del relativo thread primario. Questi handle vengono creati con diritti di accesso completi e, soggetti al controllo di accesso di sicurezza, possono essere usati in qualsiasi funzione che accetta handle di thread o processi. Questi handle possono essere ereditati dai processi figlio, a seconda del flag di ereditarietà specificato al momento della creazione. Gli handle sono validi fino alla chiusura, anche dopo che il processo o il thread che rappresentano è stato terminato.

La [**funzione CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) restituisce anche un identificatore che identifica in modo univoco il processo in tutto il sistema. Un processo può usare la [**funzione GetCurrentProcessId**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentprocessid) per ottenere il proprio identificatore di processo (noto anche come ID processo o PID). L'identificatore è valido dal momento in cui il processo viene creato fino a quando il processo non è stato terminato. Un processo può usare la [**funzione Process32First**](/windows/win32/api/tlhelp32/nf-tlhelp32-process32first) per ottenere l'identificatore del processo padre.

Se si dispone di un identificatore di processo, è possibile ottenere l'handle del processo chiamando la [**funzione OpenProcess.**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openprocess) **OpenProcess** consente di specificare i diritti di accesso dell'handle e se può essere ereditato.

Un processo può usare la [**funzione GetCurrentProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentprocess) per recuperare uno pseudo handle per il proprio oggetto processo. Questo pseudo handle è valido solo per il processo chiamante. non può essere ereditato o duplicato per l'uso da parte di altri processi. Per ottenere l'handle reale per il processo, chiamare la [**funzione DuplicateHandle.**](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle)

 

 
