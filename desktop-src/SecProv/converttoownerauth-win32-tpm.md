---
description: Converte un input di passphrase fornito dall'utente in un'autorizzazione proprietaria di 20 byte che può essere utilizzata per interagire con il TPM. Per i metodi come TakeOwnership e ResetAuthLockOut è necessario il valore di autorizzazione del proprietario risultante.
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
ms.openlocfilehash: f3de5803d10458156fb453e964d782f7c9760333
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314672"
---
# <a name="converttoownerauth-method-of-the-win32_tpm-class"></a>Metodo ConvertToOwnerAuth della \_ classe TPM Win32

Il metodo **ConvertToOwnerAuth** della classe [**\_ TPM Win32**](win32-tpm.md) converte un input di passphrase fornito dall'utente in un'autorizzazione proprietaria di 20 byte che può essere utilizzata per interagire con il TPM. Per i metodi come [**TakeOwnership**](takeownership-win32-tpm.md) e [**ResetAuthLockOut**](resetauthlockout-win32-tpm.md) è necessario il valore di autorizzazione del proprietario risultante.

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

*OwnerPassPhrase* \[ in\]
</dt> <dd>

Tipo: **stringa**

Stringa da convertire in un valore di autorizzazione del proprietario. La stringa può contenere un numero qualsiasi di caratteri alfanumerici.

</dd> <dt>

*OwnerAuth* \[ out\]
</dt> <dd>

Tipo: **stringa**

Stringa derivata dal parametro *OwnerPassPhrase* . Questo valore è un valore binario a 20 byte codificato in una stringa Base64 con terminazione **null** a 28 byte.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **UInt32**

È possibile restituire tutti gli errori del TPM, nonché gli errori specifici dei servizi di base TPM.

Nelle tabelle seguenti sono elencati alcuni dei codici restituiti comuni.



| Codice/valore restituito                                                                                                                                 | Descrizione                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl> | Il metodo è stato eseguito correttamente.<br/> |



 

## <a name="remarks"></a>Commenti

Una stringa codificata UTF-16LE Unicode viene convertita nel valore di autorizzazione del proprietario del TPM a 20 byte prendendo l'hash SHA-1 della rappresentazione binaria della stringa. La terminazione **null** della stringa Unicode non è inclusa nell'hash. Nessun salt viene utilizzato nell'hash SHA-1.

Ad esempio, per convertire la passphrase del proprietario del TPM "1Sample" in un valore di autorizzazione del proprietario del TPM, l'hash SHA-1 viene ricavato dal flusso di byte seguente:

`0x31 0x00 0x53 0x00 0x61 0x00 0x6D 0x00 0x70 0x00 0x6C 0x00 0x65 0x00`

Per convertire una passphrase di lunghezza zero in un valore di autorizzazione del proprietario, l'hash SHA-1 viene accettato dal flusso di byte **null** .

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

[**TakeOwnership**](takeownership-win32-tpm.md)
</dt> </dl>

 

 
