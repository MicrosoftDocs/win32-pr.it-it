---
description: Un'applicazione può aggiungere identificatori di sicurezza (SID) a un contesto client esistente chiamando la funzione AuthzAddSidsToContext.
ms.assetid: d49ce47b-e91a-452b-b423-07e8d282d28a
title: Aggiunta di SID a un contesto client
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a601f485110ddacea0fdb54cb7dcef587a25cb9a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104529730"
---
# <a name="adding-sids-to-a-client-context"></a>Aggiunta di SID a un contesto client

Un'applicazione può aggiungere [*identificatori di sicurezza*](/windows/desktop/SecGloss/s-gly) (SID) a un contesto client esistente chiamando la funzione [**AuthzAddSidsToContext**](/windows/desktop/api/Authz/nf-authz-authzaddsidstocontext) . La funzione [**AuthzAddSidsToContext**](/windows/desktop/api/Authz/nf-authz-authzaddsidstocontext) consente a un'applicazione di specificare sia un elenco di SID che un elenco di SID di restrizione al contesto client specificato.

Il sistema utilizza l'elenco dei SID di restrizione quando controlla l'accesso del token a un oggetto a protezione diretta. Quando un processo o un thread con restrizioni tenta di accedere a un oggetto a protezione diretta, il sistema esegue due controlli di accesso: uno usando i SID abilitati del token e un altro usando l'elenco dei SID di restrizione. L'accesso viene concesso solo se entrambi i controlli di accesso consentono i diritti di accesso richiesti.

Le variabili di attributo devono essere sotto forma di espressione se utilizzate con operatori logici; in caso contrario, vengono valutati come sconosciuti.

## <a name="example"></a>Esempio

Nell'esempio seguente vengono aggiunti un SID e un SID restrittivo al contesto client creato dall'esempio nell' [inizializzazione di un contesto client](initializing-a-client-context.md).


```C++
BOOL AddSidsToContext(AUTHZ_CLIENT_CONTEXT_HANDLE *phClientContext)
{
    AUTHZ_CLIENT_CONTEXT_HANDLE        NewContext = NULL;
    PSID                            pEveryoneSid = NULL;
    PSID                            pLocalSid = NULL;
    SID_AND_ATTRIBUTES                Sids;
    SID_AND_ATTRIBUTES                RestrictedSids;
    DWORD                            SidCount = 0;
    DWORD                            RestrictedSidCount = 0;

    //Create a PSID from the "Everyone" well-known SID.
    if(!ConvertStringSidToSid(L"S-1-1-0", &pEveryoneSid))
    {
        printf_s("ConvertStringSidToSid failed with %d\n", GetLastError());
        return FALSE;
    }

    //Create a PSID from the "Local" well-known SID.
    if(!ConvertStringSidToSid(L"S-1-2-0", &pLocalSid))
    {
        printf_s("ConvertStringSidToSid failed with %d\n", GetLastError);
        return FALSE;
    }

    //Set the members of the SID_AND_ATTRIBUTES structure to be added.
    Sids.Sid = pEveryoneSid;
    Sids.Attributes = SE_GROUP_ENABLED;

    //Set the members of the SID_AND_ATTRIBUTES structure for the restricting SID.
    RestrictedSids.Sid = pLocalSid;
    RestrictedSids.Attributes = SE_GROUP_ENABLED;

    

    //Create a new context with the new "Everyone" SID and "Local" restricting SID.
    if(!AuthzAddSidsToContext(
        *phClientContext,
        &Sids,
        1,
        &RestrictedSids,
        1,
        &NewContext))
    {
        printf_s("AuthzAddSidsToContext failed with %d\n", GetLastError());
        if(pEveryoneSid)
        {
            FreeSid(pEveryoneSid);
        }
        if(pLocalSid)
        {
            FreeSid(pLocalSid);
        }
        return FALSE;
    }

    if(pEveryoneSid)
        {
            FreeSid(pEveryoneSid);
        }
        if(pLocalSid)
        {
            FreeSid(pLocalSid);
        }
        
        AuthzFreeContext(*phClientContext);
        *phClientContext = NewContext;

    return TRUE;

}
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Memorizzazione nella cache di controlli di accesso](caching-access-checks.md)
</dt> <dt>

[Verifica dell'accesso con l'API Authz](checking-access-with-authz-api.md)
</dt> <dt>

[Inizializzazione di un contesto client](initializing-a-client-context.md)
</dt> <dt>

[Esecuzione di query su un contesto client](querying-a-client-context.md)
</dt> </dl>

 

 
