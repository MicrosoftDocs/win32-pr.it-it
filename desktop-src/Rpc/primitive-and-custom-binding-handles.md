---
title: Handle di associazione primitivi e personalizzati
description: Tutti gli handle dichiarati con i tipi handle t o \_ RPC BINDING HANDLE sono handle di associazione \_ \_ primitivi.
ms.assetid: 7a948aad-02fa-421d-b32c-f5dab071bd04
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e0e1d6f7cc2ad4d11e268e0f5c83b0275fcd2677a32303820507272f550b834
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120019151"
---
# <a name="primitive-and-custom-binding-handles"></a>Handle di associazione primitivi e personalizzati

Tutti gli handle dichiarati con [i tipi handle \_ t](/windows/desktop/Midl/handle-t) o [**RPC BINDING \_ \_ HANDLE**](rpc-binding-handle.md) sono handle di associazione primitivi. È possibile estendere i tipi [handle \_ t](/windows/desktop/Midl/handle-t) o [**RPC BINDING \_ \_ HANDLE**](rpc-binding-handle.md) per includere più informazioni o informazioni diverse da quelle contenute nel tipo di handle primitivo. In questo caso, si crea un handle di associazione personalizzato.

Per creare un handle di associazione personalizzato per l'applicazione distribuita, è necessario creare un tipo di dati personalizzato e specificare l'attributo handle in una definizione di tipo nel \[ [](/windows/desktop/Midl/handle) \] file IDL. In definitiva, i file stub esempre il mapping di handle di associazione personalizzati agli handle primitivi.

Se si crea un tipo di handle di associazione personalizzato, è necessario fornire anche routine di associazione e annullamento dell'associazione utilizzate dal client stub per eseguire il mapping di un handle personalizzato a un handle primitivo. Lo stub chiama le routine bind e unbind all'inizio e alla fine di ogni chiamata di procedura remota. Le routine bind e unbind devono essere conformi ai prototipi di funzione seguenti.



| Prototipo di funzione                     | Descrizione       |
|----------------------------------------|-------------------|
| handle \_ t type \_ bind(*type*)           | Routine di associazione   |
| void type \_ unbind(*type*, *handle \_ t*) | Routine di annullamento dell'associazione |



 

L'esempio seguente illustra come è possibile definire un handle di associazione personalizzato nel file IDL:

``` syntax
/* usrdef.idl */
[
  uuid(20B309B1-015C-101A-B308-02608C4C9B53),
  version(1.0),
  pointer_default(unique)
]
interface usrdef
{
  typedef struct _DATA_TYPE 
  {
      unsigned char * pszUuid;
      unsigned char * pszProtocolSequence;
      unsigned char * pszNetworkAddress;
      unsigned char * pszEndpoint;
      unsigned char * pszOptions;
  } DATA_TYPE;
 
  typedef [handle] DATA_TYPE * DATA_HANDLE_TYPE;
  void UsrdefProc([in] DATA_HANDLE_TYPE  hBinding,
                  [in, string] unsigned char *   pszString);
 
  void Shutdown([in] DATA_HANDLE_TYPE hBinding);
}
```

Se la routine di associazione rileva un errore, deve generare un'eccezione usando la [**funzione RpcRaiseException.**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcraiseexception) Lo stub client verrà quindi pulito e l'eccezione verrà filtrata fino al blocco di eccezioni che circonda la chiamata di procedura remota sul lato client. Se la routine di associazione restituisce **semplicemente NULL,** il codice client riceve l'errore RPC \_ S INVALID \_ \_ BINDING. Anche se questo potrebbe essere accettabile in determinate situazioni, altre situazioni (ad esempio memoria insufficiente) non rispondono bene. La routine unbind deve essere progettata in modo da non avere esito negativo. La routine unbind non deve generare eccezioni.

Le routine bind e unbind definite dal programmatore vengono visualizzate nell'applicazione client. Nell'esempio seguente la routine di associazione chiama [**RpcBindingFromStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfromstringbinding) per convertire le informazioni di associazione di stringa in un handle di associazione. La routine unbind chiama [**RpcBindingFree**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfree) per liberare l'handle di associazione.

Il nome dell'handle di associazione definito dal programmatore, DATA HANDLE TYPE, viene visualizzato come \_ parte del nome delle \_ funzioni. Viene usato anche come tipo di parametro nei parametri della funzione.

``` syntax
/* The client stub calls this _bind routine at the */
/* beginning of each remote procedure call                */
 
RPC_BINDING_HANDLE __RPC_USER DATA_HANDLE_TYPE_bind(
    DATA_HANDLE_TYPE dh1)
{
    RPC_BINDING_HANDLE hBinding;
    RPC_STATUS status;
 
    unsigned char *pszStringBinding;
 
    status = RpcStringBindingCompose(
          dh1.pszUuid,
          dh1.pszProtocolSequence,
          dh1.pszNetworkAddress,
          dh1.pszEndpoint,
          dh1.pszOptions,
          &pszStringBinding);
          ...
 
    status = RpcBindingFromStringBinding(
          pszStringBinding,
          &hBinding);
          ...
 
    status = RpcStringFree(&pszStringBinding); 
    ...
 
    return(hBinding);
}
 
/* The client stub calls this _unbind routine */
/* after each remote procedure call.                            */
void __RPC_USER DATA_HANDLE_TYPE_unbind(
    DATA_HANDLE_TYPE dh1, 
    RPC_BINDING_HANDLE h1)
{
    RPC_STATUS status;
    status = RpcBindingFree(&h1); 
    ...
}
```

Entrambi gli handle di associazione impliciti ed espliciti possono essere handle primitivi o personalizzati. Ciò significa che un handle può essere:

-   Primitivo e implicito
-   Personalizzato e implicito
-   Primitivo ed esplicito
-   Personalizzato ed esplicito

 

 