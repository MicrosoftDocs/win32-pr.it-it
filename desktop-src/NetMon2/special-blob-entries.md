---
description: Negli esempi seguenti viene usata la funzione SetStringInBlob per creare voci di BLOB speciali.
ms.assetid: 4a921b0d-9934-48e2-8837-be0bd7b7fa7a
title: Voci BLOB speciali
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5cfc40029e0a0f88c2f7bd242881b0d750a5dfa1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103752175"
---
# <a name="special-blob-entries"></a><span data-ttu-id="59107-103">Voci BLOB speciali</span><span class="sxs-lookup"><span data-stu-id="59107-103">Special BLOB Entries</span></span>

<span data-ttu-id="59107-104">Negli esempi seguenti viene usata la funzione [**SetStringInBlob**](setstringinblob.md) per creare voci di BLOB speciali.</span><span class="sxs-lookup"><span data-stu-id="59107-104">The following examples use the [**SetStringInBlob**](setstringinblob.md) function to create special BLOB entries.</span></span>

## <a name="npp-name"></a><span data-ttu-id="59107-105">Nome della NPP</span><span class="sxs-lookup"><span data-stu-id="59107-105">NPP Name</span></span>

``` syntax
SetStringInBlob(
   hBlob,
   OWNER_NPP,
   CATEGORY_LOCATION,
   TAG_NAME,
   "My NPP Name"); 
```

## <a name="npp-class-identifier"></a><span data-ttu-id="59107-106">Identificatore di classe NPP</span><span class="sxs-lookup"><span data-stu-id="59107-106">NPP Class Identifier</span></span>

``` syntax
SetClassIDInBlob(
   hBlob,
   OWNER_NPP,
   CATEGORY_LOCATION,
   TAG_CLASSID,
   &CLSID_ThisNPP);
```

## <a name="cfgproc-procedure-name"></a><span data-ttu-id="59107-107">Nome della procedura CFGPROC</span><span class="sxs-lookup"><span data-stu-id="59107-107">CFGPROC Procedure Name</span></span>

``` syntax
SetStringInBlob(
   hBlob,
   OWNER_NPP,
   CATEGORY_FINDER,
   TAG_PROCNAME,
   "MyGetNPPBlobs");
```

## <a name="tree-root-name-for-finder-ui"></a><span data-ttu-id="59107-108">Nome radice dell'albero per l'interfaccia utente di Finder</span><span class="sxs-lookup"><span data-stu-id="59107-108">Tree Root Name for Finder UI</span></span>

``` syntax
SetStringInBlob(
   hBlob,
   OWNER_NPP,
   CATEGORY_FINDER,
   TAG_ROOT,
   "My Tree Root name");
```

## <a name="display-string-for-finder-ui"></a><span data-ttu-id="59107-109">Stringa di visualizzazione per l'interfaccia utente di Finder</span><span class="sxs-lookup"><span data-stu-id="59107-109">Display String for Finder UI</span></span>

``` syntax
SetStringInBlob(
   hBlob,
   OWNER_NPP,
   CATEGORY_FINDER,
   TAG_DISP_STRING,
   "Double click to select my UI");
```

## <a name="interface-tags"></a><span data-ttu-id="59107-110">Tag di interfaccia</span><span class="sxs-lookup"><span data-stu-id="59107-110">Interface Tags</span></span>

<span data-ttu-id="59107-111">Questo esempio include tutte le interfacce supportate dall'oggetto NPP.</span><span class="sxs-lookup"><span data-stu-id="59107-111">This example includes every interface supported by the NPP.</span></span>

``` syntax
SetBoolInBlob(  
   hBlob,
   OWNER_NPP,
   CATEGORY_CONFIG,
   TAG_INTERFACE_REALTIME_CAPTURE,
   TRUE);
```

 

 



