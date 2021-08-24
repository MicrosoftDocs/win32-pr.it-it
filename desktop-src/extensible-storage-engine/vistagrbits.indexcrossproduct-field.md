---
description: 'Altre informazioni su: Campo VistaGrbits.IndexCrossProduct'
title: Campo VistaGrbits.IndexCrossProduct (Microsoft.Isam.Esent.Interop.Vista)
TOCTitle: IndexCrossProduct field
ms:assetid: F:Microsoft.Isam.Esent.Interop.Vista.VistaGrbits.IndexCrossProduct
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.vistagrbits.indexcrossproduct(v=EXCHG.10)
ms:contentKeyID: 55104426
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.VistaGrbits.IndexCrossProduct
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.VistaGrbits.IndexCrossProduct
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ad3828411177d1c500c1b21b62797f093143ba1ac5b9770d9d6444d5c1a7aa9f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119471131"
---
# <a name="vistagrbitsindexcrossproduct-field"></a>Campo VistaGrbits.IndexCrossProduct

Se si specifica questo flag per un indice con più di una colonna chiave che è una colonna multivalore, verrà creata una voce di indice per ogni risultato di un prodotto incrociato di tutti i valori in tali colonne chiave. In caso contrario, l'indice avrebbe una sola voce per ogni multivalore nella colonna chiave più significativa che è una colonna multivalore e ognuna di queste voci di indice userebbe il primo multivalore di qualsiasi altra colonna chiave che sono colonne multivalore. Ad esempio, se è stato specificato questo flag per un indice sulla colonna A con i valori "red" e "blue" e sulla colonna B con i valori "1" e "2", verranno create le voci di indice seguenti: "red", "1"; "red", "2"; "blue", "1"; "blue", "2". In caso contrario, verranno create le voci di indice seguenti: "red", "1"; "blue", "1".

**Spazio dei nomi:**  [Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintassi

``` vb
'Declaration
Public Const IndexCrossProduct As CreateIndexGrbit
'Usage
Dim value As CreateIndexGrbit

value = VistaGrbits.IndexCrossProduct
```

``` csharp
public const CreateIndexGrbit IndexCrossProduct
```

## <a name="see-also"></a>Vedere anche

#### <a name="reference"></a>Riferimento

[Classe VistaGrbits](./vistagrbits-class.md)

[Membri di VistaGrbits](./vistagrbits-members.md)

[Spazio dei nomi Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)
