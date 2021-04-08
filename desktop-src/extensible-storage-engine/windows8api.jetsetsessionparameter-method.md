---
description: 'Altre informazioni su: Windows8Api. JetSetSessionParameter, metodo'
title: Metodo Windows8Api. JetSetSessionParameter (Microsoft. ISAM. esent. Interop. Windows8)
TOCTitle: 'JetSetSessionParameter method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Windows8.Windows8Api.JetSetSessionParameter(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.Windows8.JET_sesparam,System.Byte[],System.Int32)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.windows8.windows8api.jetsetsessionparameter(v=EXCHG.10)
ms:contentKeyID: 55104461
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Windows8.Windows8Api.JetSetSessionParameter
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Windows8.Windows8Api.JetSetSessionParameter
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b73331c765e1f8026b39c28dde5268417601663c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103879942"
---
# <a name="windows8apijetsetsessionparameter-method"></a><span data-ttu-id="0f389-103">Windows8Api. JetSetSessionParameter, metodo</span><span class="sxs-lookup"><span data-stu-id="0f389-103">Windows8Api.JetSetSessionParameter method</span></span>

<span data-ttu-id="0f389-104">Imposta un parametro nello stato della sessione specificato, utilizzato per la durata della sessione o fino alla reimpostazione.</span><span class="sxs-lookup"><span data-stu-id="0f389-104">Sets a parameter on the provided session state, used for the lifetime of this session or until reset.</span></span>

<span data-ttu-id="0f389-105">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop. Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="0f389-105">**Namespace:**  [Microsoft.Isam.Esent.Interop.Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)</span></span>  
<span data-ttu-id="0f389-106">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="0f389-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="0f389-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0f389-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetSetSessionParameter ( _
    sesid As JET_SESID, _
    sesparamid As JET_sesparam, _
    data As Byte(), _
    dataSize As Integer _
)
'Usage
Dim sesid As JET_SESID
Dim sesparamid As JET_sesparam
Dim data As Byte()
Dim dataSize As IntegerWindows8Api.JetSetSessionParameter(sesid, _
    sesparamid, data, dataSize)
```

``` csharp
public static void JetSetSessionParameter(
    JET_SESID sesid,
    JET_sesparam sesparamid,
    byte[] data,
    int dataSize
)
```

#### <a name="parameters"></a><span data-ttu-id="0f389-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="0f389-108">Parameters</span></span>

  - <span data-ttu-id="0f389-109">sesid</span><span class="sxs-lookup"><span data-stu-id="0f389-109">sesid</span></span>  
    <span data-ttu-id="0f389-110">Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="0f389-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="0f389-111">Sessione in cui impostare il parametro.</span><span class="sxs-lookup"><span data-stu-id="0f389-111">The session to set the parameter on.</span></span>

<!-- end list -->

  - <span data-ttu-id="0f389-112">sesparamid</span><span class="sxs-lookup"><span data-stu-id="0f389-112">sesparamid</span></span>  
    <span data-ttu-id="0f389-113">Tipo: [Microsoft.ISAM.esent.Interop.Windows8.JET_sesparam](./jet-sesparam-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="0f389-113">Type: [Microsoft.Isam.Esent.Interop.Windows8.JET_sesparam](./jet-sesparam-enumeration.md)</span></span>  
    
    <span data-ttu-id="0f389-114">ID del parametro della sessione da impostare.</span><span class="sxs-lookup"><span data-stu-id="0f389-114">The ID of the session parameter to set.</span></span>

<!-- end list -->

  - <span data-ttu-id="0f389-115">data</span><span class="sxs-lookup"><span data-stu-id="0f389-115">data</span></span>  
    <span data-ttu-id="0f389-116">Tipo \[\]</span><span class="sxs-lookup"><span data-stu-id="0f389-116">Type: \[\]</span></span>  
    
    <span data-ttu-id="0f389-117">Dati da impostare in questo parametro della sessione.</span><span class="sxs-lookup"><span data-stu-id="0f389-117">Data to set in this session parameter.</span></span>

<!-- end list -->

  - <span data-ttu-id="0f389-118">dataSize</span><span class="sxs-lookup"><span data-stu-id="0f389-118">dataSize</span></span>  
    <span data-ttu-id="0f389-119">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="0f389-119">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="0f389-120">Dimensione dei dati forniti.</span><span class="sxs-lookup"><span data-stu-id="0f389-120">Size of the data provided.</span></span>

## <a name="see-also"></a><span data-ttu-id="0f389-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0f389-121">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="0f389-122">Riferimento</span><span class="sxs-lookup"><span data-stu-id="0f389-122">Reference</span></span>

[<span data-ttu-id="0f389-123">Classe Windows8Api</span><span class="sxs-lookup"><span data-stu-id="0f389-123">Windows8Api class</span></span>](./windows8api-class.md)

[<span data-ttu-id="0f389-124">Membri di Windows8Api</span><span class="sxs-lookup"><span data-stu-id="0f389-124">Windows8Api members</span></span>](./windows8api-members.md)

[<span data-ttu-id="0f389-125">Spazio dei nomi Microsoft. ISAM. esent. Interop. Windows8</span><span class="sxs-lookup"><span data-stu-id="0f389-125">Microsoft.Isam.Esent.Interop.Windows8 namespace</span></span>](./microsoft.isam.esent.interop.windows8-namespace.md)
