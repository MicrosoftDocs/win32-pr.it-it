---
description: Un'applicazione deve creare un contesto client prima di poter usare Authz API per eseguire i controlli di accesso o il controllo.
ms.assetid: 82f207ff-cac4-4e9a-a9e6-ddb3f6c8b30a
title: Inizializzazione di un contesto client
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da8a3c3191f323cf6ce35fda90f4bd75299dac67183986998cf21a80c0ee6995
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119908041"
---
# <a name="initializing-a-client-context"></a>Inizializzazione di un contesto client

Un'applicazione deve creare un contesto client prima di poter usare Authz API per eseguire i controlli di accesso o il controllo.

Un'applicazione deve chiamare la [**funzione AuthzInitializeResourceManager**](/windows/desktop/api/Authz/nf-authz-authzinitializeresourcemanager) per inizializzare il gestore di risorse. L'applicazione può quindi chiamare una delle diverse funzioni per creare un contesto client. Inoltre, se si eseguono controlli di accesso o controlli in remoto, è necessario usare la funzione [**AuthzInitializeRemoteResourceManager.**](/windows/desktop/api/Authz/nf-authz-authzinitializeremoteresourcemanager)

Per creare un contesto client basato su un contesto client esistente, chiamare la [**funzione AuthzInitializeContextFromAuthzContext.**](/windows/desktop/api/Authz/nf-authz-authzinitializecontextfromauthzcontext)

La [**funzione AuthzInitializeContextFromToken**](/windows/desktop/api/Authz/nf-authz-authzinitializecontextfromtoken) crea un nuovo contesto client usando le informazioni in un token di accesso. La [**funzione AuthzInitializeContextFromSid**](/windows/desktop/api/Authz/nf-authz-authzinitializecontextfromsid) crea un nuovo contesto client usando il [**SID specificato.**](/windows/desktop/api/Winnt/ns-winnt-sid)

Se possibile, chiamare la [**funzione AuthzInitializeContextFromToken**](/windows/desktop/api/Authz/nf-authz-authzinitializecontextfromtoken) anziché [**AuthzInitializeContextFromSid**](/windows/desktop/api/Authz/nf-authz-authzinitializecontextfromsid). **AuthzInitializeContextFromSid** tenta di recuperare le informazioni disponibili in un token di accesso a cui il client ha effettivamente eseguito l'accesso. Un token di accesso effettivo fornisce ulteriori informazioni, ad esempio il tipo di accesso e le proprietà di accesso, e riflette il comportamento del pacchetto di autenticazione utilizzato per l'accesso. Il contesto client creato da **AuthzInitializeContextFromToken** usa un token di accesso e il contesto client risultante è più completo e accurato rispetto a un contesto client creato da **AuthzInitializeContextFromSid**.

> [!Note]  
> Le variabili degli attributi di sicurezza devono essere presenti nel contesto client se si fa riferimento a in un'espressione condizionale. In caso contrario, il termine espressione condizionale che vi fa riferimento verrà valutato come sconosciuto. Per altre informazioni sulle espressioni condizionali, vedere l'argomento [Linguaggio di definizione del descrittore di](security-descriptor-definition-language-for-conditional-aces-.md) sicurezza per ACE condizionali.

 

## <a name="example"></a>Esempio

L'esempio seguente inizializza il gestore di risorse Authz e chiama la funzione [**AuthzInitializeContextFromToken**](/windows/desktop/api/Authz/nf-authz-authzinitializecontextfromtoken) per creare un contesto client dal token di accesso associato al processo corrente.


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

[Caching Controlli di accesso](caching-access-checks.md)
</dt> <dt>

[Controllo dell'accesso con Authz API](checking-access-with-authz-api.md)
</dt> <dt>

[Funzionamento di AccessCheck](how-dacls-control-access-to-an-object.md)
</dt> <dt>

[Esecuzione di query su un contesto client](querying-a-client-context.md)
</dt> <dt>

[Linguaggio di definizione del descrittore di sicurezza per ACE condizionali](security-descriptor-definition-language-for-conditional-aces-.md)
</dt> <dt>

[**AuthzInitializeRemoteResourceManager**](/windows/desktop/api/Authz/nf-authz-authzinitializeremoteresourcemanager)
</dt> <dt>

[**AuthzInitializeResourceManager**](/windows/desktop/api/Authz/nf-authz-authzinitializeresourcemanager)
</dt> </dl>

 

 



