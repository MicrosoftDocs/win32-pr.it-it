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
ms.openlocfilehash: be491c0bfefe77c2bf016789786212047d5ca8d00570c84057b8e8e346fb382e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118317025"
---
# <a name="postjoinfilter-qualifier"></a>Qualificatore PostJoinFilter

È possibile filtrare le istanze di una classe di visualizzazione join assegnando una query WQL al qualificatore **PostJoinFilter.** Il valore della query WQL viene applicato alle istanze della classe di visualizzazione join. È possibile usare questo qualificatore per limitare le istanze della classe di visualizzazione a quelle che soddisfano condizioni specifiche. La query WQL seguente filtra le istanze di una classe di join denominata in base alle istanze di [**\_ LogicalDisk Win32.**](/windows/desktop/CIMWin32Prov/win32-logicaldisk)


```C++
PostJoinFilter("SELECT * FROM JoinDrive" +
    " WHERE FreeSpace > 1000000" +
    " and Description = \"3 1/2 Inch Floppy Drive\"")
```



Esistono diverse restrizioni per l'uso di questo qualificatore:

-   **PostJoinFilter è** disponibile solo per unire le classi di visualizzazione.
-   Il nome della classe e i nomi delle proprietà specificati nella query fanno riferimento alle proprietà della classe di visualizzazione, non alla classe di origine.
-   Non è consentita alcuna esclusione di proprietà. Sono `SELECT *` consentite solo query di tipo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>       |
| Server minimo supportato<br/> | Windows Server 2008<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Qualificatori specifici del provider di visualizzazione**](qualifiers-specific-to-the-view-provider.md)
</dt> </dl>

 

