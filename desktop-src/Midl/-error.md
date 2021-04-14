---
title: opzione/error
description: L'opzione/error determina i tipi di controllo degli errori che gli stub generati eseguiranno in fase di esecuzione.
ms.assetid: abd3616a-2d2c-4a7d-bf3a-c84a43387894
keywords:
- /Error switch MIDL
topic_type:
- apiref
api_name:
- /error
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f84a56c1ae3d57ab1931ec175aa8dc9010ea6b8a
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "104397882"
---
# <a name="error-switch"></a><span data-ttu-id="ce434-104">opzione/error</span><span class="sxs-lookup"><span data-stu-id="ce434-104">/error switch</span></span>

<span data-ttu-id="ce434-105">L'opzione **/Error** determina i tipi di controllo degli errori che gli stub generati eseguiranno in fase di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="ce434-105">The **/error** switch determines the types of error checking that the generated stubs will perform at run time.</span></span>

> [!Note]  
> <span data-ttu-id="ce434-106">Questa funzionalità è obsoleta e non è più supportata.</span><span class="sxs-lookup"><span data-stu-id="ce434-106">This feature is obsolete and no longer supported.</span></span> <span data-ttu-id="ce434-107">È consigliabile usare l'opzione [**/robust**](-robust.md) .</span><span class="sxs-lookup"><span data-stu-id="ce434-107">The use of the [**/robust**](-robust.md) switch is recommended.</span></span>

 

``` syntax
midl /error { allocation | stub_data | ref | bounds_check | none | all }
```

## <a name="switch-options"></a><span data-ttu-id="ce434-108">Opzioni switch</span><span class="sxs-lookup"><span data-stu-id="ce434-108">Switch Options</span></span>

<dl> <dt>

 
</dt> <dd>

<dt>

<span id="allocation"></span><span id="ALLOCATION"></span>

<span data-ttu-id="ce434-109"><span id="allocation"></span><span id="ALLOCATION"></span>allocazione \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="ce434-109"><span id="allocation"></span><span id="ALLOCATION"></span>\*\*\*\*allocation\*\*\*\*</span></span>


</dt> <dd>

<span data-ttu-id="ce434-110">Verifica se [**l' \_ utente MIDL \_ allocate**](midl-user-allocate-1.md) restituisce un valore **null** , che indica un errore di memoria insufficiente.</span><span class="sxs-lookup"><span data-stu-id="ce434-110">Checks whether [**midl\_user\_allocate**](midl-user-allocate-1.md) returns a **NULL** value, indicating an out-of-memory error.</span></span>

</dd> <dt>

<span id="stub_data"></span><span id="STUB_DATA"></span>

<span data-ttu-id="ce434-111"><span id="stub_data"></span><span id="STUB_DATA"></span>\_dati Stub \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="ce434-111"><span id="stub_data"></span><span id="STUB_DATA"></span>\*\*\*\*stub\_data\*\*\*\*</span></span>


</dt> <dd>

<span data-ttu-id="ce434-112">Genera uno stub che rileva le eccezioni di unmarshalling sul lato server e le propaga nuovamente al client.</span><span class="sxs-lookup"><span data-stu-id="ce434-112">Generates a stub that catches unmarshaling exceptions on the server side and propagates them back to the client.</span></span>

</dd> <dt>

<span id="ref"></span><span id="REF"></span>

<span data-ttu-id="ce434-113"><span id="ref"></span><span id="REF"></span>Ref \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="ce434-113"><span id="ref"></span><span id="REF"></span>\*\*\*\*ref\*\*\*\*</span></span>


</dt> <dd>

<span data-ttu-id="ce434-114">Genera codice che esegue un controllo in fase di esecuzione per garantire che nessun puntatori di riferimento **null** venga passato agli stub client e genera un' \_ eccezione del \_ puntatore ref null di RPC X \_ \_ se ne trova uno.</span><span class="sxs-lookup"><span data-stu-id="ce434-114">Generates code that runs a check at run time to ensure that no **NULL** reference pointers are being passed to the client stubs and raises an RPC\_X\_NULL\_REF\_POINTER exception if it finds any.</span></span>

</dd> <dt>

<span id="bounds_check"></span><span id="BOUNDS_CHECK"></span>

<span data-ttu-id="ce434-115"><span id="bounds_check"></span><span id="BOUNDS_CHECK"></span>controllo dei limiti \_ \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="ce434-115"><span id="bounds_check"></span><span id="BOUNDS_CHECK"></span>\*\*\*\*bounds\_check\*\*\*\*</span></span>


</dt> <dd>

<span data-ttu-id="ce434-116">Verifica le dimensioni delle matrici variabili e variabili conformi rispetto alla specifica della lunghezza di trasmissione.</span><span class="sxs-lookup"><span data-stu-id="ce434-116">Checks size of conformant-varying and varying arrays against transmission length specification.</span></span>

</dd> <dt>

<span id="none"></span><span id="NONE"></span>

<span data-ttu-id="ce434-117"><span id="none"></span><span id="NONE"></span>nessuno \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="ce434-117"><span id="none"></span><span id="NONE"></span>\*\*\*\*none\*\*\*\*</span></span>


</dt> <dd>

<span data-ttu-id="ce434-118">Non esegue alcun controllo degli errori.</span><span class="sxs-lookup"><span data-stu-id="ce434-118">Performs no error checking.</span></span>

</dd> <dt>

<span id="all"></span><span id="ALL"></span>

<span data-ttu-id="ce434-119"><span id="all"></span><span id="ALL"></span>tutti i \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="ce434-119"><span id="all"></span><span id="ALL"></span>\*\*\*\*all\*\*\*\*</span></span>


</dt> <dd>

<span data-ttu-id="ce434-120">Esegue tutto il controllo degli errori.</span><span class="sxs-lookup"><span data-stu-id="ce434-120">Performs all error checking.</span></span> <span data-ttu-id="ce434-121">Efficace con MIDL versione 5,0, si tratta di un'opzione predefinita del compilatore.</span><span class="sxs-lookup"><span data-stu-id="ce434-121">Effective with MIDL version 5.0, this is a default compiler switch.</span></span>

</dd> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ce434-122">Commenti</span><span class="sxs-lookup"><span data-stu-id="ce434-122">Remarks</span></span>

<span data-ttu-id="ce434-123">L'opzione **/Error** consente di selezionare il numero di verifiche degli errori che i file stub generati eseguiranno.</span><span class="sxs-lookup"><span data-stu-id="ce434-123">The **/error** switch selects the number of error checks that the generated stub files will perform.</span></span> <span data-ttu-id="ce434-124">A partire da MIDL versione 5,0, l'impostazione predefinita è **/Error all**.</span><span class="sxs-lookup"><span data-stu-id="ce434-124">Effective with MIDL version 5.0, the default setting is **/error all**.</span></span>

<span data-ttu-id="ce434-125">Gli errori di enumerazione controllati (per impostazione predefinita in tutte le versioni di MIDL) sono errori di troncamento causati dalla conversione tra tipi di **enumerazione Long** (interi a 32 bit) e tipi di **enumerazione Short** (la rappresentazione di dati di rete di [**enum**](enum.md)) e il numero di identificatori in un'enumerazione che supera 32.767.</span><span class="sxs-lookup"><span data-stu-id="ce434-125">The enum errors that are checked (by default in all versions of MIDL) are truncation errors caused when converting between **long enum** types (32-bit integers) and **short enum** types (the network-data representation of [**enum**](enum.md)), and the number of identifiers in an enumeration exceeding 32,767.</span></span>

<span data-ttu-id="ce434-126">Il controllo degli errori di accesso alla memoria (anche per impostazione predefinita in tutte le versioni di MIDL) è per i puntatori che superano la fine del buffer nel codice di marshalling e per le matrici conformi la cui dimensione è minore di zero.</span><span class="sxs-lookup"><span data-stu-id="ce434-126">The memory-access error checking (also by default in all versions of MIDL) is for pointers that exceed the end of the buffer in marshaling code and for conformant arrays whose size is less than zero.</span></span> <span data-ttu-id="ce434-127">Usare il flag di **\_ controllo dei limiti di/Error** per verificare la presenza di altri limiti di matrice non validi.</span><span class="sxs-lookup"><span data-stu-id="ce434-127">Use the **/error bounds\_check** flag to check for other invalid array bounds.</span></span>

<span data-ttu-id="ce434-128">Quando si specifica l' **allocazione/Error**, gli stub includono il codice che genera un'eccezione quando l' [**\_ utente MIDL \_ allocate**](midl-user-allocate-1.md) restituisce 0.</span><span class="sxs-lookup"><span data-stu-id="ce434-128">When you specify **/error allocation**, the stubs include code that raises an exception when [**midl\_user\_allocate**](midl-user-allocate-1.md) returns 0.</span></span>

<span data-ttu-id="ce434-129">L'opzione **/Error Stub \_ Data** impedisce che i dati client arrestino in modo anomalo il server durante l'esecuzione dell'unmarshalling, fornendo un metodo più affidabile per gestire l'operazione di unmarshalling.</span><span class="sxs-lookup"><span data-stu-id="ce434-129">The **/error stub\_data** option prevents client data from crashing the server during unmarshaling, effectively providing a more robust method of handling the unmarshaling operation.</span></span>

<span data-ttu-id="ce434-130">A partire da Windows 2000, il motore di marshalling del recapito di run-time sottostante esegue la maggior parte di questi controlli.</span><span class="sxs-lookup"><span data-stu-id="ce434-130">Effective with WindowsÂ 2000, the underlying run-time NDR marshaling engine performs most of these checks.</span></span> <span data-ttu-id="ce434-131">Ciò significa che se si utilizza una delle modalità completamente interpretate ([**/OI**](-oi.md), **/OIF**) della generazione Stub, la scelta di diverse opzioni di controllo degli errori non avrà un effetto marcato sulle prestazioni.</span><span class="sxs-lookup"><span data-stu-id="ce434-131">This means that if you are using one of the fully-interpreted modes ([**/Oi**](-oi.md), **/Oif**) of stub generation, choosing different error checking options will not have a marked effect on performance.</span></span>

## <a name="examples"></a><span data-ttu-id="ce434-132">Esempio</span><span class="sxs-lookup"><span data-stu-id="ce434-132">Examples</span></span>

<span data-ttu-id="ce434-133">**nome file di allocazione/Error MIDL. idl**</span><span class="sxs-lookup"><span data-stu-id="ce434-133">**midl /error allocation filename.idl**</span></span>

<span data-ttu-id="ce434-134">**MIDL/error none nomefile. idl**</span><span class="sxs-lookup"><span data-stu-id="ce434-134">**midl /error none filename.idl**</span></span>

## <a name="see-also"></a><span data-ttu-id="ce434-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ce434-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ce434-136">Sintassi della riga di comando MIDL generale</span><span class="sxs-lookup"><span data-stu-id="ce434-136">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="ce434-137">**/Robust**</span><span class="sxs-lookup"><span data-stu-id="ce434-137">**/robust**</span></span>](-robust.md)
</dt> </dl>

 

 




