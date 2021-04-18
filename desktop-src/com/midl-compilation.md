---
title: Compilazione MIDL
description: Compilazione MIDL
ms.assetid: 2797ee3b-82fd-4cb5-9e95-23b2f2a8f011
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e281fa66ec1b8f997dd58fc55a67c19a801d2d36
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "104474342"
---
# <a name="midl-compilation"></a><span data-ttu-id="4ed97-103">Compilazione MIDL</span><span class="sxs-lookup"><span data-stu-id="4ed97-103">MIDL Compilation</span></span>

<span data-ttu-id="4ed97-104">Dato un file IDL, ad esempio [example2. idl](anatomy-of-an-idl-file.md), che definisce una o più interfacce com e una libreria dei tipi, il compilatore MIDL (Midl.exe) genera i file descritti nella tabella seguente come output predefinito.</span><span class="sxs-lookup"><span data-stu-id="4ed97-104">Given an IDL file, such as [Example2.idl](anatomy-of-an-idl-file.md), that defines one or more COM interfaces and a type library, the MIDL compiler (Midl.exe) generates the files described in the following table as the default output.</span></span>



| <span data-ttu-id="4ed97-105">Nome file</span><span class="sxs-lookup"><span data-stu-id="4ed97-105">Filename</span></span>                 | <span data-ttu-id="4ed97-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4ed97-106">Description</span></span>                                                                                                                                                                                           |
|--------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4ed97-107">Example2. h</span><span class="sxs-lookup"><span data-stu-id="4ed97-107">Example2.h</span></span><br/>    | <span data-ttu-id="4ed97-108">Il file di intestazione, che contiene le definizioni di tipo e le dichiarazioni di funzione per tutte le interfacce definite nel file IDL, nonché le dichiarazioni con il nome per le routine chiamate dagli stub.</span><span class="sxs-lookup"><span data-stu-id="4ed97-108">The header file, containing type definitions and function declarations for all of the interfaces defined in the IDL file as well as forward declarations for routines that the stubs call.</span></span><br/> |
| <span data-ttu-id="4ed97-109">Example2 \_ p. c</span><span class="sxs-lookup"><span data-stu-id="4ed97-109">Example2\_p.c</span></span><br/> | <span data-ttu-id="4ed97-110">Il file proxy/stub, che include i punti di ingresso surrogati per i client e per i server.</span><span class="sxs-lookup"><span data-stu-id="4ed97-110">The proxy/stub file, which includes the surrogate entry points both for clients and for servers.</span></span><br/>                                                                                           |
| <span data-ttu-id="4ed97-111">Example2 \_ i. c</span><span class="sxs-lookup"><span data-stu-id="4ed97-111">Example2\_i.c</span></span><br/> | <span data-ttu-id="4ed97-112">Il file dell'ID di interfaccia, che definisce il GUID per ogni interfaccia specificata nel file IDL.</span><span class="sxs-lookup"><span data-stu-id="4ed97-112">The interface ID file, which defines the GUID for every interface specified in the IDL file.</span></span><br/>                                                                                               |
| <span data-ttu-id="4ed97-113">Example2. tlb</span><span class="sxs-lookup"><span data-stu-id="4ed97-113">Example2.tlb</span></span><br/>  | <span data-ttu-id="4ed97-114">Un file di documento composto che contiene informazioni su tipi e oggetti.</span><span class="sxs-lookup"><span data-stu-id="4ed97-114">A compound document file that contains information about types and objects.</span></span><br/>                                                                                                                |
| <span data-ttu-id="4ed97-115">Dlldata. c</span><span class="sxs-lookup"><span data-stu-id="4ed97-115">Dlldata.c</span></span><br/>     | <span data-ttu-id="4ed97-116">Contiene i dati necessari per creare una DLL proxy/stub.</span><span class="sxs-lookup"><span data-stu-id="4ed97-116">Contains the data you need to create a proxy/stub DLL.</span></span><br/>                                                                                                                                     |



 

<span data-ttu-id="4ed97-117">Utilizzare il file di intestazione e tutti i file con estensione c per [creare una DLL proxy](building-and-registering-a-proxy-dll.md) in grado di supportare l'interfaccia quando viene utilizzata da applicazioni client e da server oggetti.</span><span class="sxs-lookup"><span data-stu-id="4ed97-117">You use the header file and all of the .c files to [create a proxy DLL](building-and-registering-a-proxy-dll.md) that can support the interface when used both by client applications and by object servers.</span></span> <span data-ttu-id="4ed97-118">Usare il file di intestazione dell'interfaccia (example2. h) e il file dell'ID di interfaccia (example2 \_ i. c) quando si crea il file eseguibile per un'applicazione client che usa l'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="4ed97-118">You use the interface header file (Example2.h) and the interface ID (Example2\_i.c) file when creating the executable file for a client application that uses the interface.</span></span> <span data-ttu-id="4ed97-119">È possibile scegliere di includere il file della libreria dei tipi come risorsa nel file EXE o DLL oppure è possibile inviarlo come file separato.</span><span class="sxs-lookup"><span data-stu-id="4ed97-119">You can choose to include the type library file as a resource in your EXE or DLL, or you can ship it as a separate file.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4ed97-120">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="4ed97-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4ed97-121">File generati per un'interfaccia COM</span><span class="sxs-lookup"><span data-stu-id="4ed97-121">Files Generated for a COM Interface</span></span>](/windows/desktop/Midl/files-generated-for-a-com-interface)
</dt> <dt>

[<span data-ttu-id="4ed97-122">Opzioni del compilatore MIDL</span><span class="sxs-lookup"><span data-stu-id="4ed97-122">MIDL Compiler Options</span></span>](midl-compiler-options.md)
</dt> </dl>

 

