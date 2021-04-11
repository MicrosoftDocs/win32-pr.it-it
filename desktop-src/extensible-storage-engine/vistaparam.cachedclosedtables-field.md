---
description: 'Altre informazioni su: campo VistaParam. CachedClosedTables'
title: Campo VistaParam. CachedClosedTables (Microsoft. ISAM. esent. Interop. vista)
TOCTitle: CachedClosedTables field
ms:assetid: F:Microsoft.Isam.Esent.Interop.Vista.VistaParam.CachedClosedTables
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.vistaparam.cachedclosedtables(v=EXCHG.10)
ms:contentKeyID: 55104337
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.VistaParam.CachedClosedTables
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.VistaParam.CachedClosedTables
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ff72925e34c731e57d11170753ecff13f4b96a39
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128150"
---
# <a name="vistaparamcachedclosedtables-field"></a>Campo VistaParam. CachedClosedTables

Questo parametro controlla il numero di risorse dell'albero B + memorizzato nella cache dall'istanza dopo che le tabelle che rappresentano sono state chiuse dall'applicazione. I valori di grandi dimensioni per questo parametro comportano l'utilizzo di una maggiore quantità di memoria da parte del motore di database, ma aumentano la velocità con cui l'applicazione può aprire in modo casuale un numero elevato di tabelle. Questa operazione è utile per le applicazioni che dispongono di uno schema con un numero molto elevato di tabelle.

**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop. vista](./microsoft.isam.esent.interop.vista-namespace.md)  
**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintassi

``` vb
'Declaration
Public Const CachedClosedTables As JET_param
'Usage
Dim value As JET_param

value = VistaParam.CachedClosedTables
```

``` csharp
public const JET_param CachedClosedTables
```

## <a name="see-also"></a>Vedere anche

#### <a name="reference"></a>Riferimento

[Classe VistaParam](./vistaparam-class.md)

[Membri di VistaParam](./vistaparam-members.md)

[Spazio dei nomi Microsoft. ISAM. esent. Interop. vista](./microsoft.isam.esent.interop.vista-namespace.md)
