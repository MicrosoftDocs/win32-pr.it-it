---
description: 'Altre informazioni su: metodo API. JetGetSystemParameter (JET_INSTANCE, JET_SESID, JET_param, Int32, String, Int32)'
title: Metodo API. JetGetSystemParameter (JET_INSTANCE, JET_SESID, JET_param, Int32, String, Int32)
TOCTitle: JetGetSystemParameter method (JET_INSTANCE, JET_SESID, JET_param, Int32, String, Int32)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetGetSystemParameter(Microsoft.Isam.Esent.Interop.JET_INSTANCE,Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_param,System.Int32@,System.String@,System.Int32)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetgetsystemparameter(v=EXCHG.10)
ms:contentKeyID: 55100727
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetGetSystemParameter
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 840c17ef1d74b57b4bee75b9efafe5a314f09a57
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103878873"
---
# <a name="apijetgetsystemparameter-method-jet_instance-jet_sesid-jet_param-int32-string-int32"></a><span data-ttu-id="6c9b3-103">Metodo API. JetGetSystemParameter (JET_INSTANCE, JET_SESID, JET_param, Int32, String, Int32)</span><span class="sxs-lookup"><span data-stu-id="6c9b3-103">Api.JetGetSystemParameter method (JET_INSTANCE, JET_SESID, JET_param, Int32, String, Int32)</span></span>

<span data-ttu-id="6c9b3-104">Ottiene le opzioni di configurazione del database.</span><span class="sxs-lookup"><span data-stu-id="6c9b3-104">Gets database configuration options.</span></span>

<span data-ttu-id="6c9b3-105">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="6c9b3-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="6c9b3-106">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="6c9b3-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="6c9b3-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6c9b3-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Function JetGetSystemParameter ( _
    instance As JET_INSTANCE, _
    sesid As JET_SESID, _
    paramid As JET_param, _
    ByRef paramValue As Integer, _
    <OutAttribute> ByRef paramString As String, _
    maxParam As Integer _
) As JET_wrn
'Usage
Dim instance As JET_INSTANCE
Dim sesid As JET_SESID
Dim paramid As JET_param
Dim paramValue As Integer
Dim paramString As String
Dim maxParam As Integer
Dim returnValue As JET_wrn

returnValue = Api.JetGetSystemParameter(instance, _
    sesid, paramid, paramValue, paramString, _
    maxParam)
```

``` csharp
public static JET_wrn JetGetSystemParameter(
    JET_INSTANCE instance,
    JET_SESID sesid,
    JET_param paramid,
    ref int paramValue,
    out string paramString,
    int maxParam
)
```

#### <a name="parameters"></a><span data-ttu-id="6c9b3-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="6c9b3-108">Parameters</span></span>

  - <span data-ttu-id="6c9b3-109">instance</span><span class="sxs-lookup"><span data-stu-id="6c9b3-109">instance</span></span>  
    <span data-ttu-id="6c9b3-110">Tipo: [Microsoft.ISAM.esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span><span class="sxs-lookup"><span data-stu-id="6c9b3-110">Type: [Microsoft.Isam.Esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span></span>  
    
    <span data-ttu-id="6c9b3-111">Istanza da cui recuperare le opzioni.</span><span class="sxs-lookup"><span data-stu-id="6c9b3-111">The instance to retrieve the options from.</span></span>

<!-- end list -->

  - <span data-ttu-id="6c9b3-112">sesid</span><span class="sxs-lookup"><span data-stu-id="6c9b3-112">sesid</span></span>  
    <span data-ttu-id="6c9b3-113">Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="6c9b3-113">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="6c9b3-114">Sessione da utilizzare.</span><span class="sxs-lookup"><span data-stu-id="6c9b3-114">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="6c9b3-115">paramid</span><span class="sxs-lookup"><span data-stu-id="6c9b3-115">paramid</span></span>  
    <span data-ttu-id="6c9b3-116">Tipo: [Microsoft.ISAM.esent.Interop.JET_param](./jet-param-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="6c9b3-116">Type: [Microsoft.Isam.Esent.Interop.JET_param](./jet-param-enumeration.md)</span></span>  
    
    <span data-ttu-id="6c9b3-117">Parametro da ottenere.</span><span class="sxs-lookup"><span data-stu-id="6c9b3-117">The parameter to get.</span></span>

<!-- end list -->

  - <span data-ttu-id="6c9b3-118">paramValue</span><span class="sxs-lookup"><span data-stu-id="6c9b3-118">paramValue</span></span>  
    <span data-ttu-id="6c9b3-119">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="6c9b3-119">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="6c9b3-120">Restituisce il valore del parametro, se il valore è un numero intero.</span><span class="sxs-lookup"><span data-stu-id="6c9b3-120">Returns the value of the parameter, if the value is an integer.</span></span>

<!-- end list -->

  - <span data-ttu-id="6c9b3-121">paramString</span><span class="sxs-lookup"><span data-stu-id="6c9b3-121">paramString</span></span>  
    <span data-ttu-id="6c9b3-122">Tipo: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="6c9b3-122">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="6c9b3-123">Restituisce il valore del parametro, se il valore è una stringa.</span><span class="sxs-lookup"><span data-stu-id="6c9b3-123">Returns the value of the parameter, if the value is a string.</span></span>

<!-- end list -->

  - <span data-ttu-id="6c9b3-124">maxParam</span><span class="sxs-lookup"><span data-stu-id="6c9b3-124">maxParam</span></span>  
    <span data-ttu-id="6c9b3-125">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="6c9b3-125">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="6c9b3-126">Dimensione massima della stringa di parametro.</span><span class="sxs-lookup"><span data-stu-id="6c9b3-126">The maximum size of the parameter string.</span></span>

#### <a name="return-value"></a><span data-ttu-id="6c9b3-127">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="6c9b3-127">Return value</span></span>

<span data-ttu-id="6c9b3-128">Tipo: [Microsoft.ISAM.esent.Interop.JET_wrn](./jet-wrn-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="6c9b3-128">Type: [Microsoft.Isam.Esent.Interop.JET_wrn](./jet-wrn-enumeration.md)</span></span>  
<span data-ttu-id="6c9b3-129">Codice di avviso ESENT.</span><span class="sxs-lookup"><span data-stu-id="6c9b3-129">An ESENT warning code.</span></span>  

## <a name="remarks"></a><span data-ttu-id="6c9b3-130">Commenti</span><span class="sxs-lookup"><span data-stu-id="6c9b3-130">Remarks</span></span>

<span data-ttu-id="6c9b3-131">[ErrorToString](./jet-param-enumeration.md) passa il numero di errore in paramValue, motivo per cui si tratta di un parametro ref e non di un parametro out.</span><span class="sxs-lookup"><span data-stu-id="6c9b3-131">[ErrorToString](./jet-param-enumeration.md) passes in the error number in the paramValue, which is why it is a ref parameter and not an out parameter.</span></span>

## <a name="see-also"></a><span data-ttu-id="6c9b3-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6c9b3-132">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="6c9b3-133">Riferimento</span><span class="sxs-lookup"><span data-stu-id="6c9b3-133">Reference</span></span>

[<span data-ttu-id="6c9b3-134">Classe API</span><span class="sxs-lookup"><span data-stu-id="6c9b3-134">Api class</span></span>](./api-class.md)

[<span data-ttu-id="6c9b3-135">Membri API</span><span class="sxs-lookup"><span data-stu-id="6c9b3-135">Api members</span></span>](./api-members.md)

[<span data-ttu-id="6c9b3-136">Overload JetGetSystemParameter</span><span class="sxs-lookup"><span data-stu-id="6c9b3-136">JetGetSystemParameter overload</span></span>](./api.jetgetsystemparameter-method.md)

[<span data-ttu-id="6c9b3-137">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="6c9b3-137">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
