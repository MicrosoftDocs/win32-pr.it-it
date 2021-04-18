---
description: 'Altre informazioni su: VistaApi. JetInit3, metodo'
title: Metodo VistaApi. JetInit3 (Microsoft. ISAM. esent. Interop. vista)
TOCTitle: 'JetInit3 method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Vista.VistaApi.JetInit3(Microsoft.Isam.Esent.Interop.JET_INSTANCE@,Microsoft.Isam.Esent.Interop.JET_RSTINFO,Microsoft.Isam.Esent.Interop.InitGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.vistaapi.jetinit3(v=EXCHG.10)
ms:contentKeyID: 55104198
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.VistaApi.JetInit3
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.VistaApi.JetInit3
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7c5fa7d1450240a8250e66e2bbe6d8ef0b97c136
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307786"
---
# <a name="vistaapijetinit3-method"></a><span data-ttu-id="f50d0-103">VistaApi. JetInit3, metodo</span><span class="sxs-lookup"><span data-stu-id="f50d0-103">VistaApi.JetInit3 method</span></span>

<span data-ttu-id="f50d0-104">Inizializzare il motore di database ESENT.</span><span class="sxs-lookup"><span data-stu-id="f50d0-104">Initialize the ESENT database engine.</span></span>

<span data-ttu-id="f50d0-105">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop. vista](./microsoft.isam.esent.interop.vista-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="f50d0-105">**Namespace:**  [Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span></span>  
<span data-ttu-id="f50d0-106">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="f50d0-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="f50d0-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f50d0-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Function JetInit3 ( _
    ByRef instance As JET_INSTANCE, _
    recoveryOptions As JET_RSTINFO, _
    grbit As InitGrbit _
) As JET_wrn
'Usage
Dim instance As JET_INSTANCE
Dim recoveryOptions As JET_RSTINFO
Dim grbit As InitGrbit
Dim returnValue As JET_wrn

returnValue = VistaApi.JetInit3(instance, _
    recoveryOptions, grbit)
```

``` csharp
public static JET_wrn JetInit3(
    ref JET_INSTANCE instance,
    JET_RSTINFO recoveryOptions,
    InitGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="f50d0-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="f50d0-108">Parameters</span></span>

  - <span data-ttu-id="f50d0-109">instance</span><span class="sxs-lookup"><span data-stu-id="f50d0-109">instance</span></span>  
    <span data-ttu-id="f50d0-110">Tipo: [Microsoft.ISAM.esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span><span class="sxs-lookup"><span data-stu-id="f50d0-110">Type: [Microsoft.Isam.Esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span></span>  
    
    <span data-ttu-id="f50d0-111">Istanza di da inizializzare.</span><span class="sxs-lookup"><span data-stu-id="f50d0-111">The instance to initialize.</span></span> <span data-ttu-id="f50d0-112">Se un'istanza non è stata allocata, ne viene creata una nuova e il motore funziona in modalità a istanza singola.</span><span class="sxs-lookup"><span data-stu-id="f50d0-112">If an instance hasn't been allocated then a new one is created and the engine will operate in single-instance mode.</span></span>

<!-- end list -->

  - <span data-ttu-id="f50d0-113">recoveryOptions</span><span class="sxs-lookup"><span data-stu-id="f50d0-113">recoveryOptions</span></span>  
    <span data-ttu-id="f50d0-114">Tipo: [Microsoft.ISAM.esent.Interop.JET_RSTINFO](./jet-rstinfo-class.md)</span><span class="sxs-lookup"><span data-stu-id="f50d0-114">Type: [Microsoft.Isam.Esent.Interop.JET_RSTINFO](./jet-rstinfo-class.md)</span></span>  
    
    <span data-ttu-id="f50d0-115">Parametri di ripristino aggiuntivi per la modifica del mapping dei database durante il ripristino, posizione in cui arrestare il ripristino o stato di ripristino.</span><span class="sxs-lookup"><span data-stu-id="f50d0-115">Additional recovery parameters for remapping databases during recovery, position where to stop recovery at, or recovery status.</span></span>

<!-- end list -->

  - <span data-ttu-id="f50d0-116">grbit</span><span class="sxs-lookup"><span data-stu-id="f50d0-116">grbit</span></span>  
    <span data-ttu-id="f50d0-117">Tipo: [Microsoft.Isam.Esent.Interop.InitGrbit](./initgrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="f50d0-117">Type: [Microsoft.Isam.Esent.Interop.InitGrbit](./initgrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="f50d0-118">Opzioni di inizializzazione.</span><span class="sxs-lookup"><span data-stu-id="f50d0-118">Initialization options.</span></span>

#### <a name="return-value"></a><span data-ttu-id="f50d0-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f50d0-119">Return value</span></span>

<span data-ttu-id="f50d0-120">Tipo: [Microsoft.ISAM.esent.Interop.JET_wrn](./jet-wrn-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="f50d0-120">Type: [Microsoft.Isam.Esent.Interop.JET_wrn](./jet-wrn-enumeration.md)</span></span>  
<span data-ttu-id="f50d0-121">Codice di avviso.</span><span class="sxs-lookup"><span data-stu-id="f50d0-121">A warning code.</span></span>  

## <a name="see-also"></a><span data-ttu-id="f50d0-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f50d0-122">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="f50d0-123">Riferimento</span><span class="sxs-lookup"><span data-stu-id="f50d0-123">Reference</span></span>

[<span data-ttu-id="f50d0-124">Classe VistaApi</span><span class="sxs-lookup"><span data-stu-id="f50d0-124">VistaApi class</span></span>](./vistaapi-class.md)

[<span data-ttu-id="f50d0-125">Membri di VistaApi</span><span class="sxs-lookup"><span data-stu-id="f50d0-125">VistaApi members</span></span>](./vistaapi-members.md)

[<span data-ttu-id="f50d0-126">Spazio dei nomi Microsoft. ISAM. esent. Interop. vista</span><span class="sxs-lookup"><span data-stu-id="f50d0-126">Microsoft.Isam.Esent.Interop.Vista namespace</span></span>](./microsoft.isam.esent.interop.vista-namespace.md)
