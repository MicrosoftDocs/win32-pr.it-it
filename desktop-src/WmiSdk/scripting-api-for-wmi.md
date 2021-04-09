---
description: Il riferimento di scripting WMI contiene le definizioni per l'API di scripting WMI.
ms.assetid: 83fc78fc-929d-4d32-940e-9147543a6324
ms.tgt_platform: multiple
title: API di scripting per WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6c43587fd8f40c2524bcabd79fe80e3d00d74b1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103880442"
---
# <a name="scripting-api-for-wmi"></a><span data-ttu-id="4d73e-103">API di scripting per WMI</span><span class="sxs-lookup"><span data-stu-id="4d73e-103">Scripting API for WMI</span></span>

<span data-ttu-id="4d73e-104">Il riferimento di scripting WMI contiene le definizioni per l'API di scripting WMI.</span><span class="sxs-lookup"><span data-stu-id="4d73e-104">The WMI scripting reference contains definitions for the WMI Scripting API.</span></span> <span data-ttu-id="4d73e-105">Usare questa API se si scrivono applicazioni con Microsoft Visual Basic, Visual Basic, Applications Edition, Visual Basic Scripting Edition (VBScript) o qualsiasi altro linguaggio di script che supporta le tecnologie di scripting.</span><span class="sxs-lookup"><span data-stu-id="4d73e-105">Use this API if writing applications with Microsoft Visual Basic, Visual Basic for Applications, Visual Basic Scripting Edition (VBScript), or any other scripting language that supports active scripting technologies.</span></span>

> [!Note]  
> <span data-ttu-id="4d73e-106">PowerShell è inoltre disponibile per lo scripting con WMI.</span><span class="sxs-lookup"><span data-stu-id="4d73e-106">PowerShell is also available for scripting with WMI.</span></span> <span data-ttu-id="4d73e-107">Il cmdlet Get-WMI e i tre acceleratori di tipo ( \[ WMI \] , \[ WMIClass \] e \[ WMISEARCHER \] ) abilitano l'accesso amministrativo di base a WMI.</span><span class="sxs-lookup"><span data-stu-id="4d73e-107">The Get-WMI cmdlet and the three type accelerators (\[wmi\], \[wmiclass\], and \[wmisearcher\]) enable basic administrative access to WMI.</span></span> <span data-ttu-id="4d73e-108">Per altre informazioni, vedere Creazione di [script con Windows PowerShell](https://TechNet.Microsoft.Com/library/bb978526.aspx).</span><span class="sxs-lookup"><span data-stu-id="4d73e-108">For more information, see [Scripting with Windows PowerShell](https://TechNet.Microsoft.Com/library/bb978526.aspx).</span></span>

 

<span data-ttu-id="4d73e-109">Gli oggetti di scripting WMI, ad eccezione di [**SWbemDateTime**](swbemdatetime.md) , non sono contrassegnati come sicuri per lo scripting per gli script in esecuzione sulle pagine HTML in Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="4d73e-109">WMI scripting objects, except for [**SWbemDateTime**](swbemdatetime.md) are not marked safe for scripting for scripts running on HTML pages in Internet Explorer.</span></span> <span data-ttu-id="4d73e-110">Pertanto, a meno che il livello di sicurezza in Internet Explorer non venga ridotto, lo script avrà esito negativo.</span><span class="sxs-lookup"><span data-stu-id="4d73e-110">Therefore, unless the security level within Internet Explorer is lowered, the script will fail.</span></span> <span data-ttu-id="4d73e-111">**SWbemDateTime** è contrassegnato come Safe per l'inizializzazione e lo scripting.</span><span class="sxs-lookup"><span data-stu-id="4d73e-111">**SWbemDateTime** is marked safe for initialization and scripting.</span></span> <span data-ttu-id="4d73e-112">Tuttavia, utilizzare tutti gli oggetti di scripting WMI nelle chiamate **GetObject** e **CreateObject** sul codice sul lato server in Active Server Pages (ASP).</span><span class="sxs-lookup"><span data-stu-id="4d73e-112">However, use all WMI scripting objects in **GetObject** and **CreateObject** calls on server-side code in Active Server Pages (ASP).</span></span>

-   [<span data-ttu-id="4d73e-113">Modello a oggetti API di scripting</span><span class="sxs-lookup"><span data-stu-id="4d73e-113">Scripting API Object Model</span></span>](scripting-api-object-model.md)
-   [<span data-ttu-id="4d73e-114">Convenzioni dei documenti per l'API di scripting</span><span class="sxs-lookup"><span data-stu-id="4d73e-114">Document Conventions for the Scripting API</span></span>](document-conventions-for-the-scripting-api.md)
-   [<span data-ttu-id="4d73e-115">Oggetti API di scripting</span><span class="sxs-lookup"><span data-stu-id="4d73e-115">Scripting API Objects</span></span>](scripting-api-objects.md)
-   [<span data-ttu-id="4d73e-116">Esecuzione di script di costanti API</span><span class="sxs-lookup"><span data-stu-id="4d73e-116">Scripting API Constants</span></span>](scripting-api-constants.md)

## <a name="related-topics"></a><span data-ttu-id="4d73e-117">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="4d73e-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4d73e-118">Informazioni di riferimento su WMI</span><span class="sxs-lookup"><span data-stu-id="4d73e-118">WMI Reference</span></span>](wmi-reference.md)
</dt> <dt>

[<span data-ttu-id="4d73e-119">Codici restituiti WMI</span><span class="sxs-lookup"><span data-stu-id="4d73e-119">WMI Return Codes</span></span>](wmi-return-codes.md)
</dt> </dl>

 

 



