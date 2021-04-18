---
title: File segnaposto
description: File segnaposto
ms.assetid: E14655DA-CEA0-4106-B882-C9E9116FC234
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93c15037b0daec7a6521a299b6c4587c956e0be3
ms.sourcegitcommit: 46376be61d3fa308f9b1a06d7e2fa122a39755af
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/10/2020
ms.locfileid: "106300637"
---
# <a name="placeholder-files"></a><span data-ttu-id="5f84a-103">File segnaposto</span><span class="sxs-lookup"><span data-stu-id="5f84a-103">Placeholder files</span></span>

## <a name="platform"></a><span data-ttu-id="5f84a-104">Piattaforma</span><span class="sxs-lookup"><span data-stu-id="5f84a-104">Platform</span></span>

<span data-ttu-id="5f84a-105">**Client-** Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="5f84a-105">**Clients -** Windows 8.1</span></span>  
<span data-ttu-id="5f84a-106">**Server-** Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="5f84a-106">**Servers -** Windows Server 2012 R2</span></span>  

## <a name="description"></a><span data-ttu-id="5f84a-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5f84a-107">Description</span></span>

<span data-ttu-id="5f84a-108">I file segnaposto consentono agli utenti di visualizzare e gestire i file di Microsoft OneDrive indipendentemente dalla connettività.</span><span class="sxs-lookup"><span data-stu-id="5f84a-108">Placeholder files enable users to view and manage Microsoft OneDrive files regardless of connectivity.</span></span> <span data-ttu-id="5f84a-109">I file segnaposto rappresentano lo spazio dei nomi OneDrive, anche quando i file non sono memorizzati nella cache locale.</span><span class="sxs-lookup"><span data-stu-id="5f84a-109">Placeholder files represent the OneDrive namespace, even when files are not cached locally.</span></span> <span data-ttu-id="5f84a-110">Contengono i metadati dei file e le immagini di anteprima delle foto.</span><span class="sxs-lookup"><span data-stu-id="5f84a-110">They contain file metadata and thumbnail images of photos.</span></span>

## <a name="manifestation"></a><span data-ttu-id="5f84a-111">Manifestazione</span><span class="sxs-lookup"><span data-stu-id="5f84a-111">Manifestation</span></span>

<span data-ttu-id="5f84a-112">Per gli utenti e gli sviluppatori finali, i file segnaposto sembrano comportarsi quasi come i file locali.</span><span class="sxs-lookup"><span data-stu-id="5f84a-112">To end users and developers, placeholder files look and behave almost the same as the local files.</span></span>

<span data-ttu-id="5f84a-113">Se l'app usa la finestra di dialogo file comune per enumerare la file system, l'app non verrà interessata.</span><span class="sxs-lookup"><span data-stu-id="5f84a-113">If your app uses the Common File Dialog to enumerate the file system, your app will not be impacted.</span></span> <span data-ttu-id="5f84a-114">Quando l'utente tenta di aprire il file dalla finestra di dialogo/file comune, il contenuto del file verrà scaricato e verrà passato all'app.</span><span class="sxs-lookup"><span data-stu-id="5f84a-114">When the user tries to open the file from the common /file Dialog, the file content will be downloaded and will be passed to your app.</span></span>

<span data-ttu-id="5f84a-115">Se l'app accede direttamente al file system, è possibile che l'app sfrutti i file segnaposto usando le linee guida riportate di seguito.</span><span class="sxs-lookup"><span data-stu-id="5f84a-115">If your app accesses the file system directly, then your app may take advantage of the placeholder files by using the guidelines below.</span></span>

## <a name="solution"></a><span data-ttu-id="5f84a-116">Soluzione</span><span class="sxs-lookup"><span data-stu-id="5f84a-116">Solution</span></span>

-   <span data-ttu-id="5f84a-117">I segnaposto sono nascosti per convenzione in base agli attributi</span><span class="sxs-lookup"><span data-stu-id="5f84a-117">Placeholders are hidden by convention based on attributes</span></span>
-   <span data-ttu-id="5f84a-118">Identificare i segnaposto usando reparse Tag ID i/o \_ \_ file di tag \_ \_ segnaposto</span><span class="sxs-lookup"><span data-stu-id="5f84a-118">Identify placeholders using reparse tag ID IO\_REPARSE\_TAG\_FILE\_PLACEHOLDER</span></span>

<span data-ttu-id="5f84a-119">Usare il modello di dati della Shell per un comportamento uniforme:</span><span class="sxs-lookup"><span data-stu-id="5f84a-119">Use the shell data model for seamless behavior:</span></span>

-   <span data-ttu-id="5f84a-120">Usare SHCreateItemFromParsingName () per creare un elemento della shell</span><span class="sxs-lookup"><span data-stu-id="5f84a-120">Use SHCreateItemFromParsingName() to create a shell item</span></span>
-   <span data-ttu-id="5f84a-121">Eseguire l'associazione al flusso usando IShellItem:: BindToHandler ( \_ flusso BHID)</span><span class="sxs-lookup"><span data-stu-id="5f84a-121">Bind to the stream using IShellItem::BindToHandler(BHID\_Stream)</span></span>
-   <span data-ttu-id="5f84a-122">Gestore proprietà utente per l'accesso alle proprietà (IShellItem2:: GetPropertyHandler)</span><span class="sxs-lookup"><span data-stu-id="5f84a-122">User property handler for property access (IShellItem2::GetPropertyHandler)</span></span>
-   <span data-ttu-id="5f84a-123">Thumbnailhandler della shell utente per ottenere le immagini di anteprima per i segnaposto</span><span class="sxs-lookup"><span data-stu-id="5f84a-123">User shell thumbnailhandler to get thumbnail images for placeholders</span></span>
-   <span data-ttu-id="5f84a-124">Specificare SupportedProtocols: recupera = nell' \* implementazione del verbo se il verbo viene associato al flusso tramite BindToHandler</span><span class="sxs-lookup"><span data-stu-id="5f84a-124">Specify SupportedProtocols=\* on your verb implementation if the verb binds to the stream via BindToHandler</span></span>


```
#include <winnth> //for IO_REPARSE_TAG_FILE_PLACEHOLDER
//  Helper that indicates this is a 
bool IsFilePlaceholder(WIN32_FIND_DATA const &findData)
{
  return (findData.dwFileAttributes & FILE_ATTRIBUTE_REPARSE_POINT) &&
    (findData.dwReserved0 == IO_REPARSE_TAG_FILE_PLACEHOLDER);
}
bool IsFilePlaceholder(_In_PCWSTR filePath)
{
  bool isPlaceholder = false;
  WIN32_FIND_DATA findData;
  HANDLE hFind = FindFirstFile(filePath, &findData);
  if (hFind ! = INVALID_HANDLE_VALUE)
  {
    isPlaceholder = (findData.dwFileAttributes &    FILE_ATTRIBUTE_REPARSE_POINT) &&
    (findData.dwReserved0 == IO_REPARSE_TAG_FILE_PLACEHOLDER);
    FindClose(hFind);
  }
  Return isPlaceholder;
}
```



 

 




