---
description: 'Metodo GetErrorEx della classe Msvm_CollectionReferencePointExportJob : recupera informazioni aggiuntive su un errore.'
ms.assetid: 64a90f18-3ae7-4021-857f-64adf8c40430
title: Metodo GetErrorEx della classe Msvm_CollectionReferencePointExportJob
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectionReferencePointExportJob.GetErrorEx
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 56eec72d70acbaa55374b54ba0e1eda161ba0b6e608069cc86a07518d8b735da
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119681961"
---
# <a name="geterrorex-method-of-the-msvm_collectionreferencepointexportjob-class"></a>Metodo GetErrorEx della classe Msvm \_ CollectionReferencePointExportJob

Recupera informazioni aggiuntive su un errore. Quando il processo è in esecuzione o è terminato senza errori, **GetErrorEx** non restituisce alcuna [**istanza di Msvm \_ Error.**](msvm-error.md) Tuttavia, se il processo non è riuscito a causa di un problema interno o perché il processo è stato terminato da un client, **GetErrorEx** restituisce una o più **istanze di Msvm \_ Error.**

## <a name="syntax"></a>Sintassi


```mof
uint32 GetErrorEx(
  [out] string Errors[]
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Errori* \[ Cambio\]
</dt> <dd>

Se lo stato operativo del processo non è "OK", questo parametro restituisce una matrice di [**istanze di Msvm \_ Error.**](msvm-error.md) In caso contrario, se il processo è "OK", questo parametro contiene **NULL.**

</dd> </dl>

## <a name="return-value"></a>Valore restituito

In caso di esito positivo, restituisce 0; In caso contrario, restituisce uno dei valori di errore seguenti:

<dl> <dt>

**Completata senza errori** (0)
</dt> <dt>

**Non riuscito** (32768)
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
| Client minimo supportato<br/> | Windows 10, solo app desktop versione 1703 \[\]<br/>                                               |
| Server minimo supportato<br/> | Windows Server 2016<br/>                                                                          |
| Spazio dei nomi<br/>                | Virtualizzazione \\ radice \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Msvm \_ CollectionReferencePointExportJob**](msvm-collectionreferencepointexportjob.md)
</dt> </dl>

 

 




