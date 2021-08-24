---
description: Il metodo IsPhysicalPresenceHardwareEnabled della classe Tpm Win32 indica se la presenza fisica nella piattaforma può essere impostata \_ con un segnale hardware.
ms.assetid: 65dabfa9-bfbe-4b9b-8e80-02269895c7ad
title: Metodo IsPhysicalPresenceHardwareEnabled della Win32_Tpm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.IsPhysicalPresenceHardwareEnabled
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: 499ec39741b23583b599407ef43696ab82164f365626c8042586b6b6e4b56deb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119797041"
---
# <a name="isphysicalpresencehardwareenabled-method-of-the-win32_tpm-class"></a>Metodo IsPhysicalPresenceHardwareEnabled della classe Tpm Win32 \_

Il **metodo IsPhysicalPresenceHardwareEnabled** della classe [**\_ Tpm Win32**](win32-tpm.md) indica se la presenza fisica nella piattaforma può essere impostata con un segnale hardware. Questo valore viene configurato dal produttore della piattaforma in base alla progettazione della piattaforma. La documentazione del produttore della piattaforma può fornire informazioni aggiuntive.

## <a name="syntax"></a>Sintassi


```mof
uint32 IsPhysicalPresenceHardwareEnabled(
  [out] boolean IsPhysicalPresenceHardwareEnabled
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*IsPhysicalPresenceHardwareEnabled* \[ Cambio\]
</dt> <dd>

Tipo: **booleano**

Se **true,** la presenza fisica nella piattaforma può essere impostata con un segnale hardware.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **uint32**

È possibile restituire tutti gli errori TPM e gli errori specifici dei servizi di base TPM.

I codici restituiti comuni sono elencati di seguito.



| Codice/valore restituito                                                                                                                                 | Descrizione                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl> | Il metodo è stato eseguito correttamente.<br/> |



 

## <a name="remarks"></a>Commenti

Managed Object Format (MOF) contengono le definizioni per le classi WMI (Windows Management Instrumentation). I file MOF non vengono installati come parte di Windows SDK. Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager. Per altre informazioni sui file MOF, vedere [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                            |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                                      |
| Spazio dei nomi<br/>                | Root \\ CIMV2 \\ Security \\ MicrosoftTpm<br/>                                            |
| MOF<br/>                      | <dl> <dt>Win32 \_ tpm.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Win32 \_tpm.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Win32 \_ Tpm**](win32-tpm.md)
</dt> </dl>

 

 
