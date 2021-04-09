---
title: DefaultIcon
description: Fornisce informazioni sulle icone predefinite per le presentazioni iconiche degli oggetti.
ms.assetid: 45a3289b-d9c4-4857-bf48-1fd664ce4430
keywords:
- DefaultIcon chiave del registro di sistema COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0079fb02f4429c1939f54d643e0a6b08fbc90eb
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "104047415"
---
# <a name="defaulticon"></a><span data-ttu-id="72a4b-104">DefaultIcon</span><span class="sxs-lookup"><span data-stu-id="72a4b-104">DefaultIcon</span></span>

<span data-ttu-id="72a4b-105">Fornisce informazioni sulle icone predefinite per le presentazioni iconiche degli oggetti.</span><span class="sxs-lookup"><span data-stu-id="72a4b-105">Provides default icon information for iconic presentations of objects.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="72a4b-106">Voce del Registro di sistema</span><span class="sxs-lookup"><span data-stu-id="72a4b-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      DefaultIcon = path, resourceID
```

## <a name="remarks"></a><span data-ttu-id="72a4b-107">Commenti</span><span class="sxs-lookup"><span data-stu-id="72a4b-107">Remarks</span></span>

<span data-ttu-id="72a4b-108">Si tratta di un valore **reg \_ SZ** che specifica il percorso completo del nome dell'eseguibile dell'applicazione oggetto e l'indice di risorsa dell'icona all'interno del file eseguibile.</span><span class="sxs-lookup"><span data-stu-id="72a4b-108">This is a **REG\_SZ** value that specifies the full path to the executable name of the object application and the resource index of the icon within the executable.</span></span>

<span data-ttu-id="72a4b-109">**DefaultIcon** identifica l'icona da usare quando, ad esempio, un controllo è ridotto a icona.</span><span class="sxs-lookup"><span data-stu-id="72a4b-109">**DefaultIcon** identifies the icon to use when, for example, a control is minimized to an icon.</span></span> <span data-ttu-id="72a4b-110">Questa voce contiene il percorso completo del nome dell'eseguibile dell'applicazione server e l'indice di risorsa dell'icona all'interno del file eseguibile.</span><span class="sxs-lookup"><span data-stu-id="72a4b-110">This entry contains the full path to the executable name of the server application and the resource index of the icon within the executable.</span></span> <span data-ttu-id="72a4b-111">Le applicazioni possono usare le informazioni fornite da **DefaultIcon** per ottenere un handle di icona con [**ExtractIcon**](/windows/win32/api/shellapi/nf-shellapi-extracticona).</span><span class="sxs-lookup"><span data-stu-id="72a4b-111">Applications can use the information provided by **DefaultIcon** to obtain an icon handle with [**ExtractIcon**](/windows/win32/api/shellapi/nf-shellapi-extracticona).</span></span>

 

 