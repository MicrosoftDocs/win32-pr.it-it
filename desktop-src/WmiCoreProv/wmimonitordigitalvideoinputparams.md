---
description: Rappresenta i parametri di input per il video digitale.
ms.assetid: aa459612-db79-477b-891f-28c9d0b1b497
title: Classe WmiMonitorDigitalVideoInputParams
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WmiMonitorDigitalVideoInputParams
- WmiMonitorDigitalVideoInputParams.Active
- WmiMonitorDigitalVideoInputParams.InstanceName
- WmiMonitorDigitalVideoInputParams.IsDFP1xCompatible
api_type:
- DllExport
api_location:
- WmiProv.dll
ms.openlocfilehash: fa86add32d77a5b2838fc78eaf097c11b8a15db3f0fde9186f93046691ebc3f2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117926567"
---
# <a name="wmimonitordigitalvideoinputparams-class"></a>Classe WmiMonitorDigitalVideoInputParams

**WmiMonitorDigitalVideoInputParams rappresenta** i parametri di input per il video digitale. I dati in questa classe corrispondono ai dati dello standard VIDEO Input Definition of Video Electronics Standard Association (VESA) Enhanced Extended Display Identification Data (E-EDID). Un'istanza di questa classe è disponibile solo quando il valore della proprietà **VideoInputType** della classe [**WmiMonitorBasicDisplayParams**](wmimonitorbasicdisplayparams.md) è "Digital".

## <a name="syntax"></a>Sintassi

``` syntax
class WmiMonitorDigitalVideoInputParams : MSMonitorClass
{
  boolean Active;
  string  InstanceName;
  boolean IsDFP1xCompatible;
};
```

## <a name="members"></a>Members

La **classe WmiMonitorDigitalVideoInputParams** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe WmiMonitorDigitalVideoInputParams** ha queste proprietà.

<dl> <dt>

**Attivo**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica il monitoraggio attivo.

</dd> <dt>

**InstanceName**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **chiave**
</dt> </dl>

Nome dell'istanza del monitoraggio specifica.

</dd> <dt>

**IsDFP1xCompatible**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

VESA DFP 1.x o compatibile. Se impostata, l'interfaccia è compatibile con il segnale con CRGB (Transition Minimized Differential Signaling) 1.x Transition Minimized Differential Signaling (TMDS) CRGB, 1 pixel/clock, fino a 8 bit/colore con bit più significativo (MSB) allineato, DE active high.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                               |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                         |
| Spazio dei nomi<br/>                | Wmi \\ radice<br/>                                                                   |
| MOF<br/>                      | <dl> <dt>WmiCore.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>WmiProv.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**MSMonitorClass**](msmonitorclass.md)
</dt> </dl>

 

 




