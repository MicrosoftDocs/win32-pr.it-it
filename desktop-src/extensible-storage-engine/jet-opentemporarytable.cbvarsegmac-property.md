---
description: 'Altre informazioni su: Proprietà JET_OPENTEMPORARYTABLE. cbVarSegMac'
title: Proprietà JET_OPENTEMPORARYTABLE. cbVarSegMac (Microsoft. ISAM. esent. Interop. vista)
TOCTitle: 'cbVarSegMac property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.Vista.JET_OPENTEMPORARYTABLE.cbVarSegMac
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.jet_opentemporarytable.cbvarsegmac(v=EXCHG.10)
ms:contentKeyID: 55104115
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.JET_OPENTEMPORARYTABLE.cbVarSegMac
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.JET_OPENTEMPORARYTABLE.cbVarSegMac
- Microsoft.Isam.Esent.Interop.Vista.JET_OPENTEMPORARYTABLE.get_cbVarSegMac
- Microsoft.Isam.Esent.Interop.Vista.JET_OPENTEMPORARYTABLE.set_cbVarSegMac
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 37fe218a9741235410d2452f04f082dc6673eaf5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313116"
---
# <a name="jet_opentemporarytablecbvarsegmac-property"></a><span data-ttu-id="111d3-103">Proprietà JET_OPENTEMPORARYTABLE. cbVarSegMac</span><span class="sxs-lookup"><span data-stu-id="111d3-103">JET_OPENTEMPORARYTABLE.cbVarSegMac property</span></span>

<span data-ttu-id="111d3-104">Ottiene o imposta la quantità massima di dati che verranno utilizzati da qualsiasi variabile lengthcolumn per costruire una chiave per una determinata riga.</span><span class="sxs-lookup"><span data-stu-id="111d3-104">Gets or sets maximum amount of data that will be used from any variable lengthcolumn to construct a key for a given row.</span></span> <span data-ttu-id="111d3-105">Questo parametro può essere utilizzato per controllare la quantità di spazio chiave utilizzata da una determinata colonna chiave.</span><span class="sxs-lookup"><span data-stu-id="111d3-105">This parameter may be used to control the amount of key space consumed by any given key column.</span></span> <span data-ttu-id="111d3-106">Questo limite è in byte.</span><span class="sxs-lookup"><span data-stu-id="111d3-106">This limit is in bytes.</span></span> <span data-ttu-id="111d3-107">Se questo parametro è zero o è uguale alla proprietà [cbKeyMost](./jet-opentemporarytable.cbkeymost-property.md) , non è attivo alcun limite.</span><span class="sxs-lookup"><span data-stu-id="111d3-107">If this parameter is zero or is the same as the [cbKeyMost](./jet-opentemporarytable.cbkeymost-property.md) property then no limit is in effect.</span></span>

<span data-ttu-id="111d3-108">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop. vista](./microsoft.isam.esent.interop.vista-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="111d3-108">**Namespace:**  [Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span></span>  
<span data-ttu-id="111d3-109">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="111d3-109">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="111d3-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="111d3-110">Syntax</span></span>

``` vb
'Declaration
Public Property cbVarSegMac As Integer
    Get
    Set
'Usage
Dim instance As JET_OPENTEMPORARYTABLE
Dim value As Integer

value = instance.cbVarSegMac

instance.cbVarSegMac = value
```

``` csharp
public int cbVarSegMac { get; set; }
```

#### <a name="property-value"></a><span data-ttu-id="111d3-111">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="111d3-111">Property value</span></span>

<span data-ttu-id="111d3-112">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="111d3-112">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  

## <a name="see-also"></a><span data-ttu-id="111d3-113">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="111d3-113">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="111d3-114">Riferimento</span><span class="sxs-lookup"><span data-stu-id="111d3-114">Reference</span></span>

[<span data-ttu-id="111d3-115">Classe JET_OPENTEMPORARYTABLE</span><span class="sxs-lookup"><span data-stu-id="111d3-115">JET_OPENTEMPORARYTABLE class</span></span>](./jet-opentemporarytable-class.md)

[<span data-ttu-id="111d3-116">Membri JET_OPENTEMPORARYTABLE</span><span class="sxs-lookup"><span data-stu-id="111d3-116">JET_OPENTEMPORARYTABLE members</span></span>](./jet-opentemporarytable-members.md)

[<span data-ttu-id="111d3-117">Spazio dei nomi Microsoft. ISAM. esent. Interop. vista</span><span class="sxs-lookup"><span data-stu-id="111d3-117">Microsoft.Isam.Esent.Interop.Vista namespace</span></span>](./microsoft.isam.esent.interop.vista-namespace.md)
