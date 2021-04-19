---
description: 'Altre informazioni su: Proprietà JET_OPENTEMPORARYTABLE. cbKeyMost'
title: Proprietà JET_OPENTEMPORARYTABLE. cbKeyMost (Microsoft. ISAM. esent. Interop. vista)
TOCTitle: 'cbKeyMost property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.Vista.JET_OPENTEMPORARYTABLE.cbKeyMost
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.jet_opentemporarytable.cbkeymost(v=EXCHG.10)
ms:contentKeyID: 55104228
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.JET_OPENTEMPORARYTABLE.cbKeyMost
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.JET_OPENTEMPORARYTABLE.set_cbKeyMost
- Microsoft.Isam.Esent.Interop.Vista.JET_OPENTEMPORARYTABLE.cbKeyMost
- Microsoft.Isam.Esent.Interop.Vista.JET_OPENTEMPORARYTABLE.get_cbKeyMost
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b8e608d1419cd381c507874bf1f1c334d192ae2b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318121"
---
# <a name="jet_opentemporarytablecbkeymost-property"></a><span data-ttu-id="0bd30-103">Proprietà JET_OPENTEMPORARYTABLE. cbKeyMost</span><span class="sxs-lookup"><span data-stu-id="0bd30-103">JET_OPENTEMPORARYTABLE.cbKeyMost property</span></span>

<span data-ttu-id="0bd30-104">Ottiene o imposta la dimensione massima per una chiave che rappresenta una determinata riga.</span><span class="sxs-lookup"><span data-stu-id="0bd30-104">Gets or sets the maximum size for a key representing a given row.</span></span> <span data-ttu-id="0bd30-105">È possibile impostare la dimensione massima della chiave per controllare la modalità di troncamento delle chiavi.</span><span class="sxs-lookup"><span data-stu-id="0bd30-105">The maximum key size may be set to control how keys are truncated.</span></span> <span data-ttu-id="0bd30-106">Il troncamento della chiave è importante perché può influire sul fatto che le righe siano considerate distinte.</span><span class="sxs-lookup"><span data-stu-id="0bd30-106">Key truncation is important because it can affect when rows are considered to be distinct.</span></span> <span data-ttu-id="0bd30-107">Se questo parametro è impostato su 0 o 255, le dimensioni massime della chiave e la relativa semantica rimarranno identiche alle dimensioni massime della chiave supportate da Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="0bd30-107">If this parameter is set to 0 or 255 then the maximum key size and its semantics will remain identical to the maximum key size supported by Windows Server 2003.</span></span> <span data-ttu-id="0bd30-108">Questo parametro può essere impostato anche su un valore maggiore come funzione delle dimensioni della pagina del database per l'istanza [DatabasePageSize](./jet-param-enumeration.md).</span><span class="sxs-lookup"><span data-stu-id="0bd30-108">This parameter may also be set to a larger value as a function of the database page size for the instance [DatabasePageSize](./jet-param-enumeration.md).</span></span> <span data-ttu-id="0bd30-109">Per [ulteriori](./vistaparam.keymost-field.md) informazioni, vedere.</span><span class="sxs-lookup"><span data-stu-id="0bd30-109">See [KeyMost](./vistaparam.keymost-field.md) for more information.</span></span>

<span data-ttu-id="0bd30-110">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop. vista](./microsoft.isam.esent.interop.vista-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="0bd30-110">**Namespace:**  [Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span></span>  
<span data-ttu-id="0bd30-111">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="0bd30-111">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="0bd30-112">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0bd30-112">Syntax</span></span>

``` vb
'Declaration
Public Property cbKeyMost As Integer
    Get
    Set
'Usage
Dim instance As JET_OPENTEMPORARYTABLE
Dim value As Integer

value = instance.cbKeyMost

instance.cbKeyMost = value
```

``` csharp
public int cbKeyMost { get; set; }
```

#### <a name="property-value"></a><span data-ttu-id="0bd30-113">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="0bd30-113">Property value</span></span>

<span data-ttu-id="0bd30-114">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="0bd30-114">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  

## <a name="see-also"></a><span data-ttu-id="0bd30-115">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0bd30-115">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="0bd30-116">Riferimento</span><span class="sxs-lookup"><span data-stu-id="0bd30-116">Reference</span></span>

[<span data-ttu-id="0bd30-117">Classe JET_OPENTEMPORARYTABLE</span><span class="sxs-lookup"><span data-stu-id="0bd30-117">JET_OPENTEMPORARYTABLE class</span></span>](./jet-opentemporarytable-class.md)

[<span data-ttu-id="0bd30-118">Membri JET_OPENTEMPORARYTABLE</span><span class="sxs-lookup"><span data-stu-id="0bd30-118">JET_OPENTEMPORARYTABLE members</span></span>](./jet-opentemporarytable-members.md)

[<span data-ttu-id="0bd30-119">Spazio dei nomi Microsoft. ISAM. esent. Interop. vista</span><span class="sxs-lookup"><span data-stu-id="0bd30-119">Microsoft.Isam.Esent.Interop.Vista namespace</span></span>](./microsoft.isam.esent.interop.vista-namespace.md)
