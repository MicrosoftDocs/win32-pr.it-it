---
description: Tutte le classi di visualizzazione devono avere un qualificatore di matrice di stringhe denominato ViewSources.
ms.assetid: aefa8cda-962f-4f6c-92a0-a8825d48db60
ms.tgt_platform: multiple
title: Qualificatore ViewSources
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ViewSources
api_type:
- NA
api_location: ''
ms.openlocfilehash: b2a0cadf3e1469fbdaf347b269813e76b780348d28482a00b4de290aaf4e0f28
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120120761"
---
# <a name="viewsources-qualifier"></a>Qualificatore ViewSources

Tutte le classi di visualizzazione devono avere un qualificatore di matrice di stringhe **denominato ViewSources.** Il **qualificatore ViewSources** contiene le query di origine che definiscono le istanze di origine usate nella classe di visualizzazione. Il valore del **qualificatore ViewSources** è una matrice di stringhe [*contenente WMI Query Language query WQL.*](gloss-w.md) È possibile definire classi di origine e limitare le istanze di origine utilizzate dalla classe di visualizzazione con la clausola[WHERE](where-clause.md) [WQL](querying-with-wql.md)per creare una vista filtrata.

Il [provider di](view-provider.md) visualizzazione abbina le query di origine nel qualificatore **ViewSources** agli spazi dei nomi elencati nel qualificatore [ViewSpaces](viewspaces-qualifier.md) nell'ordine in cui sono elencate le query e gli spazi dei nomi. Il numero di query di origine deve corrispondere al numero di spazi dei nomi elencati nel qualificatore ViewSpaces. L'ordine in cui vengono elencate le query di origine determina gli spazi dei nomi da cui vengono disegnate le istanze di origine.

Nell'esempio seguente vengono selezionate solo le istanze della classe **LocalDisk** in cui il valore della proprietà **FileSystem** è "NTFS" e le istanze della classe **RemoteDisk** in cui il valore della proprietà **FreeSpace** è maggiore di 45 megabyte:


```sql
ViewSources{
"SELECT __Namespace, 
   Description, 
   DeviceID, 
   FileSystem, 
   FreeSpace, 
   VolumeName FROM LocalDisk 
 WHERE FileSystem = \"NTFS\"", 
   "SELECT __Namespace, 
   Description,
   DeviceID, 
   FileSystem, 
   FreeSpace, 
   VolumeName FROM RemoteDisk 
 WHERE FreeSpace > 45000000"}
```



> [!Note]  
> Il numero di query di origine che è possibile definire per le classi di vista join dipende dal numero di istanze restituite da queste query e dal numero di modi in cui è possibile unire tali istanze. Poiché il numero di possibili combinazioni di istanze di origine per le classi di visualizzazione aumenta in modo esponenziale, mantenere le query di origine per le classi di visualizzazione join il più semplici possibile.

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>       |
| Server minimo supportato<br/> | Windows Server 2008<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Qualificatori specifici del provider di visualizzazione**](qualifiers-specific-to-the-view-provider.md)
</dt> </dl>

 

 




