---
title: AuxUserType
description: Specifica il nome visualizzato breve e i nomi delle applicazioni di un'applicazione.
ms.assetid: 3367eb68-01f4-4cb9-b1d0-27554c28b68d
keywords:
- AuxUserType chiave del registro di sistema COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c66fcfbcdc2886e93d08040659b39c42d47c291
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103707033"
---
# <a name="auxusertype"></a><span data-ttu-id="5508f-104">AuxUserType</span><span class="sxs-lookup"><span data-stu-id="5508f-104">AuxUserType</span></span>

<span data-ttu-id="5508f-105">Specifica il nome visualizzato breve e i nomi delle applicazioni di un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="5508f-105">Specifies an application's short display name and application names.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="5508f-106">Voce del Registro di sistema</span><span class="sxs-lookup"><span data-stu-id="5508f-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      AuxUserType
         2 = ShortDisplayName
         3 = ApplicationName
```

## <a name="remarks"></a><span data-ttu-id="5508f-107">Commenti</span><span class="sxs-lookup"><span data-stu-id="5508f-107">Remarks</span></span>

<span data-ttu-id="5508f-108">La lunghezza massima consigliata per *ShortDisplayName* è di 15 caratteri.</span><span class="sxs-lookup"><span data-stu-id="5508f-108">The recommended maximum length for *ShortDisplayName* is 15 characters.</span></span> <span data-ttu-id="5508f-109">Questo nome viene usato nei menu, inclusi i menu a comparsa.</span><span class="sxs-lookup"><span data-stu-id="5508f-109">This name is used in menus, including pop-up menus.</span></span>

<span data-ttu-id="5508f-110">*ApplicationName* deve contenere il nome effettivo dell'applicazione, ad esempio "Acme disegnato 2,0".</span><span class="sxs-lookup"><span data-stu-id="5508f-110">*ApplicationName* should contain the actual name of the application (such as "Acme Draw 2.0").</span></span> <span data-ttu-id="5508f-111">Questo nome viene usato nel campo **risultati** della finestra di dialogo **Incolla speciale** .</span><span class="sxs-lookup"><span data-stu-id="5508f-111">This name is used in the **Results** field of the **Paste Special** dialog box.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5508f-112">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="5508f-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5508f-113">**IOleObject:: GetUserType**</span><span class="sxs-lookup"><span data-stu-id="5508f-113">**IOleObject::GetUserType**</span></span>](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-getusertype)
</dt> </dl>

 

 




