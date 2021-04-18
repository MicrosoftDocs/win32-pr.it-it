---
title: Opzione/OS
description: L'opzione/OS specifica il metodo in modalità mista per il marshalling del codice stub passato tra client e server.
ms.assetid: dc5cafbb-dcc6-4fcb-a04f-1bc9720a13cb
keywords:
- /OS switch MIDL
topic_type:
- apiref
api_name:
- /Os
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bbbef54501e195c91bdcc0cec8045f2eec763820
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "106299051"
---
# <a name="os-switch"></a><span data-ttu-id="eb9b1-104">Opzione/OS</span><span class="sxs-lookup"><span data-stu-id="eb9b1-104">/Os switch</span></span>

<span data-ttu-id="eb9b1-105">L'opzione **/OS** specifica il metodo in modalità mista per il marshalling del codice stub passato tra client e server.</span><span class="sxs-lookup"><span data-stu-id="eb9b1-105">The **/Os** switch specifies the mixed-mode method to marshal stub code passed between client and server.</span></span>

``` syntax
midl /Os
```

## <a name="switch-options"></a><span data-ttu-id="eb9b1-106">Opzioni switch</span><span class="sxs-lookup"><span data-stu-id="eb9b1-106">Switch Options</span></span>

<span data-ttu-id="eb9b1-107">Questa opzione non ha parametri.</span><span class="sxs-lookup"><span data-stu-id="eb9b1-107">This switch has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="eb9b1-108">Commenti</span><span class="sxs-lookup"><span data-stu-id="eb9b1-108">Remarks</span></span>

<span data-ttu-id="eb9b1-109">Ci sono aspetti importanti da considerare prima di decidere il metodo per il marshalling del codice.</span><span class="sxs-lookup"><span data-stu-id="eb9b1-109">There are important issues to consider before deciding on the method for marshaling code.</span></span> <span data-ttu-id="eb9b1-110">Questi problemi riguardano le dimensioni e le prestazioni.</span><span class="sxs-lookup"><span data-stu-id="eb9b1-110">These issues concern size and performance.</span></span> <span data-ttu-id="eb9b1-111">Il compilatore MIDL fornisce due metodi per il marshalling del codice: modalità mista (**/OS**) e completamente interpretato ([**/OI**](-oi.md)).</span><span class="sxs-lookup"><span data-stu-id="eb9b1-111">The MIDL compiler provides two methods for marshaling code: mixed-mode (**/Os**) and fully-interpreted ([**/Oi**](-oi.md)).</span></span> <span data-ttu-id="eb9b1-112">Il metodo completamente interpretato esegue il marshalling dei dati completamente offline.</span><span class="sxs-lookup"><span data-stu-id="eb9b1-112">The fully-interpreted method marshals data completely offline.</span></span> <span data-ttu-id="eb9b1-113">In questo modo si riduce considerevolmente le dimensioni del codice dello stub, ma si riducono anche le prestazioni.</span><span class="sxs-lookup"><span data-stu-id="eb9b1-113">This reduces the size of the stub code considerably, but it also results in decreased performance.</span></span>

<span data-ttu-id="eb9b1-114">Usare la modalità predefinita MIDL **/Oicf** /robust per tutti gli scopi diversi dalla compatibilità con le versioni precedenti.</span><span class="sxs-lookup"><span data-stu-id="eb9b1-114">Use MIDL default mode **/Oicf** /robust for all purposes other than backward compatibility.</span></span> <span data-ttu-id="eb9b1-115">Questa modalità è la modalità standard sicura del compilatore MIDL; tutte le altre modalità devono essere utilizzate solo dopo un'attenta considerazione per le implicazioni di sicurezza, con la consapevolezza che le future estensioni verranno implementate solo per la modalità predefinita.</span><span class="sxs-lookup"><span data-stu-id="eb9b1-115">This mode is the secure standard mode of MIDL compiler; any other mode should be used only after careful consideration to the security implication, realizing that future extensions will only be implemented for default mode.</span></span> <span data-ttu-id="eb9b1-116">In modalità mista, il compilatore esegue il marshalling di alcuni parametri inline negli stub generati.</span><span class="sxs-lookup"><span data-stu-id="eb9b1-116">In mixed mode, the compiler marshals some parameters inline in the generated stubs.</span></span> <span data-ttu-id="eb9b1-117">Anche se ciò comporta dimensioni di stub più grandi, può offrire prestazioni migliori.</span><span class="sxs-lookup"><span data-stu-id="eb9b1-117">While this results in larger stub size, it also may offer increased performance.</span></span>

<span data-ttu-id="eb9b1-118">MIDL fornisce supporto completo per le matrici multidimensionali e i puntatori di dimensioni multidimensionali solo in modalità [**/Oicf**](-oi.md) .</span><span class="sxs-lookup"><span data-stu-id="eb9b1-118">MIDL provides full support for multidimensional arrays and multidimensional-sized pointers only in [**/Oicf**](-oi.md) mode.</span></span> <span data-ttu-id="eb9b1-119">Nelle modalità **/OS** e **/OI** il compilatore supporta i casi semplici, ad esempio le matrici a dimensione fissa.</span><span class="sxs-lookup"><span data-stu-id="eb9b1-119">In **/Os** and **/Oi** modes, the compiler supports simple cases, such as fixed-size arrays.</span></span> <span data-ttu-id="eb9b1-120">L'utilizzo di matrici multidimensionali in modalità **/OS** o **/OI** può causare parametri di cui non è stato effettuato il marshalling correttamente.</span><span class="sxs-lookup"><span data-stu-id="eb9b1-120">Using multidimensional arrays in **/Os** or **/Oi** modes can result in parameters that are not marshaled correctly.</span></span> <span data-ttu-id="eb9b1-121">Microsoft consiglia di utilizzare l'opzione della riga di comando **/Oicf** quando l'interfaccia definisce parametri che sono matrici multidimensionali o puntatori di dimensioni multidimensionali.</span><span class="sxs-lookup"><span data-stu-id="eb9b1-121">Microsoft recommends that you use the **/Oicf** command line switch when your interface defines parameters that are multidimensional arrays or multidimensional-sized pointers.</span></span>

<span data-ttu-id="eb9b1-122">Per definire ulteriormente il livello di gradazione nel modo in cui viene effettuato il marshalling dei dati, questa versione di RPC fornisce un \[ attributo [**optimize**](optimize.md) \] .</span><span class="sxs-lookup"><span data-stu-id="eb9b1-122">To further define the level of gradation in how data is marshaled, this version of RPC provides an \[[**optimize**](optimize.md)\] attribute.</span></span> <span data-ttu-id="eb9b1-123">Questo attributo viene usato come attributo dell'interfaccia ACF o attributo Operation per selezionare la modalità di marshalling.</span><span class="sxs-lookup"><span data-stu-id="eb9b1-123">This attribute is used as an ACF interface attribute or operation attribute to select the marshaling mode.</span></span>

## <a name="examples"></a><span data-ttu-id="eb9b1-124">Esempio</span><span class="sxs-lookup"><span data-stu-id="eb9b1-124">Examples</span></span>

<span data-ttu-id="eb9b1-125">**MIDL/OS nomefile. idl**</span><span class="sxs-lookup"><span data-stu-id="eb9b1-125">**midl /Os filename.idl**</span></span>

## <a name="see-also"></a><span data-ttu-id="eb9b1-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="eb9b1-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eb9b1-127">Sintassi della riga di comando MIDL generale</span><span class="sxs-lookup"><span data-stu-id="eb9b1-127">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="eb9b1-128">**/OI**</span><span class="sxs-lookup"><span data-stu-id="eb9b1-128">**/Oi**</span></span>](-oi.md)
</dt> <dt>

[<span data-ttu-id="eb9b1-129">**ottimizzare**</span><span class="sxs-lookup"><span data-stu-id="eb9b1-129">**optimize**</span></span>](optimize.md)
</dt> <dt>

[<span data-ttu-id="eb9b1-130">**/No \_ Format \_ opz**</span><span class="sxs-lookup"><span data-stu-id="eb9b1-130">**/no\_format\_opt**</span></span>](-no-format-opt.md)
</dt> </dl>

 

 




