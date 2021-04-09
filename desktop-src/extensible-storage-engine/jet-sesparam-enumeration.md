---
description: 'Altre informazioni su: Enumerazione JET_sesparam'
title: Enumerazione JET_sesparam (Microsoft. ISAM. esent. Interop. Windows8)
TOCTitle: JET_sesparam enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.Windows8.JET_sesparam
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.windows8.jet_sesparam(v=EXCHG.10)
ms:contentKeyID: 55104452
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Windows8.JET_sesparam
- Microsoft.Isam.Esent.Interop.Windows8.JET_sesparam.Base
- Microsoft.Isam.Esent.Interop.Windows8.JET_sesparam.CommitDefault
- Microsoft.Isam.Esent.Interop.Windows8.JET_sesparam.CommitGenericContext
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Windows8.JET_sesparam.Base
- Microsoft.Isam.Esent.Interop.Windows8.JET_sesparam.CommitGenericContext
- Microsoft.Isam.Esent.Interop.Windows8.JET_sesparam.CommitDefault
- Microsoft.Isam.Esent.Interop.Windows8.JET_sesparam
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d5ddfd613eecf5e9a6d9b6cec9eebcbab04e9b38
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128650"
---
# <a name="jet_sesparam-enumeration"></a><span data-ttu-id="f1da2-103">Enumerazione JET_sesparam</span><span class="sxs-lookup"><span data-stu-id="f1da2-103">JET_sesparam enumeration</span></span>

<span data-ttu-id="f1da2-104">Parametri della sessione ESENT.</span><span class="sxs-lookup"><span data-stu-id="f1da2-104">ESENT session parameters.</span></span>

<span data-ttu-id="f1da2-105">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop. Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="f1da2-105">**Namespace:**  [Microsoft.Isam.Esent.Interop.Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)</span></span>  
<span data-ttu-id="f1da2-106">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="f1da2-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="f1da2-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f1da2-107">Syntax</span></span>

``` vb
'Declaration
Public Enumeration JET_sesparam
'Usage
Dim instance As JET_sesparam
```

``` csharp
public enum JET_sesparam
```

## <a name="members"></a><span data-ttu-id="f1da2-108">Members</span><span class="sxs-lookup"><span data-stu-id="f1da2-108">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="f1da2-109">Nome del membro</span><span class="sxs-lookup"><span data-stu-id="f1da2-109">Member name</span></span></th>
<th><span data-ttu-id="f1da2-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f1da2-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="f1da2-111">Base</span><span class="sxs-lookup"><span data-stu-id="f1da2-111">Base</span></span></td>
<td><span data-ttu-id="f1da2-112">Questo parametro non è destinato a essere utilizzato.</span><span class="sxs-lookup"><span data-stu-id="f1da2-112">This parameter is not meant to be used.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="f1da2-113">CommitDefault</span><span class="sxs-lookup"><span data-stu-id="f1da2-113">CommitDefault</span></span></td>
<td><span data-ttu-id="f1da2-114">Questo parametro imposta il grbits per il commit.</span><span class="sxs-lookup"><span data-stu-id="f1da2-114">This parameter sets the grbits for commit.</span></span> <span data-ttu-id="f1da2-115">Dal punto di vista funzionale corrisponde al parametro di sistema JET_param. CommitDefault quando viene usato con un'istanza di e un sesid.</span><span class="sxs-lookup"><span data-stu-id="f1da2-115">It is functionally the same as the system parameter JET_param.CommitDefault when used with an instance and a sesid.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="f1da2-116">CommitGenericContext</span><span class="sxs-lookup"><span data-stu-id="f1da2-116">CommitGenericContext</span></span></td>
<td><span data-ttu-id="f1da2-117">Questo parametro imposta un contesto di commit specifico dell'utente che verrà inserito nel log delle transazioni al commit del livello 0.</span><span class="sxs-lookup"><span data-stu-id="f1da2-117">This parameter sets a user specific commit context that will be placed in the transaction log on commit to level 0.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="f1da2-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f1da2-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="f1da2-119">Riferimento</span><span class="sxs-lookup"><span data-stu-id="f1da2-119">Reference</span></span>

[<span data-ttu-id="f1da2-120">Spazio dei nomi Microsoft. ISAM. esent. Interop. Windows8</span><span class="sxs-lookup"><span data-stu-id="f1da2-120">Microsoft.Isam.Esent.Interop.Windows8 namespace</span></span>](./microsoft.isam.esent.interop.windows8-namespace.md)
