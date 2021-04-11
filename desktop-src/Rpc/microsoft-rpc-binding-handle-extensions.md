---
title: Microsoft RPC Binding-Handle Extensions
description: Le estensioni Microsoft per il linguaggio IDL supportano più parametri di handle che vengono visualizzati in posizioni diverse dal primo parametro, più a sinistra.
ms.assetid: 084b0d8e-0c8a-43b9-b3ae-4f69cab3a2c2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a947c10465cb24012be9c3f845fbd874f9de0567
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/08/2020
ms.locfileid: "104047507"
---
# <a name="microsoft-rpc-binding-handle-extensions"></a>Microsoft RPC Binding-Handle Extensions

Le estensioni Microsoft per il linguaggio IDL supportano più parametri di handle che vengono visualizzati in posizioni diverse dal primo parametro, più a sinistra. I passaggi seguenti descrivono la sequenza che il compilatore MIDL passa per risolvere il parametro binding-handle in modalità di compatibilità DCE (/**OSF**) e in modalità predefinita (Microsoft-Extended).

## <a name="dce-compatibility-mode"></a>Modalità di compatibilità DCE

-   Handle di associazione visualizzato nella prima posizione.
-   Più \[ [**a sinistra in**](/windows/desktop/Midl/in), parametro dell' [**\_ handle del contesto**](/windows/desktop/Midl/context-handle) \] .
-   Handle di associazione implicito specificato dall' \[ [**\_ handle implicito**](/windows/desktop/Midl/implicit-handle) \] o dall' \[ [**\_ handle automatico**](/windows/desktop/Midl/auto-handle) \] .
-   Se non è presente alcun ACF, per impostazione predefinita viene utilizzato l' \[ **\_ handle automatico** \] .

## <a name="default-mode"></a>Modalità predefinita

-   Handle di binding esplicito più a sinistra.
-   Handle di associazione implicito specificato dall' \[ [**\_ handle implicito**](/windows/desktop/Midl/implicit-handle) \] o dall' \[ [**\_ handle automatico**](/windows/desktop/Midl/auto-handle) \] .
-   Se non è presente alcun ACF, per impostazione predefinita viene utilizzato l' \[ [**\_ handle automatico**](/windows/desktop/Midl/auto-handle) \] .

I compilatori IDL DCE cercano un handle di binding esplicito come primo parametro. Quando il primo parametro non è un handle di binding e vengono specificati uno o più handle di contesto, viene utilizzato l'handle del contesto più a sinistra come handle di associazione. Quando il primo parametro non è un handle e non sono presenti handle di contesto, la procedura usa l'associazione implicita usando l'handle \[ [**implicito \_**](/windows/desktop/Midl/implicit-handle) dell'attributo ACF \] o l' \[ [**\_ handle automatico**](/windows/desktop/Midl/auto-handle) \] .

Le estensioni Microsoft per IDL consentono all'handle di associazione di trovarsi in una posizione diversa dal primo parametro. Il punto di controllo più \[ [**a sinistra nel parametro di**](/windows/desktop/Midl/in) \] handle esplicito, che si tratti di un handle primitivo, definito dal programmatore o di contesto, è l'handle di associazione. Quando non sono presenti parametri di handle, la procedura usa l'associazione implicita usando l'handle \[ [**implicito \_**](/windows/desktop/Midl/implicit-handle) dell'attributo ACF \] o l' \[ [**\_ handle automatico**](/windows/desktop/Midl/auto-handle) \] .

Le regole seguenti si applicano sia alla modalità di compatibilità DCE (/OSF) che alla modalità predefinita:

-   Quando non è presente alcun ACF, viene usata l'associazione di handle automatico.
-   Esplicito \[ [**in**](/windows/desktop/Midl/in) \] o \[ **in**, gli handle [**out**](/windows/desktop/Midl/out-idl) \] per una singola funzione hanno la precedenza su qualsiasi associazione implicita specificata per l'interfaccia.
-   Più \[ [**in**](/windows/desktop/Midl/in) \] o \[ **in**, gli \] handle primitivi non sono supportati.
-   Più \[ [**in**](/windows/desktop/Midl/in) \] o \[ **in**, \] sono consentiti gli handle del contesto espliciti.
-   Tutti i parametri di handle definiti dal programmatore, ad eccezione del parametro binding-handle, vengono trattati come dati trasmissibili.

La tabella seguente contiene esempi e descrive come vengono assegnati gli handle di associazione in ogni modalità del compilatore.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Esempio</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre class="syntax" data-space="preserve"><code>void proc1( void );</code></pre></td>
<td>Nessun handle esplicito specificato. Viene utilizzato l'handle di associazione implicito, specificato da [ <a href="/windows/desktop/Midl/implicit-handle">implicit_handle</a>] o [ <a href="/windows/desktop/Midl/auto-handle">auto_handle</a>]. Quando non è presente alcun ACF, viene usato un handle automatico.</td>
</tr>
<tr class="even">
<td><pre class="syntax" data-space="preserve"><code>void proc2([in] handle_t H,
           [in] short s );</code></pre></td>
<td>Viene specificato un handle esplicito di tipo handle_t. Il parametro <em>H</em> è l'handle di associazione per la procedura.</td>
</tr>
<tr class="odd">
<td><pre class="syntax" data-space="preserve"><code>void proc3([in] short s,
           [in] handle_t H );</code></pre></td>
<td>Il primo parametro non è un handle. In modalità predefinita, il parametro dell'handle più a sinistra, <em>H</em>, è l'handle di associazione. In modalità/OSF viene utilizzata l'associazione implicita. Viene restituito un errore perché si prevede che il secondo parametro sia trasmissibile e non handle_t possibile trasmettere.</td>
</tr>
<tr class="even">
<td><pre class="syntax" data-space="preserve"><code>typedef [handle] short * MY_HDL;

void proc1([in] short s,
           [in] MY_HDL H );</code></pre></td>
<td>Il primo parametro non è un handle. In modalità predefinita, il parametro dell'handle più a sinistra, <em>H</em>, è l'handle di associazione. Gli stub chiamano le routine fornite dall'utente MY_HDL_bind e MY_HDL_unbind. In modalità/OSF, viene utilizzata l'associazione implicita. Il parametro <em>H</em> dell'handle definito dal programmatore viene considerato come dati trasmissibili.</td>
</tr>
<tr class="odd">
<td><pre class="syntax" data-space="preserve"><code>Typedef [handle] short * MY_HDL;

void proc1([in] MY_HDL H, 
           [in] MY_HDL p );</code></pre></td>
<td>Il primo parametro è un handle di associazione. Il parametro <em>H</em> è il parametro dell'handle di binding. Il secondo parametro dell'handle definito dal programmatore viene considerato come dati trasmissibili.</td>
</tr>
<tr class="even">
<td><pre class="syntax" data-space="preserve"><code>Typedef [context_handle] 
void * CTXT_HDL;

void proc1([in] short s,
           [in] long l,
           [in] CTXT_HDL H ,
           [in] char c);</code></pre></td>
<td>L'handle di associazione è un handle di contesto. Il parametro <em>H</em> è l'handle di associazione.</td>
</tr>
</tbody>
</table>



 

 

 