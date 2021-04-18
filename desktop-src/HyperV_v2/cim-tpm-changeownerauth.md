---
description: Modifica le credenziali di autorizzazione del proprietario del dispositivo TPM. Sono necessarie le password di autorizzazione del proprietario precedenti e nuove.
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
ms.openlocfilehash: 2d5a2895e6a0049b2284b55aea1dc9a1849341c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310574"
---
# <a name="changeownerauth-method-of-the-cim_tpm-class"></a>Metodo ChangeOwnerAuth della classe del \_ TPM CIM

Modifica le credenziali di autorizzazione del proprietario del dispositivo TPM. Sono necessarie le password di autorizzazione del proprietario precedenti e nuove.

## <a name="syntax"></a>Sintassi


```mof
uint32 ChangeOwnerAuth(
  [in] string OldOwnerAuth,
  [in] string NewOwnerAuth
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*OldOwnerAuth* \[ in\]
</dt> <dd>

Rappresenta le credenziali di autorizzazione del proprietario precedenti necessarie per assumere la proprietà del dispositivo TPM. La sottoclasse **CIM \_ SharedCredential** può essere obbligatoria con un valore non null del **\_ SharedCredential CIM**.**Proprietà Secret** per il parametro.

</dd> <dt>

*NewOwnerAuth* \[ in\]
</dt> <dd>

Rappresenta le nuove credenziali di autorizzazione del proprietario necessarie per assumere la proprietà del dispositivo TPM. La sottoclasse **CIM \_ SharedCredential** può essere obbligatoria con un valore non null del **\_ SharedCredential CIM**.**Proprietà Secret** per il parametro.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce 0 in caso di esito positivo; in caso contrario, restituisce un errore.

<dl> <dt>

**Completato senza errori** (0)
</dt> <dt>

**Non supportato** (1)
</dt> <dt>

**Errore sconosciuto/non specificato** (2)
</dt> <dt>

**DMTF riservato** (3.. 4095)
</dt> <dt>

**Metodo riservato** (4096.. 32767)
</dt> <dt>

**Fornitore specificato** (32768.. 65535)
</dt> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows 10\]<br/>                                                             |
| Server minimo supportato<br/> | Windows Server 2016<br/>                                                                          |
| Spazio dei nomi<br/>                | \\Virtualizzazione radice \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_TPM CIM**](cim-tpm.md)
</dt> </dl>

 

 




