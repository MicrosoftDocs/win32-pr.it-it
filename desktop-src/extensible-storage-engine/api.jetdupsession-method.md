---
description: 'Altre informazioni su: metodo API. JetDupSession'
title: API. JetDupSession, metodo
TOCTitle: 'JetDupSession method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetDupSession(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_SESID@)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetdupsession(v=EXCHG.10)
ms:contentKeyID: 55100689
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetDupSession
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetDupSession
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 9013c3c99c1d6c6067386038ec4a51f37f978650
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128710"
---
# <a name="apijetdupsession-method"></a><span data-ttu-id="ddc08-103">API. JetDupSession, metodo</span><span class="sxs-lookup"><span data-stu-id="ddc08-103">Api.JetDupSession method</span></span>

<span data-ttu-id="ddc08-104">Inizializzare una nuova sessione ESE nella stessa istanza del sesid specificato.</span><span class="sxs-lookup"><span data-stu-id="ddc08-104">Initialize a new ESE session in the same instance as the given sesid.</span></span>

<span data-ttu-id="ddc08-105">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="ddc08-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="ddc08-106">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="ddc08-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="ddc08-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ddc08-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetDupSession ( _
    sesid As JET_SESID, _
    <OutAttribute> ByRef newSesid As JET_SESID _
)
'Usage
Dim sesid As JET_SESID
Dim newSesid As JET_SESIDApi.JetDupSession(sesid, newSesid)
```

``` csharp
public static void JetDupSession(
    JET_SESID sesid,
    out JET_SESID newSesid
)
```

#### <a name="parameters"></a><span data-ttu-id="ddc08-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="ddc08-108">Parameters</span></span>

  - <span data-ttu-id="ddc08-109">sesid</span><span class="sxs-lookup"><span data-stu-id="ddc08-109">sesid</span></span>  
    <span data-ttu-id="ddc08-110">Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="ddc08-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="ddc08-111">Sessione da duplicare.</span><span class="sxs-lookup"><span data-stu-id="ddc08-111">The session to duplicate.</span></span>

<!-- end list -->

  - <span data-ttu-id="ddc08-112">newSesid</span><span class="sxs-lookup"><span data-stu-id="ddc08-112">newSesid</span></span>  
    <span data-ttu-id="ddc08-113">Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="ddc08-113">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="ddc08-114">Restituisce la nuova sessione.</span><span class="sxs-lookup"><span data-stu-id="ddc08-114">Returns the new session.</span></span>

## <a name="see-also"></a><span data-ttu-id="ddc08-115">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ddc08-115">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="ddc08-116">Riferimento</span><span class="sxs-lookup"><span data-stu-id="ddc08-116">Reference</span></span>

[<span data-ttu-id="ddc08-117">Classe API</span><span class="sxs-lookup"><span data-stu-id="ddc08-117">Api class</span></span>](./api-class.md)

[<span data-ttu-id="ddc08-118">Membri API</span><span class="sxs-lookup"><span data-stu-id="ddc08-118">Api members</span></span>](./api-members.md)

[<span data-ttu-id="ddc08-119">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="ddc08-119">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
