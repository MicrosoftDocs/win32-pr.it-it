---
description: 'Altre informazioni su: <T> interfaccia IContentEquatable'
title: Interfaccia IContentEquatable (T)
TOCTitle: IContentEquatable(T) interface
ms:assetid: T:Microsoft.Isam.Esent.Interop.IContentEquatable`1
ms:mtpsurl: https://msdn.microsoft.com/library/Hh578046(v=EXCHG.10)
ms:contentKeyID: 39511318
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.IContentEquatable`1
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.IContentEquatable`1
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 02e237714f020f5bafa3ce8b7465f1c8e2615c01
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309158"
---
# <a name="icontentequatablet-interface"></a>\<T\>Interfaccia IContentEquatable

Interfaccia per gli oggetti il cui contenuto può essere confrontato tra loro. Questa operazione deve essere utilizzata per i confronti di uguaglianza sugli oggetti di riferimento modificabili in cui l'override di Equals () e GetHashCode () non è un'idea efficace.

**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintassi

``` vb
'Declaration
Public Interface IContentEquatable(Of T)
'Usage
Dim instance As IContentEquatable(Of T)
```

``` csharp
public interface IContentEquatable<T>
```

#### <a name="type-parameters"></a>Parametri di tipo

  - T  
    Tipo di oggetti da comapre.

## <a name="see-also"></a>Vedi anche

#### <a name="reference"></a>Riferimento

[Membri di IContentEquatable \<T\>](./icontentequatable-t-members.md)

[Spazio dei nomi Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
