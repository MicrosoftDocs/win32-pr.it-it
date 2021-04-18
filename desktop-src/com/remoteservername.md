---
title: RemoteServerName
description: Configura il client per richiedere che l'oggetto venga eseguito in un determinato computer ogni volta che viene chiamata una funzione di attivazione per la quale non è specificata una struttura COSERVERINFO.
ms.assetid: 0413564e-e8ba-4e6e-ad29-62997c63aab3
keywords:
- Valore RemoteServerName del registro di sistema COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0634d858b04fbbdf5d3a6024dbd9fdea4ee06d99
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "106300552"
---
# <a name="remoteservername"></a><span data-ttu-id="43582-104">RemoteServerName</span><span class="sxs-lookup"><span data-stu-id="43582-104">RemoteServerName</span></span>

<span data-ttu-id="43582-105">Configura il client per richiedere che l'oggetto venga eseguito in un determinato computer ogni volta che viene chiamata una funzione di attivazione per la quale non è specificata una struttura [**COSERVERINFO**](/windows/win32/api/objidlbase/ns-objidlbase-coserverinfo) .</span><span class="sxs-lookup"><span data-stu-id="43582-105">Configures the client to request the object be run at a particular computer whenever an activation function is called for which a [**COSERVERINFO**](/windows/win32/api/objidlbase/ns-objidlbase-coserverinfo) structure is not specified.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="43582-106">Voce del Registro di sistema</span><span class="sxs-lookup"><span data-stu-id="43582-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\AppID
   {AppID_GUID}
      RemoteServerName = name
```

## <a name="remarks"></a><span data-ttu-id="43582-107">Commenti</span><span class="sxs-lookup"><span data-stu-id="43582-107">Remarks</span></span>

<span data-ttu-id="43582-108">**RemoteServerName** consente una gestione semplificata della configurazione delle applicazioni client. possono essere scritti senza nomi di server hardcoded e possono essere configurati modificando i valori del registro di sistema **RemoteServerName** delle classi di oggetti usati.</span><span class="sxs-lookup"><span data-stu-id="43582-108">**RemoteServerName** allows simple configuration management of client applications; they may be written without hard-coded server names and can be configured by modifying the **RemoteServerName** registry values of the classes of objects they use.</span></span>

<span data-ttu-id="43582-109">Come descritto nella documentazione per l'enumerazione [**CLSCTX**](/windows/win32/api/wtypesbase/ne-wtypesbase-clsctx) e la struttura [**COSERVERINFO**](/windows/win32/api/objidlbase/ns-objidlbase-coserverinfo) , uno dei parametri dell'attivazione com distribuita è un puntatore a una struttura **COSERVERINFO** .</span><span class="sxs-lookup"><span data-stu-id="43582-109">As described in the documentation for the [**CLSCTX**](/windows/win32/api/wtypesbase/ne-wtypesbase-clsctx) enumeration and the [**COSERVERINFO**](/windows/win32/api/objidlbase/ns-objidlbase-coserverinfo) structure, one of the parameters of the distributed COM activation is a pointer to a **COSERVERINFO** structure.</span></span> <span data-ttu-id="43582-110">Quando questo valore non è **null**, le informazioni nella struttura **COSERVERINFO** eseguono l'override dell'impostazione della chiave **RemoteServerName** per la chiamata di funzione.</span><span class="sxs-lookup"><span data-stu-id="43582-110">When this value is not **NULL**, the information in the **COSERVERINFO** structure overrides the setting of the **RemoteServerName** key for the function call.</span></span>

## <a name="related-topics"></a><span data-ttu-id="43582-111">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="43582-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="43582-112">Registrazione di server COM</span><span class="sxs-lookup"><span data-stu-id="43582-112">Registering COM Servers</span></span>](registering-com-servers.md)
</dt> </dl>

 

 