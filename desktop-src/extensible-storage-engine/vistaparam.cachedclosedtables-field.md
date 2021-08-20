---
description: Altre informazioni sul campo VistaParam.CachedClosedTables
title: Campo VistaParam.CachedClosedTables (Microsoft.Isam.Esent.Interop.Vista)
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
ms.openlocfilehash: 444456bc49b1cf2358feb32cadb36bec85cef5585436639dcf38caa02308af34
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119038659"
---
# <a name="vistaparamcachedclosedtables-field"></a>Campo VistaParam.CachedClosedTables

Questo parametro controlla il numero di risorse albero B+ memorizzate nella cache dall'istanza dopo che le tabelle che rappresentano sono state chiuse dall'applicazione. I valori di grandi dimensioni per questo parametro determinano l'uso di una maggiore quantità di memoria da parte del motore di database, ma aumentano la velocità con cui un numero elevato di tabelle può essere aperto in modo casuale dall'applicazione. Ciò è utile per le applicazioni che dispongono di uno schema con un numero molto elevato di tabelle.

**Spazio dei nomi:**  [Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

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

[Spazio dei nomi Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)
