---
description: 'Altre informazioni su: JET_LOGTIME. Metodo ToDateTime'
title: JET_LOGTIME. Metodo ToDateTime
TOCTitle: 'ToDateTime method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_LOGTIME.ToDateTime
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_logtime.todatetime(v=EXCHG.10)
ms:contentKeyID: 39512964
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_LOGTIME.ToDateTime
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_LOGTIME.ToDateTime
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: add66724ff34b3871462eef129dc6efd549159b39243a19565d4ca40d2f05b04
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118979851"
---
# <a name="jet_logtimetodatetime-method"></a>JET_LOGTIME. Metodo ToDateTime

Generare una rappresentazione DateTime di questo JET_LOGTIME.

**Spazio dei nomi:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintassi

``` vb
'Declaration
Public Function ToDateTime As Nullable(Of DateTime)
'Usage
Dim instance As JET_LOGTIME
Dim returnValue As Nullable(Of DateTime)

returnValue = instance.ToDateTime()
```

``` csharp
public Nullable<DateTime> ToDateTime()
```

#### <a name="return-value"></a>Valore restituito

Tipo: [System.Nullable](/dotnet/api/system.nullable-1)\<[DateTime](/dotnet/api/system.datetime)\>  
Oggetto DateTime che rappresenta l'JET_LOGTIME. Se il JET_LOGTIME è null, viene restituito null.  

#### <a name="implements"></a>Implementazioni

[IJET_LOGTIME. ToDateTime()](./ijet-logtime.todatetime-method.md)  

## <a name="see-also"></a>Vedi anche

#### <a name="reference"></a>Riferimento

[JET_LOGTIME struttura](./jet-logtime-structure2.md)

[JET_LOGTIME membri](./jet-logtime-members.md)

[Spazio dei nomi Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
