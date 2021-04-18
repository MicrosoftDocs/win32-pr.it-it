---
description: 'Altre informazioni su: JET_UNICODEINDEX. Metodo GetEffectiveLocaleName'
title: JET_UNICODEINDEX. Metodo GetEffectiveLocaleName
TOCTitle: 'GetEffectiveLocaleName method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_UNICODEINDEX.GetEffectiveLocaleName
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_unicodeindex.geteffectivelocalename(v=EXCHG.10)
ms:contentKeyID: 55103988
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_UNICODEINDEX.GetEffectiveLocaleName
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_UNICODEINDEX.GetEffectiveLocaleName
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 012ed93015705454efdf5e329d4b385924f1a343
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305742"
---
# <a name="jet_unicodeindexgeteffectivelocalename-method"></a><span data-ttu-id="4cb90-103">JET_UNICODEINDEX. Metodo GetEffectiveLocaleName</span><span class="sxs-lookup"><span data-stu-id="4cb90-103">JET_UNICODEINDEX.GetEffectiveLocaleName method</span></span>

<span data-ttu-id="4cb90-104">Come soluzione alternativa per i sistemi che non dispongono del supporto LCID, viene convertito un numero molto limitato di LCID nei nomi delle impostazioni locali.</span><span class="sxs-lookup"><span data-stu-id="4cb90-104">As a workaround for systems that do not have LCID support, we will convert a VERY limited number of LCIDs to locale names.</span></span>

<span data-ttu-id="4cb90-105">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="4cb90-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="4cb90-106">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="4cb90-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="4cb90-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4cb90-107">Syntax</span></span>

``` vb
'Declaration
Public Function GetEffectiveLocaleName As String
'Usage
Dim instance As JET_UNICODEINDEX
Dim returnValue As String

returnValue = instance.GetEffectiveLocaleName()
```

``` csharp
public string GetEffectiveLocaleName()
```

#### <a name="return-value"></a><span data-ttu-id="4cb90-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4cb90-108">Return value</span></span>

<span data-ttu-id="4cb90-109">Tipo: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="4cb90-109">Type: [System.String](/dotnet/api/system.string)</span></span>  
<span data-ttu-id="4cb90-110">Nome delle impostazioni locali dello stile BCP-47.</span><span class="sxs-lookup"><span data-stu-id="4cb90-110">A BCP-47 style locale name.</span></span>  

## <a name="see-also"></a><span data-ttu-id="4cb90-111">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4cb90-111">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="4cb90-112">Riferimento</span><span class="sxs-lookup"><span data-stu-id="4cb90-112">Reference</span></span>

[<span data-ttu-id="4cb90-113">Classe JET_UNICODEINDEX</span><span class="sxs-lookup"><span data-stu-id="4cb90-113">JET_UNICODEINDEX class</span></span>](./jet-unicodeindex-class.md)

[<span data-ttu-id="4cb90-114">Membri JET_UNICODEINDEX</span><span class="sxs-lookup"><span data-stu-id="4cb90-114">JET_UNICODEINDEX members</span></span>](./jet-unicodeindex-members.md)

[<span data-ttu-id="4cb90-115">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="4cb90-115">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
