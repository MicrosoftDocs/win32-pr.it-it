---
description: 'Altre informazioni su: JET_LOGTIME. ToDateTime (metodo)'
title: JET_LOGTIME. ToDateTime (metodo)
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
ms.openlocfilehash: 14d427d1c7e4a6f37c27677ed9617d92eb8ff644
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103760544"
---
# <a name="jet_logtimetodatetime-method"></a>JET_LOGTIME. ToDateTime (metodo)

Genera una rappresentazione DateTime di questo JET_LOGTIME.

**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)

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

Tipo: [System. Nullable](/dotnet/api/system.nullable-1)\<[DateTime](/dotnet/api/system.datetime)\>  
Valore DateTime che rappresenta il JET_LOGTIME. Se il JET_LOGTIME è null, viene restituito null.  

#### <a name="implements"></a>Implementazioni

[IJET_LOGTIME. ToDateTime ()](./ijet-logtime.todatetime-method.md)  

## <a name="see-also"></a>Vedi anche

#### <a name="reference"></a>Riferimento

[Struttura JET_LOGTIME](./jet-logtime-structure2.md)

[Membri JET_LOGTIME](./jet-logtime-members.md)

[Spazio dei nomi Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
