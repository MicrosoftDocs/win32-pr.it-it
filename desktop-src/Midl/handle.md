---
title: handle (attributo)
description: L'attributo \ handle \ specifica un oggetto definito dall'utente o \ 0034; personalizzato \ 0034; tipo di handle.
ms.assetid: db5c6ea6-6081-4cea-9265-5e2f67fd8c14
keywords:
- Gestisci attributo MIDL
topic_type:
- apiref
api_name:
- handle
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d4560de53bf3f24238e9ff96e01c74716729749
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103872517"
---
# <a name="handle-attribute"></a><span data-ttu-id="45285-104">handle (attributo)</span><span class="sxs-lookup"><span data-stu-id="45285-104">handle attribute</span></span>

<span data-ttu-id="45285-105">L' \[ attributo **handle** \] specifica un tipo di handle definito dall'utente o personalizzato.</span><span class="sxs-lookup"><span data-stu-id="45285-105">The \[**handle**\] attribute specifies a user-defined or "customized" handle type.</span></span>

``` syntax
typedef [handle] typename;  
handle_t __RPC_USER typename_bind (typename);
void __RPC_USER typename_unbind (typename, handle_t);
```

## <a name="parameters"></a><span data-ttu-id="45285-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="45285-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="45285-107">*typeName*</span><span class="sxs-lookup"><span data-stu-id="45285-107">*typename*</span></span> 
</dt> <dd>

<span data-ttu-id="45285-108">Specifica il nome del tipo di handle di binding definito dall'utente.</span><span class="sxs-lookup"><span data-stu-id="45285-108">Specifies the name of the user-defined binding-handle type.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="45285-109">Commenti</span><span class="sxs-lookup"><span data-stu-id="45285-109">Remarks</span></span>

<span data-ttu-id="45285-110">Gli handle definiti dall'utente consentono agli sviluppatori di progettare handle significativi per l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="45285-110">User-defined handles permit developers to design handles that are meaningful to the application.</span></span> <span data-ttu-id="45285-111">Un handle definito dall'utente può essere definito solo in una dichiarazione di tipo, non in un dichiaratore di funzione.</span><span class="sxs-lookup"><span data-stu-id="45285-111">A user-defined handle can only be defined in a type declaration, not in a function declarator.</span></span>

<span data-ttu-id="45285-112">Un parametro di un tipo definito dall'attributo \[ **handle** \] viene utilizzato per determinare l'associazione per la chiamata e viene trasmesso alla routine chiamata.</span><span class="sxs-lookup"><span data-stu-id="45285-112">A parameter of a type defined by the \[**handle**\] attribute is used to determine the binding for the call and is transmitted to the called procedure.</span></span>

<span data-ttu-id="45285-113">L'utente deve fornire routine di binding e di annullamento dell'associazione per eseguire la conversione tra tipi primitivi e di handle definiti dall'utente.</span><span class="sxs-lookup"><span data-stu-id="45285-113">The user must provide binding and unbinding routines to convert between primitive and user-defined handle types.</span></span> <span data-ttu-id="45285-114">Dato un handle definito dall'utente di tipo *typeName*, l'utente deve fornire le routine *typeName* \_ **Bind** e *typeName* \_ **UNBIND**.</span><span class="sxs-lookup"><span data-stu-id="45285-114">Given a user-defined handle of type *typename*, the user must supply the routines *typename*\_**bind** and *typename*\_**unbind**.</span></span> <span data-ttu-id="45285-115">Se, ad esempio, il tipo di handle definito dall'utente è denominato HANDLE, le routine sono denominate HANDLE \_ **Bind** e handler \_ **UNBIND**.</span><span class="sxs-lookup"><span data-stu-id="45285-115">For example, if the user-defined handle type is named MYHANDLE, the routines are named MYHANDLE\_**bind** and MYHANDLE\_**unbind**.</span></span>

<span data-ttu-id="45285-116">In caso di esito positivo, la  \_ routine **Bind** typeName deve restituire un handle di associazione primitivo valido.</span><span class="sxs-lookup"><span data-stu-id="45285-116">If successful, the *typename*\_**bind** routine should return a valid primitive binding handle.</span></span> <span data-ttu-id="45285-117">Se ha esito negativo, la routine deve restituire un **valore null**.</span><span class="sxs-lookup"><span data-stu-id="45285-117">If unsuccessful, the routine should return a **NULL**.</span></span> <span data-ttu-id="45285-118">Se la routine restituisce **null**, la routine *typeName* \_ **UNBIND** non verrà chiamata.</span><span class="sxs-lookup"><span data-stu-id="45285-118">If the routine returns **NULL**, the *typename*\_**unbind** routine will not be called.</span></span> <span data-ttu-id="45285-119">Se la routine di associazione restituisce un handle di binding non valido diverso da **null**, il comportamento dello stub non è definito.</span><span class="sxs-lookup"><span data-stu-id="45285-119">If the binding routine returns an invalid binding handle different from **NULL**, the stub behavior is undefined.</span></span>

<span data-ttu-id="45285-120">Quando la procedura remota dispone di un handle definito dall'utente come parametro o come handle implicito, gli stub client chiamano la routine di associazione prima di chiamare la procedura remota.</span><span class="sxs-lookup"><span data-stu-id="45285-120">When the remote procedure has a user-defined handle as a parameter or as an implicit handle, the client stubs call the binding routine before calling the remote procedure.</span></span> <span data-ttu-id="45285-121">Gli stub client chiamano la routine unbinding dopo la chiamata remota.</span><span class="sxs-lookup"><span data-stu-id="45285-121">The client stubs call the unbinding routine after the remote call.</span></span>

<span data-ttu-id="45285-122">In DCE IDL, un parametro con l' \[ attributo **handle** \] deve apparire come primo parametro nell'elenco di argomenti della procedura remota.</span><span class="sxs-lookup"><span data-stu-id="45285-122">In DCE IDL, a parameter with the \[**handle**\] attribute must appear as the first parameter in the remote procedure argument list.</span></span> <span data-ttu-id="45285-123">I parametri successivi, inclusi altri attributi dell' \[ **handle** \] , vengono trattati come parametri normali.</span><span class="sxs-lookup"><span data-stu-id="45285-123">Subsequent parameters, including other \[**handle**\] attributes, are treated as ordinary parameters.</span></span> <span data-ttu-id="45285-124">Microsoft supporta un'estensione di DCE IDL che consente la visualizzazione del parametro dell'handle definito dall'utente \[  \] in posizioni diverse dal primo parametro.</span><span class="sxs-lookup"><span data-stu-id="45285-124">Microsoft supports an extension to DCE IDL that allows the user-defined \[**handle**\] parameter to appear in positions other than the first parameter.</span></span>

## <a name="examples"></a><span data-ttu-id="45285-125">Esempi</span><span class="sxs-lookup"><span data-stu-id="45285-125">Examples</span></span>

``` syntax
typedef [handle] struct 
{ 
    char machine[8]; 
    char nmpipe[256]; 
} h_service; 
 
handle_t __RPC_USER h_service_bind(h_service); 
void __RPC_USER h_service_unbind(h_service, handle_t);
```

## <a name="see-also"></a><span data-ttu-id="45285-126">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="45285-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="45285-127">Binding e handle</span><span class="sxs-lookup"><span data-stu-id="45285-127">Binding and Handles</span></span>](/windows/desktop/Rpc/binding-and-handles)
</dt> <dt>

[<span data-ttu-id="45285-128">File di definizione dell'interfaccia (IDL)</span><span class="sxs-lookup"><span data-stu-id="45285-128">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="45285-129">**handle implicito \_**</span><span class="sxs-lookup"><span data-stu-id="45285-129">**implicit\_handle**</span></span>](implicit-handle.md)
</dt> <dt>

[<span data-ttu-id="45285-130">**typedef**</span><span class="sxs-lookup"><span data-stu-id="45285-130">**typedef**</span></span>](typedef.md)
</dt> </dl>

 

 