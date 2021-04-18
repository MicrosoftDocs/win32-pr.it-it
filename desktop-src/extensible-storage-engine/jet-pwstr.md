---
description: 'Altre informazioni su: JET_PWSTR'
title: JET_PWSTR
TOCTitle: JET_PWSTR
ms:assetid: 6575f0f0-d022-4e70-9f17-c1d884d9e226
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269271(v=EXCHG.10)
ms:contentKeyID: 32765573
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 536ef3bba465f6d152e3483436c1dc1e82277339
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315647"
---
# <a name="jet_pwstr"></a><span data-ttu-id="9c25c-103">JET_PWSTR</span><span class="sxs-lookup"><span data-stu-id="9c25c-103">JET_PWSTR</span></span>


<span data-ttu-id="9c25c-104">_**Si applica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="9c25c-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_pwstr"></a><span data-ttu-id="9c25c-105">JET_PWSTR</span><span class="sxs-lookup"><span data-stu-id="9c25c-105">JET_PWSTR</span></span>

<span data-ttu-id="9c25c-106">Il tipo di dati **JET_PWSTR** contiene una stringa **Unicode** con terminazione null (char \* ).</span><span class="sxs-lookup"><span data-stu-id="9c25c-106">The **JET_PWSTR** data type contains a null-terminated **Unicode** string (char \*).</span></span>

<span data-ttu-id="9c25c-107">**Windows Vista: JET_PWSTR** è stato introdotto in Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="9c25c-107">**Windows Vista:  JET_PWSTR** is introduced in Windows Vista.</span></span>

```cpp
    typedef __nullterminated WCHAR * JET_PWSTR;
```

### <a name="data-types"></a><span data-ttu-id="9c25c-108">Tipi di dati</span><span class="sxs-lookup"><span data-stu-id="9c25c-108">Data Types</span></span>

<span data-ttu-id="9c25c-109">JET_PWSTR</span><span class="sxs-lookup"><span data-stu-id="9c25c-109">JET_PWSTR</span></span>

<span data-ttu-id="9c25c-110">Con terminazione null, stringa Unicode (char \* ).</span><span class="sxs-lookup"><span data-stu-id="9c25c-110">Null-terminated, Unicode string (char \*).</span></span>

### <a name="requirements"></a><span data-ttu-id="9c25c-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9c25c-111">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9c25c-112"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="9c25c-112"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="9c25c-113">Richiede Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="9c25c-113">Requires Windows Vista.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9c25c-114"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="9c25c-114"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="9c25c-115">Richiede Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="9c25c-115">Requires Windows Server 2008.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9c25c-116"><strong>Intestazione</strong></span><span class="sxs-lookup"><span data-stu-id="9c25c-116"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="9c25c-117">Dichiarata in esent. h.</span><span class="sxs-lookup"><span data-stu-id="9c25c-117">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>

