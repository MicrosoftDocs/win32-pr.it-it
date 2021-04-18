---
description: 'Altre informazioni su: Enumerazione RollbackTransactionGrbit'
title: Enumerazione RollbackTransactionGrbit
TOCTitle: RollbackTransactionGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.RollbackTransactionGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.rollbacktransactiongrbit(v=EXCHG.10)
ms:contentKeyID: 39513584
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.RollbackTransactionGrbit
- Microsoft.Isam.Esent.Interop.RollbackTransactionGrbit.None
- Microsoft.Isam.Esent.Interop.RollbackTransactionGrbit.RollbackAll
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.RollbackTransactionGrbit.RollbackAll
- Microsoft.Isam.Esent.Interop.RollbackTransactionGrbit.None
- Microsoft.Isam.Esent.Interop.RollbackTransactionGrbit
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: bf2635d94070fc47bebbd6cdd0e53deddeb4c5eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313076"
---
# <a name="rollbacktransactiongrbit-enumeration"></a><span data-ttu-id="c8dfd-103">Enumerazione RollbackTransactionGrbit</span><span class="sxs-lookup"><span data-stu-id="c8dfd-103">RollbackTransactionGrbit enumeration</span></span>

<span data-ttu-id="c8dfd-104">Opzioni per JetRollbackTransaction.</span><span class="sxs-lookup"><span data-stu-id="c8dfd-104">Options for JetRollbackTransaction.</span></span>

<span data-ttu-id="c8dfd-105">Questa enumerazione ha un attributo [FlagsAttribute](/dotnet/api/system.flagsattribute) che consente una combinazione bit per bit dei valori del relativo membro.</span><span class="sxs-lookup"><span data-stu-id="c8dfd-105">This enumeration has a [FlagsAttribute](/dotnet/api/system.flagsattribute) attribute that allows a bitwise combination of its member values.</span></span>

<span data-ttu-id="c8dfd-106">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="c8dfd-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="c8dfd-107">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="c8dfd-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="c8dfd-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c8dfd-108">Syntax</span></span>

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration RollbackTransactionGrbit
'Usage
Dim instance As RollbackTransactionGrbit
```

``` csharp
[FlagsAttribute]
public enum RollbackTransactionGrbit
```

## <a name="members"></a><span data-ttu-id="c8dfd-109">Members</span><span class="sxs-lookup"><span data-stu-id="c8dfd-109">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="c8dfd-110">Nome del membro</span><span class="sxs-lookup"><span data-stu-id="c8dfd-110">Member name</span></span></th>
<th><span data-ttu-id="c8dfd-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c8dfd-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="c8dfd-112">nessuno</span><span class="sxs-lookup"><span data-stu-id="c8dfd-112">None</span></span></td>
<td><span data-ttu-id="c8dfd-113">Opzioni predefinite.</span><span class="sxs-lookup"><span data-stu-id="c8dfd-113">Default options.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="c8dfd-114">RollbackAll</span><span class="sxs-lookup"><span data-stu-id="c8dfd-114">RollbackAll</span></span></td>
<td><span data-ttu-id="c8dfd-115">Questa opzione richiede che vengano annullate tutte le modifiche apportate allo stato del database durante tutti i punti di salvataggio.</span><span class="sxs-lookup"><span data-stu-id="c8dfd-115">This option requests that all changes made to the state of the database during all save points be undone.</span></span> <span data-ttu-id="c8dfd-116">Di conseguenza, la sessione uscirà dalla transazione.</span><span class="sxs-lookup"><span data-stu-id="c8dfd-116">As a result, the session will exit the transaction.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="c8dfd-117">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c8dfd-117">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="c8dfd-118">Riferimento</span><span class="sxs-lookup"><span data-stu-id="c8dfd-118">Reference</span></span>

[<span data-ttu-id="c8dfd-119">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="c8dfd-119">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
