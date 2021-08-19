---
description: Le applicazioni client speciali potrebbero richiamare operazioni con privilegi.
ms.assetid: e09fcadc-282f-4f07-b69c-b15bfdb07a7d
ms.tgt_platform: multiple
title: Esecuzione di operazioni con privilegi con C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e83667cd4a4cd81439392f1f58d77fb56109f79c2dd6d826c9390d62008553b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119050889"
---
# <a name="executing-privileged-operations-using-c"></a>Esecuzione di operazioni con privilegi con C++

Le applicazioni client speciali potrebbero richiamare operazioni con privilegi. Ad esempio, un'applicazione potrebbe consentire a un responsabile di riavviare un computer dell'ufficio che non risponde. Utilizzando strumentazione Windows (WMI) è possibile eseguire un'operazione con privilegi chiamando il provider WMI per l'operazione con privilegi.

Nella procedura seguente viene descritto come chiamare un provider per un'operazione con privilegi.

**Per chiamare un provider per un'operazione con privilegi**

1.  Ottenere le autorizzazioni per il processo client per eseguire l'operazione con privilegi.

    In genere, un amministratore imposta le autorizzazioni usando gli strumenti di amministrazione di sistema, prima di eseguire il processo.

2.  Ottenere l'autorizzazione per il processo del provider per abilitare l'operazione con privilegi.

    In genere, è possibile impostare le autorizzazioni del provider con una chiamata alla [**funzione AdjustTokenPrivileges.**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges)

3.  Ottenere l'autorizzazione per il processo client per abilitare l'operazione con privilegi.

    Questo passaggio è necessario solo se il provider è locale per il client. Se il client e il provider sono presenti nello stesso computer, il client deve abilitare in modo specifico l'operazione con privilegi utilizzando una delle tecniche seguenti:

    -   Se il client è proprietario del processo, può usare [**AdjustTokenPrivileges**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges) per modificare il token del processo prima di chiamare WMI. In questo caso, non è necessario codificare ulteriormente.
    -   Se il client non può accedere al token client, il client può usare la procedura seguente per creare un token di thread e [**usare AdjustTokenPrivileges**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges) su tale token.

La procedura seguente descrive come creare un token di thread e [**usare AdjustTokenPrivileges**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges) su tale token.

**Per creare un token di thread e usare AdjustTokenPrivileges su tale token**

1.  Creare una copia del token del processo chiamando [**ImpersonateSelf.**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-impersonateself)
2.  Recuperare il token del thread appena creato chiamando [**GetTokenInformation.**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-gettokeninformation)
3.  Abilitare l'operazione con privilegi con una [**chiamata a AdjustTokenPrivileges**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges) nel nuovo token.
4.  Ottenere un puntatore [**a IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices).
5.  Cloak del puntatore [**a IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) con una chiamata a [**CoSetProxyBlanket.**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket)
6.  Ripetere i passaggi da 1 a 5 per ogni chiamata a WMI.

    > [!Note]  
    > È necessario ripetere i passaggi perché COM memorizza i token nella cache in modo errato.

     

L'esempio di codice in questo argomento richiede la corretta \# compilazione dell'istruzione include seguente.


```C++
#include <wbemidl.h>
```



Nell'esempio di codice seguente viene illustrato come abilitare i privilegi in un computer locale.


```C++
// Get the privileges 
// The token has been obtained outside the scope of this code sample
// ================== 
DWORD dwLen;
bool bRes;
HANDLE hToken;

// obtain dwLen
bRes = GetTokenInformation(
  hToken, 
  TokenPrivileges, 
  NULL, 
  0,
  &dwLen
); 

BYTE* pBuffer = new BYTE[dwLen];
if(pBuffer == NULL)
{
  CloseHandle(hToken);
  return WBEM_E_OUT_OF_MEMORY;
} 

bRes = GetTokenInformation(
  hToken, 
  TokenPrivileges, 
  pBuffer,     
  dwLen,        
  &dwLen
);

if (!bRes)
{
  CloseHandle(hToken);
  delete [] pBuffer;
  return WBEM_E_ACCESS_DENIED;
} 

// Iterate through all the privileges and enable them all
// ====================================================== 
TOKEN_PRIVILEGES* pPrivs = (TOKEN_PRIVILEGES*)pBuffer;
for (DWORD i = 0; i < pPrivs->PrivilegeCount; i++)
{
  pPrivs->Privileges[i].Attributes |= SE_PRIVILEGE_ENABLED;
} 
// Store the information back in the token
// ========================================= 
bRes = AdjustTokenPrivileges(
  hToken, 
  FALSE, 
  pPrivs, 
  0, NULL, NULL
);

delete [] pBuffer;
CloseHandle(hToken); 

if (!bRes)
  return WBEM_E_ACCESS_DENIED;
else
  return WBEM_S_NO_ERROR;
```



 

 
