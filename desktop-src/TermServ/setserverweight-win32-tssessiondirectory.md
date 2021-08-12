---
title: Metodo SetServerWeight della classe Win32_TSSessionDirectory
description: Imposta il valore del peso del server per il bilanciamento del carico Connessione Desktop remoto Broker di connessione Desktop remoto.
ms.assetid: 9c7563e5-bb45-495d-90b0-43170b58581e
ms.tgt_platform: multiple
keywords:
- Metodo SetServerWeight Servizi Desktop remoto
- Metodo SetServerWeight Servizi Desktop remoto , Win32_TSSessionDirectory classe
- Win32_TSSessionDirectory classe Servizi Desktop remoto metodo SetServerWeight
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
ms.openlocfilehash: 96d8c9af7995f2d42f02075fde8ae43f4b5f5e9a5ccb7d3fa6f4635cb9645464
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118604630"
---
# <a name="setserverweight-method-of-the-win32_tssessiondirectory-class"></a>Metodo SetServerWeight della classe \_ TSSessionDirectory Win32

Imposta il valore del peso del server per il bilanciamento del carico Connessione Desktop remoto Broker di connessione Desktop remoto.

## <a name="syntax"></a>Sintassi


```mof
uint32 SetServerWeight(
  [in] uint32 ServerWeightValue
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ServerWeightValue* \[ Pollici\]
</dt> <dd>

Tipo: **uint32**

Valore del peso del server. L'intervallo valido è compreso tra 1 e 10000.

</dd> </dl>

## <a name="remarks"></a>Commenti

Per impostazione predefinita nell'interfaccia utente di Servizi Desktop remoto, il valore del peso del server è 100. Il peso del server è relativo. Pertanto, se si assegna a un server un valore pari a 100 e un valore pari a 200, il server con un peso relativo pari a 200 riceverà il doppio del numero di sessioni.

Managed Object Format (MOF) contengono le definizioni per le classi WMI (Windows Management Instrumentation). I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK). Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager. Per altre informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                               |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Spazio dei nomi<br/>                | TerminalServices \\ CIMv2 \\ radice<br/>                                                |
| MOF<br/>                      | <dl> <dt>TSCfgWmi.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Win32 \_ TSSessionDirectory**](win32-tssessiondirectory.md)
</dt> </dl>

 

