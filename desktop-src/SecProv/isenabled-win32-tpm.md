---
description: Il Metodo IsEnabled della \_ classe TPM Win32 indica se il dispositivo è abilitato. Questo valore può essere modificato dai metodi Enable e Disable.
ms.assetid: e1d5513f-33eb-49e3-9582-d6c103ca5d03
title: Metodo IsEnabled della classe Win32_Tpm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.IsEnabled
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: d808bb68e53b1a24ff668d1b7a9680b5d57b5e9a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306388"
---
# <a name="isenabled-method-of-the-win32_tpm-class"></a>Metodo IsEnabled della \_ classe TPM Win32

Il metodo **IsEnabled** della classe [**\_ TPM Win32**](win32-tpm.md) indica se il dispositivo è abilitato. Questo valore può essere modificato dai metodi [**Enable**](enable-win32-tpm.md) e [**Disable**](disable-win32-tpm.md) .

## <a name="syntax"></a>Sintassi


```mof
uint32 IsEnabled(
  [out] boolean IsEnabled
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*IsEnabled* \[ out\]
</dt> <dd>

Tipo: **booleano**

Se **true**, il dispositivo è abilitato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **UInt32**

È possibile restituire tutti gli errori del TPM, nonché gli errori specifici dei servizi di base TPM.

I codici restituiti comuni sono elencati di seguito.



| Codice/valore restituito                                                                                                                                 | Descrizione                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl> | Il metodo è stato eseguito correttamente.<br/> |



 

## <a name="remarks"></a>Commenti

In base alla specifica Trusted Computing Group (TCG) v 1.2 sono disponibili solo i comandi seguenti quando il dispositivo è in uno stato disattivato.

-   \_CONTINUESELFTEST TPM
-   \_DSAP TPM
-   \_FLUSHSPECIFIC TPM
-   Getfunzionalità TPM \_
-   \_GETTESTRESULT TPM
-   \_Init TPM
-   \_OIAP TPM
-   \_OSAP TPM
-   \_OWNERSETDISABLE TPM
-   \_Reimpostazione PCR TPM \_
-   \_PHYSICALDISABLE TPM
-   \_PHYSICALENABLE TPM
-   \_PHYSICALSETDEACTIVATED TPM
-   \_Ripristino TPM
-   \_SAVESTATE TPM
-   \_SELFTESTFULL TPM
-   Funzionalità del TPM \_
-   \_SHA1COMPLETE TPM
-   \_SHA1START TPM
-   \_SHA1UPDATE TPM
-   \_Avvio TPM
-   \_TAKEOWNERSHIP TPM
-   \_Handle di terminazione TPM \_

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
</dt> <dt>

[**Disabilita**](disable-win32-tpm.md)
</dt> <dt>

[**Abilitare**](enable-win32-tpm.md)
</dt> </dl>

 

 
