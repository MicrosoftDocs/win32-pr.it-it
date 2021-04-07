---
description: 'Altre informazioni su: Metodo Windows7Api. JetPrereadKeys (JET_SESID, JET_TABLEID, byte [] [], Int32, Int32, Int32, PrereadKeysGrbit)'
title: Metodo Windows7Api. JetPrereadKeys (JET_SESID, JET_TABLEID, byte [] [], Int32, Int32, Int32, PrereadKeysGrbit) (Microsoft. ISAM. esent. Interop. Windows7)
TOCTitle: JetPrereadKeys method (JET_SESID, JET_TABLEID, Byte[][], Int32 , Int32, Int32, PrereadKeysGrbit)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Windows7.Windows7Api.JetPrereadKeys(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,System.Byte[][],System.Int32[],System.Int32,System.Int32@,Microsoft.Isam.Esent.Interop.Windows7.PrereadKeysGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.windows7.windows7api.jetprereadkeys(v=EXCHG.10)
ms:contentKeyID: 55107785
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Windows7.Windows7Api.JetPrereadKeys
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 66f85c08c1fccc58702d4ac4cf170d6b0493ab8a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049349"
---
# <a name="windows7apijetprereadkeys-method-jet_sesid-jet_tableid-byte-int32--int32-int32-prereadkeysgrbit"></a><span data-ttu-id="b2f89-103">Metodo Windows7Api. JetPrereadKeys (JET_SESID, JET_TABLEID, byte \[ \] \[ \] , Int32, Int32, Int32, PrereadKeysGrbit)</span><span class="sxs-lookup"><span data-stu-id="b2f89-103">Windows7Api.JetPrereadKeys method (JET_SESID, JET_TABLEID, Byte\[\]\[\], Int32 , Int32, Int32, PrereadKeysGrbit)</span></span>

<span data-ttu-id="b2f89-104">Se i record con le chiavi specificate non sono presenti nella cache buffer, avviare le letture asincrone per inserire i record nella cache buffer del database.</span><span class="sxs-lookup"><span data-stu-id="b2f89-104">If the records with the specified keys are not in the buffer cache then start asynchronous reads to bring the records into the database buffer cache.</span></span>

<span data-ttu-id="b2f89-105">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop. Windows7](./microsoft.isam.esent.interop.windows7-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="b2f89-105">**Namespace:**  [Microsoft.Isam.Esent.Interop.Windows7](./microsoft.isam.esent.interop.windows7-namespace.md)</span></span>  
<span data-ttu-id="b2f89-106">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="b2f89-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="b2f89-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b2f89-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetPrereadKeys ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    keys As Byte()(), _
    keyLengths As Integer(), _
    keyCount As Integer, _
    <OutAttribute> ByRef keysPreread As Integer, _
    grbit As PrereadKeysGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim keys As Byte()()
Dim keyLengths As Integer()
Dim keyCount As Integer
Dim keysPreread As Integer
Dim grbit As PrereadKeysGrbitWindows7Api.JetPrereadKeys(sesid, tableid, _
    keys, keyLengths, keyCount, keysPreread, _
    grbit)
```

``` csharp
public static void JetPrereadKeys(
    JET_SESID sesid,
    JET_TABLEID tableid,
    byte[][] keys,
    int[] keyLengths,
    int keyCount,
    out int keysPreread,
    PrereadKeysGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="b2f89-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="b2f89-108">Parameters</span></span>

  - <span data-ttu-id="b2f89-109">sesid</span><span class="sxs-lookup"><span data-stu-id="b2f89-109">sesid</span></span>  
    <span data-ttu-id="b2f89-110">Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="b2f89-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="b2f89-111">Sessione da utilizzare.</span><span class="sxs-lookup"><span data-stu-id="b2f89-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="b2f89-112">TableID</span><span class="sxs-lookup"><span data-stu-id="b2f89-112">tableid</span></span>  
    <span data-ttu-id="b2f89-113">Tipo: [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="b2f89-113">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="b2f89-114">Tabella su cui eseguire le preletture.</span><span class="sxs-lookup"><span data-stu-id="b2f89-114">The table to issue the prereads against.</span></span>

<!-- end list -->

  - <span data-ttu-id="b2f89-115">chiavi</span><span class="sxs-lookup"><span data-stu-id="b2f89-115">keys</span></span>  
    <span data-ttu-id="b2f89-116">Tipo \[\]</span><span class="sxs-lookup"><span data-stu-id="b2f89-116">Type: \[\]</span></span>  
    
    <span data-ttu-id="b2f89-117">Chiavi da preleggere.</span><span class="sxs-lookup"><span data-stu-id="b2f89-117">The keys to preread.</span></span> <span data-ttu-id="b2f89-118">Le chiavi devono essere ordinate.</span><span class="sxs-lookup"><span data-stu-id="b2f89-118">The keys must be sorted.</span></span>

<!-- end list -->

  - <span data-ttu-id="b2f89-119">Lunghezze di pagina</span><span class="sxs-lookup"><span data-stu-id="b2f89-119">keyLengths</span></span>  
    <span data-ttu-id="b2f89-120">Tipo \[\]</span><span class="sxs-lookup"><span data-stu-id="b2f89-120">Type: \[\]</span></span>  
    
    <span data-ttu-id="b2f89-121">Lunghezza delle chiavi da preleggere.</span><span class="sxs-lookup"><span data-stu-id="b2f89-121">The lengths of the keys to preread.</span></span>

<!-- end list -->

  - <span data-ttu-id="b2f89-122">Numero di conteggio</span><span class="sxs-lookup"><span data-stu-id="b2f89-122">keyCount</span></span>  
    <span data-ttu-id="b2f89-123">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="b2f89-123">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="b2f89-124">Numero massimo di chiavi da preleggere.</span><span class="sxs-lookup"><span data-stu-id="b2f89-124">The maximum number of keys to preread.</span></span>

<!-- end list -->

  - <span data-ttu-id="b2f89-125">keysPreread</span><span class="sxs-lookup"><span data-stu-id="b2f89-125">keysPreread</span></span>  
    <span data-ttu-id="b2f89-126">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="b2f89-126">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="b2f89-127">Restituisce il numero di chiavi da preleggere effettivamente.</span><span class="sxs-lookup"><span data-stu-id="b2f89-127">Returns the number of keys to actually preread.</span></span>

<!-- end list -->

  - <span data-ttu-id="b2f89-128">grbit</span><span class="sxs-lookup"><span data-stu-id="b2f89-128">grbit</span></span>  
    <span data-ttu-id="b2f89-129">Tipo: [Microsoft. ISAM. esent. Interop. Windows7. PrereadKeysGrbit](./prereadkeysgrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="b2f89-129">Type: [Microsoft.Isam.Esent.Interop.Windows7.PrereadKeysGrbit](./prereadkeysgrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="b2f89-130">Opzioni di prelettura.</span><span class="sxs-lookup"><span data-stu-id="b2f89-130">Preread options.</span></span> <span data-ttu-id="b2f89-131">Utilizzato per specificare la direzione della prelettura.</span><span class="sxs-lookup"><span data-stu-id="b2f89-131">Used to specify the direction of the preread.</span></span>

## <a name="see-also"></a><span data-ttu-id="b2f89-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b2f89-132">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="b2f89-133">Riferimento</span><span class="sxs-lookup"><span data-stu-id="b2f89-133">Reference</span></span>

[<span data-ttu-id="b2f89-134">Classe Windows7Api</span><span class="sxs-lookup"><span data-stu-id="b2f89-134">Windows7Api class</span></span>](./windows7api-class.md)

[<span data-ttu-id="b2f89-135">Membri di Windows7Api</span><span class="sxs-lookup"><span data-stu-id="b2f89-135">Windows7Api members</span></span>](./windows7api-members.md)

[<span data-ttu-id="b2f89-136">Overload JetPrereadKeys</span><span class="sxs-lookup"><span data-stu-id="b2f89-136">JetPrereadKeys overload</span></span>](./windows7api.jetprereadkeys-method.md)

[<span data-ttu-id="b2f89-137">Spazio dei nomi Microsoft. ISAM. esent. Interop. Windows7</span><span class="sxs-lookup"><span data-stu-id="b2f89-137">Microsoft.Isam.Esent.Interop.Windows7 namespace</span></span>](./microsoft.isam.esent.interop.windows7-namespace.md)
