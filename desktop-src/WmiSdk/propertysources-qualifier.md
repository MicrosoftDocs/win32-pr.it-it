---
description: Ogni proprietà in una classe di visualizzazione deve avere un qualificatore di matrice di stringhe denominato PropertySources.
ms.assetid: df89680b-8ea7-4f38-81ba-c4132b944f37
ms.tgt_platform: multiple
title: Qualificatore PropertySources
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PropertySources
api_type:
- NA
api_location: ''
ms.openlocfilehash: 3809977282a2bdf82d0b51ef8f566541b74fe28a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308840"
---
# <a name="propertysources-qualifier"></a>Qualificatore PropertySources

Ogni proprietà in una classe di visualizzazione deve avere un qualificatore di matrice di stringhe denominato **PropertySources**. Il qualificatore **PropertySources** contiene il nome della proprietà o delle proprietà della classe di origine da cui questa proprietà della classe di visualizzazione Ottiene i dati. L'ordine dei valori in questa matrice corrisponde all'ordine delle classi di origine definite per il [qualificatore ViewSources](viewsources-qualifier.md). Nell'esempio seguente viene illustrato come definire una proprietà per una classe di visualizzazione Unione che rappresenta l'Unione della classe [**Win32 \_ disco logico**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) da due computer diversi:


```mof
[PropertySources{"DeviceID", "DeviceID"},key] String Devname;
```



La prima proprietà **DeviceID** corrisponde alla proprietà **DeviceID** della classe nella prima query di origine. La seconda proprietà **DeviceID** è la proprietà **DeviceID** della classe nella seconda query di origine.

Quando si definiscono le proprietà per le classi di visualizzazione join, è necessario definire una proprietà di visualizzazione separata per ognuna delle proprietà della classe di origine, a meno che le proprietà della classe di origine non siano le basi della classe di visualizzazione join. Nell'esempio seguente vengono create proprietà in una classe di visualizzazione join su proprietà simili dalla classe di origine della [**\_ stampante Win32**](/windows/desktop/CIMWin32Prov/win32-printer) e dalla classe di origine [**Win32 \_ PrinterConfiguration**](/windows/desktop/CIMWin32Prov/win32-printerconfiguration) :


```mof
[PropertySources{"VerticalResolution", ""}] Uint32 Vres;
[PropertySources{"", "YResolution"}] Uint32 Yres;
```



Se le due classi di origine vengono unite in join da una proprietà comune, è possibile definire solo una singola proprietà della classe di visualizzazione, perché il valore di entrambe le proprietà della classe di origine è sempre lo stesso. Nell'esempio seguente viene illustrato come unire in join la classe [**\_ Printer Win32**](/windows/desktop/CIMWin32Prov/win32-printer) e la [**\_ PrinterConfiguration Win32**](/windows/desktop/CIMWin32Prov/win32-printerconfiguration) mediante un valore di proprietà comune:


```mof
[PropertySources{"DeviceId", "DeviceName "}] String Name;
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>       |
| Server minimo supportato<br/> | Windows Server 2008<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Qualificatori specifici del provider di visualizzazione**](qualifiers-specific-to-the-view-provider.md)
</dt> </dl>

 

