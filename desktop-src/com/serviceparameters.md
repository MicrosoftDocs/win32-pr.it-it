---
title: ServiceParameters
description: Specifica i parametri della riga di comando da passare a un oggetto installato per l'uso da parte di COM tramite il valore del registro di sistema LocalService.
ms.assetid: da11e422-c0f2-4e44-9728-740ea6b61421
keywords:
- Valore ServiceParameters del registro di sistema COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 235de1052df72e88e2093647928ed68ab67451cd
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104330164"
---
# <a name="serviceparameters"></a><span data-ttu-id="fa165-104">ServiceParameters</span><span class="sxs-lookup"><span data-stu-id="fa165-104">ServiceParameters</span></span>

<span data-ttu-id="fa165-105">Specifica i parametri della riga di comando da passare a un oggetto installato per l'uso da parte di COM tramite il valore del registro di sistema [**LocalService**](localservice.md) .</span><span class="sxs-lookup"><span data-stu-id="fa165-105">Specifies the command-line parameters to be passed to an object installed for use by COM through the [**LocalService**](localservice.md) registry value.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="fa165-106">Voce del Registro di sistema</span><span class="sxs-lookup"><span data-stu-id="fa165-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\AppID
   {AppID_GUID}
      ServiceParameters = parameter
```

## <a name="remarks"></a><span data-ttu-id="fa165-107">Commenti</span><span class="sxs-lookup"><span data-stu-id="fa165-107">Remarks</span></span>

<span data-ttu-id="fa165-108">Si tratta di un valore **reg \_ SZ** .</span><span class="sxs-lookup"><span data-stu-id="fa165-108">This is a **REG\_SZ** value.</span></span> <span data-ttu-id="fa165-109">Questa stringa viene passata al servizio come argomento della riga di comando mentre viene avviata.</span><span class="sxs-lookup"><span data-stu-id="fa165-109">This string is passed to the service as a command-line argument as it is being launched.</span></span>

## <a name="related-topics"></a><span data-ttu-id="fa165-110">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="fa165-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fa165-111">**LocalService**</span><span class="sxs-lookup"><span data-stu-id="fa165-111">**LocalService**</span></span>](localservice.md)
</dt> <dt>

[<span data-ttu-id="fa165-112">Registrazione di server COM</span><span class="sxs-lookup"><span data-stu-id="fa165-112">Registering COM Servers</span></span>](registering-com-servers.md)
</dt> </dl>

 

 




