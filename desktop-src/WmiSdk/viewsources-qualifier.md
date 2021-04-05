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
ms.openlocfilehash: 1f39146f8065401052c352472b28c4946cca6b98
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103757760"
---
# <a name="viewsources-qualifier"></a>Qualificatore ViewSources

Tutte le classi di visualizzazione devono avere un qualificatore di matrice di stringhe denominato **ViewSources**. Il qualificatore **ViewSources** contiene le query di origine che definiscono le istanze di origine utilizzate nella classe di visualizzazione. Il valore del qualificatore **ViewSources** è una matrice di stringhe contenente le query [*WQL (WMI Query Language)*](gloss-w.md) . È possibile definire le classi di origine e limitare le istanze di origine utilizzate dalla classe di visualizzazione con la[clausola WHERE](where-clause.md) di [query con WQL](querying-with-wql.md)per creare una visualizzazione filtrata.

Il [provider di viste](view-provider.md) corrisponde alle query di origine nel qualificatore **ViewSources** per gli spazi dei nomi elencati nel [qualificatore ViewSpaces](viewspaces-qualifier.md) nell'ordine in cui sono elencate le query e gli spazi dei nomi. Il numero di query di origine deve corrispondere al numero di spazi dei nomi elencati nel qualificatore ViewSpaces. L'ordine in cui vengono elencate le query di origine determina gli spazi dei nomi da cui vengono disegnate le istanze di origine.

Nell'esempio seguente vengono selezionate solo le istanze della classe **LocalDisk** in cui il valore della proprietà **filesystem** è "NTFS" e le istanze della classe **RemoteDisk** in cui il valore della proprietà **FreeSpace** è maggiore di 45 megabyte:


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
> Il numero di query di origine che è possibile definire per le classi di visualizzazione join dipende dal numero di istanze restituite da queste query e dal numero di modi in cui tali istanze possono essere unite in join. Il numero di possibili combinazioni di istanze di origine per le classi di visualizzazione cresce in modo esponenziale, quindi è possibile usare le query di origine per le classi di visualizzazione join il più semplice possibile.

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>       |
| Server minimo supportato<br/> | Windows Server 2008<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Qualificatori specifici del provider di visualizzazione**](qualifiers-specific-to-the-view-provider.md)
</dt> </dl>

 

 




