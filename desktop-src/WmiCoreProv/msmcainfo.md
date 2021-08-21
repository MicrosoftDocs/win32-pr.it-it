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
ms.openlocfilehash: cef9878ea8e9dd6c11c6b18a62d332e17f24810548360e0edb9c117e02a710c4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119051189"
---
# <a name="msmcainfo-class"></a>Classe MSMCAInfo

La **classe MSMCAInfo** è una classe di base astratta da cui derivano tutte le classi di dati del provider MCA (Machine Check Architecture), ad esempio [**MSMCAInfo \_ RawMCAData.**](msmcainfo-rawmcadata.md) Il provider MCA include anche classi di evento, derivate da [**WMIEvent**](wmievent.md). Questa classe è disponibile solo nei sistemi Windows a 64 bit.

La sintassi seguente è semplificata dal Managed Object Format (MOF) e include tutte le proprietà ereditate. Le proprietà e i metodi sono in ordine alfabetico, non in ordine MOF.

## <a name="syntax"></a>Sintassi

``` syntax
class MSMCAInfo
{
};
```

## <a name="members"></a>Members

La **classe MSMCAInfo** non definisce membri.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows XP<br/>                                                                  |
| Server minimo supportato<br/> | Windows Server 2003<br/>                                                         |
| Spazio dei nomi<br/>                | Wmi \\ radice<br/>                                                                   |
| MOF<br/>                      | <dl> <dt>Wmicore.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wmiprov.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Classi MSMCA](msmca-classes.md)
</dt> <dt>

[**Intestazione \_ MSMCAEvent**](msmcaevent-header.md)
</dt> <dt>

[**WMIEvent**](wmievent.md)
</dt> </dl>

 

 




