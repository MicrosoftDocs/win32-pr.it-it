---
description: Ottiene l'identificazione digitale della chiave radice di archiviazione per un determinato modulo della parte pubblica della chiave radice di archiviazione TPM.
ms.assetid: 08CBEB19-ECF5-4E43-B4A4-0F35987173E1
title: 'Metodo Win32_Tpm:: GetSrkADThumbprint'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.GetSrkADThumbprint
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: 81e1ec53596a3d5ce469d412e9bd7ca17e1ad8b1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306370"
---
# <a name="win32_tpmgetsrkadthumbprint-method"></a>\_Metodo Win32 TPM:: GetSrkADThumbprint

Ottiene l'identificazione digitale della chiave radice di archiviazione per un determinato modulo della parte pubblica della chiave radice di archiviazione TPM. L'identificazione personale viene utilizzata per indicizzare le chiavi radice di archiviazione nel server Active Directory se il backup Active Directory delle informazioni di autorizzazione del proprietario del TPM viene abilitato tramite Criteri di gruppo impostazione.

> [!Note]  
> A partire da Windows 10, versione 1607, l'autorizzazione del proprietario del TPM non viene mai sottoposta a backup in Active Directory.

 

Questo metodo è accessibile solo agli amministratori locali.

## <a name="syntax"></a>Sintassi


```C++
uint32 GetSrkADThumbprint(
  [in]  uint8 SrkPublicKeyModulus,
  [out] uint8 SrkADThumbprint
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*SrkPublicKeyModulus* \[ in\]
</dt> <dd>

Modulo della parte pubblica della chiave radice di archiviazione TPM. È possibile ottenerlo anche usando il metodo [**GetSrkPublicKeyModulus**](win32-tpm-getsrkpublickeymodulus.md) della classe [ \_ TPM Win32](win32-tpm.md) .

</dd> <dt>

*SrkADThumbprint* \[ out\]
</dt> <dd>

Restituisce una matrice di 20 byte contenente l'identificazione digitale della chiave radice di archiviazione per il modulo specificato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

È possibile restituire tutti gli errori del TPM, nonché gli errori specifici [dei servizi di base TPM](../tbs/tbs-return-codes.md) .

I codici restituiti comuni sono elencati di seguito.



| Codice/valore restituito                                                                                                                                 | Descrizione                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl> | Il metodo è stato eseguito correttamente.<br/> |



 

## <a name="remarks"></a>Commenti

I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI). I file MOF non sono installati come parte del Windows SDK. Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager. Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 8\]<br/>                                                |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2012\]<br/>                                      |
| Spazio dei nomi<br/>                | \\\\.\\ radice \\ CIMV2 \\ sicurezza \\ MicrosoftTpm<br/>                                     |
| MOF<br/>                      | <dl> <dt>\_TPM Win32. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>\_tpm.dllWin32</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_TPM Win32**](win32-tpm.md)
</dt> </dl>

 

 
