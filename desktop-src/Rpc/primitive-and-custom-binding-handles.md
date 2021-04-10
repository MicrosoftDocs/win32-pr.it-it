---
title: Handle di binding primitivi e personalizzati
description: Tutti gli handle dichiarati con i \_ tipi handle t o \_ binding RPC \_ sono handle di associazione primitivi.
ms.assetid: 7a948aad-02fa-421d-b32c-f5dab071bd04
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d496a9a54ba0ee7b9552326f7c4dc15792a72bce
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104047245"
---
# <a name="primitive-and-custom-binding-handles"></a>Handle di binding primitivi e personalizzati

Tutti gli handle dichiarati con i tipi handle [ \_ t](/windows/desktop/Midl/handle-t) o [**\_ binding RPC \_**](rpc-binding-handle.md) sono handle di associazione primitivi. È possibile estendere i tipi handle [ \_ t](/windows/desktop/Midl/handle-t) o [**\_ binding \_ RPC**](rpc-binding-handle.md) per includere informazioni più o diverse rispetto a quelle contenute nel tipo di handle primitivo. Quando si esegue questa operazione, viene creato un handle di binding personalizzato.

Per creare un handle di binding personalizzato per l'applicazione distribuita, è necessario creare un tipo di dati personalizzato e specificare l' \[ attributo [handle](/windows/desktop/Midl/handle) in \] una definizione di tipo nel file IDL. Infine, i file stub mappano gli handle di associazione personalizzati agli handle primitivi.

Se si crea un tipo di handle di binding personalizzato, è necessario fornire anche le routine BIND e UNBIND che lo stub client usa per eseguire il mapping di un handle personalizzato a un handle primitivo. Lo stub chiama le routine BIND e UNBIND all'inizio e alla fine di ogni chiamata di procedura remota. Le routine BIND e UNBIND devono essere conformi ai prototipi di funzione seguenti.



| Prototipo di funzione                     | Descrizione       |
|----------------------------------------|-------------------|
| \_binding di tipo handle t \_ (*tipo*)           | Routine di associazione   |
| void Type \_ UNBIND (*Type*, *handle \_ t*) | Annullamento dell'associazione della routine |



 

Nell'esempio seguente viene illustrato come è possibile definire un handle di binding personalizzato nel file IDL:

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

Se la routine di binding rileva un errore, deve generare un'eccezione usando la funzione [**RpcRaiseException**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcraiseexception) . Lo stub client eseguirà quindi la pulizia e configurerà il filtro eccezioni per il blocco di eccezioni che circonda la chiamata RPC sul lato client. Se la routine BIND restituisce semplicemente **null**, il codice client ottiene l'errore di \_ binding RPC S \_ non valido \_ . Sebbene questo potrebbe essere accettabile in determinate situazioni, altre situazioni, ad esempio memoria insufficiente, non rispondono correttamente. La routine UNBIND deve essere progettata in modo da non avere esito negativo. La routine UNBIND non deve generare eccezioni.

Nell'applicazione client vengono visualizzate le routine BIND e UNBIND definite dal programmatore. Nell'esempio seguente, la routine BIND chiama [**errore in RpcBindingFromStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfromstringbinding) per convertire le informazioni di associazione di stringa in un handle di associazione. La routine UNBIND chiama [**RpcBindingFree**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfree) per liberare l'handle di associazione.

Il nome dell'handle di binding definito dal programmatore, il \_ tipo di handle di dati \_ , viene visualizzato come parte del nome delle funzioni. Viene anche usato come tipo di parametro nei parametri della funzione.

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

Gli handle di associazione impliciti ed espliciti possono essere di tipo primitivo o personalizzato. Ovvero, un handle può essere:

-   Primitive e implicite
-   Personalizzata e implicita
-   Primitive ed esplicite
-   Personalizzata ed esplicita

 

 