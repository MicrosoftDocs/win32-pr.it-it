---
description: Un'applicazione deve creare un contesto client prima di poter usare l'API Authz per eseguire verifiche di accesso o controllo.
ms.assetid: 82f207ff-cac4-4e9a-a9e6-ddb3f6c8b30a
title: Inizializzazione di un contesto client
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be229a60a12e33ab0c2bbd3e52fc533cf29ed1bf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317045"
---
# <a name="initializing-a-client-context"></a>Inizializzazione di un contesto client

Un'applicazione deve creare un contesto client prima di poter usare l'API Authz per eseguire verifiche di accesso o controllo.

Per inizializzare Resource Manager, un'applicazione deve chiamare la funzione [**AuthzInitializeResourceManager**](/windows/desktop/api/Authz/nf-authz-authzinitializeresourcemanager) . L'applicazione può quindi chiamare una delle diverse funzioni per creare un contesto client. Inoltre, se si eseguono controlli di accesso o di controllo in modalità remota, è necessario utilizzare la funzione [**AuthzInitializeRemoteResourceManager**](/windows/desktop/api/Authz/nf-authz-authzinitializeremoteresourcemanager) .

Per creare un contesto client basato su un contesto client esistente, chiamare la funzione [**AuthzInitializeContextFromAuthzContext**](/windows/desktop/api/Authz/nf-authz-authzinitializecontextfromauthzcontext) .

La funzione [**AuthzInitializeContextFromToken**](/windows/desktop/api/Authz/nf-authz-authzinitializecontextfromtoken) crea un nuovo contesto client usando le informazioni contenute in un token di accesso. La funzione [**AuthzInitializeContextFromSid**](/windows/desktop/api/Authz/nf-authz-authzinitializecontextfromsid) crea un nuovo contesto client usando il [**SID**](/windows/desktop/api/Winnt/ns-winnt-sid)specificato.

Se possibile, chiamare la funzione [**AuthzInitializeContextFromToken**](/windows/desktop/api/Authz/nf-authz-authzinitializecontextfromtoken) anziché [**AuthzInitializeContextFromSid**](/windows/desktop/api/Authz/nf-authz-authzinitializecontextfromsid). **AuthzInitializeContextFromSid** tenta di recuperare le informazioni disponibili in un token di accesso se il client ha effettivamente effettuato l'accesso. Un token di accesso effettivo fornisce ulteriori informazioni, ad esempio il tipo di accesso e le proprietà di accesso, e riflette il comportamento del pacchetto di autenticazione utilizzato per l'accesso. Il contesto client creato da **AuthzInitializeContextFromToken** utilizza un token di accesso e il contesto client risultante è più completo e accurato rispetto a un contesto client creato da **AuthzInitializeContextFromSid**.

> [!Note]  
> Le variabili degli attributi di sicurezza devono essere presenti nel contesto client se si fa riferimento a in un'espressione condizionale. in caso contrario, il termine dell'espressione condizionale che vi fa riferimento verrà valutato come sconosciuto. Per altre informazioni sulle espressioni condizionali, vedere il [linguaggio di definizione del descrittore di sicurezza per le voci ACE condizionali](security-descriptor-definition-language-for-conditional-aces-.md) .

 

## <a name="example"></a>Esempio

Nell'esempio seguente viene inizializzato il gestore di risorse Authz e viene chiamata la funzione [**AuthzInitializeContextFromToken**](/windows/desktop/api/Authz/nf-authz-authzinitializecontextfromtoken) per creare un contesto client dal token di accesso associato al processo corrente.


```C++
BOOL AuthzInitFromToken(AUTHZ_CLIENT_CONTEXT_HANDLE *phClientContext)
{

    HANDLE                            hToken = NULL;
    LUID                            Luid = {0, 0};

    
    ULONG                            uFlags = 0;


    //Initialize Resource Manager
    if(!AuthzInitializeResourceManager(
        AUTHZ_RM_FLAG_NO_AUDIT,
        NULL,
        NULL,
        NULL,
        L"My Resource Manager",
        &g_hResourceManager
        ))
    {
        printf_s("AuthzInitializeResourceManager failed with %d\n", GetLastError);
        return FALSE;
    }
    

    //Get the current token.

    if(!OpenProcessToken(GetCurrentProcess(), TOKEN_ALL_ACCESS, &hToken))
    {
        printf_s("OpenProcessToken failed with %d\n", GetLastError);
        return FALSE;
    }


    //Initialize the client context

    if(!AuthzInitializeContextFromToken(
        0,
        hToken,
        g_hResourceManager,
        NULL,
        Luid,
        NULL,
        phClientContext
        ))
    {    
        printf_s("AuthzInitializeContextFromToken failed with %d\n", GetLastError);
        return FALSE;
    }

    
    printf_s("Initialized client context. \n");
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

[Esecuzione di query su un contesto client](querying-a-client-context.md)
</dt> <dt>

[Linguaggio di definizione del descrittore di sicurezza per le voci](security-descriptor-definition-language-for-conditional-aces-.md)
</dt> <dt>

[**AuthzInitializeRemoteResourceManager**](/windows/desktop/api/Authz/nf-authz-authzinitializeremoteresourcemanager)
</dt> <dt>

[**AuthzInitializeResourceManager**](/windows/desktop/api/Authz/nf-authz-authzinitializeresourcemanager)
</dt> </dl>

 

 



