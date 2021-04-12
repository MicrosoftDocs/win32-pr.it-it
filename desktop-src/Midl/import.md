---
title: import (attributo)
description: La direttiva Import specifica un altro file IDL, FAD o di intestazione contenente le definizioni a cui si vuole fare riferimento dal file IDL principale.
ms.assetid: b52fb2c7-ce60-474f-8833-7a821844f747
keywords:
- Importa attributo MIDL
topic_type:
- apiref
api_name:
- import
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 64ff13c069c6bba819720a9d1120a42c25af4b51
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104336983"
---
# <a name="import-attribute"></a><span data-ttu-id="b3f1d-104">import (attributo)</span><span class="sxs-lookup"><span data-stu-id="b3f1d-104">import attribute</span></span>

<span data-ttu-id="b3f1d-105">La direttiva **Import** specifica un altro file IDL, FAD o di intestazione contenente le definizioni a cui si vuole fare riferimento dal file IDL principale.</span><span class="sxs-lookup"><span data-stu-id="b3f1d-105">The **import** directive specifies another IDL, ODL, or header file containing definitions you wish to reference from your main IDL file.</span></span>

``` syntax
import "filename" [[ , ... ]] ;
```

## <a name="parameters"></a><span data-ttu-id="b3f1d-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="b3f1d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b3f1d-107">*filename*</span><span class="sxs-lookup"><span data-stu-id="b3f1d-107">*filename*</span></span> 
</dt> <dd>

<span data-ttu-id="b3f1d-108">Specifica il nome del file di intestazione, IDL o FAD da importare.</span><span class="sxs-lookup"><span data-stu-id="b3f1d-108">Specifies the name of the header, IDL, or ODL file to import.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b3f1d-109">Commenti</span><span class="sxs-lookup"><span data-stu-id="b3f1d-109">Remarks</span></span>

<span data-ttu-id="b3f1d-110">Con la direttiva **Import** , tutte le istruzioni IDL nel file importato, ad esempio i typedef, le dichiarazioni di costanti e le definizioni di interfaccia, diventano disponibili per l'importazione. File IDL.</span><span class="sxs-lookup"><span data-stu-id="b3f1d-110">With the **import** directive, all IDL statements in the imported file, such as typedefs, constant declarations, and interface definitions become available to the importing .IDL file.</span></span>

<span data-ttu-id="b3f1d-111">Il file importato viene elaborato separatamente (ovvero il preprocessore CPP viene richiamato in modo indipendente) dal file IDL di importazione.</span><span class="sxs-lookup"><span data-stu-id="b3f1d-111">The imported file is processed separately (meaning that CPP preprocessor is invoked independently) from the importing IDL file.</span></span> <span data-ttu-id="b3f1d-112">In questo modo, le direttive del preprocessore, ad esempio \# define, non vengono riportate da un'intestazione importata o da un file IDL al file IDL di importazione.</span><span class="sxs-lookup"><span data-stu-id="b3f1d-112">In this way, pre-processor directives, such as \#define, do not carry over from an imported header or IDL file to the importing IDL file.</span></span>

<span data-ttu-id="b3f1d-113">Come la macro del preprocessore del linguaggio C **\# include**, la direttiva **Import** indica al compilatore di includere i tipi di dati definiti nei file IDL importati.</span><span class="sxs-lookup"><span data-stu-id="b3f1d-113">Like the C-language preprocessor macro **\#include**, the **import** directive tells the compiler to include data types that were defined in the imported IDL files.</span></span> <span data-ttu-id="b3f1d-114">A differenza della direttiva **\# include** , la direttiva **Import** ignora i prototipi di routine, perché non vengono generati stub per alcun elemento nel file importato.</span><span class="sxs-lookup"><span data-stu-id="b3f1d-114">Unlike the **\#include** directive, the **import** directive ignores procedure prototypes, since no stubs are generated for anything in the imported file.</span></span>

<span data-ttu-id="b3f1d-115">Per informazioni specifiche sull'utilizzo di **Importa** per includere i file di intestazione in un file IDL, vedere [importazione di file di intestazione di sistema](importing-system-header-files.md).</span><span class="sxs-lookup"><span data-stu-id="b3f1d-115">For specific information on using **import** to include header files in an IDL file, see [Importing System Header Files](importing-system-header-files.md).</span></span>

<span data-ttu-id="b3f1d-116">Intestazione del linguaggio C (. H) il file generato per l'interfaccia non contiene direttamente i tipi importati, ma genera invece una direttiva **\# include** per il file di intestazione corrispondente all'interfaccia importata.</span><span class="sxs-lookup"><span data-stu-id="b3f1d-116">The C-language header (.H) file generated for the interface does not directly contain the imported types but instead generates a **\#include** directive for the header file corresponding to the imported interface.</span></span> <span data-ttu-id="b3f1d-117">Ad esempio, quando si importa BASE. IDL nel derivato. IDL, il file di intestazione generato derivato. H conterrà la direttiva **\# include** base. h.</span><span class="sxs-lookup"><span data-stu-id="b3f1d-117">For example, when you import BASE.IDL into your DERIVED.IDL, the generated header file DERIVED.H will contain the directive **\#include** BASE.H.</span></span>

<span data-ttu-id="b3f1d-118">Sono applicabili le regole seguenti:</span><span class="sxs-lookup"><span data-stu-id="b3f1d-118">The following rules apply:</span></span>

-   <span data-ttu-id="b3f1d-119">La parola chiave **Import** è facoltativa e può essere visualizzata zero o più volte nel file IDL.</span><span class="sxs-lookup"><span data-stu-id="b3f1d-119">The **import** keyword is optional and can appear zero or more times in the IDL file.</span></span>
-   <span data-ttu-id="b3f1d-120">Ogni parola chiave **Import** può essere associata a più di un nome di file.</span><span class="sxs-lookup"><span data-stu-id="b3f1d-120">Each **import** keyword can be associated with more than one file name.</span></span>
-   <span data-ttu-id="b3f1d-121">Separare più nomi di file con virgole.</span><span class="sxs-lookup"><span data-stu-id="b3f1d-121">Separate multiple file names with commas.</span></span>
-   <span data-ttu-id="b3f1d-122">È necessario racchiudere il nome file tra virgolette e terminare l'istruzione import con un punto e virgola (;).</span><span class="sxs-lookup"><span data-stu-id="b3f1d-122">You must enclose the file name within quotation marks and end the import statement with a semicolon (;).</span></span>
-   <span data-ttu-id="b3f1d-123">È possibile importare un'interfaccia senza attributi in un altro file IDL.</span><span class="sxs-lookup"><span data-stu-id="b3f1d-123">You can import an interface that has no attributes into another IDL file.</span></span> <span data-ttu-id="b3f1d-124">Tuttavia, l'interfaccia deve contenere solo tipi di oggetto. non può contenere alcuna routine.</span><span class="sxs-lookup"><span data-stu-id="b3f1d-124">However, the interface must contain only datatypes; it cannot contain any procedures.</span></span> <span data-ttu-id="b3f1d-125">Se nell'interfaccia importata è inclusa anche una routine, è necessario specificare un attributo [**local**](local.md) o [**UUID**](uuid.md) .</span><span class="sxs-lookup"><span data-stu-id="b3f1d-125">If even one procedure is contained in the imported interface, you must specify a [**local**](local.md) or [**UUID**](uuid.md) attribute.</span></span>
-   <span data-ttu-id="b3f1d-126">La funzione di **importazione** è idempotentÂ â € ", ovvero l'importazione di un'interfaccia più di una volta non ha alcun effetto aggiuntivo.</span><span class="sxs-lookup"><span data-stu-id="b3f1d-126">The **import** function is idempotentÂ â€”Â that is, importing an interface more than once has no additional effect.</span></span>

> [!Note]  
> <span data-ttu-id="b3f1d-127">Il comportamento della direttiva **Import** è indipendente dalle modalità del compilatore MIDL Switch [**/MS \_ ext**](-ms-ext.md) (impostazione predefinita), [**/OSF**](-osf.md)e [**/app \_ config**](-app-config.md).</span><span class="sxs-lookup"><span data-stu-id="b3f1d-127">The behavior of the **import** directive is independent of the MIDL compiler mode switches [**/ms\_ext**](-ms-ext.md) (the default), [**/osf**](-osf.md), and [**/app\_config**](-app-config.md).</span></span> <span data-ttu-id="b3f1d-128">Tuttavia, la modalità del compilatore (**/OSF** o **/MS \_ ext**) può influenzare la decorazione degli attributi dei puntatori sui tipi importati.</span><span class="sxs-lookup"><span data-stu-id="b3f1d-128">However, the compiler mode (**/osf** or **/ms\_ext**) can affect pointer attribute decoration on imported types.</span></span> <span data-ttu-id="b3f1d-129">Per informazioni dettagliate [, vedere ereditarietà del tipo di attributo puntatore](/windows/desktop/Rpc/pointer-attribute-type-inheritance).</span><span class="sxs-lookup"><span data-stu-id="b3f1d-129">For details see [Pointer-Attribute Type Inheritance](/windows/desktop/Rpc/pointer-attribute-type-inheritance).</span></span>

 

## <a name="examples"></a><span data-ttu-id="b3f1d-130">Esempi</span><span class="sxs-lookup"><span data-stu-id="b3f1d-130">Examples</span></span>

``` syntax
import "myoldodl.odl";  
import "unknwn.idl";
import "part1.idl", "part2.idl", "part3.idl"; 
```

## <a name="see-also"></a><span data-ttu-id="b3f1d-131">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="b3f1d-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b3f1d-132">**configurazione di/app \_**</span><span class="sxs-lookup"><span data-stu-id="b3f1d-132">**/app\_config**</span></span>](-app-config.md)
</dt> <dt>

[<span data-ttu-id="b3f1d-133">File di definizione dell'interfaccia (IDL)</span><span class="sxs-lookup"><span data-stu-id="b3f1d-133">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="b3f1d-134">**importlib**</span><span class="sxs-lookup"><span data-stu-id="b3f1d-134">**importlib**</span></span>](importlib.md)
</dt> <dt>

[<span data-ttu-id="b3f1d-135">**includere**</span><span class="sxs-lookup"><span data-stu-id="b3f1d-135">**include**</span></span>](include.md)
</dt> <dt>

[<span data-ttu-id="b3f1d-136">Importazione di file di intestazione di sistema</span><span class="sxs-lookup"><span data-stu-id="b3f1d-136">Importing System Header Files</span></span>](importing-system-header-files.md)
</dt> <dt>

[<span data-ttu-id="b3f1d-137">Importazione di file e librerie dei tipi</span><span class="sxs-lookup"><span data-stu-id="b3f1d-137">Importing Files and Type Libraries</span></span>](importing-files-and-type-libraries.md)
</dt> <dt>

[<span data-ttu-id="b3f1d-138">**/MS \_ ext**</span><span class="sxs-lookup"><span data-stu-id="b3f1d-138">**/ms\_ext**</span></span>](-ms-ext.md)
</dt> <dt>

[<span data-ttu-id="b3f1d-139">**/osf**</span><span class="sxs-lookup"><span data-stu-id="b3f1d-139">**/osf**</span></span>](-osf.md)
</dt> </dl>

 

 