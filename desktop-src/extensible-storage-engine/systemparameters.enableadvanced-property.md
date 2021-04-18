---
description: 'Altre informazioni su: Proprietà SystemParameters. EnableAdvanced'
title: Proprietà SystemParameters. EnableAdvanced
TOCTitle: 'EnableAdvanced property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.SystemParameters.EnableAdvanced
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.systemparameters.enableadvanced(v=EXCHG.10)
ms:contentKeyID: 55104116
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.SystemParameters.EnableAdvanced
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.SystemParameters.set_EnableAdvanced
- Microsoft.Isam.Esent.Interop.SystemParameters.get_EnableAdvanced
- Microsoft.Isam.Esent.Interop.SystemParameters.EnableAdvanced
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e311685bf5ef436be11d4593523aceee73b955b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317340"
---
# <a name="systemparametersenableadvanced-property"></a><span data-ttu-id="fe6f4-103">Proprietà SystemParameters. EnableAdvanced</span><span class="sxs-lookup"><span data-stu-id="fe6f4-103">SystemParameters.EnableAdvanced property</span></span>

<span data-ttu-id="fe6f4-104">Ottiene o imposta un valore che indica se il motore di database accetta o rifiuta le modifiche apportate a un subset dei parametri di sistema.</span><span class="sxs-lookup"><span data-stu-id="fe6f4-104">Gets or sets a value indicating whether the database engine accepts or rejects changes to a subset of the system parameters.</span></span> <span data-ttu-id="fe6f4-105">Questo parametro viene usato in combinazione con la [configurazione](./systemparameters.configuration-property.md) per impedire che alcuni parametri di sistema vengano impostati dalle impostazioni predefinite della configurazione selezionata.</span><span class="sxs-lookup"><span data-stu-id="fe6f4-105">This parameter is used in conjunction with [Configuration](./systemparameters.configuration-property.md) to prevent some system parameters from being set away from the selected configuration's defaults.</span></span> <span data-ttu-id="fe6f4-106">Supportato in Windows Vista e in alto.</span><span class="sxs-lookup"><span data-stu-id="fe6f4-106">Supported on Windows Vista and up.</span></span> <span data-ttu-id="fe6f4-107">Ignorato in Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="fe6f4-107">Ignored on Windows XP and Windows Server 2003.</span></span>

<span data-ttu-id="fe6f4-108">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="fe6f4-108">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="fe6f4-109">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="fe6f4-109">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="fe6f4-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="fe6f4-110">Syntax</span></span>

``` vb
'Declaration
Public Shared Property EnableAdvanced As Boolean
    Get
    Set
'Usage
Dim value As Boolean

value = SystemParameters.EnableAdvanced

SystemParameters.EnableAdvanced = value
```

``` csharp
public static bool EnableAdvanced { get; set; }
```

#### <a name="property-value"></a><span data-ttu-id="fe6f4-111">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="fe6f4-111">Property value</span></span>

<span data-ttu-id="fe6f4-112">Tipo: [System. Boolean](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="fe6f4-112">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  

## <a name="see-also"></a><span data-ttu-id="fe6f4-113">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="fe6f4-113">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="fe6f4-114">Riferimento</span><span class="sxs-lookup"><span data-stu-id="fe6f4-114">Reference</span></span>

[<span data-ttu-id="fe6f4-115">SystemParameters (classe)</span><span class="sxs-lookup"><span data-stu-id="fe6f4-115">SystemParameters class</span></span>](./systemparameters-class.md)

[<span data-ttu-id="fe6f4-116">Membri SystemParameters</span><span class="sxs-lookup"><span data-stu-id="fe6f4-116">SystemParameters members</span></span>](./systemparameters-members.md)

[<span data-ttu-id="fe6f4-117">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="fe6f4-117">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
