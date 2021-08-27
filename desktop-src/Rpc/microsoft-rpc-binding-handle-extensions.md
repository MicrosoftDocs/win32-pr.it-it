---
title: Estensioni Binding-Handle RPC Microsoft
description: Le estensioni Microsoft al linguaggio IDL supportano più parametri di handle visualizzati in posizioni diverse dal primo parametro più a sinistra.
ms.assetid: 084b0d8e-0c8a-43b9-b3ae-4f69cab3a2c2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c93b68b20628bf6f7f65cee026412846e0b497d
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122475367"
---
# <a name="microsoft-rpc-binding-handle-extensions"></a>Estensioni Binding-Handle RPC Microsoft

Le estensioni Microsoft al linguaggio IDL supportano più parametri di handle visualizzati in posizioni diverse dal primo parametro più a sinistra. I passaggi seguenti descrivono la sequenza passata dal compilatore MIDL per risolvere il parametro binding-handle in modalità di compatibilità DCE **(/osf)** e in modalità predefinita (estesa a Microsoft).

## <a name="dce-compatibility-mode"></a>Modalità di compatibilità DCE

-   Handle di associazione visualizzato nella prima posizione.
-   All'estrema \[ [**sinistra in**](/windows/desktop/Midl/in), [**parametro \_ dell'handle di**](/windows/desktop/Midl/context-handle) \] contesto.
-   Handle di associazione implicito specificato \[ [**\_ dall'handle implicito**](/windows/desktop/Midl/implicit-handle) \] o \[ [**dall'handle \_ automatico**](/windows/desktop/Midl/auto-handle) \] .
-   Se non è presente alcun file ACF, per impostazione predefinita viene utilizzato \[ **l'handle \_ automatico** \] .

## <a name="default-mode"></a>Modalità predefinita

-   Handle di associazione esplicito più a sinistra.
-   Handle di associazione implicito specificato \[ [**\_ dall'handle implicito**](/windows/desktop/Midl/implicit-handle) \] o \[ [**dall'handle \_ automatico**](/windows/desktop/Midl/auto-handle) \] .
-   Se non è presente alcun file ACF, per impostazione predefinita viene utilizzato \[ [**l'handle \_ automatico**](/windows/desktop/Midl/auto-handle) \] .

I compilatori IDL DCE ricercano un handle di associazione esplicito come primo parametro. Quando il primo parametro non è un handle di associazione e vengono specificati uno o più handle di contesto, come handle di associazione viene usato l'handle di contesto più a sinistra. Quando il primo parametro non è un handle e non sono presenti handle di contesto, la procedura usa l'associazione implicita usando l'handle implicito dell'attributo ACF \[ [**\_**](/windows/desktop/Midl/implicit-handle) \] o \[ [**l'handle \_ automatico**](/windows/desktop/Midl/auto-handle) \] .

Le estensioni Microsoft al linguaggio IDL consentono all'handle di associazione di essere in una posizione diversa dal primo parametro. L'handle di associazione è l'handle di associazione più a sinistra nel parametro explicit-handle, sia che si tratta di un \[ [](/windows/desktop/Midl/in) handle primitivo, definito dal programmatore o di \] contesto. Quando non sono presenti parametri handle, la routine usa l'associazione implicita usando l'handle implicito dell'attributo ACF \[ [**\_**](/windows/desktop/Midl/implicit-handle) \] o \[ [**l'handle \_ automatico**](/windows/desktop/Midl/auto-handle) \] .

Le regole seguenti si applicano sia alla modalità di compatibilità DCE (/osf) che alla modalità predefinita:

-   L'associazione a handle automatico viene usata quando non è presente alcun file ACF.
-   Gli handle out espliciti in o in per una singola funzione prescindono da qualsiasi \[ [](/windows/desktop/Midl/in) \] \[  [](/windows/desktop/Midl/out-idl) \] associazione implicita specificata per l'interfaccia.
-   Non \[ [**sono supportati**](/windows/desktop/Midl/in) più \] handle \[ primitivi out in o \] in .
-   Sono \[ [**consentiti**](/windows/desktop/Midl/in) \] più handle di contesto \[  \] espliciti in o in .
-   Tutti i parametri di handle definiti dal programmatore, ad eccezione del parametro binding-handle, vengono considerati dati trasmissibili.

La tabella seguente contiene esempi e descrive come vengono assegnati gli handle di associazione in ogni modalità del compilatore.




| Esempio | Descrizione | 
|---------|-------------|
| <pre class="syntax" data-space="preserve"><code>void proc1( void );</code></pre> | Non è stato specificato alcun handle esplicito. Viene usato l'handle di associazione implicito, specificato da [ <a href="/windows/desktop/Midl/implicit-handle">implicit_handle</a>] o [ <a href="/windows/desktop/Midl/auto-handle">auto_handle</a>]. Quando non è presente alcun file ACF, viene usato un handle automatico. | 
| <pre class="syntax" data-space="preserve"><code>void proc2([in] handle_t H,           [in] short s );</code></pre> | È specificato un handle esplicito handle_t tipo. Il parametro <em>H</em> è l'handle di associazione per la procedura. | 
| <pre class="syntax" data-space="preserve"><code>void proc3([in] short s,           [in] handle_t H );</code></pre> | Il primo parametro non è un handle. In modalità predefinita, il parametro handle più a sinistra, <em>H</em>, è l'handle di associazione. In modalità /osf viene usata l'associazione implicita. Viene segnalato un errore perché è previsto che il secondo parametro sia trasmissibile e handle_t non può essere trasmesso. | 
| <pre class="syntax" data-space="preserve"><code>typedef [handle] short * MY_HDL;void proc1([in] short s,           [in] MY_HDL H );</code></pre> | Il primo parametro non è un handle. In modalità predefinita, il parametro handle più a sinistra, <em>H</em>, è l'handle di associazione. Gli stub chiamano le routine fornite dall'utente MY_HDL_bind e MY_HDL_unbind. In modalità osf viene usata l'associazione implicita. Il parametro handle definito dal programmatore <em>H</em> viene considerato come dati trasmissibili. | 
| <pre class="syntax" data-space="preserve"><code>Typedef [handle] short * MY_HDL;void proc1([in] MY_HDL H,            [in] MY_HDL p );</code></pre> | Il primo parametro è un handle di associazione. Il parametro <em>H</em> è il parametro dell'handle di associazione. Il secondo parametro handle definito dal programmatore viene considerato come dati trasmissibili. | 
| <pre class="syntax" data-space="preserve"><code>Typedef [context_handle] void * CTXT_HDL;void proc1([in] short s,           [in] long l,           [in] CTXT_HDL H ,           [in] char c);</code></pre> | L'handle di associazione è un handle di contesto. Il parametro <em>H è</em> l'handle di associazione. | 




 

 

 
