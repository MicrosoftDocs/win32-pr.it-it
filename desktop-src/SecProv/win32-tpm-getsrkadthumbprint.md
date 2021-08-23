---
description: Ottiene l Archiviazione'identificazione personale della chiave radice per un modulo specificato della parte pubblica del TPM Archiviazione radice.
ms.assetid: 08CBEB19-ECF5-4E43-B4A4-0F35987173E1
title: Win32_Tpm::GetSrkADThumbprint
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
ms.openlocfilehash: 9be4b7f02a9b645c29b431a9d974f5871ad5a95fc001e43df17bfe459483974e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119004109"
---
# <a name="win32_tpmgetsrkadthumbprint-method"></a>Metodo Win32 \_ Tpm::GetSrkADThumbprint

Ottiene l Archiviazione'identificazione personale della chiave radice per un modulo specificato della parte pubblica del TPM Archiviazione radice. L'identificazione personale viene usata per indicizzare le chiavi radice di Archiviazione nel server Active Directory se il backup di Active Directory delle informazioni di autorizzazione del proprietario TPM viene abilitato tramite l Criteri di gruppo predefinita.

> [!Note]  
> A partire da Windows 10 versione 1607, non viene mai eseguito il backup dell'autorizzazione del proprietario del TPM in Active Directory.

 

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

*SrkPublicKeyModulus* \[ Pollici\]
</dt> <dd>

Modulo della parte pubblica del TPM Archiviazione radice. Può anche essere ottenuto usando il [**metodo GetSrkPublicKeyModulus**](win32-tpm-getsrkpublickeymodulus.md) della [classe \_ Win32 TPM.](win32-tpm.md)

</dd> <dt>

*SrkADThumbprint* \[ Cambio\]
</dt> <dd>

Restituisce una matrice di 20 byte contenente l'identificazione personale della chiave radice di archiviazione per il modulo specificato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

È possibile restituire tutti gli errori TPM e gli errori specifici dei servizi [di base TPM.](../tbs/tbs-return-codes.md)

I codici restituiti comuni sono elencati di seguito.



| Codice/valore restituito                                                                                                                                 | Descrizione                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl> | Il metodo è stato eseguito correttamente.<br/> |



 

## <a name="remarks"></a>Commenti

Managed Object Format (MOF) contengono le definizioni per le Windows WMI (Management Instrumentation). I file MOF non vengono installati come parte di Windows SDK. Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager. Per altre informazioni sui file MOF, [vedere Managed Object Format (MOF).](../wmisdk/managed-object-format--mof-.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8 solo app desktop\]<br/>                                                |
| Server minimo supportato<br/> | \[Windows Server 2012 solo app desktop\]<br/>                                      |
| Spazio dei nomi<br/>                | \\\\.\\ Root \\ CIMV2 \\ Security \\ MicrosoftTpm<br/>                                     |
| MOF<br/>                      | <dl> <dt>Win32 \_ tpm.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Win32 \_tpm.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Win32 \_ Tpm**](win32-tpm.md)
</dt> </dl>

 

 
