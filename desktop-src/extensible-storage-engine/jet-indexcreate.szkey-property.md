---
description: 'Altre informazioni su: JET_INDEXCREATE.szKey'
title: JET_INDEXCREATE.szKey
TOCTitle: 'szKey property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_INDEXCREATE.szKey
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_indexcreate.szkey(v=EXCHG.10)
ms:contentKeyID: 55103656
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_INDEXCREATE.szKey
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_INDEXCREATE.get_szKey
- Microsoft.Isam.Esent.Interop.JET_INDEXCREATE.set_szKey
- Microsoft.Isam.Esent.Interop.JET_INDEXCREATE.szKey
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 905bc6e72704121617a2fcc2b9b368bee9014f897ce157f473e3f9ced5a92c72
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119720571"
---
# <a name="jet_indexcreateszkey-property"></a>JET_INDEXCREATE.szKey

Ottiene o imposta la descrizione della chiave di indice. Si tratta di una stringa con terminazione Null doppia di token delimitati da Null. Ogni token ha il formato \[ direction-specifier \] \[ column-name \] , dove direction-specification è "+" o "-". Ad esempio, un valore szKey di "+abc \\ 0-def 0+ghi 0" indicizza le tre colonne \\ \\ "abc" (in ordine crescente), "def" (in ordine decrescente) e "ghi" (in ordine crescente).

**Spazio dei**  [nomi: Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintassi

``` vb
'Declaration
Public Property szKey As String
    Get
    Set
'Usage
Dim instance As JET_INDEXCREATE
Dim value As String

value = instance.szKey

instance.szKey = value
```

``` csharp
public string szKey { get; set; }
```

#### <a name="property-value"></a>Valore proprietà

Tipo: [System.String](/dotnet/api/system.string)  

## <a name="see-also"></a>Vedi anche

#### <a name="reference"></a>Riferimento

[JET_INDEXCREATE classe](./jet-indexcreate-class.md)

[JET_INDEXCREATE membri](./jet-indexcreate-members.md)

[Spazio dei nomi Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
