---
title: Enumerazione delle risorse
description: In questo argomento vengono illustrate le funzioni usate per ottenere elenchi di risorse.
ms.assetid: 388deaa1-3b04-43fa-aad2-8b52376d570c
ms.topic: article
ms.date: 05/31/2018
ms.custom: project-verbatim
ms.openlocfilehash: b978636303f3fc5bcae8c1d854289dde42ae0247
ms.sourcegitcommit: 78ce1d1e3f12ee3e08390868e5b93c034f437657
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/10/2021
ms.locfileid: "111910270"
---
# <a name="enumerating-resources"></a><span data-ttu-id="1ee91-103">Enumerazione delle risorse</span><span class="sxs-lookup"><span data-stu-id="1ee91-103">Enumerating resources</span></span>

<span data-ttu-id="1ee91-104">In alcune situazioni può essere necessario individuare il contenuto delle risorse di un modulo PE (Portable Executable) sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="1ee91-104">In certain situations, you might want to discover the resource contents of an unknown portable executable (PE) module.</span></span> <span data-ttu-id="1ee91-105">Il Windows SDK funzioni di enumerazione delle risorse che consentono all'applicazione di ottenere elenchi di tipi di risorse, nomi e linguaggi in un modulo specificato.</span><span class="sxs-lookup"><span data-stu-id="1ee91-105">The Windows SDK provides resource enumeration functions that enable your application to obtain lists of resource types, names, and languages in a specified module.</span></span>

* <span data-ttu-id="1ee91-106">Le [**funzioni EnumResourceTypeW**](/windows/win32/api/Winbase/nf-winbase-enumresourcetypesw) [**ed EnumResourceTypesExW**](/windows/win32/api/libloaderapi/nf-libloaderapi-enumresourcetypesexw) forniscono un elenco dei tipi di risorse disponibili nel modulo.</span><span class="sxs-lookup"><span data-stu-id="1ee91-106">The [**EnumResourceTypeW**](/windows/win32/api/Winbase/nf-winbase-enumresourcetypesw) and [**EnumResourceTypesExW**](/windows/win32/api/libloaderapi/nf-libloaderapi-enumresourcetypesexw) functions provide a list of resource types found in the module.</span></span>
* <span data-ttu-id="1ee91-107">Le [**funzioni EnumResourceNamesW**](/windows/win32/api/libloaderapi/nf-libloaderapi-enumresourcenamesw) ed [**EnumResourceNamesExW**](/windows/win32/api/libloaderapi/nf-libloaderapi-enumresourcenamesexw) forniscono il nome di ogni risorsa all'interno di un determinato tipo.</span><span class="sxs-lookup"><span data-stu-id="1ee91-107">The [**EnumResourceNamesW**](/windows/win32/api/libloaderapi/nf-libloaderapi-enumresourcenamesw) and [**EnumResourceNamesExW**](/windows/win32/api/libloaderapi/nf-libloaderapi-enumresourcenamesexw) functions provide the name of each resource within a given type.</span></span>
* <span data-ttu-id="1ee91-108">Le [**funzioni EnumResourceLanguagesW**](/windows/win32/api/Winbase/nf-winbase-enumresourcelanguagesw) ed [**EnumResourceLanguagesExW**](/windows/win32/api/libloaderapi/nf-libloaderapi-enumresourcelanguagesexw) forniscono la lingua di ogni risorsa di un determinato nome e tipo.</span><span class="sxs-lookup"><span data-stu-id="1ee91-108">The [**EnumResourceLanguagesW**](/windows/win32/api/Winbase/nf-winbase-enumresourcelanguagesw) and [**EnumResourceLanguagesExW**](/windows/win32/api/libloaderapi/nf-libloaderapi-enumresourcelanguagesexw) functions provide the language of each resource of a given name and type.</span></span> 

<span data-ttu-id="1ee91-109">Queste funzioni e le funzioni di callback associate consentono all'applicazione di creare un elenco di tutte le risorse in un modulo.</span><span class="sxs-lookup"><span data-stu-id="1ee91-109">These functions and their associated callback functions enable your application to create a list of all resources in a module.</span></span> <span data-ttu-id="1ee91-110">Questo processo è descritto in [Creazione di un elenco di risorse.](using-resources.md)</span><span class="sxs-lookup"><span data-stu-id="1ee91-110">This process is described in [Creating a resource list](using-resources.md).</span></span>

## <a name="-see-also"></a><span data-ttu-id="1ee91-111">-see-also</span><span class="sxs-lookup"><span data-stu-id="1ee91-111">-see-also</span></span>

[<span data-ttu-id="1ee91-112">Msistuff.exe app di esempio</span><span class="sxs-lookup"><span data-stu-id="1ee91-112">Msistuff.exe sample app</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/sysmgmt/msi/msistuff)
