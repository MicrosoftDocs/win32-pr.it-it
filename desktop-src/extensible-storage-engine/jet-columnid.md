---
description: 'Altre informazioni su: JET_COLUMNID'
title: JET_COLUMNID
TOCTitle: JET_COLUMNID
ms:assetid: d6c74c5c-ba61-4e1c-a1b1-495e925b6b68
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294104(v=EXCHG.10)
ms:contentKeyID: 32765719
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: fbdc03342187cfc2adfa1dcd3ed650f532e1dbc0
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/26/2021
ms.locfileid: "122982944"
---
# <a name="jet_columnid"></a>JET_COLUMNID


_**Si applica a:** Windows | Windows Server_

## <a name="jet_columnid"></a>JET_COLUMNID

Il **JET_COLUMNID** di dati identifica una colonna all'interno di una tabella.

```cpp
    typedef unsigned long JET_COLUMNID;
```

### <a name="data-types"></a>Tipi di dati

JET_COLUMNID

Identifica una colonna all'interno di una tabella.

### <a name="remarks"></a>Commenti

Gli ID colonna sono univoci all'interno di una singola tabella. Una volta che una colonna ha un determinato ID di colonna, avrà sempre tale ID colonna. Il ripristino da backup non modificherà il valore di un ID colonna. Tuttavia, se una o più colonne della tabella, prima di una colonna di tabella specifica, vengono eliminate, un database compatto può quindi modificare il valore di un ID colonna.

In alcuni casi, gli ID colonna sono l'unico mezzo per identificare le colonne. Quando viene creata una tabella temporanea, le colonne non hanno nomi, ma la funzione create restituisce una matrice di ID di colonna.

Le colonne in tabelle diverse possono avere lo stesso ID colonna.

### <a name="requirements"></a>Requisiti


| Requisito | Valore |
|------------|----------|
| <p><strong>Client</strong></p> | <p>Richiede Windows Vista, Windows XP o Windows 2000 Professional.</p> | 
| <p><strong>Server</strong></p> | <p>Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p> | 
| <p><strong>Intestazione</strong></p> | <p>Dichiarato in Esent.h.</p> | 


