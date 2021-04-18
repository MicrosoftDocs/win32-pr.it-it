---
description: Le applicazioni possono chiamare la funzione AuthzGetInformationFromContext per eseguire query sulle informazioni relative a un contesto client esistente.
ms.assetid: 32655e54-499e-439e-8d4f-f2b4eaa0b184
title: Esecuzione di query su un contesto client
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 101c35466e675d9ecba942089bbe7b5e82cffd90
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308145"
---
# <a name="querying-a-client-context"></a>Esecuzione di query su un contesto client

Le applicazioni possono chiamare la funzione [**AuthzGetInformationFromContext**](/windows/desktop/api/Authz/nf-authz-authzgetinformationfromcontext) per eseguire query sulle informazioni relative a un contesto client esistente.

Il parametro *InfoClass* della funzione [**AuthzGetInformationFromContext**](/windows/desktop/api/Authz/nf-authz-authzgetinformationfromcontext) accetta un valore dall'enumerazione della [**\_ \_ \_ classe di informazioni sul contesto AUTHZ**](/windows/desktop/api/Authz/ne-authz-authz_context_information_class) che specifica il tipo di informazioni che la funzione esegue query.

Le variabili degli attributi di sicurezza devono essere presenti nel contesto client se si fa riferimento a in un'espressione condizionale. in caso contrario, il termine dell'espressione condizionale che vi fa riferimento verrà valutato come sconosciuto. Per altre informazioni sulle espressioni condizionali, vedere il [linguaggio di definizione del descrittore di sicurezza per le voci ACE condizionali](security-descriptor-definition-language-for-conditional-aces-.md) .

## <a name="example"></a>Esempio

Nell'esempio seguente viene eseguita una query sul contesto client creato nell'esempio dall' [inizializzazione di un contesto client](initializing-a-client-context.md) per recuperare l'elenco dei [**SID**](/windows/desktop/api/Winnt/ns-winnt-sid) dei gruppi associati a tale contesto client.


```C++
BOOL GetGroupsFromContext(AUTHZ_CLIENT_CONTEXT_HANDLE hClientContext)
{

    DWORD                cbSize = 0;
    PTOKEN_GROUPS        pTokenGroups=NULL;
    LPTSTR                StringSid = NULL;
    BOOL                bResult = FALSE;
    int i = 0;

    //Call the AuthzGetInformationFromContext function with a NULL output buffer to get the required buffer size.
    AuthzGetInformationFromContext(hClientContext, AuthzContextInfoGroupsSids, 0, &cbSize, NULL);
    
        
    

    //Allocate the buffer for the TOKEN_GROUPS structure.
    pTokenGroups = (PTOKEN_GROUPS)malloc(cbSize);
    if (!pTokenGroups)
        return FALSE;

    //Get the SIDs of groups associated with the client context. 
    if(!AuthzGetInformationFromContext(hClientContext, AuthzContextInfoGroupsSids, cbSize, &cbSize, pTokenGroups))
    {    
        printf_s("AuthzGetInformationFromContext failed with %d\n", GetLastError);
        free(pTokenGroups);
        return FALSE;
    }

    //Enumerate and display the group SIDs.
    for (i=pTokenGroups->GroupCount-1; i >= 0; --i)
    {
        //Convert a SID to a string.
        if(!ConvertSidToStringSid(
            pTokenGroups->Groups[i].Sid,
            &StringSid
            ))
        {
            LocalFree(StringSid);
            return FALSE;
        }


        wprintf_s(L"%s \n", StringSid);
        
    }

    free(pTokenGroups);

    return TRUE;
}
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Aggiunta di SID a un contesto client](adding-sids-to-a-client-context.md)
</dt> <dt>

[Memorizzazione nella cache di controlli di accesso](caching-access-checks.md)
</dt> <dt>

[Verifica dell'accesso con l'API Authz](checking-access-with-authz-api.md)
</dt> <dt>

[Funzionamento di AccessCheck](how-dacls-control-access-to-an-object.md)
</dt> <dt>

[Inizializzazione di un contesto client](initializing-a-client-context.md)
</dt> <dt>

[Linguaggio di definizione del descrittore di sicurezza per le voci](security-descriptor-definition-language-for-conditional-aces-.md)
</dt> </dl>

 

 



