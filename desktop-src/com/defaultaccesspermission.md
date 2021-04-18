---
title: DefaultAccessPermission
description: Imposta l'elenco di controllo di accesso (ACL) delle entità che possono accedere alle classi per le quali non è disponibile alcuna impostazione di AccessPermission.
ms.assetid: 02675d0e-a96c-476e-820e-e6ff3c2d1be1
keywords:
- Valore DefaultAccessPermission del registro di sistema COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e6c132096807b8c234259071758ebd361421f8f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106297748"
---
# <a name="defaultaccesspermission"></a><span data-ttu-id="38543-104">DefaultAccessPermission</span><span class="sxs-lookup"><span data-stu-id="38543-104">DefaultAccessPermission</span></span>

<span data-ttu-id="38543-105">Imposta l'elenco di controllo di accesso (ACL) delle entità che possono accedere alle classi per le quali non è disponibile alcuna impostazione di [**AccessPermission**](accesspermission.md) .</span><span class="sxs-lookup"><span data-stu-id="38543-105">Sets the Access Control List (ACL) of the principals that can access classes for which there is no [**AccessPermission**](accesspermission.md) setting.</span></span> <span data-ttu-id="38543-106">Questo ACL viene usato solo da applicazioni che non chiamano [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) e non hanno un valore **AccessPermission** nella chiave [**AppID**](appid-key.md) .</span><span class="sxs-lookup"><span data-stu-id="38543-106">This ACL is used only by applications that do not call [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) and do not have an **AccessPermission** value under their [**AppID**](appid-key.md) key.</span></span>

> [!Caution]  
> <span data-ttu-id="38543-107">Non è consigliabile modificare questo valore, perché questo influirà su tutte le applicazioni server COM che non impostano la propria sicurezza a livello di processo e potrebbe impedire il corretto funzionamento.</span><span class="sxs-lookup"><span data-stu-id="38543-107">It is not recommended that you change this value, because this will affect all COM server applications that do not set their own process-wide security, and might prevent them from working properly.</span></span> <span data-ttu-id="38543-108">Se si modifica questo valore in modo da influire sulle impostazioni di sicurezza di una particolare applicazione COM, è necessario modificare le impostazioni di sicurezza a livello di processo per quella particolare applicazione COM.</span><span class="sxs-lookup"><span data-stu-id="38543-108">If you are changing this value to affect the security settings for a particular COM application, then you should instead change the process-wide security settings for that particular COM application.</span></span> <span data-ttu-id="38543-109">Per altre informazioni sull'impostazione della sicurezza a livello di processo, vedere [impostazione della sicurezza a livello di processo](setting-processwide-security.md).</span><span class="sxs-lookup"><span data-stu-id="38543-109">For more information on setting process-wide security, see [Setting Process-wide Security](setting-processwide-security.md).</span></span>

 

## <a name="registry-entry"></a><span data-ttu-id="38543-110">Voce del Registro di sistema</span><span class="sxs-lookup"><span data-stu-id="38543-110">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole
   DefaultAccessPermission = ACL
```

## <a name="remarks"></a><span data-ttu-id="38543-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="38543-111">Remarks</span></span>

<span data-ttu-id="38543-112">Si tratta di un valore **\_ binario REG** .</span><span class="sxs-lookup"><span data-stu-id="38543-112">This is a **REG\_BINARY** value.</span></span>

<span data-ttu-id="38543-113">Il runtime COM nel server controlla l'ACL descritto da questo valore durante la rappresentazione del chiamante che sta tentando di connettersi all'oggetto e il suo esito positivo determina se l'accesso è consentito o non consentito.</span><span class="sxs-lookup"><span data-stu-id="38543-113">The COM runtime in the server checks the ACL described by this value while impersonating the caller that is attempting to connect to the object, and its success determines whether the access is allowed or disallowed.</span></span> <span data-ttu-id="38543-114">Se la verifica dell'accesso ha esito negativo, la connessione all'oggetto non è consentita.</span><span class="sxs-lookup"><span data-stu-id="38543-114">If the access-check fails, the connection to the object is disallowed.</span></span> <span data-ttu-id="38543-115">Se questo valore denominato non esiste, solo l'entità server e il sistema locale possono chiamare il server.</span><span class="sxs-lookup"><span data-stu-id="38543-115">If this named value does not exist, only the server principal and local system are allowed to call the server.</span></span>

<span data-ttu-id="38543-116">Per impostazione predefinita, questo valore non contiene voci.</span><span class="sxs-lookup"><span data-stu-id="38543-116">By default, this value has no entries in it.</span></span> <span data-ttu-id="38543-117">Solo l'entità server e il sistema sono autorizzati a chiamare il server.</span><span class="sxs-lookup"><span data-stu-id="38543-117">Only the server principal and system are allowed to call the server.</span></span>

<span data-ttu-id="38543-118">Questo valore fornisce un semplice livello di amministrazione centralizzata dell'accesso alla connessione predefinito per l'esecuzione di oggetti in un computer.</span><span class="sxs-lookup"><span data-stu-id="38543-118">This value provides a simple level of centralized administration of the default connection access to running objects on a computer.</span></span>

## <a name="related-topics"></a><span data-ttu-id="38543-119">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="38543-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="38543-120">**AccessPermission**</span><span class="sxs-lookup"><span data-stu-id="38543-120">**AccessPermission**</span></span>](accesspermission.md)
</dt> <dt>

[<span data-ttu-id="38543-121">Registrazione di server COM</span><span class="sxs-lookup"><span data-stu-id="38543-121">Registering COM Servers</span></span>](registering-com-servers.md)
</dt> <dt>

[<span data-ttu-id="38543-122">Impostazione della sicurezza a livello di processo</span><span class="sxs-lookup"><span data-stu-id="38543-122">Setting Process-wide Security</span></span>](setting-processwide-security.md)
</dt> </dl>

 

 




