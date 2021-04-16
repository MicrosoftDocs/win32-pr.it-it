---
title: Metodo SetServerWeight della classe Win32_TSSessionDirectory
description: Imposta il valore del peso del server per il bilanciamento del carico di Connessione Desktop remoto broker (gestore connessione Desktop remoto).
ms.assetid: 9c7563e5-bb45-495d-90b0-43170b58581e
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo SetServerWeight
- Metodo SetServerWeight Servizi Desktop remoto, classe Win32_TSSessionDirectory
- Classe Win32_TSSessionDirectory Servizi Desktop remoto, metodo SetServerWeight
topic_type:
- apiref
api_name:
- Win32_TSSessionDirectory.SetServerWeight
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 46e8456fa590de0c9d6236f96f3b09c16087d730
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477716"
---
# <a name="setserverweight-method-of-the-win32_tssessiondirectory-class"></a>Metodo SetServerWeight della \_ classe TSSessionDirectory Win32

Imposta il valore del peso del server per il bilanciamento del carico di Connessione Desktop remoto broker (gestore connessione Desktop remoto).

## <a name="syntax"></a>Sintassi


```mof
uint32 SetServerWeight(
  [in] uint32 ServerWeightValue
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ServerWeightValue* \[ in\]
</dt> <dd>

Tipo: **UInt32**

Valore del peso del server. L'intervallo valido è compreso tra 1 e 10000.

</dd> </dl>

## <a name="remarks"></a>Commenti

Per impostazione predefinita, nell'interfaccia utente di Servizi Desktop remoto configurazione, il valore del peso del server è 100. Il peso del server è relativo. Se pertanto si assegna un server a un valore 100 e un valore pari a 200, il server con un peso relativo di 200 riceverà il doppio del numero di sessioni.

I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI). I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK). Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager. Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                               |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Spazio dei nomi<br/>                | Radice \\ CIMv2 \\ TerminalServices<br/>                                                |
| MOF<br/>                      | <dl> <dt>TSCfgWmi. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_TSSessionDirectory Win32**](win32-tssessiondirectory.md)
</dt> </dl>

 

