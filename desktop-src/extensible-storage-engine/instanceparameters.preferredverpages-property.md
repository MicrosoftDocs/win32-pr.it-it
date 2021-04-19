---
description: 'Altre informazioni su: Proprietà InstanceParameters. PreferredVerPages'
title: Proprietà InstanceParameters. PreferredVerPages
TOCTitle: 'PreferredVerPages property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.InstanceParameters.PreferredVerPages
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instanceparameters.preferredverpages(v=EXCHG.10)
ms:contentKeyID: 55103322
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.InstanceParameters.PreferredVerPages
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.InstanceParameters.set_PreferredVerPages
- Microsoft.Isam.Esent.Interop.InstanceParameters.PreferredVerPages
- Microsoft.Isam.Esent.Interop.InstanceParameters.get_PreferredVerPages
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 067d41cd3fb945b2f18d3cd6154b1eef6793b1e9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313556"
---
# <a name="instanceparameterspreferredverpages-property"></a><span data-ttu-id="0dfde-103">Proprietà InstanceParameters. PreferredVerPages</span><span class="sxs-lookup"><span data-stu-id="0dfde-103">InstanceParameters.PreferredVerPages property</span></span>

<span data-ttu-id="0dfde-104">Ottiene o imposta il numero preferito di pagine dell'archivio versioni riservate per questa istanza.</span><span class="sxs-lookup"><span data-stu-id="0dfde-104">Gets or sets the preferred number of version store pages reserved for this instance.</span></span> <span data-ttu-id="0dfde-105">Se la dimensione dell'archivio versioni supera questa soglia, le informazioni utilizzate solo per le attività in background facoltative, ad esempio il ripristino dello spazio eliminato nel database, vengono invece sacrificate per mantenere la stanza per le informazioni transazionali.</span><span class="sxs-lookup"><span data-stu-id="0dfde-105">If the size of the version store exceeds this threshold then any information that is only used for optional background tasks, such as reclaiming deleted space in the database, is instead sacrificed to preserve room for transactional information.</span></span>

<span data-ttu-id="0dfde-106">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="0dfde-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="0dfde-107">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="0dfde-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="0dfde-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0dfde-108">Syntax</span></span>

``` vb
'Declaration
Public Property PreferredVerPages As Integer
    Get
    Set
'Usage
Dim instance As InstanceParameters
Dim value As Integer

value = instance.PreferredVerPages

instance.PreferredVerPages = value
```

``` csharp
public int PreferredVerPages { get; set; }
```

#### <a name="property-value"></a><span data-ttu-id="0dfde-109">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="0dfde-109">Property value</span></span>

<span data-ttu-id="0dfde-110">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="0dfde-110">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  

## <a name="see-also"></a><span data-ttu-id="0dfde-111">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0dfde-111">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="0dfde-112">Riferimento</span><span class="sxs-lookup"><span data-stu-id="0dfde-112">Reference</span></span>

[<span data-ttu-id="0dfde-113">Classe InstanceParameters</span><span class="sxs-lookup"><span data-stu-id="0dfde-113">InstanceParameters class</span></span>](./instanceparameters-class.md)

[<span data-ttu-id="0dfde-114">Membri di InstanceParameters</span><span class="sxs-lookup"><span data-stu-id="0dfde-114">InstanceParameters members</span></span>](./instanceparameters-members.md)

[<span data-ttu-id="0dfde-115">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="0dfde-115">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
