---
title: AccessPermission
description: Descrive l'elenco di controllo di accesso (ACL) delle entità che possono accedere alle istanze di questa classe. Questo ACL viene usato solo da applicazioni che non chiamano CoInitializeSecurity.
ms.assetid: 92518de0-66ca-4d7a-8d91-63b41e6d3c24
keywords:
- Valore AccessPermission del registro di sistema COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e6210eba77f614b16c8fde59948b350ad150909
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "104474302"
---
# <a name="accesspermission"></a><span data-ttu-id="00b42-105">AccessPermission</span><span class="sxs-lookup"><span data-stu-id="00b42-105">AccessPermission</span></span>

<span data-ttu-id="00b42-106">Descrive l'elenco di controllo di accesso (ACL) delle entità che possono accedere alle istanze di questa classe.</span><span class="sxs-lookup"><span data-stu-id="00b42-106">Describes the Access Control List (ACL) of the principals that can access instances of this class.</span></span> <span data-ttu-id="00b42-107">Questo ACL viene usato solo da applicazioni che non chiamano [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity).</span><span class="sxs-lookup"><span data-stu-id="00b42-107">This ACL is used only by applications that do not call [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity).</span></span>

## <a name="registry-entry"></a><span data-ttu-id="00b42-108">Voce del Registro di sistema</span><span class="sxs-lookup"><span data-stu-id="00b42-108">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\AppID
   {AppID_GUID}
      AccessPermission = ACL
```

## <a name="remarks"></a><span data-ttu-id="00b42-109">Commenti</span><span class="sxs-lookup"><span data-stu-id="00b42-109">Remarks</span></span>

<span data-ttu-id="00b42-110">Si tratta di un valore **\_ binario REG** .</span><span class="sxs-lookup"><span data-stu-id="00b42-110">This is a **REG\_BINARY** value.</span></span> <span data-ttu-id="00b42-111">Contiene dati che descrivono l'elenco di controllo di accesso (ACL) delle entità che possono accedere alle istanze di questa classe.</span><span class="sxs-lookup"><span data-stu-id="00b42-111">It contains data describing the Access Control List (ACL) of the principals that can access instances of this class.</span></span> <span data-ttu-id="00b42-112">Quando riceve una richiesta di connessione a un oggetto esistente di questa classe, l'ACL viene controllato dall'applicazione chiamata durante la rappresentazione del chiamante.</span><span class="sxs-lookup"><span data-stu-id="00b42-112">Upon receiving a request to connect to an existing object of this class, the ACL is checked by the application being called while impersonating the caller.</span></span> <span data-ttu-id="00b42-113">Se la verifica dell'accesso ha esito negativo, la connessione non è consentita.</span><span class="sxs-lookup"><span data-stu-id="00b42-113">If the access-check fails, the connection is disallowed.</span></span> <span data-ttu-id="00b42-114">Se questo valore denominato non esiste, viene testato l'ACL [**DefaultAccessPermission**](defaultaccesspermission.md) per determinare se la connessione deve essere consentita.</span><span class="sxs-lookup"><span data-stu-id="00b42-114">If this named value does not exist, the [**DefaultAccessPermission**](defaultaccesspermission.md) ACL is tested to determine whether the connection is to be allowed.</span></span>

<span data-ttu-id="00b42-115">Per le applicazioni che non chiamano [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) o non usano l'interfaccia [**IGlobalOptions**](/windows/win32/api/objidlbase/nn-objidlbase-iglobaloptions) per specificare l'AppID, l'eseguibile del file binario dell'applicazione deve essere mappato all'AppID dell'applicazione come descritto in [**AppID**](appid.md).</span><span class="sxs-lookup"><span data-stu-id="00b42-115">For applications that do not call [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) or do not use the [**IGlobalOptions**](/windows/win32/api/objidlbase/nn-objidlbase-iglobaloptions) interface to specify the AppID, the executable of the application's binary must be mapped to the AppID of the application as described in [**AppID**](appid.md).</span></span> <span data-ttu-id="00b42-116">Questa operazione è necessaria affinché COM possa individuare l'AppID dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="00b42-116">This is required so that COM can locate the AppID of the application.</span></span>

## <a name="related-topics"></a><span data-ttu-id="00b42-117">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="00b42-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="00b42-118">**CoInitializeSecurity**</span><span class="sxs-lookup"><span data-stu-id="00b42-118">**CoInitializeSecurity**</span></span>](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity)
</dt> <dt>

[<span data-ttu-id="00b42-119">**DefaultAccessPermission**</span><span class="sxs-lookup"><span data-stu-id="00b42-119">**DefaultAccessPermission**</span></span>](defaultaccesspermission.md)
</dt> <dt>

[<span data-ttu-id="00b42-120">Sicurezza in COM</span><span class="sxs-lookup"><span data-stu-id="00b42-120">Security in COM</span></span>](security-in-com.md)
</dt> </dl>

 

 