---
description: 'Altre informazioni su: Proprietà JET_INDEXCREATE. szKey'
title: Proprietà JET_INDEXCREATE. szKey
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
ms.openlocfilehash: 86ade65ee28eef6314d31653772b0c22657476d1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104348801"
---
# <a name="jet_indexcreateszkey-property"></a>Proprietà JET_INDEXCREATE. szKey

Ottiene o imposta la descrizione della chiave di indice. Si tratta di una stringa doppia con terminazione null di token delimitati da null. Ogni token è del form \[ Direction-specifier \] \[ Column-Name \] , dove Direction-Specification è "+" o "-". ad esempio, un szKey di "+ ABC \\ 0-def \\ 0 + ghi \\ 0" effettuerà l'indice sulle tre colonne "ABC" (in ordine crescente), "def" (in ordine decrescente) e "ghi" (in ordine crescente).

**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)

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

Tipo: [System. String](/dotnet/api/system.string)  

## <a name="see-also"></a>Vedi anche

#### <a name="reference"></a>Riferimento

[Classe JET_INDEXCREATE](./jet-indexcreate-class.md)

[Membri JET_INDEXCREATE](./jet-indexcreate-members.md)

[Spazio dei nomi Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
