---
description: Consente di visualizzare in anteprima il nome wwpn (World Wide Port Name) corrente senza che il WWPN sia riservato.
ms.assetid: 7fc02099-744e-4a56-ae4b-1f5fd6a1eb45
title: Metodo GetCurrentWwpnFromGenerator della Msvm_VirtualSystemManagementService
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
ms.openlocfilehash: 196ad781075128eab42c6daabf7d6ccd6906df1e67e348ebea0d9418cbb08c24
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118393283"
---
# <a name="getcurrentwwpnfromgenerator-method-of-the-msvm_virtualsystemmanagementservice-class"></a>Metodo GetCurrentWwpnFromGenerator della classe Msvm \_ VirtualSystemManagementService

Consente di visualizzare in anteprima il nome wwpn (World Wide Port Name) corrente senza che il WWPN sia riservato. Il WWPN viene generato dall'interno dell'intervallo preconfigurato definito dalle proprietà **MinimumWWPNAddress** e **MaximumWWPNAddress** della [**classe Msvm \_ VirtualSystemManagementServiceSettingData.**](msvm-virtualsystemmanagementservicesettingdata.md) Se l'intervallo definito da queste proprietà è esaurito, il WWPN generato avrà la voce non valida "000000000000000" e il valore restituito indicherà l'esito positivo (0).

## <a name="syntax"></a>Sintassi


```mof
uint32 GetCurrentWwpnFromGenerator(
  [out] string CurrentWwpn
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*CurrentWwpn* \[ Cambio\]
</dt> <dd>

Stringa che avrà il valore del WWPN corrente usato dal generatore WWPN. Questo sarà lo stesso valore che sarà il primo WWPN generato dalla chiamata successiva a [**GenerateWwpn**](generatewwpn-msvm-virtualsystemmanagementservice.md). Verrà formattato in formato stringa come "01:23:45:67:89:ab:cd:ef".

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo restituisce uno dei valori seguenti.

<dl> <dt>

**Completato senza errori** (0)
</dt> <dt>

**Operazione non** riuscita (32768)
</dt> <dt>

**Accesso negato** (32769)
</dt> <dt>

**Non supportato** (32770)
</dt> <dt>

**Lo stato è sconosciuto** (32771)
</dt> <dt>

**Timeout** (32772)
</dt> <dt>

**Parametro non** valido (32773)
</dt> <dt>

**Sistema in uso** (32774)
</dt> <dt>

**Stato non valido per questa operazione** (32775)
</dt> <dt>

**Tipo di dati non** corretto (32776)
</dt> <dt>

**Il sistema non è disponibile** (32777)
</dt> <dt>

**Memoria insufficiente** (32778)
</dt> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8 solo app desktop\]<br/>                                                              |
| Server minimo supportato<br/> | \[Windows Server 2012 solo app desktop\]<br/>                                                    |
| Spazio dei nomi<br/>                | Virtualizzazione \\ radice \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Msvm \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

 




