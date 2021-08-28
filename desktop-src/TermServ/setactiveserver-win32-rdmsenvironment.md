---
title: Metodo SetActiveServer della classe Win32_RDMSEnvironment
description: Imposta il nome fqdn dell'Desktop remoto Management Services (RDMS) sul nodo corrente.
ms.assetid: ed7b71cf-c3a4-4d2f-856a-31332f94fac9
ms.tgt_platform: multiple
keywords:
- Metodo SetActiveServer Servizi Desktop remoto
- Metodo SetActiveServer Servizi Desktop remoto , Win32_RDMSEnvironment classe
- Win32_RDMSEnvironment classe Servizi Desktop remoto , metodo SetActiveServer
topic_type:
- apiref
api_name:
- Win32_RDMSEnvironment.SetActiveServer
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b68a8f9c6661e78932893ef25278234fb4c944d22297cb87cc95aebe9bc8d8ef
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119865491"
---
# <a name="setactiveserver-method-of-the-win32_rdmsenvironment-class"></a>Metodo SetActiveServer della classe \_ RDMSEnvironment Win32

Imposta il nome fqdn dell'Desktop remoto Management Services (RDMS) sul nodo corrente.

## <a name="syntax"></a>Sintassi


```mof
uint32 SetActiveServer();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce 0 in caso di esito positivo. In caso contrario, restituisce un codice di errore WMI.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                                   |
| Server minimo supportato<br/> | Windows Server 2012<br/>                                                              |
| Spazio dei nomi<br/>                | Root \\ CIMv2 \\ rdms<br/>                                                                |
| MOF<br/>                      | <dl> <dt>RDManagement.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>RDMS.dll</dt> </dl>         |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Win32 \_ RDMSEnvironment**](win32-rdmsenvironment.md)
</dt> </dl>

 

 





