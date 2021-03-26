---
description: Per ottenere un GUID del provider o GUID di una classe di traccia eventi, è possibile usare lo strumento Uuidgen.exe o Guidgen.exe.
ms.assetid: 07483a78-ee67-4586-a75b-d376aa3351b7
title: Ottenere un provider e un GUID della classe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c12554cdb39459d824bf6622cd9d50e52f8c788d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980111"
---
# <a name="obtaining-a-provider-and-class-guid"></a><span data-ttu-id="9921c-103">Ottenere un provider e un GUID della classe</span><span class="sxs-lookup"><span data-stu-id="9921c-103">Obtaining a Provider and Class GUID</span></span>

<span data-ttu-id="9921c-104">Per ottenere un GUID del provider o GUID di una classe di traccia eventi, è possibile usare lo strumento Uuidgen.exe o Guidgen.exe.</span><span class="sxs-lookup"><span data-stu-id="9921c-104">To obtain a provider GUID or event trace class GUIDs, you can use the Uuidgen.exe or Guidgen.exe tool.</span></span>

<span data-ttu-id="9921c-105">Se si utilizza lo strumento Uuidgen.exe, utilizzare l'opzione-d per creare una macro Definisci \_ GUID C, come illustrato nell'esempio seguente.</span><span class="sxs-lookup"><span data-stu-id="9921c-105">If you use the Uuidgen.exe tool, use the -d option to create a DEFINE\_GUID C macro, as shown in the following example.</span></span> <span data-ttu-id="9921c-106">Per informazioni sull'utilizzo dello strumento Uuidgen.exe, utilizzare il-?</span><span class="sxs-lookup"><span data-stu-id="9921c-106">For information about using the Uuidgen.exe tool, use the -?</span></span> <span data-ttu-id="9921c-107">opzione.</span><span class="sxs-lookup"><span data-stu-id="9921c-107">option.</span></span> <span data-ttu-id="9921c-108">Se si usa la macro Definisci \_ GUID C per definire il GUID, è necessario includere \# define Initguid prima delle definizioni del GUID, come illustrato nell'esempio seguente.</span><span class="sxs-lookup"><span data-stu-id="9921c-108">If you use the DEFINE\_GUID C macro to define your GUID, you must include \#define INITGUID before your GUID definitions, as shown in the following example.</span></span>

``` syntax
#define INITGUID

DEFINE_GUID (
  ProviderGuid,
  0xf4dc272d, 
  0x88dd, 
  0x4472, 
  0xa3, 0xb1, 0xcb, 0x6d, 0xa4, 0x86, 0xf0, 0xbe
  );
```

<span data-ttu-id="9921c-109">Il Software Development Kit (SDK) di Microsoft Windows e Microsoft Visual Studio includono lo strumento Guidgen.exe.</span><span class="sxs-lookup"><span data-stu-id="9921c-109">The Microsoft Windows Software Development Kit (SDK) and Microsoft Visual Studio include the Guidgen.exe tool.</span></span> <span data-ttu-id="9921c-110">Lo strumento Guidgen.exe dispone di un'interfaccia utente che consente di scegliere tra diversi formati.</span><span class="sxs-lookup"><span data-stu-id="9921c-110">The Guidgen.exe tool has a user interface that lets you select from several formats.</span></span> <span data-ttu-id="9921c-111">È necessario usare il formato che consente di creare un GUID costante statico, come illustrato nell'esempio seguente.</span><span class="sxs-lookup"><span data-stu-id="9921c-111">You should use the format that creates a static constant GUID, as shown in the following example.</span></span>

``` syntax
// {7C214FB1-9CAC-4b8d-BAED-7BF48BF63BB3}
static const GUID ProviderGuid = 
{ 0x7c214fb1, 0x9cac, 0x4b8d, { 0xba, 0xed, 0x7b, 0xf4, 0x8b, 0xf6, 0x3b, 0xb3 } };
```

 

 



