---
description: 'Altre informazioni su: SystemParameters.Configproprietà uration'
title: SystemParameters.Configproprietà uration
TOCTitle: 'Configuration property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.SystemParameters.Configuration
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.systemparameters.configuration(v=EXCHG.10)
ms:contentKeyID: 55104117
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.SystemParameters.Configuration
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.SystemParameters.Configuration
- Microsoft.Isam.Esent.Interop.SystemParameters.set_Configuration
- Microsoft.Isam.Esent.Interop.SystemParameters.get_Configuration
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5eaa387f63df1dd91641ff38f2a6f6450629fe99
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103882246"
---
# <a name="systemparametersconfiguration-property"></a><span data-ttu-id="2113f-103">SystemParameters.Configproprietà uration</span><span class="sxs-lookup"><span data-stu-id="2113f-103">SystemParameters.Configuration property</span></span>

<span data-ttu-id="2113f-104">Ottiene o imposta un valore che specifica i valori predefiniti per l'intero set di parametri di sistema.</span><span class="sxs-lookup"><span data-stu-id="2113f-104">Gets or sets a value specifying the default values for the entire set of system parameters.</span></span> <span data-ttu-id="2113f-105">Quando questo parametro è impostato su una configurazione specifica, tutti i valori dei parametri di sistema vengono reimpostati sui valori predefiniti per tale configurazione.</span><span class="sxs-lookup"><span data-stu-id="2113f-105">When this parameter is set to a specific configuration, all system parameter values are reset to their default values for that configuration.</span></span> <span data-ttu-id="2113f-106">Se la configurazione è impostata per un'istanza specifica, i parametri di sistema globali non verranno reimpostati sui valori predefiniti.</span><span class="sxs-lookup"><span data-stu-id="2113f-106">If the configuration is set for a specific instance then global system parameters will not be reset to their default values.</span></span> <span data-ttu-id="2113f-107">Small Configuration (0): il motore di database è ottimizzato per l'uso della memoria.</span><span class="sxs-lookup"><span data-stu-id="2113f-107">Small Configuration (0): The database engine is optimized for memory use.</span></span> <span data-ttu-id="2113f-108">Configurazione legacy (1): il motore di database presenta le impostazioni predefinite tradizionali.</span><span class="sxs-lookup"><span data-stu-id="2113f-108">Legacy Configuration (1): The database engine has its traditional defaults.</span></span> <span data-ttu-id="2113f-109">Supportato in Windows Vista e in alto.</span><span class="sxs-lookup"><span data-stu-id="2113f-109">Supported on Windows Vista and up.</span></span> <span data-ttu-id="2113f-110">Ignorato in Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="2113f-110">Ignored on Windows XP and Windows Server 2003.</span></span>

<span data-ttu-id="2113f-111">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="2113f-111">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="2113f-112">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="2113f-112">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="2113f-113">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2113f-113">Syntax</span></span>

``` vb
'Declaration
Public Shared Property Configuration As Integer
    Get
    Set
'Usage
Dim value As Integer

value = SystemParameters.Configuration

SystemParameters.Configuration = value
```

``` csharp
public static int Configuration { get; set; }
```

#### <a name="property-value"></a><span data-ttu-id="2113f-114">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="2113f-114">Property value</span></span>

<span data-ttu-id="2113f-115">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="2113f-115">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  

## <a name="see-also"></a><span data-ttu-id="2113f-116">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2113f-116">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="2113f-117">Riferimento</span><span class="sxs-lookup"><span data-stu-id="2113f-117">Reference</span></span>

[<span data-ttu-id="2113f-118">SystemParameters (classe)</span><span class="sxs-lookup"><span data-stu-id="2113f-118">SystemParameters class</span></span>](./systemparameters-class.md)

[<span data-ttu-id="2113f-119">Membri SystemParameters</span><span class="sxs-lookup"><span data-stu-id="2113f-119">SystemParameters members</span></span>](./systemparameters-members.md)

[<span data-ttu-id="2113f-120">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="2113f-120">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
