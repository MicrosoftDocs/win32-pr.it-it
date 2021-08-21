---
description: Converte un input di passphrase fornito dall'utente in un'autorizzazione del proprietario a 20 byte che può essere usata per interagire con il TPM. Metodi come TakeOwnership e ResetAuthLockOut richiedono il valore di autorizzazione del proprietario risultante.
ms.assetid: 69eed934-1668-495a-b5b7-cd4a87df1ab3
title: Metodo ConvertToOwnerAuth della classe Win32_Tpm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.ConvertToOwnerAuth
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: 88d1b0f2056d6a10ac623421a7fe261acb832657d08c030ab3247f0acf1a0629
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119004649"
---
# <a name="converttoownerauth-method-of-the-win32_tpm-class"></a>Metodo ConvertToOwnerAuth della classe Tpm Win32 \_

Il **metodo ConvertToOwnerAuth** della classe [**\_ Win32 Tpm**](win32-tpm.md) converte un input di passphrase fornito dall'utente in un'autorizzazione del proprietario di 20 byte che può essere usata per interagire con il TPM. Metodi come [**TakeOwnership**](takeownership-win32-tpm.md) e [**ResetAuthLockOut**](resetauthlockout-win32-tpm.md) richiedono il valore di autorizzazione del proprietario risultante.

Il processo di conversione segue le specifiche del [Trusted Computing Group](https://www.trustedcomputinggroup.org/).

## <a name="syntax"></a>Sintassi


```mof
uint32 ConvertToOwnerAuth(
  [in]  string OwnerPassPhrase,
  [out] string OwnerAuth
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*OwnerPassPhrase* \[ Pollici\]
</dt> <dd>

Tipo: **stringa**

Stringa da convertire in un valore di autorizzazione proprietario. La stringa può contenere un numero qualsiasi di caratteri alfanumerici.

</dd> <dt>

*OwnerAuth* \[ Cambio\]
</dt> <dd>

Tipo: **stringa**

Stringa derivata dal *parametro OwnerPassPhrase.* Questo valore è un valore binario a 20 byte codificato in una stringa con terminazione **Null** base64 a 28 byte.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **uint32**

È possibile restituire tutti gli errori TPM e gli errori specifici dei servizi di base TPM.

Le tabelle seguenti elencano alcuni dei codici restituiti comuni.



| Codice/valore restituito                                                                                                                                 | Descrizione                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl> | Il metodo è stato eseguito correttamente.<br/> |



 

## <a name="remarks"></a>Commenti

Una stringa con codifica Unicode UTF-16LE viene convertita nel valore di autorizzazione del proprietario TPM a 20 byte prendendo l'hash SHA-1 della rappresentazione binaria della stringa. La **terminazione Null** della stringa Unicode non è inclusa nell'hash. Nell'hash SHA-1 non viene usato alcun valore salt.

Ad esempio, per convertire la passphrase proprietaria TPM "1Sample" in un valore di autorizzazione del proprietario TPM, l'hash SHA-1 viene tratto dal flusso di byte seguente:

`0x31 0x00 0x53 0x00 0x61 0x00 0x6D 0x00 0x70 0x00 0x6C 0x00 0x65 0x00`

Per convertire una passphrase di lunghezza zero in un valore di autorizzazione proprietario, l'hash SHA-1 viene preso dal flusso di byte **NULL.**

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
</dt> <dt>

[**TakeOwnership**](takeownership-win32-tpm.md)
</dt> </dl>

 

 
