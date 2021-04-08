---
description: 'Altre informazioni su: Enumerazione EscrowUpdateGrbit'
title: Enumerazione EscrowUpdateGrbit
TOCTitle: EscrowUpdateGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.EscrowUpdateGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.escrowupdategrbit(v=EXCHG.10)
ms:contentKeyID: 39514160
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EscrowUpdateGrbit
- Microsoft.Isam.Esent.Interop.EscrowUpdateGrbit.None
- Microsoft.Isam.Esent.Interop.EscrowUpdateGrbit.NoRollback
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EscrowUpdateGrbit
- Microsoft.Isam.Esent.Interop.EscrowUpdateGrbit.None
- Microsoft.Isam.Esent.Interop.EscrowUpdateGrbit.NoRollback
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d301ef801a5685057a9e33beb794f3b6cf13e646
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968535"
---
# <a name="escrowupdategrbit-enumeration"></a><span data-ttu-id="9eee1-103">Enumerazione EscrowUpdateGrbit</span><span class="sxs-lookup"><span data-stu-id="9eee1-103">EscrowUpdateGrbit enumeration</span></span>

<span data-ttu-id="9eee1-104">Opzioni per JetEscrowUpdate.</span><span class="sxs-lookup"><span data-stu-id="9eee1-104">Options for JetEscrowUpdate.</span></span>

<span data-ttu-id="9eee1-105">Questa enumerazione ha un attributo [FlagsAttribute](/dotnet/api/system.flagsattribute) che consente una combinazione bit per bit dei valori del relativo membro.</span><span class="sxs-lookup"><span data-stu-id="9eee1-105">This enumeration has a [FlagsAttribute](/dotnet/api/system.flagsattribute) attribute that allows a bitwise combination of its member values.</span></span>

<span data-ttu-id="9eee1-106">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="9eee1-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="9eee1-107">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="9eee1-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="9eee1-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9eee1-108">Syntax</span></span>

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration EscrowUpdateGrbit
'Usage
Dim instance As EscrowUpdateGrbit
```

``` csharp
[FlagsAttribute]
public enum EscrowUpdateGrbit
```

## <a name="members"></a><span data-ttu-id="9eee1-109">Members</span><span class="sxs-lookup"><span data-stu-id="9eee1-109">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="9eee1-110">Nome del membro</span><span class="sxs-lookup"><span data-stu-id="9eee1-110">Member name</span></span></th>
<th><span data-ttu-id="9eee1-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9eee1-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="9eee1-112">nessuno</span><span class="sxs-lookup"><span data-stu-id="9eee1-112">None</span></span></td>
<td><span data-ttu-id="9eee1-113">Opzioni predefinite.</span><span class="sxs-lookup"><span data-stu-id="9eee1-113">Default options.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="9eee1-114">Norollback</span><span class="sxs-lookup"><span data-stu-id="9eee1-114">NoRollback</span></span></td>
<td><span data-ttu-id="9eee1-115">Anche se la sessione che esegue l'aggiornamento del deposito a garanzia ha il rollback della transazione, questo aggiornamento non verrà annullato.</span><span class="sxs-lookup"><span data-stu-id="9eee1-115">Even if the session performing the escrow update has its transaction rollback this update will not be undone.</span></span> <span data-ttu-id="9eee1-116">Poiché è possibile che i record del log non vengano scaricati su disco, gli aggiornamenti del deposito recenti eseguiti con questo flag potrebbero andare persi in caso di arresto anomalo del sistema.</span><span class="sxs-lookup"><span data-stu-id="9eee1-116">As the log records may not be flushed to disk, recent escrow updates done with this flag may be lost if there is a crash.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="9eee1-117">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9eee1-117">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="9eee1-118">Riferimento</span><span class="sxs-lookup"><span data-stu-id="9eee1-118">Reference</span></span>

[<span data-ttu-id="9eee1-119">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="9eee1-119">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
