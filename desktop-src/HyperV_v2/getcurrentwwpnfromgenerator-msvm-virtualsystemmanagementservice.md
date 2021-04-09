---
description: Offre la possibilità di visualizzare in anteprima il nome della porta universale (WWPN) corrente senza il WWPN riservato.
ms.assetid: 7fc02099-744e-4a56-ae4b-1f5fd6a1eb45
title: Metodo GetCurrentWwpnFromGenerator della classe Msvm_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.GetCurrentWwpnFromGenerator
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 88e1fd8f19b4a0542744cbfff7058ed7e69a421d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966778"
---
# <a name="getcurrentwwpnfromgenerator-method-of-the-msvm_virtualsystemmanagementservice-class"></a>Metodo GetCurrentWwpnFromGenerator della classe MSVM \_ VirtualSystemManagementService

Offre la possibilità di visualizzare in anteprima il nome della porta universale (WWPN) corrente senza il WWPN riservato. WWPN viene generato dall'interno dell'intervallo preconfigurato definito dalle proprietà **MinimumWWPNAddress** e **MaximumWWPNAddress** della classe [**MSVM \_ VirtualSystemManagementServiceSettingData**](msvm-virtualsystemmanagementservicesettingdata.md) . Se l'intervallo definito da queste proprietà viene esaurito, il WWPN generato avrà la voce non valida "0000000000000000" e il valore restituito indicherà l'esito positivo (0).

## <a name="syntax"></a>Sintassi


```mof
uint32 GetCurrentWwpnFromGenerator(
  [out] string CurrentWwpn
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*CurrentWwpn* \[ out\]
</dt> <dd>

Stringa che avrà il valore dell'oggetto WWPN corrente usato dal generatore di WWPN. Si tratta dello stesso valore che sarà il primo WWPN generato dalla chiamata successiva a [**GenerateWwpn**](generatewwpn-msvm-virtualsystemmanagementservice.md). Verrà formattato in formato stringa come "01:23:45:67:89: AB: CD: EF".

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo restituisce uno dei valori seguenti.

<dl> <dt>

**Completato senza errori** (0)
</dt> <dt>

**Non riuscito** (32768)
</dt> <dt>

**Accesso negato** (32769)
</dt> <dt>

**Non supportato** (32770)
</dt> <dt>

**Stato sconosciuto** (32771)
</dt> <dt>

**Timeout** (32772)
</dt> <dt>

**Parametro non valido** (32773)
</dt> <dt>

Il **sistema è in uso** (32774)
</dt> <dt>

**Stato non valido per l'operazione** (32775)
</dt> <dt>

**Tipo di dati non corretto** (32776)
</dt> <dt>

**Sistema non disponibile** (32777)
</dt> <dt>

**Memoria insufficiente** (32778)
</dt> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 8\]<br/>                                                              |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2012\]<br/>                                                    |
| Spazio dei nomi<br/>                | \\Virtualizzazione radice \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_VirtualSystemManagementService MSVM**](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

 




