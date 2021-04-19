---
title: File di registrazione dell'interfaccia
description: Il file di registrazione dell'interfaccia raccoglie informazioni che consentono di registrare le interfacce COM in un file DLL o EXE.
ms.assetid: 203303dc-121e-4bf4-b648-a35b956a56ee
keywords:
- file di registrazione dell'interfaccia MIDL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1fd6f54f5e027a0ea25dc463772ec24ee5f7386
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "106299754"
---
# <a name="the-interface-registration-file"></a><span data-ttu-id="de4e1-104">File di registrazione dell'interfaccia</span><span class="sxs-lookup"><span data-stu-id="de4e1-104">The Interface Registration File</span></span>

<span data-ttu-id="de4e1-105">Il file di registrazione dell'interfaccia raccoglie informazioni che consentono di registrare le interfacce COM in un file DLL o EXE.</span><span class="sxs-lookup"><span data-stu-id="de4e1-105">The interface registration file collects information that helps in the registration of COM interfaces packaged into a DLL or EXE file.</span></span> <span data-ttu-id="de4e1-106">Il file di registrazione dell'interfaccia è diverso dagli altri file generati perché può raccogliere informazioni dalla compilazione di più file IDL diversi.</span><span class="sxs-lookup"><span data-stu-id="de4e1-106">The interface registration file is different from other generated files because it can gather information from compiling several different IDL files.</span></span> <span data-ttu-id="de4e1-107">Ogni compilatore MIDL eseguito per le interfacce COM cerca innanzitutto un file dlldata. c esistente e, se il file non viene trovato, viene creato un nuovo file dlldata. c.</span><span class="sxs-lookup"><span data-stu-id="de4e1-107">Each MIDL compiler run for COM interfaces looks for an existing dlldata.c file first, and if the file is not found, a new dlldata.c file is created.</span></span> <span data-ttu-id="de4e1-108">Se viene trovato un file dlldata. c, le informazioni sull'IDL corrente vengono aggiunte (se assenti) o sostituite.</span><span class="sxs-lookup"><span data-stu-id="de4e1-108">If a dlldata.c file is found, information about the current IDL is added (if absent) or replaced.</span></span>

<span data-ttu-id="de4e1-109">Il file di registrazione dell'interfaccia viene generato o aggiornato in modo sicuro in un ambiente multiprocessore perché le compilazioni parallele MIDL non possono scrivere nel file nello stesso momento.</span><span class="sxs-lookup"><span data-stu-id="de4e1-109">The interface registration file is safely generated or updated in a multiprocessor environment because parallel MIDL compiles are prevented from writing to the file at the same time.</span></span> <span data-ttu-id="de4e1-110">Poiché qualsiasi file dlldata. c può essere contrassegnato come di sola lettura dall'ambiente di compilazione o dall'utente, il compilatore MIDL implementa un approccio di timeout per l'attesa di un file che non può essere aperto e genera un messaggio di errore appropriato se il timeout scade.</span><span class="sxs-lookup"><span data-stu-id="de4e1-110">Because any dlldata.c file can be marked as read-only by either the build environment or the user, the MIDL compiler implements a timeout approach to waiting on a file it cannot open, and issues an appropriate error message if the timeout expires.</span></span>

<span data-ttu-id="de4e1-111">Il nome predefinito per il file di registrazione dell'interfaccia generato da un file di input è dlldata. c.</span><span class="sxs-lookup"><span data-stu-id="de4e1-111">The default name for the interface registration file generated from an input file is dlldata.c.</span></span> <span data-ttu-id="de4e1-112">L'opzione del compilatore MIDL [**/dlldata**](-dlldata.md) può essere usata per eseguire l'override del nome predefinito del file.</span><span class="sxs-lookup"><span data-stu-id="de4e1-112">The [**/dlldata**](-dlldata.md) MIDL compiler switch can be used to override the default name of the file.</span></span> <span data-ttu-id="de4e1-113">L'override del nome predefinito del file di registrazione dell'interfaccia è particolarmente utile quando alcuni file IDL inclusi in un file binario comune si trovano in directory diverse.</span><span class="sxs-lookup"><span data-stu-id="de4e1-113">Overriding the default name of the interface registration file is especially useful when some IDL files packaged to a common binary reside in different directories.</span></span>

## <a name="related-topics"></a><span data-ttu-id="de4e1-114">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="de4e1-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="de4e1-115">Compilazione e registrazione di una DLL proxy</span><span class="sxs-lookup"><span data-stu-id="de4e1-115">Building and Registering a Proxy DLL</span></span>](../com/building-and-registering-a-proxy-dll.md)
</dt> </dl>

 

 