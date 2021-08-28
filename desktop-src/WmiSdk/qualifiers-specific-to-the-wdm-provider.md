---
description: I qualificatori seguenti vengono usati dal provider WDM nei file MOF dei driver di dispositivo quando estraggono dati da WNODE per generare istanze di classi di driver WDM.
ms.assetid: 11b0af59-979f-4908-baef-c9ec564b3cfd
ms.tgt_platform: multiple
title: Qualificatori specifici del provider WDM
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Qualifiers
api_type:
- NA
api_location: ''
ms.openlocfilehash: 673b53d8cea23cd044175129af85c367f6f20c8dc92240c8bdf52f34708d96f0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119996081"
---
# <a name="qualifiers-specific-to-the-wdm-provider"></a>Qualificatori specifici del provider WDM

I qualificatori seguenti vengono usati dal provider [WDM](/windows/desktop/WmiCoreProv/wdm-provider) nei file MOF dei driver di dispositivo quando estraggono dati da WNODE per generare istanze di classi di driver WDM.

<dt>

<span id="MissingValue"></span><span id="missingvalue"></span><span id="MISSINGVALUE"></span>**MissingValue**
</dt> <dd>

Tipo di dati: **DWORD, array, uint8, uint16, uint32, sint8, sint16 o sint32.**

Si applica a: proprietà

Un valore mancante per questa proprietà deve essere rappresentato da **NULL** anziché da 0 (zero).

</dd> <dt>

<span id="WMIDataId"></span><span id="wmidataid"></span><span id="WMIDATAID"></span>**WMIDataId**
</dt> <dd>

Tipo di dati: **uint32**

Si applica a: proprietà

Indice nel nodo WNODE dei dati per la proprietà . Il provider WDM usa questo qualificatore per determinare come vengono formattati i dati durante l'estrazione dei dati da WNODE e la generazione di classi WMI. Il valore iniziale è 1.

</dd> <dt>

<span id="WMIExpense"></span><span id="wmiexpense"></span><span id="WMIEXPENSE"></span>**WMIExpense**
</dt> <dd>

Tipo di dati: **uint32**

Si applica a: classi

Indicazione del costo della risorsa per accedere al blocco di dati. Ad esempio, le informazioni sulla geometria del disco non richiedono molte risorse perché sono disponibili nell'estensione del dispositivo. Le prestazioni di lettura/scrittura su disco richiedono un uso più intensivo delle risorse perché richiedono lavoro aggiuntivo per ogni operazione di lettura/scrittura. Pertanto, il **valore del qualificatore WMIExpense** è maggiore per le prestazioni di lettura/scrittura su disco.

</dd> <dt>

<span id="WMIMethodId"></span><span id="wmimethodid"></span><span id="WMIMETHODID"></span>**WMIMethodId**
</dt> <dd>

Tipo di dati: **uint32**

Si applica a: metodi

Indice nel nodo WNODE dei dati per la proprietà . Il provider WDM usa questo qualificatore per determinare come vengono formattati i dati durante l'estrazione dei dati da WNODE e la generazione di classi WMI. Il valore iniziale è 1.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>       |
| Server minimo supportato<br/> | Windows Server 2008<br/> |



 

