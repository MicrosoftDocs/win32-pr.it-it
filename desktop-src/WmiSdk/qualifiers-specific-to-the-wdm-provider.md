---
description: I qualificatori seguenti vengono usati dal provider WDM nei file MOF dei driver di dispositivo quando estraggono dati da WNODEs per generare istanze delle classi di driver WDM.
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
ms.openlocfilehash: be2bc4593c19555dd5a851de89a1dc2e5db00596
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308835"
---
# <a name="qualifiers-specific-to-the-wdm-provider"></a>Qualificatori specifici del provider WDM

I qualificatori seguenti vengono usati dal [provider WDM](/windows/desktop/WmiCoreProv/wdm-provider) nei file MOF dei driver di dispositivo quando estraggono dati da WNODEs per generare istanze delle classi di driver WDM.

<dt>

<span id="MissingValue"></span><span id="missingvalue"></span><span id="MISSINGVALUE"></span>**MissingValue**
</dt> <dd>

Tipo di dati: **DWORD, array, Uint8, UInt16, UInt32, sint8, sint16 o sint32.**

Si applica a: Proprietà

Un valore mancante per questa proprietà deve essere rappresentato da **null** anziché da 0 (zero).

</dd> <dt>

<span id="WMIDataId"></span><span id="wmidataid"></span><span id="WMIDATAID"></span>**WMIDataId**
</dt> <dd>

Tipo di dati: **UInt32**

Si applica a: Proprietà

Indice nel WNODE dei dati per la proprietà. Il provider WDM utilizza questo qualificatore per determinare il modo in cui i dati vengono formattati durante l'estrazione dei dati da WNODE e la generazione di classi WMI. Il valore iniziale è 1.

</dd> <dt>

<span id="WMIExpense"></span><span id="wmiexpense"></span><span id="WMIEXPENSE"></span>**WMIExpense**
</dt> <dd>

Tipo di dati: **UInt32**

Si applica a: classi

Indica il costo della risorsa per accedere al blocco di dati. Ad esempio, le informazioni di geometria del disco non richiedono numerose risorse da ottenere perché sono disponibili nell'estensione del dispositivo. Le prestazioni di lettura/scrittura su disco sono molto più complesse perché richiedono un lavoro aggiuntivo per ogni operazione di lettura/scrittura. Pertanto, il valore del qualificatore **WMIExpense** è maggiore per le prestazioni di lettura/scrittura del disco.

</dd> <dt>

<span id="WMIMethodId"></span><span id="wmimethodid"></span><span id="WMIMETHODID"></span>**WMIMethodId**
</dt> <dd>

Tipo di dati: **UInt32**

Si applica a: metodi

Indice nel WNODE dei dati per la proprietà. Il provider WDM utilizza questo qualificatore per determinare il modo in cui i dati vengono formattati durante l'estrazione dei dati da WNODE e la generazione di classi WMI. Il valore iniziale è 1.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>       |
| Server minimo supportato<br/> | Windows Server 2008<br/> |



 

