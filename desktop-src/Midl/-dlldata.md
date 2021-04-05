---
title: opzione/dlldata
description: L'opzione/dlldata viene usata per specificare il nome file per il file dlldata generato per una DLL proxy. Se non si specifica l'opzione/dlldata, viene usato il nome file predefinito dlldata. c.
ms.assetid: 5211498b-c641-447f-9514-a98766e26ea9
keywords:
- /dlldata switch MIDL
topic_type:
- apiref
api_name:
- /dlldata
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e0e9c1d7f27c56f81905081fd9ef24c8c490391b
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "103718691"
---
# <a name="dlldata-switch"></a><span data-ttu-id="429e1-105">opzione/dlldata</span><span class="sxs-lookup"><span data-stu-id="429e1-105">/dlldata switch</span></span>

<span data-ttu-id="429e1-106">L'opzione **/dlldata** viene usata per specificare il nome file per il file dlldata generato per una DLL proxy.</span><span class="sxs-lookup"><span data-stu-id="429e1-106">The **/dlldata** switch is used to specify the file name for the generated dlldata file for a proxy DLL.</span></span> <span data-ttu-id="429e1-107">Se non si specifica l'opzione **/dlldata** , viene usato il nome file predefinito dlldata. c.</span><span class="sxs-lookup"><span data-stu-id="429e1-107">The default file name Dlldata.c is used if the **/dlldata** switch is not specified.</span></span>

``` syntax
midl /dlldata file-name
```

## <a name="switch-options"></a><span data-ttu-id="429e1-108">Opzioni switch</span><span class="sxs-lookup"><span data-stu-id="429e1-108">Switch Options</span></span>

<dl> <dt>

<span data-ttu-id="429e1-109">*nome file*</span><span class="sxs-lookup"><span data-stu-id="429e1-109">*file-name*</span></span> 
</dt> <dd>

<span data-ttu-id="429e1-110">Nome del file di origine C che il compilatore MIDL genererà per la DLL del proxy.</span><span class="sxs-lookup"><span data-stu-id="429e1-110">The name of the C source file the MIDL compiler will generate for the proxy DLL.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="429e1-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="429e1-111">Remarks</span></span>

<span data-ttu-id="429e1-112">Il file specificato da *nome file* deve essere collegato alla DLL del proxy.</span><span class="sxs-lookup"><span data-stu-id="429e1-112">The file specified by *file-name* must be linked to the proxy DLL.</span></span> <span data-ttu-id="429e1-113">Il file dlldata contiene i punti di ingresso e le strutture di dati richiesti dall'class factory per la DLL del proxy.</span><span class="sxs-lookup"><span data-stu-id="429e1-113">The dlldata file contains entry points and data structures required by the class factory for the proxy DLL.</span></span> <span data-ttu-id="429e1-114">Queste strutture di dati specificano le interfacce oggetto contenute nella DLL del proxy.</span><span class="sxs-lookup"><span data-stu-id="429e1-114">These data structures specify the object interfaces contained in the proxy DLL.</span></span> <span data-ttu-id="429e1-115">Il file dlldata specifica anche l'identificatore di classe del class factory per la DLL del proxy.</span><span class="sxs-lookup"><span data-stu-id="429e1-115">The dlldata file also specifies the class identifier of the class factory for the proxy DLL.</span></span> <span data-ttu-id="429e1-116">Si tratta sempre dell'UUID (IID) della prima interfaccia del primo file proxy (in ordine alfabetico).</span><span class="sxs-lookup"><span data-stu-id="429e1-116">This is always the UUID (IID) of the first interface of the first proxy file (by alphabetical order).</span></span>

<span data-ttu-id="429e1-117">È necessario specificare lo stesso file dlldata quando si richiama MIDL in tutti i file IDL che entreranno in una determinata DLL del proxy.</span><span class="sxs-lookup"><span data-stu-id="429e1-117">The same dlldata file should be specified when invoking MIDL on all the IDL files that will go into a particular proxy DLL.</span></span> <span data-ttu-id="429e1-118">Il file dlldata viene creato o aggiornato durante ogni compilazione MIDL, compilando in modo incrementale un elenco delle interfacce che verranno inserite nella DLL del proxy.</span><span class="sxs-lookup"><span data-stu-id="429e1-118">The dlldata file is created or updated during each MIDL compilation, incrementally building a list of the interfaces that will go into the proxy DLL.</span></span>

## <a name="examples"></a><span data-ttu-id="429e1-119">Esempio</span><span class="sxs-lookup"><span data-stu-id="429e1-119">Examples</span></span>

<span data-ttu-id="429e1-120">**MIDL/dlldata data. c**</span><span class="sxs-lookup"><span data-stu-id="429e1-120">**midl /dlldata data.c**</span></span>

## <a name="see-also"></a><span data-ttu-id="429e1-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="429e1-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="429e1-122">Sintassi della riga di comando MIDL generale</span><span class="sxs-lookup"><span data-stu-id="429e1-122">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> </dl>

 

 




