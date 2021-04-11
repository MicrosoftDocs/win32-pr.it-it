---
title: RPC_IF_HANDLE (rpcdce. h)
description: Il \_ tipo di dati RPC if \_ handle dichiara un handle di interfaccia.
ms.assetid: a85f3a44-7cdf-421f-a1e4-c67a9dd0c54d
keywords:
- RPC_IF_HANDLE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d9590973d5ae1e82d89d6151e224b771d9f55ecc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964684"
---
# <a name="rpc_if_handle"></a><span data-ttu-id="6ff62-104">\_gestore RPC if \_</span><span class="sxs-lookup"><span data-stu-id="6ff62-104">RPC\_IF\_HANDLE</span></span>

<span data-ttu-id="6ff62-105">Il tipo di dati **RPC \_ if \_ handle** dichiara un handle di interfaccia.</span><span class="sxs-lookup"><span data-stu-id="6ff62-105">The **RPC\_IF\_HANDLE** data type declares an interface handle.</span></span>


```C++
typedef void __RPC_FAR* RPC_IF_HANDLE;
```



## <a name="remarks"></a><span data-ttu-id="6ff62-106">Commenti</span><span class="sxs-lookup"><span data-stu-id="6ff62-106">Remarks</span></span>

<span data-ttu-id="6ff62-107">La libreria di runtime RPC utilizza gli handle di interfaccia per accedere alla struttura dei dati di specifica dell'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="6ff62-107">The RPC run-time library uses interface handles to access the interface-specification data structure.</span></span> <span data-ttu-id="6ff62-108">Il compilatore MIDL crea automaticamente una struttura di dati di specifica dell'interfaccia da ogni file IDL e crea una variabile globale di tipo RPC \_ se \_ handle per la specifica dell'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="6ff62-108">The MIDL compiler automatically creates an interface-specification data structure from each IDL file and creates a global variable of type RPC\_IF\_HANDLE for the interface specification.</span></span>

<span data-ttu-id="6ff62-109">Il compilatore MIDL include un handle di interfaccia in ogni file di intestazione generato per l'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="6ff62-109">The MIDL compiler includes an interface handle in each header file generated for the interface.</span></span> <span data-ttu-id="6ff62-110">Le funzioni che richiedono la specifica dell'interfaccia come parametro mostrano un tipo di dati di **RPC \_ if \_ handle**.</span><span class="sxs-lookup"><span data-stu-id="6ff62-110">Functions requiring the interface specification as a parameter show a data type of **RPC\_IF\_HANDLE**.</span></span> <span data-ttu-id="6ff62-111">Il formato di ogni nome dell'handle di interfaccia è il seguente:</span><span class="sxs-lookup"><span data-stu-id="6ff62-111">The form of each interface handle name is as follows:</span></span>

-   <span data-ttu-id="6ff62-112">*if-name* \_ ClientIfHandle (per il client)</span><span class="sxs-lookup"><span data-stu-id="6ff62-112">*if-name*\_ClientIfHandle (for the client)</span></span>
-   <span data-ttu-id="6ff62-113">*if-name* \_ ServerIfHandle (per il server)</span><span class="sxs-lookup"><span data-stu-id="6ff62-113">*if-name*\_ServerIfHandle (for the server)</span></span>

<span data-ttu-id="6ff62-114">La parte *if-name* specifica l'identificatore di interfaccia nel file IDL.</span><span class="sxs-lookup"><span data-stu-id="6ff62-114">The *if-name* part specifies the interface identifier in the IDL file.</span></span>

<span data-ttu-id="6ff62-115">Ad esempio:</span><span class="sxs-lookup"><span data-stu-id="6ff62-115">For example:</span></span>

<span data-ttu-id="6ff62-116">Hello \_ ClientIfHandle</span><span class="sxs-lookup"><span data-stu-id="6ff62-116">hello\_ClientIfHandle</span></span>

<span data-ttu-id="6ff62-117">Hello \_ ServerIfHandle</span><span class="sxs-lookup"><span data-stu-id="6ff62-117">hello\_ServerIfHandle</span></span>

> [!Note]  
> <span data-ttu-id="6ff62-118">La lunghezza massima del nome dell'handle dell'interfaccia è 31 caratteri.</span><span class="sxs-lookup"><span data-stu-id="6ff62-118">The maximum length of the interface handle name is 31 characters.</span></span>

 

<span data-ttu-id="6ff62-119">Poiché le \_ parti "ClientIfHandle" e " \_ ServerIfHandle" dei nomi richiedono 15 caratteri, la lunghezza dell'elemento *if-name* non può superare i 16 caratteri.</span><span class="sxs-lookup"><span data-stu-id="6ff62-119">Because the "\_ClientIfHandle" and "\_ServerIfHandle" parts of the names require 15 characters, the *if-name* element can be no more than 16 characters long.</span></span>

## <a name="requirements"></a><span data-ttu-id="6ff62-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6ff62-120">Requirements</span></span>



| <span data-ttu-id="6ff62-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="6ff62-121">Requirement</span></span> | <span data-ttu-id="6ff62-122">Valore</span><span class="sxs-lookup"><span data-stu-id="6ff62-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6ff62-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6ff62-123">Minimum supported client</span></span><br/> | <span data-ttu-id="6ff62-124">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="6ff62-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="6ff62-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6ff62-125">Minimum supported server</span></span><br/> | <span data-ttu-id="6ff62-126">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="6ff62-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="6ff62-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6ff62-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="6ff62-128"><dt>Rpcdce. h (include RPC. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6ff62-128"><dt>Rpcdce.h (include Rpc.h)</dt></span></span> </dl> |



 

 





