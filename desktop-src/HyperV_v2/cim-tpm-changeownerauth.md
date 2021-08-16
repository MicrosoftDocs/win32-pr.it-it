---
description: Modifica le credenziali di autorizzazione del proprietario del dispositivo TPM. Sono necessarie le password di autorizzazione del proprietario precedente e del nuovo.
ms.assetid: 5b7f1aec-5181-4330-982c-d80a1d5ae9e8
title: Metodo ChangeOwnerAuth della classe CIM_TPM
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_TPM.ChangeOwnerAuth
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: a92911bcf9c2739d34e8b7602ab5f4cb0032fe5a77376632063971b88f2101d4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118646663"
---
# <a name="changeownerauth-method-of-the-cim_tpm-class"></a>Metodo ChangeOwnerAuth della classe TPM CIM \_

Modifica le credenziali di autorizzazione del proprietario del dispositivo TPM. Sono necessarie le password di autorizzazione del proprietario precedente e del nuovo.

## <a name="syntax"></a>Sintassi


```mof
uint32 ChangeOwnerAuth(
  [in] string OldOwnerAuth,
  [in] string NewOwnerAuth
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*OldOwnerAuth* \[ Pollici\]
</dt> <dd>

Rappresenta le credenziali di autorizzazione del proprietario precedente necessarie per assumere la proprietà del dispositivo TPM. La **sottoclasse CIM \_ SharedCredential** può essere obbligatoria con valore non Null di **CIM \_ SharedCredential.****Proprietà** secret per il parametro .

</dd> <dt>

*NewOwnerAuth* \[ Pollici\]
</dt> <dd>

Rappresenta la nuova credenziale di autorizzazione del proprietario necessaria per assumere la proprietà del dispositivo TPM. La **sottoclasse CIM \_ SharedCredential** può essere obbligatoria con valore non Null di **CIM \_ SharedCredential.****Proprietà** secret per il parametro .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore 0 in esito positivo. In caso contrario, restituisce un errore.

<dl> <dt>

**Completato senza errori** (0)
</dt> <dt>

**Non supportato** (1)
</dt> <dt>

**Errore sconosciuto/non specificato** (2)
</dt> <dt>

**DmTF riservato** (3..4095)
</dt> <dt>

**Metodo riservato** (4096..32767)
</dt> <dt>

**Fornitore specificato** (32768..65535)
</dt> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 10 solo app desktop\]<br/>                                                             |
| Server minimo supportato<br/> | Windows Server 2016<br/>                                                                          |
| Spazio dei nomi<br/>                | Virtualizzazione \\ radice \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**CIM \_ TPM**](cim-tpm.md)
</dt> </dl>

 

 




