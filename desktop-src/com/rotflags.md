---
title: ROTFlags
description: Controlla la registrazione di un server COM nella tabella degli oggetti in esecuzione (ROT).
ms.assetid: a27c04e5-b1d3-4cb5-9b2c-9ae45663cf56
keywords:
- Valore ROTFlags del registro di sistema COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d52bc0c07ee6c86015ad1b997f2f21e33dda9a1d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298035"
---
# <a name="rotflags"></a><span data-ttu-id="27ffa-104">ROTFlags</span><span class="sxs-lookup"><span data-stu-id="27ffa-104">ROTFlags</span></span>

<span data-ttu-id="27ffa-105">Controlla la registrazione di un server COM nella tabella degli oggetti in esecuzione (ROT).</span><span class="sxs-lookup"><span data-stu-id="27ffa-105">Controls the registration of a COM server in the running object table (ROT).</span></span>

## <a name="registry-entry"></a><span data-ttu-id="27ffa-106">Voce del Registro di sistema</span><span class="sxs-lookup"><span data-stu-id="27ffa-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\AppID
   {AppID_GUID}
      ROTFlags = flags
```

## <a name="remarks"></a><span data-ttu-id="27ffa-107">Commenti</span><span class="sxs-lookup"><span data-stu-id="27ffa-107">Remarks</span></span>

<span data-ttu-id="27ffa-108">Si tratta di un valore **reg \_ DWORD** .</span><span class="sxs-lookup"><span data-stu-id="27ffa-108">This is a **REG\_DWORD** value.</span></span>



| <span data-ttu-id="27ffa-109">Valore flag</span><span class="sxs-lookup"><span data-stu-id="27ffa-109">Flag Value</span></span> | <span data-ttu-id="27ffa-110">Costante</span><span class="sxs-lookup"><span data-stu-id="27ffa-110">Constant</span></span>                        |
|------------|---------------------------------|
| <span data-ttu-id="27ffa-111">0x1</span><span class="sxs-lookup"><span data-stu-id="27ffa-111">0x1</span></span>        | <span data-ttu-id="27ffa-112">**\_ALLOWANYCLIENT ROTREGFLAGS**</span><span class="sxs-lookup"><span data-stu-id="27ffa-112">**ROTREGFLAGS\_ALLOWANYCLIENT**</span></span> |



 

### <a name="rotregflags_allowanyclient-description"></a><span data-ttu-id="27ffa-113">Descrizione di ROTREGFLAGS \_ ALLOWANYCLIENT</span><span class="sxs-lookup"><span data-stu-id="27ffa-113">ROTREGFLAGS\_ALLOWANYCLIENT Description</span></span>

<span data-ttu-id="27ffa-114">Se un server COM vuole eseguire la registrazione nella tabella ROT e consentire a qualsiasi client di accedere alla registrazione, deve usare il flag **ROTFLAGS \_ ALLOWANYCLIENT** .</span><span class="sxs-lookup"><span data-stu-id="27ffa-114">If a COM server wants to register in the ROT and allow any client to access the registration, it must use the **ROTFLAGS\_ALLOWANYCLIENT** flag.</span></span> <span data-ttu-id="27ffa-115">Un server COM "Activate As Activator" non è in grado di specificare **ROTFLAGS \_ ALLOWANYCLIENT** perché la gestione controllo servizi DCOM (Dcomscm) impone un controllo di spoofing rispetto a questo flag.</span><span class="sxs-lookup"><span data-stu-id="27ffa-115">An "Activate As Activator" COM server cannot specify **ROTFLAGS\_ALLOWANYCLIENT** because the DCOM service control manager (DCOMSCM) enforces a spoof check against this flag.</span></span> <span data-ttu-id="27ffa-116">Pertanto, in Windows Vista e versioni successive COM aggiunge il supporto per la voce del registro di sistema **ROTFlags** che consente al server di stabilire che le registrazioni Rot saranno rese disponibili per qualsiasi client.</span><span class="sxs-lookup"><span data-stu-id="27ffa-116">Therefore, in Windows Vista and later, COM adds support for the **ROTFlags** registry entry that allows the server to stipulate that its ROT registrations be made available to any client.</span></span>

<span data-ttu-id="27ffa-117">La voce deve esistere nell'hive **del \_ \_ computer locale HKEY** .</span><span class="sxs-lookup"><span data-stu-id="27ffa-117">The entry must exist in the **HKEY\_LOCAL\_MACHINE** hive.</span></span> <span data-ttu-id="27ffa-118">Questa voce fornisce un server "Activate As Activator" con la stessa funzionalità fornita da **ROTFLAGS \_ ALLOWANYCLIENT** per un server RunAs.</span><span class="sxs-lookup"><span data-stu-id="27ffa-118">This entry provides an "Activate As Activator" server with the same functionality that **ROTFLAGS\_ALLOWANYCLIENT** provides for a RunAs server.</span></span>

## <a name="related-topics"></a><span data-ttu-id="27ffa-119">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="27ffa-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="27ffa-120">Chiave AppID</span><span class="sxs-lookup"><span data-stu-id="27ffa-120">AppID Key</span></span>](appid-key.md)
</dt> <dt>

[<span data-ttu-id="27ffa-121">Registrazione di server COM</span><span class="sxs-lookup"><span data-stu-id="27ffa-121">Registering COM Servers</span></span>](registering-com-servers.md)
</dt> <dt>

[<span data-ttu-id="27ffa-122">Sicurezza in COM</span><span class="sxs-lookup"><span data-stu-id="27ffa-122">Security in COM</span></span>](security-in-com.md)
</dt> </dl>

 

 




