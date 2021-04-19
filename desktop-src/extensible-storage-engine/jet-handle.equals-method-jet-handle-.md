---
description: 'Altre informazioni su: JET_HANDLE. Metodo Equals (JET_HANDLE)'
title: JET_HANDLE. Metodo Equals (JET_HANDLE)
TOCTitle: Equals method (JET_HANDLE)
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_HANDLE.Equals(Microsoft.Isam.Esent.Interop.JET_HANDLE)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_handle.equals(v=EXCHG.10)
ms:contentKeyID: 39515292
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.JET_HANDLE.Equals
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ab4ea5df734b626e54a70bc690301e755013ae59
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318142"
---
# <a name="jet_handleequals-method-jet_handle"></a>JET_HANDLE. Metodo Equals (JET_HANDLE)

Restituisce un valore che indica se questa istanza è uguale a un'altra istanza.

**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintassi

``` vb
'Declaration
Public Function Equals ( _
    other As JET_HANDLE _
) As Boolean
'Usage
Dim instance As JET_HANDLE
Dim other As JET_HANDLE
Dim returnValue As Boolean

returnValue = instance.Equals(other)
```

``` csharp
public bool Equals(
    JET_HANDLE other
)
```

#### <a name="parameters"></a>Parametri

  - altro  
    Tipo: [Microsoft.ISAM.esent.Interop.JET_HANDLE](./jet-handle-structure.md)  
    
    Istanza di da confrontare con questa istanza.

#### <a name="return-value"></a>Valore restituito

Tipo: [System. Boolean](/dotnet/api/system.boolean)  
True se le due istanze sono uguali.  

#### <a name="implements"></a>Implementazioni

[IEquatable \<T\> . Uguale a (T)](/dotnet/api/system.iequatable-1.equals#System_IEquatable_1_Equals__0_)  

## <a name="see-also"></a>Vedi anche

#### <a name="reference"></a>Riferimento

[Struttura JET_HANDLE](./jet-handle-structure.md)

[Membri JET_HANDLE](./jet-handle-members.md)

[Confronta l'overload](./jet-handle.equals-method.md)

[Spazio dei nomi Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
