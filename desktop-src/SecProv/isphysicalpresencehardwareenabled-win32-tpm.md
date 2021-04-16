---
description: Il metodo IsPhysicalPresenceHardwareEnabled della \_ classe TPM Win32 indica se è possibile impostare la presenza fisica sulla piattaforma con un segnale hardware.
ms.assetid: 65dabfa9-bfbe-4b9b-8e80-02269895c7ad
title: Metodo IsPhysicalPresenceHardwareEnabled della classe Win32_Tpm
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
ms.openlocfilehash: 674dcaa733d8ec70af172359e3dcde0578955dfa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104401645"
---
# <a name="isphysicalpresencehardwareenabled-method-of-the-win32_tpm-class"></a>Metodo IsPhysicalPresenceHardwareEnabled della \_ classe TPM Win32

Il metodo **IsPhysicalPresenceHardwareEnabled** della classe [**\_ TPM Win32**](win32-tpm.md) indica se è possibile impostare la presenza fisica sulla piattaforma con un segnale hardware. Questo valore viene configurato dal produttore della piattaforma in base alla progettazione della piattaforma. La documentazione del produttore della piattaforma può fornire ulteriori informazioni.

## <a name="syntax"></a>Sintassi


```mof
uint32 IsPhysicalPresenceHardwareEnabled(
  [out] boolean IsPhysicalPresenceHardwareEnabled
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*IsPhysicalPresenceHardwareEnabled* \[ out\]
</dt> <dd>

Tipo: **booleano**

Se **true**, la presenza fisica sulla piattaforma può essere impostata con un segnale hardware.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **UInt32**

È possibile restituire tutti gli errori del TPM, nonché gli errori specifici dei servizi di base TPM.

I codici restituiti comuni sono elencati di seguito.



| Codice/valore restituito                                                                                                                                 | Descrizione                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl> | Il metodo è stato eseguito correttamente.<br/> |



 

## <a name="remarks"></a>Commenti

I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI). I file MOF non sono installati come parte del Windows SDK. Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager. Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                            |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                      |
| Spazio dei nomi<br/>                | Radice \\ CIMV2 \\ sicurezza \\ MicrosoftTpm<br/>                                            |
| MOF<br/>                      | <dl> <dt>\_TPM Win32. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>\_tpm.dllWin32</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_TPM Win32**](win32-tpm.md)
</dt> </dl>

 

 
