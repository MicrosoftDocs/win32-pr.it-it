---
description: Genera un set di NOMI WWPN (World Wide Port Names).
ms.assetid: 36f393eb-6f34-4ae3-a976-c5da60211f3e
title: Metodo GenerateWwpn della classe Msvm_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.GenerateWwpn
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 1952954d107185fdcc31634b9d0e19bd4cd3450db5a63d78aa3ef823cdf38afe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119532521"
---
# <a name="generatewwpn-method-of-the-msvm_virtualsystemmanagementservice-class"></a>Metodo GenerateWwpn della classe Msvm \_ VirtualSystemManagementService

Genera un set di NOMI WWPN (World Wide Port Names). I WWSPN vengono generati dall'interno dell'intervallo preconfigurato definito dalle proprietà **MinimumWWPNAddress** e **MaximumWWPNAddress** della [**classe Msvm \_ VirtualSystemManagementServiceSettingData.**](msvm-virtualsystemmanagementservicesettingdata.md) Se il numero valido di WWPN che possono essere generati è minore del numero richiesto, le voci rimanenti nella matrice *GeneratedWwpn* avranno la voce non valida "000000000000000000000" e il valore restituito indicherà l'esito positivo (0).

## <a name="syntax"></a>Sintassi


```mof
uint32 GenerateWwpn(
  [in]  uint32 NumberOfWwpns,
  [out] string GeneratedWwpn[]
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*NumberOfWwpns* \[ Pollici\]
</dt> <dd>

Numero di WWPN da generare.

</dd> <dt>

*GeneratedWwpn* \[ Cambio\]
</dt> <dd>

Matrice di stringhe, ognuna delle quali conterrà un WWPN generato. Verrà formattato in formato stringa come "01:23:45:67:89:ab:cd:ef".

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

 

 




