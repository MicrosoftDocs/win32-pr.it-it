---
description: Classe di base astratta da cui derivano tutte le classi di dati del provider MCA (Machine Check Architecture), ad esempio MSMCAInfo \_ RawMCAData. Questa classe è disponibile solo nei sistemi Windows a 64 bit.
ms.assetid: 22ec8343-fc4f-4b14-9354-26b5d6a6fe09
title: Classe MSMCAInfo
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MSMCAInfo
api_type:
- DllExport
api_location:
- Wmiprov.dll
ms.openlocfilehash: 31fc35b1d680d900af929ea8a828bcb23d222f66
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049474"
---
# <a name="msmcainfo-class"></a>Classe MSMCAInfo

La classe **MSMCAInfo** è una classe di base astratta da cui derivano tutte le classi di dati del provider MCA (Machine Check Architecture), ad esempio [**MSMCAInfo \_ RawMCAData**](msmcainfo-rawmcadata.md). Il provider MCA dispone anche di classi di evento, derivate da [**WmiEvent**](wmievent.md). Questa classe è disponibile solo nei sistemi Windows a 64 bit.

La sintassi seguente è semplificata dal codice Managed Object Format (MOF) e include tutte le relative proprietà ereditate. Le proprietà e i metodi sono in ordine alfabetico e non in ordine MOF.

## <a name="syntax"></a>Sintassi

``` syntax
class MSMCAInfo
{
};
```

## <a name="members"></a>Members

La classe **MSMCAInfo** non definisce membri.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows XP<br/>                                                                  |
| Server minimo supportato<br/> | Windows Server 2003<br/>                                                         |
| Spazio dei nomi<br/>                | \\WMI radice<br/>                                                                   |
| MOF<br/>                      | <dl> <dt>Wmicore. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wmiprov.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Classi MSMCA](msmca-classes.md)
</dt> <dt>

[**\_Intestazione MSMCAEvent**](msmcaevent-header.md)
</dt> <dt>

[**WMIEvent**](wmievent.md)
</dt> </dl>

 

 




