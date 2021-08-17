---
title: Metodo AddProgram della Win32_TSVirtualIP classe (Bdaiface.h)
description: Aggiunge un programma all'elenco di programmi che usano la virtualizzazione IP.
ms.assetid: 4d142774-fa7a-4cfb-9305-5a61b0ef5438
ms.tgt_platform: multiple
keywords:
- Metodo AddProgram Servizi Desktop remoto
- Metodo AddProgram Servizi Desktop remoto , Win32_TSVirtualIP classe
- Win32_TSVirtualIP classe Servizi Desktop remoto , metodo AddProgram
topic_type:
- apiref
api_name:
- Win32_TSVirtualIP.AddProgram
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d2f78cb461a61467867a544e954a71c23d59432e29450a7b0f35184f0edec57
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117757860"
---
# <a name="addprogram-method-of-the-win32_tsvirtualip-class"></a>Metodo AddProgram della classe \_ Win32 TSVirtualIP

Aggiunge un programma all'elenco di programmi che usano la virtualizzazione IP.

## <a name="syntax"></a>Sintassi


```mof
uint32 AddProgram(
  [in] string ProgramPath
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ProgramPath* \[ Pollici\]
</dt> <dd>

Tipo: **string**

Percorso e nome file del programma da aggiungere all'elenco.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **uint32**

Restituisce 0 in caso di esito positivo. In caso contrario, restituisce un codice di errore WMI. Fare riferimento [Servizi Desktop remoto di errore del provider WMI](terminal-services-wmi-provider-error-codes.md) per un elenco di questi valori. Il metodo restituisce un errore se l'impostazione è sotto il controllo di Criteri di gruppo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                               |
| Server minimo supportato<br/> | Windows Server 2008 R2<br/>                                                       |
| Spazio dei nomi<br/>                | Radice \\ CIMv2 \\ TerminalServices<br/>                                                |
| Intestazione<br/>                   | <dl> <dt>Bdaiface.h</dt> </dl>   |
| MOF<br/>                      | <dl> <dt>TSCfgWmi.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Win32 \_ TSVirtualIP**](win32-tsvirtualip.md)
</dt> </dl>

 

 





