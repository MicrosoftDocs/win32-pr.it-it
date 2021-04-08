---
title: opzione/OSF
description: L'opzione/OSF impone una rigida compatibilità con OSF DCE.
ms.assetid: d94228fa-24af-43d7-9596-cf3a14690e0b
keywords:
- /OSF switch MIDL
topic_type:
- apiref
api_name:
- /osf
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2936401d59bb8c2c2bcfdcffce27ba9ed978d506
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104046629"
---
# <a name="osf-switch"></a><span data-ttu-id="d635f-104">opzione/OSF</span><span class="sxs-lookup"><span data-stu-id="d635f-104">/osf switch</span></span>

<span data-ttu-id="d635f-105">L'opzione **/OSF** impone una rigida compatibilità con OSF DCE.</span><span class="sxs-lookup"><span data-stu-id="d635f-105">The **/osf** switch forces strict compatibility with OSF DCE.</span></span>

``` syntax
midl /osf
```

## <a name="switch-options"></a><span data-ttu-id="d635f-106">Opzioni switch</span><span class="sxs-lookup"><span data-stu-id="d635f-106">Switch Options</span></span>

<span data-ttu-id="d635f-107">Questa opzione non ha parametri.</span><span class="sxs-lookup"><span data-stu-id="d635f-107">This switch has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="d635f-108">Commenti</span><span class="sxs-lookup"><span data-stu-id="d635f-108">Remarks</span></span>

<span data-ttu-id="d635f-109">Usare questa opzione se l'applicazione richiede una rigida compatibilità con OSF DCE per motivi di portabilità.</span><span class="sxs-lookup"><span data-stu-id="d635f-109">Use this switch if your application requires strict compatibility with OSF DCE for portability reasons.</span></span>

<span data-ttu-id="d635f-110">In modalità **/OSF** , il pacchetto RPCSS viene abilitato automaticamente quando si usano i puntatori completi, gli argomenti richiedono l'allocazione di memoria o quando si usa l'attributo [**enable \_ allocate**](enable-allocate.md) .</span><span class="sxs-lookup"><span data-stu-id="d635f-110">In **/osf** mode, the RpcSs package is automatically enabled when you use full pointers, the arguments require memory allocation, or when you use the [**enable\_allocate**](enable-allocate.md) attribute.</span></span> <span data-ttu-id="d635f-111">Ciò significa che non è necessario fornire all'utente MIDL le funzioni [**\_ \_ gratuite**](/windows/desktop/Rpc/the-midl-user-free-function) per l' [**\_ \_ assegnazione dell'utente**](/windows/desktop/Rpc/the-midl-user-allocate-function) e l'utente MIDL nell'applicazione client e server.</span><span class="sxs-lookup"><span data-stu-id="d635f-111">This means that you do not have to supply the [**midl\_user\_allocate**](/windows/desktop/Rpc/the-midl-user-allocate-function) and [**midl\_user\_free**](/windows/desktop/Rpc/the-midl-user-free-function) functions in your client and server application.</span></span>

<span data-ttu-id="d635f-112">Le funzionalità estese Microsoft seguenti non sono disponibili quando si esegue la compilazione con l'opzione **/OSF** :</span><span class="sxs-lookup"><span data-stu-id="d635f-112">The following Microsoft-extended features are not available when you compile with the **/osf** switch:</span></span>

-   <span data-ttu-id="d635f-113">Dichiaratori astratti (parametri senza nome) nel file IDL.</span><span class="sxs-lookup"><span data-stu-id="d635f-113">Abstract declarators (unnamed parameters) in the IDL file.</span></span>
-   <span data-ttu-id="d635f-114">Definizioni di interfaccia per gli oggetti COM.</span><span class="sxs-lookup"><span data-stu-id="d635f-114">Interface definitions for COM objects.</span></span>
-   <span data-ttu-id="d635f-115">Nomi di interfaccia con più di 17 caratteri.</span><span class="sxs-lookup"><span data-stu-id="d635f-115">Interface names with more than 17 characters.</span></span>
-   <span data-ttu-id="d635f-116">Attributi solo MIDL, ad esempio [**Wire \_ marshalling**](wire-marshal.md), [**User \_ Marshal**](user-marshal.md)e The TypeLib (FAD) Extensions.</span><span class="sxs-lookup"><span data-stu-id="d635f-116">MIDL-only attributes, such as [**wire\_marshal**](wire-marshal.md), [**user\_marshal**](user-marshal.md), and the typelib (ODL)extensions.</span></span>
-   <span data-ttu-id="d635f-117">Uso delle parole chiave ACF in un file IDL (opzione di **\_ configurazione MIDL/app** ).</span><span class="sxs-lookup"><span data-stu-id="d635f-117">Using ACF keywords in an IDL file (the MIDL **/app\_config** option).</span></span>
-   <span data-ttu-id="d635f-118">Funzioni di callback statiche nel client.</span><span class="sxs-lookup"><span data-stu-id="d635f-118">Static callback functions on the client.</span></span>
-   <span data-ttu-id="d635f-119">Attributo [**asincrono**](async.md) .</span><span class="sxs-lookup"><span data-stu-id="d635f-119">The [**async**](async.md) attribute.</span></span>
-   <span data-ttu-id="d635f-120">[**\_ virgolette cpp**](cpp-quote.md) e **\# pragma MIDL \_ echo**.</span><span class="sxs-lookup"><span data-stu-id="d635f-120">[**cpp\_quote**](cpp-quote.md) and **\#pragma midl\_echo**.</span></span>
-   <span data-ttu-id="d635f-121">tipi di carattere wide, costanti e stringhe [**WCHAR \_ t**](wchar-t.md) .</span><span class="sxs-lookup"><span data-stu-id="d635f-121">[**wchar\_t**](wchar-t.md) wide-character types, constants, and strings.</span></span>
-   <span data-ttu-id="d635f-122">inizializzazione [**enum**](enum.md) (enumeratori sparse).</span><span class="sxs-lookup"><span data-stu-id="d635f-122">[**enum**](enum.md) initialization (sparse enumerators).</span></span>
-   <span data-ttu-id="d635f-123">specifica di dimensioni solo in [**uscita**](out-idl.md).</span><span class="sxs-lookup"><span data-stu-id="d635f-123">[**out**](out-idl.md)-only size specification.</span></span>
-   <span data-ttu-id="d635f-124">Puntatori a dimensione mista e matrici di dimensioni.</span><span class="sxs-lookup"><span data-stu-id="d635f-124">Mixed sized-pointers and sized arrays.</span></span>
-   <span data-ttu-id="d635f-125">Espressioni utilizzate per gli identificatori delle dimensioni e del discriminatore.</span><span class="sxs-lookup"><span data-stu-id="d635f-125">Expressions used for size and discriminator specifiers.</span></span>
-   <span data-ttu-id="d635f-126">Handle espliciti parametri in qualsiasi posizione nell'elenco di argomenti.</span><span class="sxs-lookup"><span data-stu-id="d635f-126">Explicit handle parameters in any position in the argument list.</span></span> <span data-ttu-id="d635f-127">In modalità **/OSF** , il compilatore MIDL Cerca un handle di binding esplicito come primo parametro.</span><span class="sxs-lookup"><span data-stu-id="d635f-127">In **/osf** mode, the MIDL compiler looks for an explicit binding handle as the first parameter.</span></span> <span data-ttu-id="d635f-128">Quando il primo parametro non è un handle di binding e vengono specificati uno o più handle di contesto, viene utilizzato l'handle del contesto più a sinistra come handle di associazione.</span><span class="sxs-lookup"><span data-stu-id="d635f-128">When the first parameter is not a binding handle and one or more context handles are specified, the leftmost context handle is used as the binding handle.</span></span> <span data-ttu-id="d635f-129">Quando il primo parametro non è un handle e non sono presenti handle di contesto, la procedura usa l'associazione implicita usando [**l' \_ handle implicito**](implicit-handle.md) dell'attributo ACF o l' [**\_ handle automatico**](auto-handle.md).</span><span class="sxs-lookup"><span data-stu-id="d635f-129">When the first parameter is not a handle and there are no context handles, the procedure uses implicit binding using the ACF attribute [**implicit\_handle**](implicit-handle.md) or [**auto\_handle**](auto-handle.md).</span></span>
-   <span data-ttu-id="d635f-130">Puntatore-ereditarietà del tipo di attributo.</span><span class="sxs-lookup"><span data-stu-id="d635f-130">Pointer-attribute type inheritance.</span></span> <span data-ttu-id="d635f-131">OSF DCE non consente puntatori senza attributi.</span><span class="sxs-lookup"><span data-stu-id="d635f-131">OSF DCE does not allow unattributed pointers.</span></span> <span data-ttu-id="d635f-132">Pertanto, in modalità **/OSF** ogni file IDL deve definire attributi per i relativi puntatori.</span><span class="sxs-lookup"><span data-stu-id="d635f-132">Therefore, in **/osf** mode each IDL file must define attributes for its pointers.</span></span> <span data-ttu-id="d635f-133">Se un puntatore non dispone di un attributo esplicito, per impostare il tipo di puntatore è necessario che il file IDL disponga di una specifica [**\_ predefinita del puntatore**](pointer-default.md) .</span><span class="sxs-lookup"><span data-stu-id="d635f-133">If any pointer does not have an explicit attribute, the IDL file must have a [**pointer\_default**](pointer-default.md) specification to set the pointer type.</span></span>
-   <span data-ttu-id="d635f-134">Più interfacce in un file IDL.</span><span class="sxs-lookup"><span data-stu-id="d635f-134">Multiple interfaces in an IDL file.</span></span>
-   <span data-ttu-id="d635f-135">Definizioni all'esterno del blocco di interfaccia.</span><span class="sxs-lookup"><span data-stu-id="d635f-135">Definitions outside of the interface block.</span></span>
-   <span data-ttu-id="d635f-136">Qualificatori di tipo, ad esempio **lontano** e **stdcall**.</span><span class="sxs-lookup"><span data-stu-id="d635f-136">Type qualifiers such as **far** and **stdcall**.</span></span>
-   <span data-ttu-id="d635f-137">Omissione degli attributi direzionali.</span><span class="sxs-lookup"><span data-stu-id="d635f-137">Omitting directional attributes.</span></span>

<span data-ttu-id="d635f-138">Le estensioni del linguaggio C/C++ seguenti non sono disponibili quando si esegue la compilazione con l'opzione **/OSF** :</span><span class="sxs-lookup"><span data-stu-id="d635f-138">The following C/C++ language extensions are not available when you compile with the **/osf** switch:</span></span>

-   <span data-ttu-id="d635f-139">Campi di bit in strutture e unioni.</span><span class="sxs-lookup"><span data-stu-id="d635f-139">Bit fields in structures and unions.</span></span>
-   <span data-ttu-id="d635f-140">Commenti a riga singola delimitati da due barre (//).</span><span class="sxs-lookup"><span data-stu-id="d635f-140">Single line comments delimited with two slash characters (//).</span></span>
-   <span data-ttu-id="d635f-141">Dichiarazioni esterne.</span><span class="sxs-lookup"><span data-stu-id="d635f-141">External declarations.</span></span>
-   <span data-ttu-id="d635f-142">Procedure con ellissi nell'elenco di parametri.</span><span class="sxs-lookup"><span data-stu-id="d635f-142">Procedures with ellipses in the parameter list.</span></span>
-   <span data-ttu-id="d635f-143">Digitare [**int**](int.md).</span><span class="sxs-lookup"><span data-stu-id="d635f-143">Type [**int**](int.md).</span></span>
-   <span data-ttu-id="d635f-144">Digitare **void \*** (eccetto l'attributo [**dell' \_ handle di contesto**](context-handle.md) ).</span><span class="sxs-lookup"><span data-stu-id="d635f-144">Type **void \*** (except with the [**context\_handle**](context-handle.md) attribute).</span></span>
-   <span data-ttu-id="d635f-145">I qualificatori di tipo, incluso il form con il prefisso ANSI, contengono due caratteri di sottolineatura: **\_ \_ cdecl**, **cdecl**, [**const**](const.md), **const**, **\_ \_ Export**, **Export**, **\_ \_ lontano**, **lontano**, **\_ \_ loadds**, **loadds**, **\_ \_ near**, **near**, **\_ \_ Pascal**, **Pascal**, **\_ \_ stdcall**, **stdcall**, **\_ \_ volatile** e **volatile**.</span><span class="sxs-lookup"><span data-stu-id="d635f-145">Type qualifiers, including the form with the ANSI-conformant prefix, contain two underscore characters: **\_\_cdecl**, **cdecl**, [**const**](const.md), **const**, **\_\_export**, **export**, **\_\_far**, **far**, **\_\_loadds**, **loadds**, **\_\_near**, **near**, **\_\_pascal**, **pascal**, **\_\_stdcall**, **stdcall**, **\_\_volatile**, and **volatile**.</span></span>
-   <span data-ttu-id="d635f-146">Qualsiasi \# [**pragma**](pragma.md) Warning o **\# pragma** comment.</span><span class="sxs-lookup"><span data-stu-id="d635f-146">Any \# [**pragma**](pragma.md) warning or **\#pragma** comment.</span></span>
-   <span data-ttu-id="d635f-147">Serializzazione del tipo.</span><span class="sxs-lookup"><span data-stu-id="d635f-147">Type serialization.</span></span>
-   <span data-ttu-id="d635f-148">Tipo di dati [**\_ \_ int3264**](--int3264.md) .</span><span class="sxs-lookup"><span data-stu-id="d635f-148">The [**\_\_int3264**](--int3264.md) data type.</span></span>
-   <span data-ttu-id="d635f-149">L'opzione [**/Protocol**](-protocol.md) e la sintassi ndr64 transfer.</span><span class="sxs-lookup"><span data-stu-id="d635f-149">The [**/protocol**](-protocol.md) switch, and ndr64 transfer syntax.</span></span>

## <a name="examples"></a><span data-ttu-id="d635f-150">Esempio</span><span class="sxs-lookup"><span data-stu-id="d635f-150">Examples</span></span>

<span data-ttu-id="d635f-151">**MIDL/OSF nomefile. idl**</span><span class="sxs-lookup"><span data-stu-id="d635f-151">**midl /osf filename.idl**</span></span>

<span data-ttu-id="d635f-152">**MIDL/OSF/app \_ config NomeFile. idl**</span><span class="sxs-lookup"><span data-stu-id="d635f-152">**midl /osf /app\_config filename.idl**</span></span>

## <a name="see-also"></a><span data-ttu-id="d635f-153">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d635f-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d635f-154">Sintassi della riga di comando MIDL generale</span><span class="sxs-lookup"><span data-stu-id="d635f-154">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="d635f-155">**configurazione di/app \_**</span><span class="sxs-lookup"><span data-stu-id="d635f-155">**/app\_config**</span></span>](-app-config.md)
</dt> <dt>

[<span data-ttu-id="d635f-156">**/MS \_ ext**</span><span class="sxs-lookup"><span data-stu-id="d635f-156">**/ms\_ext**</span></span>](-ms-ext.md)
</dt> <dt>

[<span data-ttu-id="d635f-157">Pacchetto di gestione della memoria RPCSS</span><span class="sxs-lookup"><span data-stu-id="d635f-157">Rpcss Memory Management Package</span></span>](/windows/desktop/Rpc/rpcss-memory-management-package)
</dt> </dl>

 

 