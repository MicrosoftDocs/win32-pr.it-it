---
description: È possibile filtrare le istanze di una classe di visualizzazione join assegnando una query WQL al qualificatore PostJoinFilter.
ms.assetid: 926a7262-ea6b-4a5a-8aa7-6ec0ae389031
ms.tgt_platform: multiple
title: Qualificatore PostJoinFilter
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PostJoinFilter
api_type:
- NA
api_location: ''
ms.openlocfilehash: ac86aeafefc8057a1612c5007e55e7633c655c59
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315194"
---
# <a name="postjoinfilter-qualifier"></a>Qualificatore PostJoinFilter

È possibile filtrare le istanze di una classe di visualizzazione join assegnando una query WQL al qualificatore **PostJoinFilter** . Il valore della query WQL viene applicato alle istanze della classe di visualizzazione join. È possibile usare questo qualificatore per limitare le istanze della classe di visualizzazione a quelle che soddisfano determinate condizioni. La query WQL seguente Filtra le istanze di una classe join chiamata in base alle istanze di [**Win32 \_ disco logico**](/windows/desktop/CIMWin32Prov/win32-logicaldisk).


```C++
PostJoinFilter("SELECT * FROM JoinDrive" +
    " WHERE FreeSpace > 1000000" +
    " and Description = \"3 1/2 Inch Floppy Drive\"")
```



L'uso di questo qualificatore presenta diverse limitazioni:

-   **PostJoinFilter** è disponibile solo per le classi di visualizzazione join.
-   Il nome della classe e i nomi di proprietà specificati nella query fanno riferimento alle proprietà della classe di visualizzazione, non alla classe di origine.
-   Non sono consentite esclusioni di proprietà; `SELECT *` sono consentite solo query di tipo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>       |
| Server minimo supportato<br/> | Windows Server 2008<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Qualificatori specifici del provider di visualizzazione**](qualifiers-specific-to-the-view-provider.md)
</dt> </dl>

 

