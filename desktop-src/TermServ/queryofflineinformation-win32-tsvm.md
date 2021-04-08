---
title: Metodo QueryOfflineInformation della classe Win32_TSVm
description: Recupera le proprietà del server di desktop virtuale (VDS) corrente, ma solo quando il server è offline.
ms.assetid: f6ce74cb-a4a4-4e05-a0a7-bac0b7f52c45
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo QueryOfflineInformation
- Metodo QueryOfflineInformation Servizi Desktop remoto, classe Win32_TSVm
- Classe Win32_TSVm Servizi Desktop remoto, metodo QueryOfflineInformation
topic_type:
- apiref
api_name:
- Win32_TSVm.QueryOfflineInformation
api_location:
- TSVmHostWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4750ebdb82b08ae1ed0350e1ac448d9aca4003b2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874073"
---
# <a name="queryofflineinformation-method-of-the-win32_tsvm-class"></a>Metodo QueryOfflineInformation della \_ classe TSVm Win32

Recupera le proprietà del server di desktop virtuale (VDS) corrente, ma solo quando il server è offline.

## <a name="syntax"></a>Sintassi


```mof
uint32 QueryOfflineInformation(
  [out] string  Build,
  [out] string  CurrentVersion,
  [out] string  InstallationType,
  [out] string  EditionId,
  [out] string  SysPrepImageState,
  [out] string  SysPrepMode,
  [out] sint32  ProcArch,
  [out] boolean fIsVmbusCapable,
  [out] boolean fIsRdvIcInstalled
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Compilazione* \[ di out\]
</dt> <dd>

In seguito a un esito positivo, restituisce la versione build del VDS.

</dd> <dt>

*CurrentVersion* \[ out\]
</dt> <dd>

In seguito a un esito positivo, restituisce la versione corrente del VDS.

</dd> <dt>

*INSTALLATIONTYPE* \[ out\]
</dt> <dd>

In seguito a un esito positivo, restituisce il tipo di installazione del VDS.

</dd> <dt>

*EditionID* \[ out\]
</dt> <dd>

In seguito all'esito positivo, restituisce l'ID edizione del VDS.

</dd> <dt>

*SysPrepImageState* \[ out\]
</dt> <dd>

In seguito all'esito positivo, restituisce lo stato dell'immagine di preparazione del sistema VDS.

</dd> <dt>

*SysPrepMode* \[ out\]
</dt> <dd>

In seguito a un esito positivo, restituisce la modalità di preparazione del sistema VDS.

</dd> <dt>

*ProcArch* \[ out\]
</dt> <dd>

In seguito a un esito positivo, restituisce un valore che indica l'architettura del processore.

<dt>

0
</dt> <dd>

x86

</dd> <dt>

1
</dt> <dd>

amd64

</dd> </dl> </dd> <dt>

*fIsVmbusCapable* \[ out\]
</dt> <dd>

con esito positivo, indica se il sistema è in grado di supportare VMBus.

</dd> <dt>

*fIsRdvIcInstalled* \[ out\]
</dt> <dd>

In caso di esito positivo, indica se RDVIC è installato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce 0 in caso di esito positivo, in caso contrario restituisce un codice di errore WMI. Per un elenco di questi valori, vedere [Servizi Desktop remoto codici di errore del provider WMI](terminal-services-wmi-provider-error-codes.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                                  |
| Server minimo supportato<br/> | Windows Server 2012<br/>                                                             |
| Spazio dei nomi<br/>                | Radice \\ CIMv2 \\ TerminalServices<br/>                                                   |
| MOF<br/>                      | <dl> <dt>TSVmHost. mof</dt> </dl>    |
| DLL<br/>                      | <dl> <dt>TSVmHostWmi.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_TSVm Win32**](win32-tsvm.md)
</dt> </dl>

 

 





