---
description: 'Altre informazioni su: Enumerazione LegacyFileNames'
title: Enumerazione LegacyFileNames (Microsoft. ISAM. esent. Interop. vista)
TOCTitle: LegacyFileNames enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.Vista.LegacyFileNames
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.legacyfilenames(v=EXCHG.10)
ms:contentKeyID: 55104275
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.LegacyFileNames
- Microsoft.Isam.Esent.Interop.Vista.LegacyFileNames.EightDotThreeSoftCompat
- Microsoft.Isam.Esent.Interop.Vista.LegacyFileNames.ESE98FileNames
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.LegacyFileNames.EightDotThreeSoftCompat
- Microsoft.Isam.Esent.Interop.Vista.LegacyFileNames
- Microsoft.Isam.Esent.Interop.Vista.LegacyFileNames.ESE98FileNames
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d7f3cade11450bcfbad13dcdd114dca6701c5369
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966783"
---
# <a name="legacyfilenames-enumeration"></a><span data-ttu-id="b2359-103">Enumerazione LegacyFileNames</span><span class="sxs-lookup"><span data-stu-id="b2359-103">LegacyFileNames enumeration</span></span>

<span data-ttu-id="b2359-104">Opzioni per LegacyFileNames</span><span class="sxs-lookup"><span data-stu-id="b2359-104">Options for LegacyFileNames</span></span>

<span data-ttu-id="b2359-105">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop. vista](./microsoft.isam.esent.interop.vista-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="b2359-105">**Namespace:**  [Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span></span>  
<span data-ttu-id="b2359-106">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="b2359-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="b2359-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b2359-107">Syntax</span></span>

``` vb
'Declaration
Public Enumeration LegacyFileNames
'Usage
Dim instance As LegacyFileNames
```

``` csharp
public enum LegacyFileNames
```

## <a name="members"></a><span data-ttu-id="b2359-108">Members</span><span class="sxs-lookup"><span data-stu-id="b2359-108">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="b2359-109">Nome del membro</span><span class="sxs-lookup"><span data-stu-id="b2359-109">Member name</span></span></th>
<th><span data-ttu-id="b2359-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b2359-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="b2359-111">ESE98FileNames</span><span class="sxs-lookup"><span data-stu-id="b2359-111">ESE98FileNames</span></span></td>
<td><span data-ttu-id="b2359-112">Quando questa opzione è presente, il motore di database utilizzerà le convenzioni di denominazione seguenti per i file: o i file di log delle transazioni utilizzeranno. LOG per l'estensione di file o i file del checkpoint utilizzeranno. CHK per la relativa estensione di file</span><span class="sxs-lookup"><span data-stu-id="b2359-112">When this option is present then the database engine will use the following naming conventions for its files: o Transaction Log files will use .LOG for their file extension o Checkpoint files will use .CHK for their file extension</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="b2359-113">EightDotThreeSoftCompat</span><span class="sxs-lookup"><span data-stu-id="b2359-113">EightDotThreeSoftCompat</span></span></td>
<td><span data-ttu-id="b2359-114">Mantenere la sintassi di denominazione 8,3 per il periodo di tempo più lungo possibile.</span><span class="sxs-lookup"><span data-stu-id="b2359-114">Preserve the 8.3 naming syntax for as long as possible.</span></span> <span data-ttu-id="b2359-115">Questa operazione non deve essere modificata, con la garanzia che non siano presenti file di log.</span><span class="sxs-lookup"><span data-stu-id="b2359-115">(this should not be changed, w/o ensuring there are no log files)</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="b2359-116">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b2359-116">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="b2359-117">Riferimento</span><span class="sxs-lookup"><span data-stu-id="b2359-117">Reference</span></span>

[<span data-ttu-id="b2359-118">Spazio dei nomi Microsoft. ISAM. esent. Interop. vista</span><span class="sxs-lookup"><span data-stu-id="b2359-118">Microsoft.Isam.Esent.Interop.Vista namespace</span></span>](./microsoft.isam.esent.interop.vista-namespace.md)
