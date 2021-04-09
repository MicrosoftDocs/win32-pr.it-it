---
title: ActivateAtStorage
description: Configura il client per creare un'istanza degli oggetti nello stesso computer dello stato persistente utilizzato o da cui vengono inizializzati.
ms.assetid: bc0f0c1c-dbfc-4b7a-b897-3646afe3f6bb
keywords:
- valore del registro di sistema COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2ddd1330191d7b7baf37973dbfb40e267a2f87e
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "104047450"
---
# <a name="activateatstorage"></a><span data-ttu-id="653af-104">ActivateAtStorage</span><span class="sxs-lookup"><span data-stu-id="653af-104">ActivateAtStorage</span></span>

<span data-ttu-id="653af-105">Configura il client per creare un'istanza degli oggetti nello stesso computer dello stato persistente utilizzato o da cui vengono inizializzati.</span><span class="sxs-lookup"><span data-stu-id="653af-105">Configures the client to instantiate objects on the same computer as the persistent state they are using or from which they are initialized.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="653af-106">Voce del Registro di sistema</span><span class="sxs-lookup"><span data-stu-id="653af-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\AppID
   {AppID_GUID}
      ActivateAtStorage = value
```

## <a name="remarks"></a><span data-ttu-id="653af-107">Commenti</span><span class="sxs-lookup"><span data-stu-id="653af-107">Remarks</span></span>

<span data-ttu-id="653af-108">Si tratta di un valore **reg \_ SZ** .</span><span class="sxs-lookup"><span data-stu-id="653af-108">This is a **REG\_SZ** value.</span></span> <span data-ttu-id="653af-109">Qualsiasi valore che inizia con ' Y ' o ' y ' indica che è necessario usare **ActivateAtStorage** .</span><span class="sxs-lookup"><span data-stu-id="653af-109">Any value that begins with 'Y' or 'y' indicates that **ActivateAtStorage** should be used.</span></span>

<span data-ttu-id="653af-110">La funzionalità **ActivateAtStorage** fornisce un modo trasparente per consentire ai client di individuare gli oggetti in esecuzione nello stesso computer dei dati utilizzati.</span><span class="sxs-lookup"><span data-stu-id="653af-110">The **ActivateAtStorage** capability provides a transparent way to allow clients to locate running objects on the same computer as the data that they use.</span></span> <span data-ttu-id="653af-111">In questo modo, il traffico di rete viene ridotto perché l'oggetto esegue chiamate a file system locali invece che chiamate attraverso la rete.</span><span class="sxs-lookup"><span data-stu-id="653af-111">This reduces network traffic because the object performs local file-system calls instead of calls across the network.</span></span>

<span data-ttu-id="653af-112">Quando viene impostato un valore per **ActivateAtStorage**, questo diventa il comportamento predefinito nelle chiamate alle funzioni [**CoGetInstanceFromFile**](/windows/desktop/api/Objbase/nf-objbase-cogetinstancefromfile) e [**CoGetInstanceFromIStorage**](/windows/desktop/api/Objbase/nf-objbase-cogetinstancefromistorage) e all'implementazione del moniker di file di [**IMoniker:: BindToObject**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtoobject).</span><span class="sxs-lookup"><span data-stu-id="653af-112">When a value is set for **ActivateAtStorage**, this becomes the default behavior in calls to the [**CoGetInstanceFromFile**](/windows/desktop/api/Objbase/nf-objbase-cogetinstancefromfile) and [**CoGetInstanceFromIStorage**](/windows/desktop/api/Objbase/nf-objbase-cogetinstancefromistorage) functions, as well as to the file moniker implementation of [**IMoniker::BindToObject**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtoobject).</span></span> <span data-ttu-id="653af-113">In tutte queste chiamate, se si specifica una struttura [**COSERVERINFO**](/windows/win32/api/objidlbase/ns-objidlbase-coserverinfo) , viene eseguito l'override dell'impostazione di **ActivateAtStorage** per la durata della chiamata di funzione.</span><span class="sxs-lookup"><span data-stu-id="653af-113">In all of these calls, specifying a [**COSERVERINFO**](/windows/win32/api/objidlbase/ns-objidlbase-coserverinfo) structure overrides the setting of **ActivateAtStorage** for the duration of the function call.</span></span> <span data-ttu-id="653af-114">Il chiamante può passare le informazioni **COSERVERINFO** a **IMoniker:: BindToObject** tramite la struttura [**Bind \_ OPTS2**](/windows/win32/api/objidl/ns-objidl-bind_opts2~r1) .</span><span class="sxs-lookup"><span data-stu-id="653af-114">The caller can pass **COSERVERINFO** information to **IMoniker::BindToObject** through the [**BIND\_OPTS2**](/windows/win32/api/objidl/ns-objidl-bind_opts2~r1) structure.</span></span>

<span data-ttu-id="653af-115">Il valore impostato per **ActivateAtStorage** è anche il comportamento predefinito quando \_ \_ viene specificato il server remoto CLSCTX se nel computer del client non sono installate informazioni sul Registro di sistema per la classe.</span><span class="sxs-lookup"><span data-stu-id="653af-115">The value set for **ActivateAtStorage** is also the default behavior when CLSCTX\_REMOTE\_SERVER is specified if no registry information for the class is installed on the client's computer.</span></span> <span data-ttu-id="653af-116">Le applicazioni client scritte per sfruttare i vantaggi di **ActivateAtStorage** possono pertanto richiedere una minore amministrazione.</span><span class="sxs-lookup"><span data-stu-id="653af-116">Client applications written to take advantage of **ActivateAtStorage** may therefore require less administration.</span></span>

## <a name="related-topics"></a><span data-ttu-id="653af-117">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="653af-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="653af-118">**CLSCTX**</span><span class="sxs-lookup"><span data-stu-id="653af-118">**CLSCTX**</span></span>](/windows/win32/api/wtypesbase/ne-wtypesbase-clsctx)
</dt> <dt>

[<span data-ttu-id="653af-119">**CoGetInstanceFromFile**</span><span class="sxs-lookup"><span data-stu-id="653af-119">**CoGetInstanceFromFile**</span></span>](/windows/desktop/api/Objbase/nf-objbase-cogetinstancefromfile)
</dt> <dt>

[<span data-ttu-id="653af-120">**CoGetInstanceFromIStorage**</span><span class="sxs-lookup"><span data-stu-id="653af-120">**CoGetInstanceFromIStorage**</span></span>](/windows/desktop/api/Objbase/nf-objbase-cogetinstancefromistorage)
</dt> <dt>

[<span data-ttu-id="653af-121">**COSERVERINFO**</span><span class="sxs-lookup"><span data-stu-id="653af-121">**COSERVERINFO**</span></span>](/windows/win32/api/objidlbase/ns-objidlbase-coserverinfo)
</dt> <dt>

[<span data-ttu-id="653af-122">**IMoniker:: BindToObject**</span><span class="sxs-lookup"><span data-stu-id="653af-122">**IMoniker::BindToObject**</span></span>](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtoobject)
</dt> <dt>

[<span data-ttu-id="653af-123">Registrazione di server COM</span><span class="sxs-lookup"><span data-stu-id="653af-123">Registering COM Servers</span></span>](registering-com-servers.md)
</dt> </dl>

 

 