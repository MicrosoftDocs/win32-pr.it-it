---
description: Altre informazioni sul metodo JET_COLUMNID.CompareTo
title: metodo JET_COLUMNID.CompareTo
TOCTitle: 'CompareTo method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_COLUMNID.CompareTo(Microsoft.Isam.Esent.Interop.JET_COLUMNID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_columnid.compareto(v=EXCHG.10)
ms:contentKeyID: 39509744
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_COLUMNID.CompareTo
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_COLUMNID.CompareTo
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: bf4271ce2ea1c146c1cbc96c9533f1c7e834126e4596c4792cc82ed2b3ad3d0a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120063601"
---
# <a name="jet_columnidcompareto-method"></a>metodo JET_COLUMNID.CompareTo

Confronta questo columnid con un altro columnid e determina se questa istanza è precedente, uguale a o dopo l'altra istanza.

**Spazio dei nomi:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintassi

``` vb
'Declaration
Public Function CompareTo ( _
    other As JET_COLUMNID _
) As Integer
'Usage
Dim instance As JET_COLUMNID
Dim other As JET_COLUMNID
Dim returnValue As Integer

returnValue = instance.CompareTo(other)
```

``` csharp
public int CompareTo(
    JET_COLUMNID other
)
```

#### <a name="parameters"></a>Parametri

  - altro  
    Tipo: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)  
    
    Columnid da confrontare con l'istanza corrente.

#### <a name="return-value"></a>Valore restituito

Tipo: [System.Int32](/dotnet/api/system.int32)  
Numero con segno che indica le posizioni relative di questa istanza e il parametro value.  

#### <a name="implements"></a>Implementazioni

[IComparable \<T\> . CompareTo(T)](/dotnet/api/system.icomparable-1.compareto#System_IComparable_1_CompareTo__0_)  

## <a name="see-also"></a>Vedi anche

#### <a name="reference"></a>Riferimento

[JET_COLUMNID struttura](./jet-columnid-structure.md)

[JET_COLUMNID membri](./jet-columnid-members.md)

[Spazio dei nomi Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
