---
description: 'Altre informazioni su: Enumerazione CreateDatabaseGrbit'
title: Enumerazione CreateDatabaseGrbit
TOCTitle: CreateDatabaseGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.CreateDatabaseGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.createdatabasegrbit(v=EXCHG.10)
ms:contentKeyID: 39515634
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.CreateDatabaseGrbit
- Microsoft.Isam.Esent.Interop.CreateDatabaseGrbit.None
- Microsoft.Isam.Esent.Interop.CreateDatabaseGrbit.OverwriteExisting
- Microsoft.Isam.Esent.Interop.CreateDatabaseGrbit.RecoveryOff
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.CreateDatabaseGrbit.OverwriteExisting
- Microsoft.Isam.Esent.Interop.CreateDatabaseGrbit.RecoveryOff
- Microsoft.Isam.Esent.Interop.CreateDatabaseGrbit.None
- Microsoft.Isam.Esent.Interop.CreateDatabaseGrbit
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8e23b7b875863b747fc5d2ba021c90d5f7f71048
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049614"
---
# <a name="createdatabasegrbit-enumeration"></a><span data-ttu-id="da3de-103">Enumerazione CreateDatabaseGrbit</span><span class="sxs-lookup"><span data-stu-id="da3de-103">CreateDatabaseGrbit enumeration</span></span>

<span data-ttu-id="da3de-104">Opzioni per [JetCreateDatabase (JET_SESID, String, String, JET_DBID, CreateDatabaseGrbit)](./api.jetcreatedatabase-method.md).</span><span class="sxs-lookup"><span data-stu-id="da3de-104">Options for [JetCreateDatabase(JET_SESID, String, String, JET_DBID, CreateDatabaseGrbit)](./api.jetcreatedatabase-method.md).</span></span>

<span data-ttu-id="da3de-105">Questa enumerazione ha un attributo [FlagsAttribute](/dotnet/api/system.flagsattribute) che consente una combinazione bit per bit dei valori del relativo membro.</span><span class="sxs-lookup"><span data-stu-id="da3de-105">This enumeration has a [FlagsAttribute](/dotnet/api/system.flagsattribute) attribute that allows a bitwise combination of its member values.</span></span>

<span data-ttu-id="da3de-106">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="da3de-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="da3de-107">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="da3de-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="da3de-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="da3de-108">Syntax</span></span>

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration CreateDatabaseGrbit
'Usage
Dim instance As CreateDatabaseGrbit
```

``` csharp
[FlagsAttribute]
public enum CreateDatabaseGrbit
```

## <a name="members"></a><span data-ttu-id="da3de-109">Members</span><span class="sxs-lookup"><span data-stu-id="da3de-109">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="da3de-110">Nome del membro</span><span class="sxs-lookup"><span data-stu-id="da3de-110">Member name</span></span></th>
<th><span data-ttu-id="da3de-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="da3de-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="da3de-112">nessuno</span><span class="sxs-lookup"><span data-stu-id="da3de-112">None</span></span></td>
<td><span data-ttu-id="da3de-113">Opzioni predefinite.</span><span class="sxs-lookup"><span data-stu-id="da3de-113">Default options.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="da3de-114">OverwriteExisting</span><span class="sxs-lookup"><span data-stu-id="da3de-114">OverwriteExisting</span></span></td>
<td><span data-ttu-id="da3de-115">Per impostazione predefinita, se viene chiamato JetCreateDatabase e il database esiste già, la chiamata API avrà esito negativo e il database originale non verrà sovrascritto.</span><span class="sxs-lookup"><span data-stu-id="da3de-115">By default, if JetCreateDatabase is called and the database already exists, the Api call will fail and the original database will not be overwritten.</span></span> <span data-ttu-id="da3de-116">OverwriteExisting modifica questo comportamento e il database precedente verrà sovrascritto con uno nuovo.</span><span class="sxs-lookup"><span data-stu-id="da3de-116">OverwriteExisting changes this behavior, and the old database will be overwritten with a new one.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="da3de-117">RecoveryOff</span><span class="sxs-lookup"><span data-stu-id="da3de-117">RecoveryOff</span></span></td>
<td><span data-ttu-id="da3de-118">Disattiva la registrazione.</span><span class="sxs-lookup"><span data-stu-id="da3de-118">Turns off logging.</span></span> <span data-ttu-id="da3de-119">L'impostazione di questo bit perde la possibilità di riprodurre i file di log e di ripristinare il database in uno stato utilizzabile coerente dopo un arresto anomalo del sistema.</span><span class="sxs-lookup"><span data-stu-id="da3de-119">Setting this bit loses the ability to replay log files and recover the database to a consistent usable state after a crash.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="da3de-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="da3de-120">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="da3de-121">Riferimento</span><span class="sxs-lookup"><span data-stu-id="da3de-121">Reference</span></span>

[<span data-ttu-id="da3de-122">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="da3de-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
