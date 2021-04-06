---
title: LaunchPermission
description: Descrive l'elenco di controllo di accesso (ACL) delle entità che possono avviare nuovi server per questa classe. Questo valore può essere aggiunto con qualsiasi chiave AppID per limitare l'attivazione da parte di client remoti di classi specifiche.
ms.assetid: 7b8c1ae4-fbbd-489f-b1b5-60ae5a04f906
keywords:
- Valore LaunchPermission del registro di sistema COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0e4c50568cae791f08b47fc44e10cc0d35fef07
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104045365"
---
# <a name="launchpermission"></a><span data-ttu-id="0f907-105">LaunchPermission</span><span class="sxs-lookup"><span data-stu-id="0f907-105">LaunchPermission</span></span>

<span data-ttu-id="0f907-106">Descrive l'elenco di controllo di accesso (ACL) delle entità che possono avviare nuovi server per questa classe.</span><span class="sxs-lookup"><span data-stu-id="0f907-106">Describes the Access Control List (ACL) of the principals that can start new servers for this class.</span></span> <span data-ttu-id="0f907-107">Questo valore può essere aggiunto con qualsiasi chiave [**AppID**](appid-key.md) per limitare l'attivazione da parte di client remoti di classi specifiche.</span><span class="sxs-lookup"><span data-stu-id="0f907-107">This value may be added under any [**AppID**](appid-key.md) key to limit activation by remote clients of specific classes.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="0f907-108">Voce del Registro di sistema</span><span class="sxs-lookup"><span data-stu-id="0f907-108">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\AppID
   {AppID_GUID}
      LaunchPermission = ACL
```

## <a name="remarks"></a><span data-ttu-id="0f907-109">Commenti</span><span class="sxs-lookup"><span data-stu-id="0f907-109">Remarks</span></span>

<span data-ttu-id="0f907-110">Si tratta di un valore **\_ binario REG** .</span><span class="sxs-lookup"><span data-stu-id="0f907-110">This is a **REG\_BINARY** value.</span></span> <span data-ttu-id="0f907-111">Quando riceve una richiesta locale o remota per avviare il server di questa classe, l'ACL descritto da questo valore viene verificato durante la rappresentazione del client e il suo esito positivo consente o impedisce l'avvio del server.</span><span class="sxs-lookup"><span data-stu-id="0f907-111">Upon receiving a local or remote request to launch the server of this class, the ACL described by this value is checked while impersonating the client, and its success either allows or disallows the launching of the server.</span></span> <span data-ttu-id="0f907-112">Se questo valore non esiste, il valore [**DefaultLaunchPermission**](defaultlaunchpermission.md) viene controllato nello stesso modo per determinare se il codice della classe può essere avviato.</span><span class="sxs-lookup"><span data-stu-id="0f907-112">If this value does not exist, the [**DefaultLaunchPermission**](defaultlaunchpermission.md) value is checked in the same way to determine whether the class code can be launched.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0f907-113">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="0f907-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0f907-114">**CoInitializeSecurity**</span><span class="sxs-lookup"><span data-stu-id="0f907-114">**CoInitializeSecurity**</span></span>](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity)
</dt> <dt>

[<span data-ttu-id="0f907-115">**DefaultLaunchPermission**</span><span class="sxs-lookup"><span data-stu-id="0f907-115">**DefaultLaunchPermission**</span></span>](defaultlaunchpermission.md)
</dt> <dt>

[<span data-ttu-id="0f907-116">Sicurezza in COM</span><span class="sxs-lookup"><span data-stu-id="0f907-116">Security in COM</span></span>](security-in-com.md)
</dt> </dl>

 

 




