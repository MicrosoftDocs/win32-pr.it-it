---
title: Attributi dell'intestazione dell'interfaccia
description: Incorporare questi attributi nell'intestazione dell'interfaccia per fornire informazioni sull'intera interfaccia.
ms.assetid: 5e30c902-1a55-4afd-afba-93fcc9e75033
keywords:
- MIDL, attributi, intestazione dell'interfaccia IDL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c3e5fc25a0e441b092749872a1b4d4735d483cae
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044520"
---
# <a name="interface-header-attributes"></a><span data-ttu-id="94671-104">Attributi dell'intestazione dell'interfaccia</span><span class="sxs-lookup"><span data-stu-id="94671-104">Interface Header Attributes</span></span>

<span data-ttu-id="94671-105">Incorporare questi attributi nell'intestazione dell'interfaccia per fornire informazioni sull'intera interfaccia.</span><span class="sxs-lookup"><span data-stu-id="94671-105">Incorporate these attributes in the interface header to convey information about the entire interface.</span></span>



| <span data-ttu-id="94671-106">Attributo</span><span class="sxs-lookup"><span data-stu-id="94671-106">Attribute</span></span>                                   | <span data-ttu-id="94671-107">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="94671-107">Usage</span></span>                                                                                                                                                                                                                                            |
|---------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="94671-108">**\_UUID asincrono**</span><span class="sxs-lookup"><span data-stu-id="94671-108">**async\_uuid**</span></span>](async-uuid.md)           | <span data-ttu-id="94671-109">Indica al compilatore MIDL di definire le versioni sincrone e asincrone di un'interfaccia COM.</span><span class="sxs-lookup"><span data-stu-id="94671-109">Directs the MIDL compiler to define both synchronous and asynchronous versions of a COM interface.</span></span>                                                                                                                                               |
| [<span data-ttu-id="94671-110">**uuid**</span><span class="sxs-lookup"><span data-stu-id="94671-110">**uuid**</span></span>](uuid.md)                        | <span data-ttu-id="94671-111">Designa un valore a 128 bit che distingue una particolare interfaccia da tutti gli altri.</span><span class="sxs-lookup"><span data-stu-id="94671-111">Designates a 128-bit value that distinguishes a particular interface from all others.</span></span> <span data-ttu-id="94671-112">Il valore effettivo può rappresentare un GUID, un CLSID o un IID.</span><span class="sxs-lookup"><span data-stu-id="94671-112">The actual value may represent a GUID, a CLSID, or an IID.</span></span>                                                                                                 |
| [<span data-ttu-id="94671-113">**locale**</span><span class="sxs-lookup"><span data-stu-id="94671-113">**local**</span></span>](local.md)                      | <span data-ttu-id="94671-114">Indica al compilatore MIDL di generare solo file di intestazione.</span><span class="sxs-lookup"><span data-stu-id="94671-114">Directs the MIDL compiler to generate header files only.</span></span> <span data-ttu-id="94671-115">Un'interfaccia deve avere un attributo [**UUID**](uuid.md) o [**local**](local.md) .</span><span class="sxs-lookup"><span data-stu-id="94671-115">An interface must have either a [**uuid**](uuid.md) or a [**local**](local.md) attribute.</span></span>                                                                                             |
| [<span data-ttu-id="94671-116">**MS \_ Union**</span><span class="sxs-lookup"><span data-stu-id="94671-116">**ms\_union**</span></span>](-ms-union.md)              | <span data-ttu-id="94671-117">Controlla l'allineamento del rapporto di recapito delle unioni non incapsulate.</span><span class="sxs-lookup"><span data-stu-id="94671-117">Controls the NDR alignment of nonencapsulated unions.</span></span> <span data-ttu-id="94671-118">Usare per la compatibilità con le versioni precedenti delle interfacce basate su MIDL 1,0 o 2,0.</span><span class="sxs-lookup"><span data-stu-id="94671-118">Use for backward compatibility with interfaces built on MIDL 1.0 or 2.0.</span></span>                                                                                                                   |
| [<span data-ttu-id="94671-119">**oggetto**</span><span class="sxs-lookup"><span data-stu-id="94671-119">**object**</span></span>](object.md)                    | <span data-ttu-id="94671-120">Identifica l'interfaccia come interfaccia COM e indica al compilatore MIDL di generare codice proxy/stub anziché stub client e server RPC.</span><span class="sxs-lookup"><span data-stu-id="94671-120">Identifies the interface as a COM interface and directs the MIDL compiler to generate proxy/stub code instead of RPC client and server stubs.</span></span>                                                                                                    |
| [<span data-ttu-id="94671-121">**Versione**</span><span class="sxs-lookup"><span data-stu-id="94671-121">**version**</span></span>](version.md)                  | <span data-ttu-id="94671-122">Identifica una particolare versione di un'interfaccia nei casi in cui esistano più versioni dell'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="94671-122">Identifies a particular version of an interface in cases where multiple versions of the interface exist.</span></span> <span data-ttu-id="94671-123">Poiché le interfacce COM non sono modificabili, non è possibile usare l'attributo [**Version**](version.md) in un'interfaccia [**oggetto**](object.md) .</span><span class="sxs-lookup"><span data-stu-id="94671-123">Because COM interfaces are immutable, you cannot use the [**version**](version.md) attribute on an [**object**](object.md) interface.</span></span> |
| [<span data-ttu-id="94671-124">**puntatore \_ predefinito**</span><span class="sxs-lookup"><span data-stu-id="94671-124">**pointer\_default**</span></span>](pointer-default.md) | <span data-ttu-id="94671-125">Specifica il tipo di puntatore predefinito per tutti i puntatori tranne quelli inclusi negli elenchi di parametri.</span><span class="sxs-lookup"><span data-stu-id="94671-125">Specifies the default pointer type for all pointers except for those included in parameter lists.</span></span> <span data-ttu-id="94671-126">Il tipo predefinito può essere [**Unique**](unique.md), [**ref**](ref.md)o [**ptr**](ptr.md).</span><span class="sxs-lookup"><span data-stu-id="94671-126">The default type can be [**unique**](unique.md), [**ref**](ref.md), or [**ptr**](ptr.md).</span></span>                                                   |
| [<span data-ttu-id="94671-127">**endpoint**</span><span class="sxs-lookup"><span data-stu-id="94671-127">**endpoint**</span></span>](endpoint.md)                | <span data-ttu-id="94671-128">Specifica un endpoint statico (noto) in cui un'applicazione server resterà in ascolto delle chiamate a procedure remote.</span><span class="sxs-lookup"><span data-stu-id="94671-128">Specifies a static (well-known) endpoint on which a server application will listen for remote procedure calls.</span></span>                                                                                                                                   |



 

<span data-ttu-id="94671-129">Vedere [attributi della libreria dei tipi](type-library-attributes.md) per attributi di interfaccia, ad esempio [**Dual**](dual.md) e [**oleautomation**](oleautomation.md), specifici delle interfacce definite o a cui si fa riferimento all'interno di un'istruzione di libreria.</span><span class="sxs-lookup"><span data-stu-id="94671-129">See [Type Library Attributes](type-library-attributes.md) for interface attributes, such as [**dual**](dual.md) and [**oleautomation**](oleautomation.md), that are specific to interfaces defined or referenced inside a library statement.</span></span>

 

 




