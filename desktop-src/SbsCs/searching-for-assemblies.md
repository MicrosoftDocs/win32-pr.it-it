---
description: Esistono due metodi mediante i quali un'applicazione host può cercare gli assembly affiancati.
ms.assetid: f34f8f39-f03c-4adf-afa8-9cb9ed48d149
title: Ricerca di assembly
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f257b7da8099508fb268623a175d8ebd8e9d8337
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317094"
---
# <a name="searching-for-assemblies"></a><span data-ttu-id="105ad-103">Ricerca di assembly</span><span class="sxs-lookup"><span data-stu-id="105ad-103">Searching for Assemblies</span></span>

<span data-ttu-id="105ad-104">Esistono due metodi mediante i quali un'applicazione host può cercare gli assembly affiancati.</span><span class="sxs-lookup"><span data-stu-id="105ad-104">There are two methods by which a hosting application can search for side-by-side assemblies.</span></span>

<span data-ttu-id="105ad-105">I moduli ospitati possono registrarsi con l'applicazione host estendendo alcune informazioni di configurazione condivise.</span><span class="sxs-lookup"><span data-stu-id="105ad-105">Hosted modules can register themselves with the hosting application by extending some shared configuration information.</span></span> <span data-ttu-id="105ad-106">L'applicazione può quindi utilizzare queste informazioni di configurazione per caricare gli assembly necessari per la nuova funzionalità.</span><span class="sxs-lookup"><span data-stu-id="105ad-106">The application can then use this configuration information to load the assemblies required for the new functionality.</span></span> <span data-ttu-id="105ad-107">Questa operazione può essere eseguita chiamando [**CreateActCtx**](/windows/desktop/api/Winbase/nf-winbase-createactctxa) nei manifesti specificati nei dati di registrazione, seguito dalla chiamata a [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) o [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) per accedere al nuovo modulo.</span><span class="sxs-lookup"><span data-stu-id="105ad-107">This could be done by calling [**CreateActCtx**](/windows/desktop/api/Winbase/nf-winbase-createactctxa) on manifests specified in the registration data, followed by calling [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) or [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) to get into the new module.</span></span> <span data-ttu-id="105ad-108">Si noti che con questo metodo, i nuovi componenti devono aggiornare lo stato di un'applicazione condivisa per indicare la loro presenza.</span><span class="sxs-lookup"><span data-stu-id="105ad-108">Note that with this method, the new components have to update some shared application state to indicate their presence.</span></span>

<span data-ttu-id="105ad-109">L'applicazione host può cercare attivamente gli assembly all'avvio usando [**FindFirstFile**](/windows/desktop/api/fileapi/nf-fileapi-findfirstfilea) e [**FindNextFile**](/windows/desktop/api/fileapi/nf-fileapi-findnextfilea) per cercare le dll o i manifesti in un percorso specificato e quindi usare [**CreateActCtx**](/windows/desktop/api/Winbase/nf-winbase-createactctxa) per accedere alle informazioni.</span><span class="sxs-lookup"><span data-stu-id="105ad-109">The hosting application can actively search for the assemblies on startup using [**FindFirstFile**](/windows/desktop/api/fileapi/nf-fileapi-findfirstfilea) and [**FindNextFile**](/windows/desktop/api/fileapi/nf-fileapi-findnextfilea) to look for DLLs or manifests in a specified location, and then use [**CreateActCtx**](/windows/desktop/api/Winbase/nf-winbase-createactctxa) to access the information.</span></span> <span data-ttu-id="105ad-110">Questo metodo non richiede la registrazione del componente.</span><span class="sxs-lookup"><span data-stu-id="105ad-110">This method requires no registration of the component.</span></span>

 

 
