---
description: Rinomina un nome di account utente.
ms.assetid: 90258256-7470-4ec8-afce-bea0f64b90fb
ms.tgt_platform: multiple
title: Rinominare il metodo della classe Win32_UserAccount
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_UserAccount.Rename
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 27d495804fb68bc74eda269c2dd7921540f05f5b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127363"
---
# <a name="rename-method-of-the-win32_useraccount-class"></a>Rinominare il metodo della \_ classe Win32 AccountUtente

Il metodo **Rinomina** [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) Rinomina un nome di account utente.

In questo argomento viene utilizzata la sintassi Managed Object Format (MOF). Per ulteriori informazioni sull'utilizzo di questo metodo, vedere [chiamata a un metodo](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintassi


```mof
uint32 Rename(
  [in] string Name
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Nome* \[ in\]
</dt> <dd>

Nome del nuovo account.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce uno dei valori elencati nell'elenco seguente. Per ulteriori codici di errore, vedere [**costanti di errore WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum). Per i valori **HRESULT** generali, vedere [codici di errore di sistema](/windows/desktop/Debug/system-error-codes).

<dl> <dt>

**Success**
</dt> <dd>

0

Esito positivo.

</dd> <dt>

**Istanza non trovata**
</dt> <dd>

1

Istanza non trovata.

</dd> <dt>

**Istanza obbligatoria**
</dt> <dd>

2

Istanza richiesta.

</dd> <dt>

**Parametro non valido**
</dt> <dd>

3

Parametro non valido.

</dd> <dt>

**Utente non trovato**
</dt> <dd>

4

Utente non trovato.

</dd> <dt>

**Dominio non trovato**
</dt> <dd>

5

Il dominio non è stato trovato.

</dd> <dt>

**L'operazione è consentita solo sul controller di dominio primario del dominio**
</dt> <dd>

6

L'operazione è consentita solo sul controller di dominio primario del dominio.

</dd> <dt>

**Operazione non consentita per l'ultimo account amministrativo.**
</dt> <dd>

7

</dd> <dt>

**Operazione non consentita per gruppi speciali specificati. utente, amministratore, locale o Guest.**
</dt> <dd>

8

Operazione non consentita per gruppi speciali specificati: utente, amministratore, locale o Guest.

</dd> <dt>

**Altro errore API**
</dt> <dd>

9

Altro errore dell'API.

</dd> <dt>

**Errore interno**
</dt> <dd>

10

Errore interno.

</dd> </dl>

## <a name="remarks"></a>Commenti

Questa funzionalità viene implementata come metodo per fornire un contesto separato per il nuovo nome che è distinguibile dal valore della proprietà chiave per il nome associato all'istanza da modificare.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Spazio dei nomi<br/>                | \\CIMV2 radice<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_AccountUtente Win32**](win32-useraccount.md)
</dt> <dt>

[Classi del sistema operativo](/previous-versions//aa392727(v=vs.85))
</dt> </dl>

 

