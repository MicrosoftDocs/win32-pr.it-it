---
description: 'Altre informazioni su: VistaParam.Configcampo uration'
title: VistaParam.Configcampo uration (Microsoft. ISAM. esent. Interop. vista)
TOCTitle: Configuration field
ms:assetid: F:Microsoft.Isam.Esent.Interop.Vista.VistaParam.Configuration
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.vistaparam.configuration(v=EXCHG.10)
ms:contentKeyID: 55104229
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.VistaParam.Configuration
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.VistaParam.Configuration
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b330afb7158c616ba7bb9683a7bbe226d8d63542
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103749695"
---
# <a name="vistaparamconfiguration-field"></a><span data-ttu-id="4382c-103">VistaParam.Configcampo uration</span><span class="sxs-lookup"><span data-stu-id="4382c-103">VistaParam.Configuration field</span></span>

<span data-ttu-id="4382c-104">Questo parametro espone più set di valori predefiniti per l'intero set di parametri di sistema.</span><span class="sxs-lookup"><span data-stu-id="4382c-104">This parameter exposes multiple sets of default values for the entire set of system parameters.</span></span> <span data-ttu-id="4382c-105">Quando questo parametro è impostato su una configurazione specifica, tutti i valori dei parametri di sistema vengono reimpostati sui valori predefiniti per tale configurazione.</span><span class="sxs-lookup"><span data-stu-id="4382c-105">When this parameter is set to a specific configuration, all system parameter values are reset to their default values for that configuration.</span></span> <span data-ttu-id="4382c-106">Se la configurazione è impostata per un'istanza specifica, i parametri di sistema globali non verranno reimpostati sui valori predefiniti.</span><span class="sxs-lookup"><span data-stu-id="4382c-106">If the configuration is set for a specific instance then global system parameters will not be reset to their default values.</span></span> <span data-ttu-id="4382c-107">Small Configuration (0): il motore di database è ottimizzato per l'uso della memoria.</span><span class="sxs-lookup"><span data-stu-id="4382c-107">Small Configuration (0): The database engine is optimized for memory use.</span></span> <span data-ttu-id="4382c-108">Configurazione legacy (1): il motore di database presenta le impostazioni predefinite tradizionali.</span><span class="sxs-lookup"><span data-stu-id="4382c-108">Legacy Configuration (1): The database engine has its traditional defaults.</span></span>

<span data-ttu-id="4382c-109">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop. vista](./microsoft.isam.esent.interop.vista-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="4382c-109">**Namespace:**  [Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span></span>  
<span data-ttu-id="4382c-110">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="4382c-110">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="4382c-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4382c-111">Syntax</span></span>

``` vb
'Declaration
Public Const Configuration As JET_param
'Usage
Dim value As JET_param

value = VistaParam.Configuration
```

``` csharp
public const JET_param Configuration
```

## <a name="see-also"></a><span data-ttu-id="4382c-112">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="4382c-112">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="4382c-113">Riferimento</span><span class="sxs-lookup"><span data-stu-id="4382c-113">Reference</span></span>

[<span data-ttu-id="4382c-114">Classe VistaParam</span><span class="sxs-lookup"><span data-stu-id="4382c-114">VistaParam class</span></span>](./vistaparam-class.md)

[<span data-ttu-id="4382c-115">Membri di VistaParam</span><span class="sxs-lookup"><span data-stu-id="4382c-115">VistaParam members</span></span>](./vistaparam-members.md)

[<span data-ttu-id="4382c-116">Spazio dei nomi Microsoft. ISAM. esent. Interop. vista</span><span class="sxs-lookup"><span data-stu-id="4382c-116">Microsoft.Isam.Esent.Interop.Vista namespace</span></span>](./microsoft.isam.esent.interop.vista-namespace.md)
