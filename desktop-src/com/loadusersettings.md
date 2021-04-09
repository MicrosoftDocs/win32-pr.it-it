---
title: LoadUserSettings
description: Determina se COM caricherà il profilo utente per i server COM in esecuzione come identità dell'applicazione di avvio dell'utente.
ms.assetid: 3e2b3249-3747-4d98-96da-f3e480a51d12
keywords:
- Valore LoadUserSettings del registro di sistema COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e14282b00bc2c2d9b989e19480047f115623d55
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955666"
---
# <a name="loadusersettings"></a><span data-ttu-id="300c1-104">LoadUserSettings</span><span class="sxs-lookup"><span data-stu-id="300c1-104">LoadUserSettings</span></span>

<span data-ttu-id="300c1-105">Determina se COM caricherà il profilo utente per i server COM in esecuzione come identità dell'applicazione di avvio dell'utente.</span><span class="sxs-lookup"><span data-stu-id="300c1-105">Determines whether COM will load the user profile for COM servers running as the launching user application identity.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="300c1-106">Voce del Registro di sistema</span><span class="sxs-lookup"><span data-stu-id="300c1-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\AppID
   {AppID_GUID}
      LoadUserSettings = value
```

## <a name="remarks"></a><span data-ttu-id="300c1-107">Commenti</span><span class="sxs-lookup"><span data-stu-id="300c1-107">Remarks</span></span>

<span data-ttu-id="300c1-108">Si tratta di un valore **reg \_ DWORD** .</span><span class="sxs-lookup"><span data-stu-id="300c1-108">This is a **REG\_DWORD** value.</span></span> <span data-ttu-id="300c1-109">Se il *valore* è diverso da zero, com carica il profilo dell'account utente con il quale avvia il server com.</span><span class="sxs-lookup"><span data-stu-id="300c1-109">If *value* is nonzero, COM loads the profile of the user account with which it launches the COM server.</span></span> <span data-ttu-id="300c1-110">Se il *valore* è zero o non è presente, com non caricherà il profilo dell'account utente con cui viene avviato il server com.</span><span class="sxs-lookup"><span data-stu-id="300c1-110">If *value* is zero or not present, COM will not load the profile of the user account with which it launches the COM server.</span></span>

<span data-ttu-id="300c1-111">Questa impostazione viene ignorata se è presente una voce [**RunAs**](runas.md) .</span><span class="sxs-lookup"><span data-stu-id="300c1-111">This setting is ignored if a [**RunAs**](runas.md) entry is present.</span></span>

 

 




